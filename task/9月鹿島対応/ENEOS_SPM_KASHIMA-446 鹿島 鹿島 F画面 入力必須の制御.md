## 必須項目のバリデーション
- office_report_itemのバリデーションについては、office_report_itemにvalid_typeのようなカラムを追加し、承認ボタン押下時に、detail_daily_schedule_task_report_itemからoffice_report_itemvalid_typeでフィルタリングして、ユーザーのグループとvalid_typeの照合を行う事でバリデーションする。

# 対応箇所
## 必須入力
- 作業内容
- 開始時間-終了時間/作業人数
- 工事エリア
- 施設管理担当
- サイン欄>監督者
- サイン欄>熱中症予防管理者（5月〜9月限定）
- 残存リスク
- 環境設定要否
	- 施設管理Grによる入力必須
## 入力制限
- 残存リスク
	- 工事担当Gr
- 立会い