[slack](https://beeb-jp.slack.com/archives/C098QLPFN3T/p1753929828673029?thread_ts=1753929768.713029&cid=C098QLPFN3T)
[[SlowQuery]]

### 現状
[CloudWatch Logs](https://ap-northeast-1.console.aws.amazon.com/cloudwatch/home?region=ap-northeast-1#logsV2:log-groups/log-group/$252Faws$252Frds$252Fcluster$252Fene-prd-db-cluster$252Fslowquery)にストリームしている。
フィルター設定は行っていないため、整理できてはいない。

### TODO
- [ ] QueryTimeでソートができるようにする
	- 正規表現でSlowQueryだけカラムとして抜き出す


### Logs Insigthsを用いた分析
https://tech.excite.co.jp/entry/2023/02/17/114538
#### クエリタイムの長い順に100件取得
```
fields @timestamp, @message
| parse @message /Query_time:\s*(?<Query_time>[0-9]+(?:\.[0-9]+)?)\s*[\s\S]*?;/
| display @timestamp, Query_time, @message
| sort Query_time desc
| limit 100
```


## 運用方針
毎週金曜日に木曜日分の集計を行います。
基本的に水曜日が本番反映日であるため、反映後1日間のSlowQueryを収集することで定点観測を行う想定でおりますがいかがでしょうか。