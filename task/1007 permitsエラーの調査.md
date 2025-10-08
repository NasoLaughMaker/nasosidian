## 途中経過
1. 不具合報告から作成した許可証
	- `detail_daily_schedule_tasks`ごとに`detail_daily_scheudles`が存在する
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：1：1
2. E画面から作成した許可証
	- `detail_daily_schedules`に対し、許可証の数分`detail_daily_schedule_with_tasks`が存在する
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：多：多（with_taskとtaskは 1：1）
3. コピーにより作成した許可証
	- `detail_daily_schedules`に対して、複数の`detail_daily_schedule_with_tasks`が存在
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：多：多（with_taskとtaskは 1：1）
## 本エラーの問題点
`detail_daily_schedule_with_task.detail_daily_schedule_permit`で No method Errorとなり、nilに対して`detail_daily_schedule_permit`を呼び出していると言われる。

## 調査の方針
どうやって`detail_daily_schedule_with_tasks`がnilとなる現象が発生するか。
また、`detail_daily_schedule_task`は存在するが、`detail_daily_schedule_with_task`がnilである状態をどうやって再現するか。（本当にこの考えが正しいかも不明）

## 削除された許可証
コピーによって作成
- [対象のログ](https://ap1.datadoghq.com/logs?query=%40controller%3A%22Api%3A%3ADailyMaintenance%3A%3AOffices%3A%3ADailySchedules%3A%3ACopiesController%22%20%40params.targetDetailDailyScheduleTaskId%3A26777&agg_m=count&agg_m_source=base&agg_t=count&cols=%40http.status_code&event=AwAAAZm3IvvzDlDQZwAAABhBWm0zSXdYRUFBQ0pmdEpoWjVrMWtRQWgAAAAkMTE5OWI3YWQtMWM5OC00OGVjLWE4MzctZjVkMjU4ODUxMDhiAACfhg&messageDisplay=inline&refresh_mode=paused&storage=hot&stream_sort=desc&viz=stream&from_ts=1759244400000&to_ts=1759849199999&live=false)
	- [session reply](https://ap1.datadoghq.com/rum/replay/sessions/8519a2a5-e146-4c69-9b29-2fc802f1898f?applicationId=c1f34704-747f-41d2-a93f-69b31d2c9aff&highlightedEventId=AwAAAZm3IvWnbFr6tQAAABhBWm0zSXZtTEFBQ1ZQUy1IR3lLMUl3QUkAAAAkMTE5OWI3YWQtMWQ2My00OTk4LTg0OGMtZDllODE2MDI1YWQxAALPNQ&ts=1759714145703&from=1759714175072)
	- E画面で作成された許可証
	- 


