## 途中経過
1. 不具合報告から作成した許可証
	- `detail_daily_schedule_tasks`ごとに`detail_daily_scheudles`が存在する
	- `detail_daily_schedules`：`detail_daily_schedule_with_tasks`：`detail_daily_schedule_task` = 1：1：1
	- G画面から作成するごとにdetail_daily_schedulesが作成される
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
	- コピー元の`daily_schedule`
		- `18825	NULL	1	TK-234　定期開放検査工事	2025-10-06	11	ConstructionCompany	803	2025-10-01 17:18:42.062091	2025-10-01 17:18:42.062091`
	- コピー元は中止済み
	- エラー発生直前に削除している
		- [datadog](https://ap1.datadoghq.com/logs?query=%40http.method%3ADELETE%20%40params.id%3A26777&agg_m=count&agg_m_source=base&agg_t=count&cols=%40http.status_code%2C%40http.method&fromUser=true&messageDisplay=inline&refresh_mode=paused&storage=hot&stream_sort=desc&viz=stream&from_ts=1759244400000&to_ts=1759849199999&live=false)

### Gemini
```
### ## 1. レースコンディション（最も可能性が高い原因）

これが本番環境で最もよくある原因です。複数の処理がごくわずかな時間差で実行されることで、データの一時的な不整合が発生します。

**シナリオの例え:** 図書館の司書（あなたのコード）と、せっかちな助手（別の処理）がいるとします。

1. **司書がリストを取得:** 司書（あなたの`each`ループが始まる前の処理）は、「返却された本（`with_tasks`）のリスト」をデータベースから受け取ります。この時点では、リストにある全ての本に、貸出記録（`task`）が正しく紐づいています。
    
2. **助手が記録をシュレッダーにかける:** 司書がリストの1冊目から処理を始めようとした**ほんの一瞬の隙**に、せっかちな助手（別のユーザー操作やバックグラウンド処理）が、リストの中のある本の貸出記録（`task`）をシュレッダーにかけました（`task.destroy`を実行）。`dependent: :destroy`が正しく働き、その貸出記録に紐づいていた本（`with_task`）も書庫（データベース）から**廃棄**されました。
    
3. **司書が古いリストを処理:** 司書はそんなこととは知らず、手元にある**古いリスト**を見ながら処理を続けます。そして、ちょうど助手が廃棄した本の番が来ました。司書はリストにある本の名前（`with_task`）を元に、貸出記録（`task`）を探しに行きますが、それは既にシュレッダーにかけられて存在しません。ここで司書は「貸出記録が見つかりません！（`task`が`nil`です！）」となり、エラーが発生します。
    

このように、データをメモリに読み込んでから、それをループで処理し終わるまでの間に、別のプロセスがそのデータを変更・削除してしまうことがレースコンディションです。
```


