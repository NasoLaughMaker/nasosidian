# 削除・修正項目
## 標準用F画面
- 施工上の注意事項
- 安全上の事項
- 火気種類
- 着工前チェック1〜5
	- 工事着工前確認
		- 可燃物や有害物質への環境設定要/否確認
		- ｵﾌｻｲﾄ工事：移動時ﾘｽｸﾁｪｯｸﾘｽﾄにより確認する
	- 保護具・機材等の準備点検
		- 指定された保護具は確実に着装する
- 着工前チェック6〜10
	- その他
		- 全部不要なため、アコーディオンごと削除する
- アスベスト含有の有無 → アスベスト含有作業
	- 文言を以下に2つで、トグルのみに変更（on , offのボタンのみ）
		- 茨城県及び労基署に許可を受けているか
		- 養生は隙間なく実施されているか
- 重機・トラック等の乗り入れ確認
	- 10 → 9にナンバリング
	- 以下削除
		- ユニック、クレーンのアウトリガーは完全張出しを確認する
		- 重機作業では、作業半径内の立入禁止措置を行う
- サイン欄修正
	- 削除
		- 作業者
		- 作業指揮者欄の一つ
	- 修正
		- 安全選任者 → 安全専任者
		- 監視人の欄に（）を追加
## 検査用F画面
- 品質特記
- 安全特記
- 共通事項
	- ｵﾌｻｲﾄ工事：移動時ﾘｽｸﾁｪｯｸﾘｽﾄにより確認する
- サイン欄
	- 削除
		- 作業者
	- 修正
		- 安全専任者の追加
		- 監査人の欄に（）を追加


## 項目一覧取得SQL
```sql
SELECT
	ore.id,
	ore.name,
	ore.title,
	ore.priority,
	ors.id,
	ors.name,
	ors.priority,
	ori.name,
	ori.item_type,
	ori.priority
FROM
	office_report_items AS ori
		JOIN
			office_report_sections AS ors
				ON
					ors.id = ori.office_report_section_id
		JOIN
			office_reports AS ore
				ON
					ore.id = ors.office_report_id
WHERE
	ore.office_id = 171
;
```
