[puma integration](https://docs.datadoghq.com/ja/integrations/puma/)

## 作業手順
- [ ] EC2にタグ付け（AWS内でタグ付け）
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
- [ENEOS_SPM_MIZUSHIMA-361](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-361) 水島：Datadog Organization移行
- [ENEOS_SPM_MARIFU-219](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-219) 麻里布：Datadog Organization移行