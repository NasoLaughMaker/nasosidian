[ENEOS23-689](https://vqit.backlog.com/view/ENEOS23-689) ２500エラーなど異常検知
[Issue](https://github.com/Bee2B/eneos-spm/issues/6133)

# TODO
https://bee2b.sentry.io/alerts/rules/?project=6663047&statsPeriod=24h
READ ONLYで設定方法や懸念点などをまとめて千葉さんに報告。
DEV → STG → 本番 で設定していく。

どこまで詳細に分けるのかは要相談。全envでチャンネル作る？

通知内に環境を載せられるならそれもやりたい

# 設定方法
Alerts > Create Alert > Errors > Issues > Set Conditions
上記で設定画面に遷移
以下を選択
### Select an environment and project
以下を選択
- env
	- 指定のenv
- Projects
	- valqua-spm

### Set Conditions
以下を選択
- WHEN
	- all
	- optional triggerは未設定で良い
- IF
	- all
	- optional triggerは未設定でよい
- THEN
	- Send a Slack notifications
		- Bee2B Co. Ltd.
		- チャンネル名
		- チャンネルID
		- env（tags）
	- Suggested Assignees, Team, or Member（メール通知...オプション）
		- Member

### Set action interval
同エラーが何分おきに通知されるか（最初の1回目以降は通知しない）

### Add a name and owner
作成するアラートの名前とオーナーを設定


## 懸念点
- 現在のアラート設定をいじるのは怖いので後回し。
- dev環境ならSentryもどちらもBee2Bの所有物なので、アラートを追加する形で実験的に対応できると思う。そこでevidenceをとってSTGに反映。最後に本番？
- 本番は編集するというより、新たに作成して問題ないことを確認したら、既存を削除するでもよい。

## 作成するチャンネル
- 汎用版
	- production（汎用・汎用保全）
- ENEOS
	- production（堺）
	- kashima-eneos
	- kawasaki-eneos
	- mizushima-eneos
- 汎用STG
	- STG2
- ENEOSSTG
	- eneos-stg
	- sakai-eneos-stg
	- kawasaki-eneos-stg
	- demo-kawasaki-eneos-stg
	- kashima-eneos-stg
	- mizushima-eneos-stg
	- marifu-eneos-stg
	- negishi-eneos-stg
- 汎用dev
	- dev-zero
- ENEOSdev
	- dev
	- gov-dev
	- dev-2-kashima
	- dev-2-mizushima
	- dev-2-marifu

### 不明 & 懸念
- production
	- 汎用版、sakaiが混ざっているので将来的に分ける必要がある。
	- 現在RAILS_ENVで分かれているので、SENTRY_ENVの設定が必要。

### 不要
- dev-zero-2

## 竹口さんへの提案
チケットで管理する。
テキストベースでチャンネル構成の叩き台を作成し、竹口さんへ連携。議題として挙げてもらう。

例）
最大何チャンネル
最小何チャンネル

いかがですか？


```
@竹口 CC: @VQ山邊 @masakazu kanazawa @千葉 孝博 @松本 紘幸 
## Sentry発報チャンネル分離について
現在全環境のSentryアラートが `#valqua-spm-alert`に発報されているため、チャンネル分離を行い、担当者がエラーを適切に検知できるように整備します。

[こちら](https://vqit.backlog.com/view/ENEOS23-689#comment-571867236)にてDEV環境のアラート分離が確認できたため、STGでの分離を行いたいと考えております。
チャンネル分離にあたり、発報チャンネルを以下のように用意したいのですが、いかがでしょうか。

### 汎用版
- 本番
- STG
- DEV

### ENEOS
- 本番
- STG
- DEMO
- DEV
```

# TODO
## 本番分離
汎用
- [ ] 汎用
- [ ] 汎用保全

ENEOS
- [ ] sakai-eneos
- [ ] kawasaki-eneos
- [ ] kashima-eneos
- [ ] mizushima-eneos

## STG分離
汎用
- [x] stg2

ENEOS
- [x] sakai-eneos-stg
- [x] kawasaki-eneos-stg
- [x] kashima-eneos-stg
- [x] mizushima-eneos-stg
- [x] marifu-eneos-stg
- [x] negishi-eneos-stg

## DEV分離
汎用
- [ ] dev-zero

ENEOS
- [x] dev
- [x] gov-dev
- [x] dev-2-kashima
- [x] dev-2-mizushima
- [x] dev-2-marifu
- [x] dev-2-negishi

## 環境変数設定
- [ ] 堺本番
- [ ] 汎用本番