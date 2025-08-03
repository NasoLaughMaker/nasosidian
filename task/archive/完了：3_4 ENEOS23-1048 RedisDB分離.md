- https://vqit.backlog.com/view/ENEOS23-1048#comment-507343086
- https://github.com/Bee2B/eneos-spm/issues/3899
# TODO
上から優先
- [x] 環境変数DB_SCHEMAの設定
- [x] `epic/3_mizushima_2nd`でrake処理実行したらどのような挙動をするのか
  - `NotValquaUserMailerConfig`はどこを見るか
  - 集計はどこのSchemaをみるか
- [x] ローカルで標準出力（puts）を用いてrakeタスク処理のログを確認
	 
## 環境構築
- [x] 堺・川崎のDB作成
- [x] 鹿島のDB作成



# `epic/3_mizushima_2nd`検証
`docker-compose.yml`
```ruby
    DB_SCHEMA: valqua_spm_development_kashima
```

`lib/tasks/send_usage_email_to_valqua.rake`
```ruby
# rubocop:disable all
# frozen_string_literal: true

# rails send_usage_email_to_valqua
desc '請求書をメール送信する'
task send_usage_email_to_valqua: :environment do |_task, _args|
  puts "=== DEBUG: 環境変数 DB_SCHEMA ==="
  puts "DB_SCHEMA: #{ENV.fetch("DB_SCHEMA") { '設定なし' }}"

  puts "=== DEBUG: 現在のデータベース接続情報 ==="
  db_config = ActiveRecord::Base.connection_db_config
  puts "Database Name: #{db_config.database}"

  offices = Office.where(send_usage_email: true)

  office_data = offices.map do |office|
    {
      office_name: office.name,
      result: ScreenLog.daily_conservation_report_created_count(office.id),
      daily_result: ScreenLog.daily_login_count(office.id),
      monthly_result: Time.zone.now.day == 1 ? ScreenLog.monthly_login_count(office.id) : nil
    }
  end

  puts "=== DEBUG: Officeのデータベース接続情報 ==="
  puts "Office Schema：#{Office.connection_db_config.database}"

  mailer = UsageEmailToValquaMailer
  mailer.notification(office_data).deliver_later
end
# rubocop:enable all
```

`app/mailers/usage_email_to_valqua_mailer.rb`
```ruby
# frozen_string_literal: true

class UsageEmailToValquaMailer < ApplicationMailer
  default from: 'valqua-spm@valqua-spm.com'

  def notification(office_data)
    @office_data = office_data
    target_user_email = User.where(valqua: :valqua).pluck(:email)
    target_user_email += NotValquaUserMailerConfig.where(mailer: self.class.name, active: true).pluck(:email)

    puts "=== DEBUG: のデータベース接続情報 ==="
    puts "NotValquaUserMailerConfig Schema：#{NotValquaUserMailerConfig.connection_db_config.database}"

    mail to: target_user_email.uniq,
         bcc: Settings.email.extract_mailer.mail_to_bee2b_service,
         subject: I18n.t('usage_email_to_valqua_mailer.notification.subject')
  end
end

```


# 本番反映後の検証
- 毎朝7:00にバッチ処理が行われる
  - 反映を行った次の日にログを確認
- コンソールからの実行はNG



## NEXTステップ
#### 前提：参照スキーマは堺であるはずだが、鹿島や水島のスキーマが参照されている。
- 堺の場合
	- コード上では参照スキーマが合っているのに、メール内容は別スキーマを参照していることになるため、別の方法での検証が必要
- 鹿島の場合
	- スキーマの参照を明示するような実装が必要になる？
- 水島の場合
	- 鹿島同様の対応
- その以外
	- 追加調査が必要

 ### スキーマの指定方法案
 - rubyで実装【PostgreSQLの場合】
```ruby
def notification(office_data)
  @office_data = office_data

  # 現在のスキーマを取得
  original_schema = ActiveRecord::Base.connection.schema_search_path

  begin
    # 必要なスキーマをセット
    ActiveRecord::Base.connection.schema_search_path = 'specific_schema'

    # 送信対象のメールアドレスを取得
    target_user_email = User.where(valqua: :valqua).pluck(:email)
    target_user_email += NotValquaUserMailerConfig.where(mailer: self.class.name, active: true).pluck(:email)

    mail to: target_user_email.uniq,
         bcc: Settings.email.extract_mailer.mail_to_bee2b_service,
         subject: I18n.t('usage_email_to_valqua_mailer.notification.subject')
  ensure
    # 必ず元のスキーマに戻す
    ActiveRecord::Base.connection.schema_search_path = original_schema
  end
end

```

