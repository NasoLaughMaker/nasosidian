# 2/5(水)
- [x] schema.xlsxの自動出力コード作成

# 2/6(木)
- [x] eneos-spm復旧作業
- [x] load average監視

# 2/7(金)
- [x] load average監視
- [x] Documentチーム合流&タスク貰う
- [ ] 査定シート記入
- [x] パスワード修正のSQL作成

# 2/10(月)
- [x] load average監視
- [x] Document作成
- [ ] 査定シート作成

# 2/12(水)
- [ ] Document作成
- [ ] 査定シート作成
- [x] ZAC説明会 15:00 ~ 16:00

# 2/13(木)
- [ ] Document作成
- [ ] 査定シート作成
- [ ] 移行PG作成

# 2/14(金)
- [x] Document引き継ぎ
- [x] 査定シート作成
- [ ] 移行PG作成

# 2/17(月)
- [x] 移行PG作成

# 2/19(水)
- [x] 移行PG作成・修正
  - [x] 移行確認SQL作成
	 
# 2/20(木)
- [ ] ドキュメント作成：案件管理画面

# 2/25(火)
- [ ] ドキュメント作成：案件管理画面
- [ ] 締結データ移行

# 2/26(水)
-  締結データ移行
	- [x] URL自動生成SQL作成
	- [x] office_usersのSQL修正
	- [ ] 検証方法の第一版 提出

# 2/27(木)
-  締結データ移行
	- [x] URL自動生成SQL作成
	- [x] active_storage_blobsのSQL修正
	- [x] 検証方法の調査・確立

# 2/28(金)
- 締結データ移行
  - [x] 宮川さんの資料作りサポート
  - [x] spreadsheeetの修正
- ドキュメント作成
  - 内部レビュー
    - [x] ユーザー一覧
	  
# 2/28(金)
- ドキュメント作成
  - 内部レビュー
    - [x] ユーザー一覧：対面レビュー
  - URL調査
    - [ ] 工事PLOT画面
	- [ ] 検査特記
	- [ ] 運転記録

# 3/5(水)
- SPM
  - メール怪奇現象調査
    - [x] ローカルで標準出力を用いてrakeタスク処理のログを確認
	  - [x] 非同期処理が原因かも。sidekiqのログで確認する。
    - [x] 本番環境で`log/crontab.log`にログを出力できるよう実装
    - [ ] backlogの出力先を保持するテーブル作成
  - [x] `release/dev`への反映手順を聞く
    - `17:00`宮川さんに話しかける
		  
# 3/6(木)
- メール送信
  - [x] `release/dev`検証
    - 宮川さんに立ち会いお願いする
	- ヴォンさんに時間の確認する
- [x] お問い合わせの調査
  - ENEOS23-1054 
- [ ] Backlogへの出力先をテーブルで管理
- [x] sentry：チケット・issue化 
  - [x] 本番エラーの調査
	 
# 3/7(金)
- [x] パスワードハッシュ化の確認
  - `confirmed_at`に値を入れれば解決 
- [ ] 出力先Backlogをテーブルで管理
- [x] ActiveRecord::RecordNotDestroyedの調査
- [ ] ENEOS23-1075
  - 次回の堺の反映に合わせる。 
- 優先度：低
  - [ ] ENEOS23-1066 調査
  - [ ] ENEOS23-1068 調査

# 3/10(月)
- [x] ENEOS23-1065
  - チケットに記載し松本さんに報告
- [x] ENEOS23-1048
  - 本番反映して何をするのか、どのように検証するのかを宮川さんに確認とる。
- [x] お問い合わせ対応：ユーザー登録
- [ ] ENEOS23-1066
  - 調査
- [ ] ENEOS23-1076
  - 実装
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy と keyerrorの調査
- https://github.com/Bee2B/eneos-spm/pull/3933#pullrequestreview-2670476174

# 3/11(火)
- [x] お問い合わせ対応
- [x] [PR#3933](https://github.com/Bee2B/eneos-spm/pull/3933#pullrequestreview-2670476174)：修正
- [ ] ENEOS23-1066
  - 調査
- [ ] ENEOS23-1076
  - 実装
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy：調査
- [ ] keyerror：調査

# 3/12(水)
- [ ] ENEOS_SPM_KASHIMA-264
- [ ] cron再起動
- [ ] ENEOS23-1066
  - 調査
- [ ] ENEOS23-1076
  - 実装
- [ ] ENEOS23-1107
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy：調査
- [ ] keyerror：調査

# 3/13(木)
- [x] cron再起動
- [x] [ENEOS23-1065](https://vqit.backlog.com/view/ENEOS23-1065#comment-511483849)
  - 調査・返信
- [ ] ENEOS23-1076
  - 実装
- [ ] ENEOS23-1107
  - 調査
- [ ] ENEOS23-1066
  - 調査
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy：調査
- [ ] keyerror：調査

# 3/14(金)
- [x] 定修 500エラー
  - [x] 調査
    - 遠瀬さんに依頼
  - [x] チケット作成
- [x] ENEOS23-1076
  - 実装完了
  - レビュー依頼中
- [ ] ENEOS23-1107
  - 調査
- [ ] ENEOS23-1066
  - 調査
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy：調査
- [ ] keyerror：調査

# 3/17(月)
- [ ] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] EC2アラート
- [ ] ENEOS23-1048
  - ログ確認
- [ ] ENEOS-1144
  - 遠瀬さんに情報提供
- [ ] ENEOS23-1107
  - 調査
  - all
- [ ] ENEOS23-1066
  - 調査
  - FileNotFound
- [x] ENEOS23-1076
  - dev検証
- [ ] 出力先Backlogをテーブルで管理
- [ ] ENEOS23-1075
- [ ] proxy：調査
- [ ] keyerror：調査

- 川崎を参考にして500エラー何番みたいな感じで整理する
	- これ何？ 松本さんに確認
 

# 3/18(火)
- [x] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] ENEOS23-1048
  - ログ確認
	  - 別のログ出し方法にして再度確認する
	  - [x]  上記を金澤さんに連絡する
- [x] 山下さんへの連絡
- [x] 松本さんにチケット渡す
- [ ] ストレージの内容をスプレッドシートにまとめる
- [x] 環境移行の状況まとめをスプレッドシートにまとめる
- [ ] ENEOS23-1107(all)
  - 調査
  - 遠瀬さんに依頼済み
### 明日移行
- [ ] ENEOS-1144
  - 遠瀬さんに情報提供
- [ ] ENEOS23-1066(FileNotFound)
  - 調査
- [x] 出力先Backlogをテーブルで管理
  - チケット作成して松本さんに渡す。
- [x] ENEOS23-1075
  - 松本さんにチケット渡す。
- [ ] proxy：調査
- [ ] keyerror：調査


# 3/18(火)
- [ ] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 山下さんの調査結果を連絡
- ENEOS23-1048
  - [x]  3月からの参照スキーマまとめる
  - [x]  参照ユーザーを一目で見れるSQL作成
- [x] ストレージの内容をスプレッドシートにまとめる
- [ ] ENEOS23-1065
- [x] ENEOS23-1107(all)
  - 調査
  - 遠瀬さんに依頼済み
  - 夜対応していただける
### 明日移行
- [ ] ENEOS-1144
  - 遠瀬さんに情報提供
- [ ] ENEOS23-1066(FileNotFound)
  - 調査
- [ ] proxy：調査
- [ ] keyerror：調査


# 3/24(月)
- [ ] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] dev検証
- [x] 500エラーチケットの状態更新
- [x] ENEOS23-1065
    - 日本語レビュー
- [x] ENEOS23-1076
	- レビュー修正
- [ ] ENEOS23-1064
	- Redisに関する対応をどうするのか宮川さんに展開できるようにしておく
	- [ ] 実装まで済ませておく
- [x] Issue#4245 レビュー
### 明日移行
- [ ] ENEOS23-1066(FileNotFound)
  - 調査
- [ ] proxy：調査
- [ ] keyerror：調査


# 3/25(火)
- [ ] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] ENEOS23-1048
	- Redisに関する対応をどうするのか宮川さんに展開できるようにしておく
	- [ ] 堺・川崎 実装
	- [x] 水島 実装
	- [x] 鹿島 実装
	- [ ] 麻里布 実装
- [x] 竹口さんのアカウント作成
- [ ] S3バックアップ問題
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068
### 明日移行
- [ ] keyerror：調査


# 3/26(水)
- [ ] `valqua-eneos`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
- [x] ENEOS23-1048
	- Redisに関する対応をどうするのか宮川さんに展開できるようにしておく
	- [x] 堺・川崎 実装
		- [x] approve
	- [x] 水島 実装
		- [x] approve
	- [x] 鹿島 実装
		- [x] approve
	- [x] 麻里布 実装
		- [x] approve
	- [x] 検証
