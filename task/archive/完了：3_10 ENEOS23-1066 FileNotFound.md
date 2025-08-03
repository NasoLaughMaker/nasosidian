- idを辿っていけば画面の特定ができる。
- ActiveStorageBlobsとattachmentsで確認できる。
- record_idとrecord_typesテーブルの特定はできる。
- テーブルからどの製油所か？どのデータか？PLOTか？

- S3のキーがないのは何故か？
- 画面上からできてしまうのか？


### 方針 3/12（火）
5/22付近でエラー多発しているため、その周辺の画像でattachementsが生き残っているやつを確認したら何かわかるかもしれない。

#### 結論
関連付けが残っているレコードはほぼなく、残っているものも`detail_daily_schedule_tasks`の外部キーなどがnullになっており、関連付けはほぼ残っていなさそう。

#### 言えること
対象となっているレコードは半年以上の前であり、古いデータであるため、検証が進められない。


### ActiveStorage::AnalyzeJobの直前で呼び出されているAPIがF画面のDailyMaintenance::offices::DailySchedulesなんじゃないの？各アラートの直前で呼び出されているAPIをリスト化しよっか。各アラートの3分前くらいのAPIリスト化かな。ユーザーも特定できるといいよね

- `3/12 01:13:44 am`
	- `1:13:43`
		- `yoshinaga.rikuto@eneos.com`
		- `/api/daily_maintenance/offices/45/daily_schedules`
- `3/06 10:35 am`
	- `10:35:40`
		- `/api/daily_maintenance/offices/163/current_user_info`
		- `takahashi.kei.252@eneos.com`
	- `10:35:36`
		- `/api/daily_maintenance/offices/45/construction_requirements`
		- `yuki.kazuya@eneos.com`
	- `10:35:28`
		- `/api/gov/offices/163/budget_types`
		- `munehara.hiroo@eneos.com`
	- `10:35:23`
		- `/api/daily_maintenance/offices/163/maintenance_search_condition`
		- `munehara.hiroo@eneos.com`
	- `10:35:12`
		- `/api/daily_maintenance/offices/163/incidental_works`
		- `takamura.yu@eneos.com`
	- `10:35:06`
		- `/api/daily_maintenance/offices/163/conservation_reports/15797/approval_requests`
		- `asano.yohei@eneos.com`
	- `10:35:04`
		- `/api/daily_maintenance/offices/163/construction_purchase_codes`
		- `yamauchi.yuto@eneos.com`
- `3/6 10:34:57`
	- `10:34:44`
		- `/api/daily_maintenance/offices/163/current_user_info`
		- `uchikado.yuu@eneos.com`
	- `10:34:43`
		- `/api/daily_maintenance/offices/45/screen_logs`
		- `yoshida.masanobu@eneos.com`
- `3/6 10:34:26`
	- `10:34:23`
		- `/api/daily_maintenance/offices/45/conservation_reports/4507`
		- `kubo.shigeki@eneos.com`
	- `10:34:18`
		- `/api/daily_maintenance/offices/45/conservation_reports`
		- `kubo.shigeki@eneos.com`
	- `10:34:15`
		- `/api/daily_maintenance/offices/45/daily_schedules/count_task_by_approval_status`
		- `koike.eiji@eneos.com`
	- `10:34:11`
		- `/api/daily_maintenance/offices/163`
		- `yamauchi.yuto@eneos.com`
	- `10:34:09`
		- `/api/daily_maintenance/offices/45/office_reports`
		- `koike.eiji@eneos.com`
	- `10:34:06`
		- `/api/daily_maintenance/offices/45/incidental_works`
		- `koike.eiji@eneos.com`
	- `10:34:04`
		- `/daily_maintenance/offices/45/conservation_reports/daily_reports`
		- `koike.eiji@eneos.com`
- `3/6 10:33:59`
	- `10:33:54`
		- `/api/daily_maintenance/offices/163/todo`
		- `takahashi.kei.252@eneos.com`
	- `10:33:54`
		- `/api/daily_maintenance/offices/163/projects`
		- `takahashi.kei.252@eneos.com`
	- `10:33:22`
		- `/api/daily_maintenance/offices/45/projects/2/detail_daily_schedule_tasks/23662/apply`
		- `c.fumihara@sankyu.co.jp`
	- `10:33:16`
		- `/api/daily_maintenance/offices/45/projects/2/detail_daily_schedule_tasks/23662`
		- `c.fumihara@sankyu.co.jp`

## 遠瀬さんの調査で分かったこと
[ActiveStorage::FileNotFoundError in AnalyzeJob due to enqueue-before-upload](https://github.com/rails/rails/issues/39107)
画面的な操作で起きたわけではなく、Sidekiqキューに入れられたActiveStorageのAnalyzeJobで起きている。AnalyzeJobは本来attachされた時にSidekiqキューに入れられるが、該当データは古く、実際には使われていないため、どうやってキューに入れられたかが不明。Redis問題のように他のスキーマの情報を見ている可能性がある。

### 期待していること
ファイルアップロードが完了するまで、Analyze Jobがエンキューされないようにする
### 実際に起きていること
ファイルのアップロードが完了する前にAnalyze Jobがエンキューされている







