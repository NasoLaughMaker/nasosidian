email：`m-yamabe@valqua.com`


# 鹿島
ユーザーは存在している。しかし、本登録が未完了。
## TODO
- [x] 本登録処理
- [x] パスワードリセット

## 手順
railsコンソールに接続
```
cd kashima/current
bin/rails c
```

コマンド実行
```ruby
> require "bcrypt"
> hashed_password = BCrypt::Password.create("Eneos-1234567")

> sql = ActiveRecord::Base.sanitize_sql_array(["UPDATE users SET confirmed_at = ?, encrypted_password = ? WHERE email = 'm-yamabe@valqua.com'", Time.now, hashed_password])
> ActiveRecord::Base.connection.execute(sql)
```

# 川崎
そもそもユーザーが存在しない。
## TODO
- [x] ユーザー登録
- [x] 本登録処理

## 手順
railsコンソールに接続
```
cd kawasaki/current
bin/rails c
```

コマンド実行
```ruby
> require 'bcrypt'
> hashed_password = BCrypt::Password.create("Eneos-1234567")
> sql=ActiveRecord::Base.sanitize_sql_array(["INSERT INTO users(name, email, encrypted_password, valqua, valqua_role, confirmed_at, created_at, updated_at, otp_required_for_login) VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?)",'山邊 雅之','m-yamabe@valqua.com',hashed_password,1,'superuser',Time.now,Time.now,Time.now,1])
> ActiveRecord::Base.connection.execute(sql)
```