- [x] ディスク状況
	- [x] 資料作成
	- [x] 千葉さん：MTG 3:30~
	- [x] 修正
- [x] 大西さんの件：MTG

### 明日移行
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068
- [ ] keyerror：調査


# 3/27(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認

## 変動作業
- [ ] ENEOS23-1066 調査
- [ ] ENEOS23-1068 調査
- [ ] ENEOS23-1188 調査

## 明日以降
- [ ] keyerror：調査
- [ ] ENEOS23-1048
	- [ ] dev検証
		- [ ] 堺
		- [ ] 川崎
	 

# 3/28(金)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認

## 変動作業
- [ ] ENEOS23-1188 実装
- [ ] ENEOS23-1066
- [ ] ENEOS23-1067
- [ ] ENEOS23-1068
- [ ] ENEOS23-1086

## 明日以降
- [ ] ENEOS23-1067
- [ ] ENEOS23-1048
	- [ ] dev検証
		- [ ] 堺
		- [ ] 川崎
	 

# 3/31(月)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認

## 変動作業
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [x] 月末処理
	- [x] 交通費申請
	- [x] ZAC
	- [x] KOT確認
	- [x] SPM稼働シート
- [x] redis cilをrelease/stgで使えるようにしておく
	- [x] [参照](https://qiita.com/ajitama/items/ad37d9795e5cfdb840d2)
		- usr/binにインストール
- [ ] ENEOS23-1273 再現
- [ ] 環境移行の状況
- [x] 鹿島cron設定
- [x] ENEOS23-1048 STG反映準備
	- [x] 各ブランチはrebaseして最新の状態にしておく
	- [x] それぞれの事業所に設定する環境変数と値をコピペすればいい状態で記載
		- issueに記載

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1067
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1048
	- [ ] `infra/3899_separate_reids_by_office` rebase作業



# 4/1(火)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認

## 優先事項
- [x] 山邊さん依頼

## 変動作業
- [x] 月末処理
	- [x] ZAC
	- [x] SPM稼働シート
- [ ] ENEOS23-1048
	- [x] `infra/3899_separate_reids_by_office` rebase作業
	- [ ] STG反映
	  - 伊豆さんに確認
- [ ] ENEOS23-1271
	- 伊豆さんに確認

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1067
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/2(水)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認

## 優先事項
- [x] データ修正

## 変動作業
- [x] ENEOS23-1048
	- [x] STG反映
	  - 伊豆さんに確認
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [ ] [環境移行の状況](https://docs.google.com/spreadsheets/d/19CsAD8EB89QUEXmHXuRo-IYTlgwC6VoFtj6BsWU4Fk0/edit?gid=0#gid=0) 修正

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1067
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/3(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認

## 優先事項

## 変動作業
- [x] ENEOS23-1048
	- [x] 本番反映
	- [x] 鹿島・検証
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [x] [環境移行の状況](https://docs.google.com/spreadsheets/d/19CsAD8EB89QUEXmHXuRo-IYTlgwC6VoFtj6BsWU4Fk0/edit?gid=0#gid=0) 修正
- [ ] 板野さんのssh接続を準備する
	- [ ] dev-2
	- [ ] 本番、STG
		- [ ] backlogで依頼

## 経過観察
- [ ] ENEOS23-1066
- [x] ENEOS23-1067
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 



# 4/4(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [x] Redisチェック

## 優先事項

## 変動作業
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [ ] 板野さんのssh接続を準備する
	- [ ] dev-2
	- [ ] 本番、STG
		- [ ] backlogで依頼

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現

	 
# 4/7(月)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] 山邊さんからの質問
	- 接続に関するモーダルの表示条件

## 変動作業
- [x] STG環境のファイル調査
- [x] プリコンパイルファイルの削除検証
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [ ] 板野さんのssh接続を準備する
	- [ ] dev-2
	- [ ] 本番、STG
		- [ ] backlogで依頼

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/8(火)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] ENEOS会
	- [x] お知らせ機能を議事録に追加
- [x] データ修正
- [ ] 板野さんのssh接続を準備する
	- [x] dev-2
	- [ ] 本番、STG
		- [x] backlogで依頼
- [ ] 山邊さん依頼対応


## 変動作業
- [x] ENEOS23-1066
	- 確認次第CLOSE
- [x] プリコンパイルファイルの削除検証
	- [x] STG
- [ ] ENEOS23-1271
	- 伊豆さんに確認

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/9(水)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] 山邊さん依頼対応

## 変動作業
- [ ] 板野さんのssh接続を準備する
	- [x] dev-2
	- [ ] 本番、STG
		- [x] backlogで依頼
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [x] ENEOS23-1292
	- [x] dev検証
	- [x] コードレビュー

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 

# 4/10(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項


## 変動作業
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] ENEOS23-1271
	- 伊豆さんに確認

## 経過観察
- [ ] ENEOS23-1066
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/11(金)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)
	- [ ] ENEOS23-1303 バグ 緊急度中E>100件表示したスクロールエラー｜浅野さんNo. 432 【バルカー SPM】お問い合わせがありました

## 優先事項


## 変動作業
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [ ] ENEOS23-1293 調査・見積もり

## 経過観察
- [ ] ENEOS23-1066
- [x] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現



# 4/14(月)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [x] Redisチェック
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)
	- [ ] ENEOS23-1303 バグ 緊急度中E>100件表示したスクロールエラー｜浅野さんNo. 432 【バルカー SPM】お問い合わせがありました

## 優先事項
- [x] ENEOS23-1297 お知らせ機能確認

## 変動作業
- [ ] load average推移表作成
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] ENEOS23-1271
	- 伊豆さんに確認
- [ ] ENEOS23-1293 調査・見積もり

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 

# 4/15(火)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)
	- [x] ENEOS23-1303 バグ 緊急度中E>100件表示したスクロールエラー｜浅野さんNo. 432 【バルカー SPM】お問い合わせがありました

## 優先事項
- [x] ENEOS23-1293 調査・見積もり
- [ ] ENEOS23-1297
	- お知らせドキュメント作成

## 変動作業
- [ ] load average推移表作成
- [ ] public/cacheの削除調査
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] ENEOS23-1271
	- develop_sakaiでPR作成
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 

# 4/16(水)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- お知らせドキュメント作成

## 変動作業
- [ ] load average推移表作成
- [ ] public/cacheの削除調査
- [x] 板野さんのssh接続
	- [x] Backlogアカウント作成
	- [ ] 本番
	- [ ] STG
- [x] ENEOS23-1271
	- develop_sakaiでPR作成
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/17(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [x] ENEOS23-1345 画面仕様書作成

## 変動作業
- [ ] load average推移表作成
- [ ] public/cacheの削除調査
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/18(金)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] ENEOS23-1345 画面仕様書作成

## 変動作業
- [ ] 板野さんのssh接続
	- [ ] 本番
	- [ ] STG
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 松本さんに依頼中
- [ ] load average推移表作成
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現



# 4/21(月)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] ENEOS23-1345 画面仕様書作成
	- [ ] 実装
		- [x] 未読数の定義について山邊さんに確認

## 変動作業
- [ ] 板野さんのssh接続
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 松本さんに依頼中
- [ ] load average推移表作成
	- [ ] 明日できたらやる。（4時間くらい？）
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/22(火)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] ENEOS23-1345 画面仕様書作成
	- [x] 実装

## 変動作業
- [ ] 板野さんのssh接続
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 松本さんに依頼中
- [ ] load average推移表作成
	- [ ] 明日できたらやる。（4時間くらい？）
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068

## 明日以降
- [ ] ENEOS23-1188
	- 実装
- [ ] ENEOS23-1086
	- 調査
- [ ] ENEOS23-1273
	- 再現
	 


# 4/23(水)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] ENEOS23-1345 画面仕様書作成
	- [x] 実装

## 変動作業
- [ ] 板野さんのssh接続
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068


# 4/24(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] ENEOS23-1345 画面仕様書作成
	- [x] 実装・修正

## 変動作業
- [ ] 板野さんのssh接続
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068


# 4/25(金)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [x] ENEOS23-1345 画面仕様書作成
	- dev検証
		- [ ] dev
		- [x] gov-dev
		- [x] kashima-dev-2
		- [ ] mizushima-dev-2
	- [ ] STG反映
- [x] ENEOS23-1351

## 変動作業
- [ ] 板野さんのssh接続：確認待ち
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す
- [ ] 締結管理：瑕疵対応
	- [x] 環境構築

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 経過観察
- [ ] ENEOS23-1068


