## 分かっていること
1. 不具合報告から作成した許可証には`detail_daily_schedule_tasks`ごとに`detail_daily_scheudles`が存在する
	1. `detail_daily_schedules`：`detail_daily_schedule_with_tasks`は1：1で存在
2. E画面から作成した許可証は、一つの`detail_daily_schedules`lにたいして許可証の数分`detail_daily_schedule_with_tasks`が存在する
	1. `detail_daily_schedules`：`detail_daily_schedule_with_tasks`は1：多で存在

## 本エラーの問題点
`detail_daily_schedule_with_task.detail_daily_schedule_permit`で No method Errorとなり、nilに対して`detail_daily_schedule_permit`を呼び出していると言われる。

## 調査の方針
どうやって`detail_daily_schedule_with_tasks`がnilとなる現象が発生するか