- `app/javascript/components/common/pages/conservation_reports/conservation_reports.vue`
	- `app/javascript/components/daily_maintenance/components/other_attachment_group/OtherAttachmentGroupDraggable.vue`
		- `app/javascript/components/DownloadButton.vue`

## 該当箇所
`OtherAttachmentGroupDraggable.vue`
`scrollHint`のコンポーネント自体が `disabled`されているため、ここの修正が必要。
![スクリーンショット 2025-04-10 14.48.25.png](../_resources/スクリーンショット%202025-04-10%2014.48.25.png)

ここに書いたことが正しい👆のじゃ不十分。
https://vqit.backlog.com/view/ENEOS23-1287#comment-525676057


https://github.com/Bee2B/eneos-spm/issues/4808

実装済み
