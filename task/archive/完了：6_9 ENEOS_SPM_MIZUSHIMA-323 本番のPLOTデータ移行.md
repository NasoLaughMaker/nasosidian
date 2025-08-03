[ENEOS_SPM_MIZUSHIMA-323](https://vqit.backlog.com/view/ENEOS_SPM_MIZUSHIMA-323) 本番のPLOTデータ移行

旧STG環境の水島から水島本番にPLOT図のデータ移行を行う。
`eneos-stg.valqua-spm-adv.com`

`active_storage_attachments以外の移行`以降のシートが対象

## S3オブジェクトの移行
STG→本番バケットに移行
`S3移行`のシートを参考にして、水島でのコマンドを一つ一つ作成する。
blobsのkeyを辿って取得する
移行対象は、STGにあるすべて。移行対象のレコードは確認必要。
- overallview
- plot
- 


## レコードの移行


## 移行対象テーブル
- Office
	- whole_image
	- 必要な画像か、どこで使用される画像かを確認したい。
- OverallView
	- overall_image
- Plot
	- image


wholeImageって何？？？
![スクリーンショット 2025-06-09 19.17.15.png](../_resources/スクリーンショット%202025-06-09%2019.17.15.png)

移行対象plot一覧
![スクリーンショット 2025-06-09 19.21.00.png](../_resources/スクリーンショット%202025-06-09%2019.21.00.png)


```sql
SELECT
	*
FROM
	active_storage_blobs
WHERE
	id IN (
		SELECT
			blob_id
		FROM
			active_storage_attachments
		WHERE
			record_type = 'OverallView'
	)
;

SELECT
	record_id,
	blob_id
FROM
	active_storage_attachments
WHERE
	record_type = 'OverallView'
;
	
	
	
	
SELECT
	*
FROM
	active_storage_blobs
WHERE
	id IN (
		SELECT
			blob_id
		FROM
			active_storage_attachments
		WHERE
			record_type = 'Office'
	)
;
```

# TODO
1. STG環境と本番環境で移行できていないデータ、移行できているデータを精査する
2. 移行できていないデータはSTGでのIDと本番でのIDを書き出す
3. 移行先にないデータはINSERTでのSQLを作成する。移行先にあるが、不備があるデータはUPDATEでのSQLを作成する。
