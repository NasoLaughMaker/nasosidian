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
	- [ ] 夕方
- [ ] ヘルスチェック集計
## 差し込みタスク
竹口さんとMTG

## 優先事項
- [ ] datadog PR作成/dev/STG反映
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