- SQL直打ち【PostgreSQLの場合】
```ruby
def notification(office_data)
  @office_data = office_data

  # 特定のスキーマからデータを取得
  target_user_email = ActiveRecord::Base.connection.execute(<<-SQL).to_a.flatten
    SELECT email FROM specific_schema.users WHERE valqua = 'valqua'
  SQL

  target_user_email += ActiveRecord::Base.connection.execute(<<-SQL).to_a.flatten
    SELECT email FROM specific_schema.not_valqua_user_mailer_configs WHERE mailer = '#{self.class.name}' AND active = true
  SQL

  mail to: target_user_email.uniq,
       bcc: Settings.email.extract_mailer.mail_to_bee2b_service,
       subject: I18n.t('usage_email_to_valqua_mailer.notification.subject')
end

```

- rubyで実装【MySQL】
```ruby
def notification(office_data)
  @office_data = office_data

  # データベースを切り替える
  ActiveRecord::Base.connection.execute("USE specific_database")

  # データ取得
  target_user_email = User.where(valqua: :valqua).pluck(:email)
  target_user_email += NotValquaUserMailerConfig.where(mailer: self.class.name, active: true).pluck(:email)

  mail to: target_user_email.uniq,
       bcc: Settings.email.extract_mailer.mail_to_bee2b_service,
       subject: I18n.t('usage_email_to_valqua_mailer.notification.subject')
ensure
  # 必要に応じてデフォルトのデータベースに戻す
  ActiveRecord::Base.connection.execute("USE default_database")
end

```


## ローカルでのログ確認方法
- `docker compose exec web bash`
	- コンテナ内で`rake`を実行したら標準出力される
- `docker log workerのコンテナID`

## 本番環境のログ確認方法
- `cd app/current/log`
- `less crontab.log`
	- 地道に探す
- `journalctl -u sidekiq`
	- サービスを指定
		- `-u ユニット名`
	- 時間を指定
		- `--since="2025-03-14 07:58:00"`
		- `--until="2025-03-14 08:10:00"`
- `journalctl -u sidekiq --since="2025-03-14 07:58:00" --until="2025-03-14 08:10:00"`



# 3/19状況確認
- 入れ込んだログが出力されていた。
- 他の日付のログを確認したところ、ログで`arguments: "UsageEmailToValquaMailer"`が確認できたのは以下日付
	- 3/1
	- 3/2
	- 3/3
	- 3/4
	- 3/5
	- 3/6
	- 3/12
	- 3/19
- sidekiqでログが残っている日付のみ正しいスキーマで参照できている可能性がある。
	- 正しいスキーマを参照してメールを送れている日付を出してもらう。
- 上記の仮説が正しいならば、mailer側でsidekiqへの接続が上手くできていない可能性が高いため（cronでの他の非同期処理は毎日実行されている）、実装側に何かしらの不備があることを考えなければならない。
### TODO
- [x] 3月に入ってからの参照スキーマをまとめる
  - 自分じゃ無理な可能性が高いため、誰か調査できる人に依頼する必要があるかもしれない
- [x] 対象ユーザーを割り出すためのSQLを作成する

## 結果
- 川崎：2/19からsidekiqのログなし
- 鹿島：`send_usage_email_to_valqua`はコメントアウトしているので、実行されるはずがない（2/25時点でコメントアウト）
	- 3/7
	- 3/8
	- 3/9
	- 3/10
	- 3/13
	- 3/15
	- 3/16
	- 3/17
	- 3/18
- 水島：`send_usage_email_to_valqua`はコメントアウトしているので、実行されるはずがない（2/25時点でコメントアウト）
	- 3/11
	- 3/14

### 3月に入ってからの`保全システムENEOS様ご利用状況のお知らせ`配信状況（sidekiqのログから確認）
- 1日：堺
- 2日：堺
- 3日：堺
- 4日：堺
- 5日：堺
- 6日：堺
- 7日：鹿島
- 8日：鹿島
- 9日：鹿島
- 10日：鹿島
- 11日：水島
- 12日：堺
- 13日：鹿島
- 14日：水島
- 15日：鹿島
- 16日：鹿島
- 17日：鹿島
- 18日：鹿島
- 19日：堺

# Redisが問題ぽいから対応考える
## 発生原因
現在の構成では、Redisサーバーが1つのみであり、全ての製油所でDBを共有している。
```ruby
## ActionCable
url: <%= "redis://#{ENV['KVS_HOST']}:6379/1" %>
## Sidekiq
config.redis = { url: "redis://#{ENV['KVS_HOST']}:6379/2" }
```

