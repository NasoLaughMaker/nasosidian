## 途中経過
1. 不具合報告から作成した許可証
	- `detail_daily_schedule_tasks`ごとに`detail_daily_scheudles`が存在する
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：1：1
2. E画面から作成した許可証
	- 一つの`detail_daily_schedules`lにたいして許可証の数分`detail_daily_schedule_with_tasks`が存在する
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：多：多（with_taskとtaskは 1：1）
3. コピーにより作成した許可証
## 本エラーの問題点
`detail_daily_schedule_with_task.detail_daily_schedule_permit`で No method Errorとなり、nilに対して`detail_daily_schedule_permit`を呼び出していると言われる。

## 調査の方針
どうやって`detail_daily_schedule_with_tasks`がnilとなる現象が発生するか


