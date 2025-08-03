[ENEOS23-1293](https://vqit.backlog.com/view/ENEOS23-1293) バグ緊急度:中｜工事台帳でTECOを外してもTECOの工事が検索される　No. 418 【バルカー SPM】お問い合わせがありました

# 該当箇所
- `app/javascript/components/daily_maintenance/offices/home/DailyMaintenanceHome.vue`
	- 193行目：`<HomeDailyMaintenanceProjectsAScreenFilterSetting />`
- `app/javascript/components/daily_maintenance/offices/home/components/HomeDailyMaintenanceProjectsAScreenFilterSetting.vue`






![スクリーンショット 2025-04-11 13.31.52.png](../_resources/スクリーンショット%202025-04-11%2013.31.52.png)
キャッシュが残ってそう。
`assets/application-XXXXXXX.js`を確認する必要あり。


# 調査結果
sessionStorageに検索条件残ってた。
元々の仕様でそうなってるみたい。
ただ、HOME画面からはsessionStorageを無視するのが正の挙動。
対応は必要。

# 6/12〆