# 4/30(水)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] ENEOS23-1297
	- [ ] STG反映
- [x] SPM-1256
	- Rspec追加
- [x] ENEOS会
- [x] 山邊さんにサイドバーを閉じるチケットの状況を報告する

## 変動作業
- [x] 稼働管理
	- [x] 交通費申請
	- [x] ZAC
	- [x] KOT

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] 板野さんのssh接続：確認待ち
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/1(木)
## 通常作業
- [ ] `valqua-eneos`、`10-eneos全体`キャンバスのチケット状況をリマインド
	- 水曜の週次定例前には整理しておく必要がある
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] ENEOS23-1297
	- [x] STG検証
- [x] 山邊さん作成チケットの見積もり出す


## 変動作業
- [x] 稼働管理
	- [x] ZAC
- [x] SPM-1256
	- 修正
- [ ] ENEOS23-1444
	- 調査

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [x] 板野さんのssh接続：確認待ち
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/7(水)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項


## 変動作業
- [x] ENEOS23-1444
	- 調査
- [ ] SPM-1256
	- テスト仕様書作成
- [x] [SPM-1264](https://vqit.backlog.com/view/SPM-1264)
	- テスト仕様書項目確認
- [ ] 4月の予実に対しての妥当性をまとめる
	- 工数くださいの方向に持っていく。
- [ ] チケット判断基準の叩き台作成
	- 瑕疵・保守・開発などどこで対応すべきチケットなのかのルール作成

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/8(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
- [x] 500エラーの内容を報告：金澤さん
- [x] SPM-1256
	- テスト仕様書作成
- [x] お知らせ機能：水島STG検証

## 変動作業
- [ ] 4月の予実に対しての妥当性をまとめる
	- 工数くださいの方向に持っていく。
- [x] チケット判断基準の叩き台作成
	- 瑕疵・保守・開発などどこで対応すべきチケットなのかのルール作成

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/9(金)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)

## 変動作業
- [ ] 4月の予実に対しての妥当性をまとめる
	- 工数くださいの方向に持っていく。
- [x] チケット判断基準の叩き台修正
	- 瑕疵・保守・開発などどこで対応すべきチケットなのかのルール作成
	- WBSに追記して完了
- [x] SPM-1224　修正
- [x] ENEOS23-1491
	- 金澤さんに報告

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/12(月)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)

## 変動作業
- [x] 4月の予実に対しての妥当性をまとめる
	- 工数くださいの方向に持っていく。
	- 千葉さんと話し合う
- [x] SPM-1224　テスト

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

# 5/13(火)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)

## 変動作業
- [x] ENEOS会

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/14(水)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)

## 変動作業

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/15(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
- [x] ENEOS_KAWASAKI-496

## 変動作業
- [x] Pマーク回答
- [ ] 500エラーをCanvasからWBSに移行する

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/15(木)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] rpsec

## 変動作業
- [x] 500エラーをCanvasからWBSに移行する

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/19(月)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] rspec

## 変動作業
- [x] WBSの優先順位記載

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/20(火)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] レビュー
	- [ ] Dev検証
	- [ ] STG検証

## 変動作業
- [x] ENEOS会
- [x] ENEOS23-1557 初期調査

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/21(水)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] レビュー
	- [x] Dev検証
	- [ ] STG検証

## 変動作業
- [ ] load average集計
- [ ] ENEOS23-1243
- [ ] ENEOS23-1510、1511の実績を金澤さんに報告

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/22(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] STG検証
	- [x] ②、③の修正
	- [ ] ①、④、⑤の修正・チケット化

## 変動作業
- [ ] ENEOS23-1243
	- [ ] https://vqit.backlog.com/view/ENEOS23-1243#comment-545083609 連絡入れる
- [x] ENEOS23-1510、1511の実績を金澤さんに報告

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/23(金)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [ ] ①
	- [x] ④
	- [ ] ⑤

