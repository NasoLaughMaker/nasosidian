### 確認事項
- root権限あるの？sudo使える？
- 起動時のオプションがどうなっているか

### Amazon Linux 2
- systemdを提供
	- systemctlを使える
	- systemctlはディレクトリに依存しないため、
- `systemctl list-units --type=service | grep cron
`


### 対応内容
- cronの状態確認
	- `sudo systemctl status cron`
		- `Active: active（running） or inactive(dead)`で確認できる。
- cronの再起動
	- `sudo systemctl restart crond`
 

#### 起動時のオプション
- `sudo systemctl enable crond`
	- デフォルトで有効化されているが、上記コマンドで自動起動を有効にできる。
 

## 手順
1. backupを取得
	1. `cd infra.tasks`
	2. `mkdir work.20250312.crontab.restart`
	3. `cd work.20250312.crontab.restart`
	4. `crontab -l > backup.txt`
2. .  現在のcronの起動状況を確認
	1.  `sudo systemctl status crond`
		1.  `Active: active (running)`を確認
3.  cronの再起動を実行
	1.  `sudo systemctl restart crond`
4.  再起動後の起動状況を確認
	1.  `sudo systemctl status crond`
		1.  `Active: active (running)`を確認