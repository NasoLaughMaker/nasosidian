[puma integration](https://docs.datadoghq.com/ja/integrations/puma/)

## 作業手順
- [x] EC2にタグ付け（AWS内でタグ付け）
	- タグのvalueは何がよいか
- [ ] 環境変数の設定
- [ ] デプロイ
- [ ] datadog-agentの設定


# TODO
- [x] pumaメトリクスを収集するため、`config/puma.rb`にcontrol_urlとcontrol_tokenを設定する
- [x] serviceファイルに`DD_ENV`と`DD_SERVICE`を設定する


```
c3BtLWVuZW9zLXdlYmFwcC1zYWthaQ==

Environment="DD_ENV=stg"

Environment="DD_SERVICE=spm-eneos-webapp-kawasaki"
```

- [ENEOS_SPM_KASHIMA-546](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-546) 鹿島：Datadog Organization移行
	- [PR](https://github.com/Bee2B/eneos-spm/pull/6587)
- [ENEOS_KAWASAKI-934](https://vqit.backlog.com/view/ENEOS_KAWASAKI-934) 川崎：Datadog Organization移行
	- [PR](https://github.com/Bee2B/eneos-spm/pull/6587)
- [ENEOS_SPM_MIZUSHIMA-361](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-361) 水島：Datadog Organization移行
	- [PR](https://github.com/Bee2B/eneos-spm/pull/6591)
- [ENEOS_SPM_MARIFU-219](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-219) 麻里布：Datadog Organization移行
	- [PR](https://github.com/Bee2B/eneos-spm/pull/6592)
- [ENEOS_SPM_NEGISHI-90](https://vqit.backlog.com/view/ENEOS_SPM_NEGISHI-90) 根岸：Datadog Organization移行
	- [PR](https://github.com/Bee2B/eneos-spm/pull/6593)

# 0827 TODO
- [x] 鹿島の日程調整
- [ ] 不要なサービスファイルの調査

# 0828 TODO
- [x] datadogの設定不備について坪井さんと擦り合わせる
	- 対応方針
		- RUMに渡す `DD_SERVICE` を `RUM_DD_SERVICE` など別名にすることで `/etc/environment` 内で `DD_SERVICE` を使わないようにする。


# メトリクスの収集をやめる
- EC2にタグを付与し、[integration > Metric Collection](https://ap1.datadoghq.com/integrations?accountId=1fdc0afd-2d80-491a-97eb-2c4f0e7f849a&integrationId=amazon-web-services&panel=metric-collection)

# Audit Trail
datadog内のCloudTrailみたいなもの
有効化には追加料金が必要