## 発生した事象
sidekiqを用いた非同期処理の際に他のスキーマを参照してしまい、異なるスキーマのユーザーを宛先としてメール送信を行なっている

## 解決策
### 短期的な策
`:6379/2`の指定先を事業所ごとに分ける
| 事業所 | ActionCable | Sidekiq |
| --- | --- | --- |
| 堺 | `/1` | `/2` |
| 川崎 | `/3` | `/4` |
| 鹿島 | `/5` | `/6` |
| 水島 | `/7` | `/8` |
| 麻里布 | `/9` | `/10` |
#### 問題点
Redisはデフォルトで0 ~ 15の16個をDBとして提供している。しかし、将来的に追加する事業所を考えると16を超えてしまうため、今後事業所を追加する際にはRedisサーバーの追加が必要になると思われる。
サーバーを増やさずにDBを増やす方法も考えられるが、インスタンス全体のキャパシティは増えないため、負荷が大きくなる。ここの調整はその時に考える必要あり？

### 将来的な策
1. Redisサーバーを完全に分離して、1事業所につき1サーバーで運用する
2. 3つ程度のサーバーを用意し、1つのサーバーに対して3程度の事業所のように、ハイブリッドで運用する

ここら辺も料金やインスタンスのキャパシティを考慮する必要があると思われる。


## 実装
```ruby
ENV.fetch(`SIDEKIQ_REDIS_DB`, 1)
```
上記だけで良いのか？
STGのマルチアプリ化が行われたらどのように実装を変える必要があるのか？

環境によって変わる部分はどうすれば良いか
今はEC2環境内で手動で設定しているが、ゆくゆくはansibleで設定できるように直していきたいため、ansibleに関する実装はしておいた方が良い。


## 修正内容
`develop_XXX`の`ansible/group_vars/eneos-stg/offices/XXX.yml`に各環境変数を設定する。
現在 release/stgがdevelop_sakaiのような立ち位置になっている。
railsコンソールでfetchできるかどうかのエビデンスを取る。


## dev-2デプロイ
### 鹿島
`docker-compose run -v $HOME/.ssh/:/root/.ssh/:ro --rm web bash`
`eval 'ssh-agent'`
`ssh-add ~/.ssh/id_rsa_bee2b`
`BRANCH=infra/3899_separate_redis_kashima cap dev2-kashima deploy`

### 水島
`docker-compose run -v $HOME/.ssh/:/root/.ssh/:ro --rm web bash`
`eval 'ssh-agent'`
`ssh-add ~/.ssh/id_rsa_bee2b`
`BRANCH=infra/3899_separate_redis_mizushima cap dev2-mizushima deploy`

## 検証
### ActionCable
`redis-cli -h 127.0.0.1 -p 6379`
`SELECT <該当番号>`
`keys *`
cableが接続されている間だけkeyに値が登録される。cableを通すために実際の画面を触っておく必要がある。

### sidekiq
`bin/rake send_usage_email_to_valqua`
上記でJobをsidekiqに登録し、`keys *` でqueueを確認

# 検証状況
- [x] dev-2
	- [x] 鹿島
	- [x] 水島
- [ ] dev
	- [ ] 堺
	- [ ] 川崎


# Redis提案内容
1. 現在1事業所につき、`ActionCable`, `Sidekiq`の2つのRedisDBを設定
2. 麻里布まで考慮するとDBは10埋まる
3. Redisは1サーバーにつきデフォルトで16個DBを提供している
4. 今後追加される9事業所全て追加したら18になるため、将来的にDBの追加が必要
5. ただ、9事業所分の負荷をRedisサーバー1つで耐えられるか考慮が必要
6. もし耐えられないなら、Redisサーバー自体を増やして、負荷を分散させるべき
7. そこの判断を付けるためにRedisサーバーの負荷状況をCWで確認できるようにしておくべき
8. どのようなメトリクスを確認すれば負荷状況を把握できるかは調べる必要あり？

### 千葉さん
まあ大丈夫でしょう
メトリクスとかあるんかな
まあおいおいで見ていこ


## ENEOS-STG反映手順
https://github.com/Bee2B/eneos-spm/issues/3899#issuecomment-2765831896

鹿島・水島に対応内容と時間を伊豆さんに確認
時間が決まったら10チャンネルで周知
デプロイ申請とマージ申請はその時連絡する

## redis-cliインストール
https://qiita.com/ajitama/items/ad37d9795e5cfdb840d2