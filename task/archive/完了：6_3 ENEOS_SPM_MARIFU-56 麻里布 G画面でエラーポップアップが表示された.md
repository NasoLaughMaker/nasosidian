[ENEOS_SPM_MARIFU-56](https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-56) 麻里布 G画面でエラーポップアップが表示された
[Issue#5398](https://github.com/Bee2B/eneos-spm/issues/5398)

# 問題
`m-fujiki+kyouryoku_1@valqua.com`でログインし、許可証の作成を試みると発生
対象不具合：`http://localhost:3000/daily_maintenance/offices/180/conservation_reports/38083/edit`
![スクリーンショット 2025-06-03 17.19.52.png](../_resources/スクリーンショット%202025-06-03%2017.19.52.png)

## 松本さん予想
`purchase_code`のscopeとかでなにか問題がある可能性あり（体験談）
model調べてみるといいかも



https://vqit.backlog.com/view/ENEOS_SPM_MARIFU-56#comment-551108523

調査完了。実装はなしなため、ステータスを完了に変更。