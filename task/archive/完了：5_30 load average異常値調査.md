active_storageのaccess.logがなんか多い？


サーバーのログじゃなくて、CloudWatchになにかしらアクセス数の推移を確認できるものがないか調べる。

# ログファイルをローカルにコピーする方法
1. `/var/log/nginx/access.log`の権限を`XX4`に変更
	- その他のユーザーに読み込み権限付与できればOK
2. ローカルで以下を実行
	- `scp valqua-spm-eneos:~/infra.tasks/logs/access.log ~/Documents/Bee2b/Documents/ENEOS_SPM_Doc/リクエスト数調査/20250602`
