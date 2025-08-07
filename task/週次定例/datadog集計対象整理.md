## 現在の集計対象
- メモリ使用率
- ロードアベレージ

## 今後の追加集計対象
- puma backlogメトリクス
	- 対応中



## 物理的な制約
- pumaの設定
- core 48
### 現状
- 設定
	- 48 worker * 5 thread
- 現実
	- 48 worker * 1 thread