## 変動作業
- [ ] ENEOS23-1243
	- [x] https://vqit.backlog.com/view/ENEOS23-1243#comment-545083609 連絡入れる

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/26(月)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] ENEOS_SPM_KASHIMA-334 鹿島 作業安全指示書(標準)、(検査用）　QRコードの表示
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [x] ①
	- [ ] ⑤

## 変動作業
- [x] ENEOS23-1243

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/27(火)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [ ] ⑤

## 変動作業

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 5/30(金)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- [ ] 堺保守：[チケット管理](https://docs.google.com/spreadsheets/d/1oFT5jy5wbLAxS_sSBTcE-0RNzlOid5EH/edit?gid=122850640#gid=122850640)

## 優先事項
- [x] load average異常値調査

## 変動作業
- [ ] [ENEOS23-1392](https://vqit.backlog.com/view/ENEOS23-1392)
	- [ ] DEV検証
	- [ ] STG検証
- [ ] 月末処理
	- [x] 交通費申請
	- [ ] ZAC
	- [x] KOT

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す


# 6/2(月)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [x] 山邊さん依頼：STGユーザー登録

## 変動作業
- [x] 月末処理
	- [x] ZAC
- [ ] ENEOS23-1458 保全ご利用状況メールに月次登録人数を出力する
- [ ] ENEOS23-1295 ６月末必須実装｜四半期ID棚卸メール

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/3(火)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項

## 変動作業
- [ ] ENEOS23-1458 保全ご利用状況メールに月次登録人数を出力する
- [ ] ENEOS23-1295 ６月末必須実装｜四半期ID棚卸メール
- [ ] load averageまとめる
- [x] ENEOS_SPM_MARIFU-56 麻里布 G画面でエラーポップアップが表示された

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/4(水)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [x] ENEOS_SPM_MARIFU-47 実装
- [x] ENEOS_SPM_MARIFU-48 実装
- [x] ENEOS_SPM_MARIFU-49 実装
- [x] ENEOS_SPM_MARIFU-53 実装
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 
- [ ] load averageまとめる

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 


# 6/5(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [x] ENEOS_SPM_MARIFU-47 レビュー
- [x] ENEOS_SPM_MARIFU-48 レビュー
- [x] ENEOS_SPM_MARIFU-49 レビュー
- [ ] ENEOS_SPM_MARIFU-53 レビュー
-  ENEOS_SPM_MARIFU-55 麻里布 E画面の未実施残数のバッチ表示
	- [x] 実装
	- [ ] レビュー
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 
- [ ] load averageまとめる

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/6(金)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [ ] ENEOS_SPM_KASHIMA-386
	- [x] api
	- [ ] FE...vuさんに依頼中
- [ ] ENEOS_SPM_MARIFU-53 レビュー
- [ ] ENEOS_SPM_MARIFU-55
	- [ ] ENEOS_SPM_KASHIMA-386 が完了次第こちらにも反映
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 
- [ ] load averageまとめる

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/9(月)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [x] load average集計
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
- [x] ENEOS_SPM_KASHIMA-388
	- 森さんに依頼する
- [x] ENEOS_SPM_MARIFU-53 レビュー
- [x] ENEOS_SPM_MARIFU-55
	- [ ] ENEOS_SPM_KASHIMA-386 が完了次第こちらにも反映
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/10(火)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [x] load average集計　修正
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
- [ ] ENEOS_SPM_MIZUSHIMA-323 本番のPLOTデータ移行
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/11(水)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [ ] ENEOS_SPM_MIZUSHIMA-323 本番のPLOTデータ移行
	- [x] evidence取り方まとめる
	- [x] 手順まとめる
	- [x] local検証
　
## 変動作業
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295 

## 松本さんに依頼中
- [ ] public/cacheの削除調査

## 明日以降
- [ ] STG：堺ドキュメントルートのパブリックのPDFを探す

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 
# 6/12(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
- [ ] ENEOS_SPM_MIZUSHIMA-323 本番のPLOTデータ移行
	- 宮川さん・松本さん確認待ち中
　
## 変動作業



## 明日以降
- [ ] - [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/13(金)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [x] ENEOS_SPM_MIZUSHIMA-323 本番のPLOTデータ移行
　
## 変動作業
- [ ] ENEOS_SPM_KASHIMA-390 

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査
- [ ] ENEOS23-1570 　STG反映に当たりリマインドする

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 


# 6/16(月)
## 通常作業
- [ ] 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
　
## 変動作業
- [x] ENEOS_SPM_KASHIMA-390 

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査
- [x] ENEOS23-1570 　STG反映に当たりリマインドする

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/17(火)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
- [x] RDS CPU使用率＆load averageの監視　16:00 ~ 16:30
	- 前日比較の結果を17:00ごろに共有する
- [ ] selenium-gridの導入
　
## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査
- [x] ENEOS23-1570 　STG反映に当たりリマインドする

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/18(水)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [x] Benchmarkによる調査・計測
- [ ] selenium-gridの導入
　
## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/19(木)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
- [x] Benchmarkによる調査・計測
	- [x] A画面
	- 永井は対応しない
- [ ] selenium-gridの導入
	- [x] 複数ユーザーでの検証
	- [x] chromiumの導入
　
## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/20(金)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [ ] selenium-gridの導入
	- [x] 100リクエストでの実施
- [ ] 集計
　
## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/23(月)
## 通常作業
- [ ] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [ ] selenium-gridの導入
	- [x] 100リクエストでの実施
- [x] 午前対応：集計
	- [datadog](https://app.datadoghq.com/logs?agg_m_a=count&agg_m_b=count&agg_m_source_a=base&agg_m_source_b=base&agg_t_a=count&agg_t_b=count&cols=%40controller%2C%40http.url_details.path&ff_display=a%2Cb&highlight=valqua-spm-api&messageDisplay=inline&query_a=env%3Aeneos%20%40controller%3AApi%5C%3A%5C%3A%2A%20%40action%3Aindex&query_b=env%3Aeneos%20%40controller%3AApi%5C%3A%5C%3A%2A%20%40action%3Aindex%20%40http.url_details.path%3A%2Fapi%2Fdaily_maintenance%2Foffices%2F45%2Fdaily_schedules&refresh_mode=paused&sort=time&spanID=2119198018421432861&storage=hot&stream_sort=time%2Cdesc&view=spans&viz=query_table&from_ts=1750409940000&to_ts=1750410000000&live=false)
	- 7:00 ~ 12:00 → 12:00 ~ 14:00 → それ以外
- [x] 鹿島：チューニング対応
	- 森さんが対応くださってる。


## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/24(火)
## 通常作業
- [x] 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [ ] selenium-gridの導入
- [x] 末松さんへBacklog回答する
	- [ ] Backlogに回答する
- [x] 職務経歴書を書く
- [ ] GithubActionsの導入

## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/25(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
- [x] 末松さん: KWNさんへのBacklog回答する
- [ ] GithubActionsの導入

## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [ ] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/26(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-443](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-443)
- [x] [ENEOS_SPM_KASHIMA-438](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-438)
- [ ] [根岸開発環境構築](https://github.com/Bee2B/eneos-spm/issues/5849)
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
- [ ] GithubActionsの導入

## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査

## 例外
- [x] E画面速度改善がindexで実現できるかどうかの確認
	- 1458, 1295の対応が完了したら勉強として確認
	 

# 6/27(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [ ] [根岸開発環境構築](https://github.com/Bee2B/eneos-spm/issues/5849)
- [ ] [ENEOS_SPM_KASHIMA-461](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-461)
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
- [ ] GithubActionsの導入

## 変動作業

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査



# 6/30(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [ ] [根岸開発環境構築](https://github.com/Bee2B/eneos-spm/issues/5849)
	- テストデプロイ
- [ ] [ENEOS_SPM_KASHIMA-461](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-461)
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
- [ ] GithubActionsの導入

## 変動作業
- [ ] [Issue](https://github.com/Bee2B/eneos-spm/issues/5856)にdatadogについてのことをまとめる

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査


# 7/1(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [x] [根岸開発環境構築](https://github.com/Bee2B/eneos-spm/issues/5849)
	- テストデプロイ
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
- [ ] GithubActionsの導入

## 変動作業
- [ ] [Issue](https://github.com/Bee2B/eneos-spm/issues/5856)にdatadogについてのことをまとめる

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査



# 7/2(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
- [x] [根岸開発環境構築](https://github.com/Bee2B/eneos-spm/issues/5849)
	- テストデプロイ
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)
- [ ] selenium-grid
	- [ ] datadogでmemory使用率メトリクスを追加
- [ ] GithubActionsの導入

## 変動作業
- [ ] [Issue](https://github.com/Bee2B/eneos-spm/issues/5856)にdatadogについてのことをまとめる

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査


# 7/3(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
	- 進捗でduyさん動けないか調整完了
- [ ] GithubActionsの導入

## 変動作業
- [ ] [Issue](https://github.com/Bee2B/eneos-spm/issues/5856)にdatadogについてのことをまとめる

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査


# 7/4(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 優先事項
- [ ] [ENEOS_KAWASAKI-736](https://vqit.backlog.com/view/ENEOS_KAWASAKI-736)
- [ ] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
	- 進捗でduyさん動けないか調整完了
- [ ] GithubActionsの導入

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査


# 7/7(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 差し込みタスク
- [x] 本番の画像データをS3から取得する
- [x] key名の特定

## 優先事項
- Sentry環境分離の調査
- [x] [ENEOS_KAWASAKI-736](https://vqit.backlog.com/view/ENEOS_KAWASAKI-736)
	- レビュー待ち
- [ ] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
	- 進捗でduyさん動けないか調整中
- [ ] GithubActionsの導入

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査


# 7/8(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
 
## 差し込みタスク
API計測の表作成

## 優先事項
- [ ] Sentry環境分離の調査
- [ ] [DATADOG_GEEKS-8](https://bee2b.backlog.com/view/DATADOG_GEEKS-8)
- [ ] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
	- [ ] datadogでmemory使用率メトリクスを追加
	- 進捗でduyさん動けないか調整中
- [ ] GithubActionsの導入

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査



# 7/9(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [x] 鹿島最新ブランチで根岸ブランチをrebaseする

## 優先事項
- [x] Sentry環境分離についてIssueにまとめる
- [x] [DATADOG_GEEKS-8](https://bee2b.backlog.com/view/DATADOG_GEEKS-8)
- [ ] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査



# 7/10(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [x] [redis空間管理表作成](https://docs.google.com/spreadsheets/d/1akB2hD_6Xk0zSzU1sICYG51DJ0aasD__/edit?gid=1770120747#gid=1770120747) リスト追加

## 優先事項
- [ ] Sentry環境分離について竹口さん宛の叩きを作成する
- [ ] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- [ ] ENEOS23-1458 
	- UserからOfficeRoleを使用するよう修正
- [ ] ENEOS23-1295
- [ ] public/cacheの削除調査



# 7/11(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-503](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-503)
	- 実装は完了したので、月曜日にevidence取ってPR挙げる
- [ ] Sentry環境分離について竹口さん宛の叩きを作成する
- [x] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- Sentryチャンネル分岐の叩き台作成：竹口さん提出用
- pumaについての資料
- Redisについての資料
- 川崎・鹿島のAPI集計


# 7/14(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-503](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-503)
	- 実装は完了したので、月曜日にevidence取ってPR挙げる
- [ ] Sentry環境分離について竹口さん宛の叩きを作成する
- [x] [ENEOS_SPM_KASHIMA-454](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-454)
- [ ] [ENEOS_SPM_KASHIMA-485](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-485)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- Sentryチャンネル分岐の叩き台作成：竹口さん提出用
- pumaについての資料
- Redisについての資料
- 川崎・鹿島のAPI集計


# 7/15(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [ ] load average集計
- [ ] Sentry発報分離

## 優先事項
- [x] Sentry環境分離について竹口さん宛の叩きを作成する
- [ ] [ENEOS_SPM_KASHIMA-485](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-485)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計


# 7/16(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [ ] load average集計
- [ ] Sentry発報分離

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-485](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-485)
- [ ] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計


# 7/17(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [x] load average集計
- [ ] Sentry発報分離

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-442](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-442)
- [x] [ENEOS_SPM_KASHIMA-501](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-501)

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計



# 7/18(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [ ] Sentry発報分離

## 優先事項
- [ ] dev環境redisラベリング対応

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計



# 7/22(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
- [ ] Sentry発報分離
- [x] load average集計

## 優先事項
- [x] datadog問い合わせ
- [x] [ENEOS_SPM_KASHIMA-485](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-485)
- [ ] dev環境redisラベリング対応

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計

---

# 7/23(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [x] Sentry坪井さん質問の回答
- [x] 根岸rebase対応
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島

## 優先事項
- [x] 鹿島STG反映
- [x] dev環境redisラベリング対応
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
	- [x] 麻里布
	- [ ] 根岸
- [ ] [ENEOS_SPM_KASHIMA-514](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-514)

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計

---

# 7/24(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島

## 優先事項
- [x] dev環境redisラベリング対応：cable修正
- [x] [ENEOS_SPM_KASHIMA-514](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-514)
- [ ] API計測

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- pumaについての資料
- 川崎・鹿島のAPI集計

---

# 7/25(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
 
## 差し込みタスク
- [ ] API計測の表作成
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島

## 優先事項
- [x] API計測
- [ ] Redisラベリング
	- [x] dev検証
- [ ] ENEOS_SPM_KASHIMA-501 修正

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- Redisラベリング
	- 手順まとめる
	- 鹿島dev-2
- API計測
	- 川崎
	- 鹿島
- ENEOS_SPM_KASHIMA-501 修正

---

# 7/28(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 差し込みタスク
- [x] https://github.com/Bee2B/eneos-spm/pull/5660#pullrequestreview-3060155121 修正

## 優先事項
- [x] Redisラベリング
	- [x] dev-2-kashima検証
- [x] ENEOS_SPM_KASHIMA-501 修正
- [x] API計測
	- [x] 川崎
	- [x] 鹿島

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降

---

# 7/29(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方

## 差し込みタスク
- [x] [ENEOS23-1993](https://vqit.backlog.com/view/ENEOS23-1993) 画像取得

## 優先事項
- [x] datadog移行手順まとめ
	- PR作成
- [ ] [ENEOS_SPM_MIZUSHIMA-324](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-324) websocketチューニング
- [ ] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降

---

# 7/30(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方

## 差し込みタスク
- [x] STG cron設定

## 優先事項
- [ ] datadog PR作成
- [x] [ENEOS23-1993](https://vqit.backlog.com/view/ENEOS23-1993) 手順まとめ
- [ ] [ENEOS_SPM_MIZUSHIMA-324](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-324) websocketチューニング
- [ ] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善
- [x] 鹿島本番反映

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降

---

# 7/31(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方

## 差し込みタスク

## 優先事項
- [x] 週次定例
- [x] 作業報告書作成
- [x] 査定シート作成
- [x] 月末処理
	- [x] 交通費
	- [x] zac
	- [x] KOT
- [x] datadog PR作成
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
	- [x] 麻里布
	- [x] 根岸
- [ ] SlowQuery対応
- [ ] [ENEOS_SPM_MIZUSHIMA-324](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-324) websocketチューニング
- [ ] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降

* * *

# 8/1(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方

## 差し込みタスク
- [x] [ENEOS23-2009](https://vqit.backlog.com/view/ENEOS23-2009) 【本番】【ENEOS堺】【500エラー】工事>進捗管理 許可証の日付移動時に発生したエラー
- [x] [ENEOS_KAWASAKI-925](https://vqit.backlog.com/view/ENEOS_KAWASAKI-925) 【本番】【ENEOS川崎】【502エラー】B画面：エクスポート時に発生するエラー

## 優先事項
- [x] 月末処理
	- [x] 交通費
	- [x] zac
	- [x] KOT
- [x] datadog PR作成
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
	- [x] 麻里布
	- [x] 根岸
- [x] SlowQuery対応
- [ ] [ENEOS_SPM_MIZUSHIMA-324](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-324) websocketチューニング
- [ ] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降

---

# 8/4(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク
- [x] [ENEOS23-2014](https://vqit.backlog.com/view/ENEOS23-2014) 【本番】【ENEOS堺】【502エラー】担当機器設定>記録>設検検査で保存ボタン押下時に発生するタイムアウトエラー
- [x] [ENEOS23-2012](https://vqit.backlog.com/view/ENEOS23-2012) 【本番】【ENEOS堺】【500エラー】定修：記録>設検記録>保存ボタン押下時にDBのタイムアウトエラーが発生
## 優先事項
- [x] SlowQuery集計
- [ ] ヘルスチェック集計
- [x] datadog集計対象の整理
- [ ] datadog dev/STG反映
	- [ ] 堺
	- [ ] 川崎
	- [ ] 鹿島
	- [ ] 水島
	- [ ] 麻里布
	- [ ] 根岸
- [x] [ENEOS_SPM_MIZUSHIMA-324](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-324) websocketチューニング
	- 伊豆さんが対応してくれたので、私の方での対応は不要
- [ ] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
	- [x] 8/15

## 明日以降


# 8/5(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- セキュリティ委員会の共有をしてもらう。

## 優先事項
- [ ] ヘルスチェック集計
- [ ] datadog dev/STG反映
	- [x] 環境変数シート作成
	- [x] タグ付け
	- [ ] 堺
	- [ ] 川崎
	- [ ] 鹿島
	- [ ] 水島
	- [ ] 麻里布
	- [ ] 根岸
- [x] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善
	- 松本さんにやってもらう

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降

---

# 8/6(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] セキュリティ委員会の共有をしてもらう。

## 優先事項
- [x] ヘルスチェック集計
- [ ] datadog dev/STG反映
	- [ ] 堺
	- [ ] 川崎
	- [ ] 鹿島
	- [ ] 水島
	- [ ] 麻里布
	- [ ] 根岸
- [x] [ENEOS_SPM_MIZUSHIMA-325](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-325) 工事予定表の速度改善
	- 松本さんにやってもらう

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降

---

# 8/7(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] ヘルスチェック集計
- [ ] datadog dev/STG反映
	- [x] 堺
	- [ ] 川崎
	- [ ] 鹿島
	- [ ] 水島
	- [ ] 麻里布
	- [ ] 根岸

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
PR作成 & STG反映
鹿島対応

---

# 8/8(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
- [x] SlowQuery集計
## 差し込みタスク
竹口さんとMTG
## 優先事項
- [x] datadog 
	- [x] PR作成
	- [x] dev反映
	- [x] STG反映
		- [x] 川崎
		- [x] 鹿島
		- [x] 水島
		- [x] 麻里布
		- [x] 根岸

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
鹿島対応
環境変数シート更新
API集計
鹿島マスタ変更

---

# 8/12(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-535](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-535) 鹿島 F画面 作業安全指示書（標準用、検査用）のフォーマット変更にともなう改修
- [x] datadog坪井さん依頼の確認

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/13(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-535](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-535) 鹿島 F画面 作業安全指示書（標準用、検査用）のフォーマット変更にともなう改修

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/14(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-535](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-535) 鹿島 F画面 作業安全指示書（標準用、検査用）のフォーマット変更にともなう改修
- [x] [ENEOS_SPM_KASHIMA-534](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-534) 鹿島 出力した作業安全指示書（標準用、検査用）のフォーマット変更

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/18(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-534](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-534) 鹿島 出力した作業安全指示書（標準用、検査用）のフォーマット変更
	- [x] レビュー
	- [ ] dev反映

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/19(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク

## 優先事項
- [x] 川崎スケールダウンの情報をまとめる 
- [x] [ENEOS_SPM_KASHIMA-534](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-534) 鹿島 出力した作業安全指示書（標準用、検査用）のフォーマット変更
	- [x] レビュー
	- [ ] dev反映
- [ ] [ENEOS_SPM_KASHIMA-536](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-536) 鹿島 E画面 環境設定要否をソート可能にする（残存リスクの下に設ける）

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/20(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-534](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-534) 鹿島 出力した作業安全指示書（標準用、検査用）のフォーマット変更
	- [x] レビュー
	- [ ] dev反映
- [ ] [ENEOS_SPM_KASHIMA-536](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-536) 鹿島 E画面 環境設定要否をソート可能にする（残存リスクの下に設ける）

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- DEMO環境の再起動（datadog環境変数反映）

---

# 8/21(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク


## 優先事項
- [x] [ENEOS_SPM_KASHIMA-536](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-536) 鹿島 E画面 環境設定要否をソート可能にする（残存リスクの下に設ける）
- [ ] アプリケーションログの精査
- [ ] バックアップ内容の調査
- [ ] DEMO環境の再起動（datadog環境変数反映）
## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- [ENEOS_SPM_KASHIMA-556](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-556) 鹿島 E画面 新規作成ボタン押下時の新規作成モーダルの「責任者」と「酸欠主任者」を削除
- [ENEOS_SPM_KASHIMA-555](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-555) 鹿島 E、F 1項目ワーディングの修正と1項目カードの色を紺色からオレンジ色にする
- [ENEOS_SPM_KASHIMA-554](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-554) 鹿島 HOME セキュリティ要件として、GM及びTLが設定画面のユーザ一覧に遷移時、自身の所属している部署のユーザしか一覧に表示されないように制限する

---

# 8/22(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク


## 優先事項
- [x] [ENEOS_SPM_KASHIMA-536](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-536) 鹿島 E画面 環境設定要否をソート可能にする（残存リスクの下に設ける）更新
	- [ ] FEレビュー
- [ ] アプリケーションログの精査
	- 金澤さんから交渉して欲しいと依頼された。交渉材料として何があるか確認 → 千葉さんに確認中
- [ ] バックアップ内容の調査
- [x] DEMO環境の再起動（datadog環境変数反映）
	- 15:30 ~
- [x] ヘルスチェック 閾値決定
- [x] Jobについての調査
	- [[完了：0825 Jobについての調査]]
- [ ] datadogの本番手順をBacklogにまとめて坪井さんからレビューをもらう
## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- レビュー
	- https://github.com/Bee2B/eneos-spm/pull/6737
	- https://github.com/Bee2B/eneos-spm/pull/6732
	- https://github.com/Bee2B/eneos-spm/issues/6736

---

# 8/25(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク


## 優先事項
- [x] [ENEOS_SPM_KASHIMA-536](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-536) 鹿島 E画面 環境設定要否をソート可能にする（残存リスクの下に設ける）更新
	- [x] FEレビュー
- [ ] アプリケーションログの精査
	- 金澤さんから交渉して欲しいと依頼された。交渉材料として何があるか確認 → 千葉さんに確認中
- [ ] バックアップ内容の調査
- [x] datadogの本番移行手順をBacklogにまとめて坪井さんからレビューをもらう
- [ ] datadogとcloudwatchの料金比較
- [x] インフラ提案v3 sidekiq等の捕捉事項入力
	- [x] sidekiqにより実行される内容
	- [x] elasticacheで保持する内容
	- [x] lambdaでanalyzeJobが実行できるのか
	- [x] analyzeJobの実行時間はどんなもんか
## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計
- レビュー
	- https://github.com/Bee2B/eneos-spm/pull/6737
	- https://github.com/Bee2B/eneos-spm/pull/6732
	- https://github.com/Bee2B/eneos-spm/issues/6736


---

# 8/26(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク


## 優先事項
- [ ] アプリケーションログの精査
	- 金澤さんから交渉して欲しいと依頼された。交渉材料として何があるか確認 → 千葉さんに確認中
- [x] バックアップ内容の調査
- [ ] datadogとcloudwatchの料金比較
## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 8/27(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク


## 優先事項
- [ ] アプリケーションログの精査
	- 金澤さんから交渉して欲しいと依頼された。交渉材料として何があるか確認 → 千葉さんに確認中
- [ ] datadogとcloudwatchの料金比較
- [ ] [[0728 datadog移行対応]]
- [ ] 千葉開発環境作成
## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計

---

# 8/28(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク


## 優先事項
- [x] [ENEOS_SPM_KASHIMA-559](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-559) 
	- [x] STG反映
	- [x] 本番反映
- [x] [[0828 アプリケーションログの精査]]
	- 最低限
- [ ] [[0728 datadog移行対応]]
- [ ] 千葉開発環境作成
- [ ] 保守対応チケット表作成

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] datadogとcloudwatchの料金比較
- [ ] [B2B_INFRA-108](https://appirits.backlog.jp/view/B2B_INFRA-108) ENEOS千葉用のサブドメイン作成

---

# 8/29(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [ ] [[0728 datadog移行対応]]
- [x] 千葉開発環境作成
	- [x] [B2B_INFRA-108](https://appirits.backlog.jp/view/B2B_INFRA-108) ENEOS千葉用のサブドメイン作成
- [x] 保守対応チケット表作成
- [x] ログ内容についての精査

## 変動作業
- [x] 週次定例
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] datadogとcloudwatchの料金比較

---

# 9/1(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク

## 優先事項
- [ ] [[0728 datadog移行対応]]
- [x] 千葉開発環境作成
- [ ] datadog環境変数設定
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [ ] 水島
	- [ ] 麻里布
	- [ ] 根岸
	- [ ] 千葉
- [ ] インフラ関連調査
- [ ] CloudWatchへログ出力

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/2(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] datadog環境変数設定
	- [x] 堺
	- [x] 川崎
	- [x] 鹿島
	- [x] 水島
	- [x] 麻里布
	- [x] 根岸
	- [x] 千葉
- [ ] インフラ関連調査
	- [ ] SQS移行に伴うpayload調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] CloudWatchへログ出力
- [x] [ENEOS_SPM_KASHIMA-571](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-571) 鹿島 作業安全指示書 撤回したコメントが帳票のコメント欄に表示されてしまう
- [ ] [[ENEOS_SPM_KASHIMA-568 鹿島 協力会社ユーザの編集がバルカー権限が付いていないと行えなくなってしまっている]]


## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---
# 9/3(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク

## 優先事項
- [x] datadog本番移行
	- [x] 堺
	- [x] 鹿島
- [ ] インフラ関連調査
	- [x] SQS移行に伴うpayload調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] CloudWatchへログ出力
- [x] [[ENEOS_SPM_KASHIMA-568 鹿島 協力会社ユーザの編集がバルカー権限が付いていないと行えなくなってしまっている]]


## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---

# 9/4(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] datadog料金についての調査
- [x] datadog本番移行
	- [x] 川崎
- [ ] インフラ関連調査
	- [ ] ログの工数見積もり
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---

# 9/5(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [x] メール送信不備についての調査
- [x] ログイン後の500エラー調査
- [x] 鹿島：本登録対応
- [ ] インフラ関連調査
	- [ ] ログの工数見積もり
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---

# 9/8(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
- ヘルスチェック集計
	- [ ] 堺
	- [ ] 川崎
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [x] ログの工数見積もり
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---

# 9/10(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
- ヘルスチェック集計
	- [x] 堺
	- [x] 川崎
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [x] ログの工数見積もり
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力
- [x] [ENEOS23-2109](https://vqit.backlog.com/view/ENEOS23-2109) 堺：アプリケーションログのログローテートを30日に変更する
- [x] 鹿島本番反映
- [x] STGのログローテートを有効化する
	- [x] 堺
	- [x] 川崎

## 変動作業
- [ ] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請
- [ ] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]

## 明日以降
- 環境変数シート更新
- API集計
- [ ] [[ENEOS_SPM_KASHIMA-446 鹿島 鹿島 F画面 入力必須の制御]]

---
# 9/11(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力
- [x] [[完了：0827 ENEOS_SPM_MARIFU-229 datadog設定関連]]
- [x] 堺のサーバースケールダウン資料作成
- [ ] datadogアラート設定閾値の頭出し資料作成
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [ ] datadogのアカウント発行
- [ ] スケールダウンの資料をDirectCloudにアップして山下さんに連携

## 変動作業
- [x] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/12(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力
- [ ] datadogアラート設定閾値の頭出し資料作成
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [ ] datadogのアカウント発行
- [x] スケールダウンの資料をDirectCloudにアップして山下さんに連携

## 変動作業
- [x] Sentry発報分離
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/16(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [x] [SPM_INFRA-2](https://vqit.backlog.com/view/SPM_INFRA-2) 【Datadog】監視不要インスタンスの設定対応
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力
- [ ] datadogアラート設定閾値の頭出し資料作成
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [x] datadogのアカウント発行

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/17(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [x] 鹿島レビュー
	- [x] [ENEOS_SPM_KASHIMA-446](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-446) 鹿島 鹿島 F画面 入力必須の制御
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
	- [ ] CloudWatchへログ出力
- [ ] datadogアラート設定閾値の頭出し資料作成
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [x] SlowQuery調査
- [ ] ログ工数出し

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [ ] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/18(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [x] ログ工数出し
- [x] dev反映・検証
- [ ] ログ工数の詳細調査と松竹梅のオプション作成

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
- [x] 夏季休暇申請

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/19(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [ ] ログ工数の詳細調査と松竹梅のオプション作成
- [ ] [ENEOS_SPM_KASHIMA-583](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-583) 鹿島 F画面のネットワーク接続エラー対応 ※堺流用
- [x] datadogのチケット作成
- [ ] 鹿島PR作成
	- F画面のsocket対応は入れれたら入れる
	- 6つのコミットは入れて松本さんに共有する

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- 環境変数シート更新
- API集計

---
# 9/24(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [x] ログ工数の詳細調査と松竹梅のオプション作成
- [x] 鹿島本番反映

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/25(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査
- [ ] sentryのアーカイブ対応
- [x] 週次定例
- [x] [ENEOS_KAWASAKI-965](https://vqit.backlog.com/view/ENEOS_KAWASAKI-965) 【本番】【ENEOS川崎】【500エラー】ファイルサイズが0Bの画像をアップロードした際に発生するエラー【DBデータ削除の一時対応チケット】

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/29(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査
- [x] sentryのアーカイブ対応
- [x] [ENEOS_SPM_MIZUSHIMA-397](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-397) 水島 意見集約 #96 サイドメニューの下部にある「管理画面」の導線非表示

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入

## 明日以降
- 環境変数シート更新
- API集計

---

# 9/30(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] 月末処理
	- [x] KOT
	- [x] 交通費
	- [ ] ZAC
- [x] 稼働請求
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---
# 10/1(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS_SPM_KASHIMA-585](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-585) 鹿島 E、F 該当のGr、施工者でなくともコメント欄をクリック時、読み取り専用でコメントのモーダルを開くようにする

## 優先事項
- [ ] インフラ工数見積もり
	- [x] ログ工数整理
	- [x] ECS整理
- [x] 月末処理
	- [x] KOT
	- [x] 交通費
	- [x] ZAC
- [x] 稼働請求
- [x] SlowQuery集計
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計
---

# 10/2(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] 週次定例
- [ ] インフラ工数見積もり
	- [ ] ログ工数整理（標準出力に変更した場合の工数）
		- [x] gov-devあたり触らせてもらう
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---
# 10/3(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] 麻里布STG反映
- [x] 麻里布本番反映

## 優先事項
- [ ] インフラ工数見積もり
	- [x] ログ工数整理（標準出力に変更した場合の工数）
	~~- [ ] nginxをシステムログへ出力~~
	- [ ] crontab.logをシステムログへ出力
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---
# 10/6(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] インフラ工数見積もり
- [x] payload調査
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] インフラ関連調査
	- [ ] メール送信`Lambda + SES`の補強調査
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/7(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x]  [[1007 川崎：パスワード再設定対応]]
- [ ] [[1007 permitsエラーの調査]]

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-497](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-497) 【本番】【ENEOS鹿島】【500エラー】E画面：開始-終了において当日or翌日の変更を試みた際に発生するエラー
- [ ] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/8(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [[1007 permitsエラーの調査]]

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-497](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-497) 【本番】【ENEOS鹿島】【500エラー】E画面：開始-終了において当日or翌日の変更を試みた際に発生するエラー
- [x] SlowQuery集計・調査
- [ ] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [x] 竹口さんへ水島datadogのスケジュール連絡
- [ ] SentryのPlan報告

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/9(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS_SPM_MARIFU-335](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-335) 【本番】【ENEOS麻里布】【500エラー】許可証から辿れるはずの不具合報告書が存在しないため発生した遅延アラートメールの送信エラー

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [ ] SentryのPlan報告
- [x] 鹿島STG 本番反映
- [x] 麻里布STG 本番反映

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---
# 10/10(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS_SPM_MARIFU-336](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-336) 【本番】【500エラー】【ENEOS麻里布】B > 添付(画像/PDF/Excel/Word/PowerPoint)：アップロード対象外のデータをアップロードして発生する変換エラー

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [ ] SentryのPlan報告

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計


---

# 10/14(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
- [ ] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [x] SentryのPlan報告
- [x] ENEOS会

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/15(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク
- [x] [ENEOS_SPM_MARIFU-343](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-343) 【本番】【ENEOS麻里布】【500エラー】お知らせ新規登録 or 編集時に、日付で過剰な値の設定を試みた場合に発生するエラー
- [x] [ENEOS_SPM_KASHIMA-593](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-593) 【本番】【ENEOS鹿島】【500エラー】E画面：バッチによる絞り込みをしている状態のURLを、別タブや別ウィンドウにコピペしてE画面を開いた際に発生するエラー

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
- [ ] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [x] SlowQuery調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/16(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
- [ ] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
	- vuさんがいつのまにか対応していた。BEの対応も必要だろうから中身見る。
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [x] [ENEOS_SPM_MIZUSHIMA-399](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-399) 水島 意見集約 #110 エリア/Tmの紐づけ設定
- [ ] wardenの調査
- [x] 週次定例

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- API集計

---

# 10/17(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
- [x] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
	- vuさんがいつのまにか対応していた。BEの対応も必要だろうから中身見る。
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---

# 10/20(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
	- [x] 施工者
	- [ ] 工事担当
	- [ ] 施設担当
- [x] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
	- レビュー待ち
- [ ] 502エラーの解消予定計画の作成
	- 種類分ける。それぞれの対応予定を出す。
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---

# 10/21(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS23-1616](https://vqit.backlog.com/view/ENEOS23-1616) マルチアプリケーションデプロイ時のsidekiq指定
	- [ ] demo-kawasakiを明日対応

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
	- [x] 施工者
	- [ ] 工事担当
	- [ ] 施設担当
- [x] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更
	- レビュー待ち
- [ ] 502エラーの解消予定計画の作成
	- 種類分ける。それぞれの対応予定を出す。
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---

# 10/22(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS23-1616](https://vqit.backlog.com/view/ENEOS23-1616) マルチアプリケーションデプロイ時のsidekiq指定
	- [ ] demo-kawasakiを明日対応

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 鹿島 リマインドメール追加 施工者-作業完了、工事担当・施設担当-工事完了ボタン未押下時のリマインドメール配信
	- [x] 施工者
	- [x] 工事担当
	- [x] 施設担当
- [ ] ElastiCache対応
	- [ ] 明日
- [x] 麻里布本番反映
- [ ] 502エラーの解消予定計画の作成
	- 種類分ける。それぞれの対応予定を出す。
- [x] SlowQuery集計
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- 環境変数シート更新

---

# 10/23(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS23-1616](https://vqit.backlog.com/view/ENEOS23-1616) マルチアプリケーションデプロイ時のsidekiq指定
	- [ ] demo-kawasakiを明日対応

## 優先事項
- [x] ElastiCache対応
- [x] [ENEOSCHIBA-94](https://vqit.backlog.com/view/ENEOSCHIBA-94) 千葉STG環境構築
- [ ] 502エラーの解消予定計画の作成
	- 種類分ける。それぞれの対応予定を出す。
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---
# 10/24(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS23-1616](https://vqit.backlog.com/view/ENEOS23-1616) マルチアプリケーションデプロイ時のsidekiq指定
	- [x] demo-kawasakiを明日対応

## 優先事項
- [x] ElastiCache対応
	- [x] シナリオテストの確認
	- [x] gov-devとdev2のElastiCache利用
- [x] 鹿島開発環境反映
- [ ] 502エラーの解消予定計画の作成
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---

# 10/27(月)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] ANS申請
- [x] 松田さん問い合わせ調査
- [ ] freee確認

## 優先事項
- [x] ElastiCache対応
	- [x] STG検証
- [ ] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 
	- [x] 休日の考慮
- [ ] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 
	- [ ] vuさんの修正確認
- [ ] 502エラーの解消予定計画の作成
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新

---

# 10/28(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] freee確認

## 優先事項
- [x] [ENEOS_SPM_KASHIMA-586](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-586) 
- [x] [ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 
	- [x] vuさんの修正確認
- [ ] 502エラーの解消予定計画の作成
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- 大分開発環境作成（今週中期限）
- EOL対応とECS以降の大雑把なスケジュール作り
- 11月の鹿島・麻里布の工数確認


---

# 10/29(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] freee確認

## 優先事項
- [x] 鹿島STG検証
- [x] 水島レビュー確認
- [x] 鹿島本番反映
- [x] ElastiCache対応
- [x] SlowQuery
- [ ] 502エラーの解消予定計画の作成
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- 大分開発環境作成（今週中期限）
- EOL対応とECS以降の大雑把なスケジュール作り
- 11月の鹿島・麻里布の工数確認

---

# 10/30(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] レイテンシー爆増APIの調査
	- [x] 川崎
	- [x] 麻里布
- [x] アイレットへの説明MTG

## 優先事項
- [x] 週次定例
- [ ] 大分開発環境作成
- [x] 麻里布本番反映
- [x] 鹿島・麻里布500エラーの調査とチケット化
- [ ] 502エラーの解消予定計画の作成
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- EOL対応とECS以降の大雑把なスケジュール作り
- 11月の鹿島・麻里布の工数確認
- 堺サーバースケールダウン資料作り

---

# 10/31(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] 大分開発環境作成
- [x] 稼働報告書作成
- [ ] 月末処理
	- [x] KOT
	- [ ] ZAC
	- [x] 交通費申請
- [ ] wardenの調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- EOL対応とECS以降の大雑把なスケジュール作り
- 11月の鹿島・麻里布の工数確認
- 堺サーバースケールダウン資料作り
- メール誤送についての原因報告（山邊さん宛て）

---

# 11/4(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] 月末処理
	- [x] ZAC
- [ ] wardenの調査
- [ ] [ENEOS_SPM_KASHIMA-598](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-598) 【本番】【ENEOS鹿島】作業完了をしている施工者にリマインドメールを誤送信してしまう

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- EOL対応とECS以降の大雑把なスケジュール作り
- 11月の鹿島・麻里布の工数確認
- 堺サーバースケールダウン資料作り
- メール誤送についての原因報告（山邊さん宛て）

---

# 11/5(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] wardenの調査
- [x] [ENEOS_SPM_KASHIMA-598](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-598) 【本番】【ENEOS鹿島】作業完了をしている施工者にリマインドメールを誤送信してしまう 
- [x] 本番反映
- [x] EOL対応とECS以降の大雑把なスケジュール作り
- [ ] 堺サーバースケールダウン資料作り
- [x] SlowQuery調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- 11月の鹿島・麻里布の工数確認
- メール誤送についての原因報告（山邊さん宛て）

---

# 11/6(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] wardenの調査
- [x] 堺サーバースケールダウン資料作り
- [ ] 麻里布工数だし
- [ ] 竹口さんへの返信
- [ ] 千葉本番サーバー構築に向けての状況整理

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- 11月の鹿島・麻里布の工数確認
- メール誤送についての原因報告（山邊さん宛て）
- convertAPIの利用状況・制限の調査


---

# 11/7(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] 麻里布工数だし
- [ ] 竹口さんへの返信
- [ ] 千葉本番サーバー構築に向けての状況整理
- [x] datadogMTG
- [x] 鹿島・お問い合わせ調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- convertAPIの利用状況・制限の調査
- [ ] wardenの調査
- [ ] 鹿島の完了IssueをCLOSEしていく


---

# 11/10(月)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] 鹿島工数見積もり

## 優先事項
- [ ] 竹口さんへの返信
- [ ] 千葉本番サーバー構築に向けての状況整理
- [ ] convertAPIの利用状況・制限の調査
- [x] インフラコスト計算のための利用料調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- [ ] wardenの調査
- [ ] 鹿島の完了IssueをCLOSEしていく

---

# 11/11(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] 鹿島工数見積もり
- [x] 保守：見積書作成

## 優先事項
- [ ] 千葉本番サーバー構築
	- [x] 開発環境構築
		- [x] 末松さんへ依頼
- [ ] convertAPIの利用状況・制限の調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- [ ] wardenの調査
- [ ] 鹿島の完了IssueをCLOSEしていく

---

# 11/12(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク
- [x] 鹿島工数見積もり
- [x] 黒沢さんのfree 1Passwordで共有

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [ ] [ENEOS_SPM_MARIFU-431](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-431) 麻里布 ガス検が表示されないことがある

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- [ ] wardenの調査
- [ ] 鹿島の完了IssueをCLOSEしていく

---

# 11/13(木)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [ ] 千葉本番サーバー構築
- [x] 水島datadog導入
- [ ] convertAPIの利用状況・制限の調査
- [ ] [ENEOS_SPM_MARIFU-431](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-431) 麻里布 ガス検が表示されないことがある
- [ ] [ENEOS_SPM_MARIFU-396](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-396) 麻里布 F 完了確認欄のONOFF連動

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- [ ] wardenの調査
- [ ] 鹿島の完了IssueをCLOSEしていく


---

# 11/14(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 水島本番反映
- [x] 麻里布本番反映
- [x] [ENEOS_SPM_MARIFU-431](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-431) 麻里布 ガス検が表示されないことがある
- [x] [ENEOS_SPM_MARIFU-396](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-396) 麻里布 F 完了確認欄のONOFF連動

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- 環境変数シート更新
- メール誤送についての原因報告（山邊さん宛て）
- [ ] wardenの調査
- [x] 鹿島の完了IssueをCLOSEしていく

---

# 11/17(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [x] セキュリティチェックシート（木曜まで）
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/18(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [ ] セキュリティチェックシート（木曜まで）
	- [ ] 内部レビュー
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/19(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [ ] セキュリティチェックシート（木曜まで）
	- [ ] 内部レビュー
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査


---

# 11/20(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [x] セキュリティチェックシート（木曜まで）
	- [x] 内部レビュー
	- [x] 資料突き合わせ
	- [x] 間山さんレビュー
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
	- [x] ヴァンさんに依頼
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 年末調整

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/21(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [x] セキュリティチェックシート（木曜まで）
	- [x] 諸々MTG
	- [x] 提出資料作成
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
	- [x] ヴァンさんレビュー
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/25(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [ ] RDSのスパイク調査

## 優先事項
- [ ] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
	- [ ] dev反映
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 資格申請

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査


---

# 11/26(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] 鹿島本番反映
	- [x] [ENEOS_SPM_KASHIMA-587](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-587) 鹿島 B 「勧告事項」のチェックボックスを設け、ONの場合、B画面の必須制御の変更
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] SlowQuery調査
- [ ] 麻里布レビュー
- [ ] 大分STG環境作成

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/27(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 麻里布本番反映
	- [x] 開発環境
	- [x] STG環境
- [ ] 麻里布実装
- [ ] 大分STG環境作成
	- [ ] inquery_type確認

## 変動作業
- [ ] selenium-gridの導入
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 11/28(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [ ] [ENEOS_SPM_MARIFU-442](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-442) 麻里布 帳票 文言変更と工事完了の日付を反映できるようにする
- [ ] [ENEOS_SPM_MARIFU-443](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-443) ホームスクリーンログ取得
- [ ] 大分STG環境作成
	- [ ] inquery_type確認
- [ ] 月末処理
	- [x] KOT
	- [x] 交通費申請
	- [ ] ZAC
- [x] 作業報告書作成

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---


# 12/1(月)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] [ENEOS_SPM_MARIFU-442](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-442) 麻里布 帳票 文言変更と工事完了の日付を反映できるようにする
- [x] [ENEOS_SPM_MARIFU-443](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-443) ホームスクリーンログ取得
- [ ] 大分STG環境作成
	- [ ] inquery_type確認
- [x] 月末処理
	- [x] KOT
	- [x] 交通費申請
	- [x] ZAC

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/2(火)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 麻里布STG反映
	- [x] [ENEOS_SPM_MARIFU-442](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-442) 麻里布 帳票 文言変更と工事完了の日付を反映できるようにする
- [x] 大分STG環境作成
	- [x] inquery_type確認

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/3(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] [ENEOS23-2210](https://vqit.backlog.com/view/ENEOS23-2210) 【本番】【ENEOS堺】【500エラー】B画面：変換対象にない形式（SVG、DWG）のファイルを添付し、保存ボタンを押下した際に発生するエラー

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 麻里布本番反映
- [x] コスト算出表の作成
- [x] SlowQuery集計

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査


---

# 12/4(木)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] マニュアルサーバー調査
- [ ] コスト・体制資料作り

## 優先事項
- [x] 堺スケールダウン
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [ ] 麻里布実装

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/5(金)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [ ] 麻里布実装

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/8(月)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [x] セキュリティチェックシート
- [ ] 千葉本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [x] 麻里布実装
- [ ] 忘年会

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/9(火)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク

## 優先事項
- [ ] 千葉・大分本番サーバー構築
- [ ] convertAPIの利用状況・制限の調査
- [ ] 忘年会予約
	- [x] ビールサーバー
	- [x] オードブル
	- [x] ピザ
	- [ ] 小物
- [ ] 鹿島実装
- [ ] 502調査
- [x] コスト算出

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/10(水)
## 通常作業
- 500アラートメール確認
	- [x] 出社後
	- [x] お昼
	- [x] 夕方
## 差し込みタスク
- [x] セキュリティチェックシート

## 優先事項
- [x] 千葉・大分本番サーバー構築
- [x] 忘年会予約
	- [x] ビールサーバー
	- [x] オードブル
	- [x] ピザ
	- [x] 小物
	- [x] 占い師
- [ ] 鹿島実装
- [ ] 502調査

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査

---

# 12/10(水)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク
- [x] 集計作業

## 優先事項
- [x] 遅延申請
- [ ] 忘年会予約
	- [ ] 当日の担当割り振り
- [x] 週次定例
- [ ] 鹿島実装
- [ ] 502調査
- [ ] 千葉・大分
	- [ ] datadog導入

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査


---

# 12/11(金)
## 通常作業
- 500アラートメール確認
	- [ ] 出社後
	- [ ] お昼
	- [ ] 夕方
## 差し込みタスク

## 優先事項
- [ ] 忘年会
	- [x] 全体連絡
	- [ ] 担当割り振り連絡
- [ ] 鹿島実装
- [ ] 502調査
- [ ] 千葉・大分
	- [ ] datadog導入

## 変動作業
- [ ] GithubActionsの導入
## 明日以降
- [ ] 環境変数シート更新
- [ ] wardenの調査