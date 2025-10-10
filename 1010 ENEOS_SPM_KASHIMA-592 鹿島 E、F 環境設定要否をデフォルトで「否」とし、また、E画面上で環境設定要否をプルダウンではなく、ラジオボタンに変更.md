[ENEOS_SPM_KASHIMA-592](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-592) 鹿島 E、F 環境設定要否をデフォルトで「否」とし、また、E画面上で環境設定要否をプルダウンではなく、ラジオボタンに変更

### 許可証作成時に呼び出されるAPI
- G画面
	- `app/controllers/api/daily_maintenance/offices/daily_schedules/bulk_inserts_controller.rb`
		- `bulk_insert`
- E画面
	- `app/controllers/api/daily_maintenance/offices/daily_schedules/bulk_inserts_controller.rb`
		- `bulk_insert_nct`

### TODO
bulk_insert系のAPIが呼び出された時に、作成したdetail_daily_schedule_taskとoffice_report_itemの中間テーブルを作成する