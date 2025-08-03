https://www.youtube.com/watch?v=a6cootrnGP8
# AWSのログ管理を一新し、課題を解決するには
## ログ管理とセキュリティ強化
既知の障害ー＞モニタリング
未知の障害ー＞オブザーバビリティ

keyword
- メトリクス
- ログ
	- 属性状況などの構造化されたログ
- トレース
	- 個別トランザクション

- NIST ST800-61r2
	- 準備
	- 検知と分析
	- 封じ込め/根絶/復旧
	- 事後対応

### イベントの適切な把握
収集・保存だけでなく検知と分析の両方で活用できるように

### 継続的な脅威モニタリングlolllll


## AWSとDatadogによる統合オブザーバビリティ
- CloudTrail
- CLoudWatch
- Flow Logs
- Config
- DNS Logs
- GuardDuty
👇
- Data Firehose
	- 機密情報のマスキングなど
- LambdaForwarder
	- メタデータの付与
	- 不必要な情報を除外
- **Datadog Agent**
	- EC2、コンテナ、Lambdaから取得
- Datadog Observability PiplelinesでAWS上のアプリケーション、セキュリティイベントを集約・整形し、Datadogで活用
- S3にアーカイブ、必要なタイミングでDatadogから活用

## CloudWatch
監視の集約
分析・トラブルシューティング

### CloudWatch Logs
Datadogに流すことも可能
### CLoudWatch Metrics
AWSのさまざまなサービスのメトリクスを基本無料で提供
### Container Insights
コンテナ化されたアプリのメトリクスとログを収集・集計・要約
タスク・コンテナレベルでの監視
### Lambda Insights
Lambda関数のモニタリング
Lambdaの拡張機能
これを使用することでLambda関数のCPU/メモリなども収集できるようになる
### Database Insights
数百のDBにわたる構成のフリート全体のビュー
SQLクエリメトリクス

## GuardDuty
不審なアクティビティを継続的にモニタリングすることができる脅威検知サービス
### 保護プラン
- S3 Protection
- EKS Protection
- Malware Protection
- RDS Protection
- Lambda Protection
- Runtime Monitoring

### 拡張脅威検出機能を発表
他段階攻撃を検知できるようになった
→ 一つ一つじゃなく、シーケンスとして攻撃を検知


## Datadog
### ログマネジメント
ログデータは指数関数的に増加している。
### 加速するログ量と複雑化する管理の背景
以下の理由からログがめちゃくちゃ増えている
- マルチクラウドの管理
- コンテナの採用
	- 短命で起動・終了が活発
- SaaS利用の拡大

### 課題
- ログが分断し、全体像が把握しにくい
- 操作性のハードルが高く、限られた人しか扱えない
	- クエリなど
- ログの増加にシステムが追いつかない
- 保管コストの高さと価値の低いログも蓄積され続ける

## 適切なログ管理に必要なもの
- 一元化
	- あらゆる種類のログを集約
- 使いやすさ
	- ログを検索・分析
- スケーラビリティ
	- ログ量が増えても保管できる
- コスト最適化
→これを提供しているのがDatadog
- WatchDogInsights機械学習を導入

## ログ管理における3つのステップ
### 収集
#### 3つの手段がある
- datadog agent
- Cloud Integration
	- AWSなどから転送
		- S3
- その他
	- プラグインを使用してDatadogへ直接送信
 #### パイプラインでログをエンリッチ
 ログを整形可能→ Observability Pipeline

 #### デモ
Logs > Configuration > Pipeline
カスタムパイプラインで独自のルールでの整形が可能

Observability Pipeline
送信前に機密情報をマスキング
 
### 保管
ログ量が増えた場合の対応
### 3つの保管先
Ingest
- インデックス
	- 頻繁にクエリされ、短期間保持する
	- アプリケーションログ
- Flex Logs
	- 緊急にクエリする必要がある中長期
	- セキュリティログ
	- ネットワークログ
- アーカイブ
	- 外部ストレージに長期保管
	- 監査ログ
	- 構成ログ
 
### Flozen Flex
ログ保持期間を7年に拡張できる
### Archive Serch
コールドストレージからログを再インデックスなしで直接検索
#### デモ
Logs > Configuration > Routing > indexes
条件に一致するログの保存期間を設定できる
Exclude Debugなどで除外もできる
- アーカイブ
	- 保管先のアーカイブストレージを選択
		- S3
		- Google Cloud Storage
		- Azure Storage

### 分析
Log Explorer
よく使用しているやつ

- 上の `Include Flex Logs`をオンにしたら、それも表示できる

Group Info > Patterns
AIでパターン化してくれる

#### Logs ExplorerでカバーできないものはLog WordspacesでSQLライクなクエリでの検索が可能
Logs > Notebooks


## QA
### datadog
- ログの転送方法でdatadog-agentを使用しない場合、
	- firehorse
		- リアルタイム性なども考慮し、一般的にはこっち
	- forwarder
- ログのマスキングはどのようにできるのか
	- どこでもできます

### AWS
- Container Insights
	- マルチアカウントの場合、一元管理し閲覧権限を分けることは可能か
		- CloudWatch Observability
- DB Insights
	- 負荷の影響は？
		- 軽量なシステムだから、0ではないが負荷はそんなに多くない
		- 複雑なSQLが多い、単位時間のログが多い場合には多少負荷があがることをある



# 次回9月にAPMに関するウェビナー