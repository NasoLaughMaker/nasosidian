1. 管理者等に依頼して公開鍵を登録してもらう
`cd .ssh`
`authorized_keys`内に公開鍵を登録

2. 接続する人の `.ssh/config`にhost情報を登録
```
Host
	# プライベートサーバのプライベートIP(DNS名でも指定可)
	HostName
	# sshポート番号(省略可能)
	Port
	# ログインするユーザ
	User
	# 踏み台サーバを経由してログイン
	# ProxyComamnd ssh stool -W %h:%p
	ProxyCommand
	# ローカル端末に保存した、プライベートサーバの秘密鍵のパス指定
	IdentityFile ~/.ssh/~~~
```

3. 接続
```
ssh "HostName"
```

`BRANCH=infra/3899_separate_redis_kashima cap dev2-kashima deploy`