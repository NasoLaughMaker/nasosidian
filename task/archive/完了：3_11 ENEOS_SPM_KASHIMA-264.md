特定のユーザーがログインできない問題について

## 3/11調査結果
[Issue#2193](https://github.com/Bee2B/eneos-spm/pull/2193)を取り込み忘れていた。すぐに対応。

## 3/12
- 同様のエラーが発生。3/11の対応で`office_roles.role = 3`のユーザーはログイン可能になったが、`office_roles.role = 4`のユーザーがログインできない。`5`のユーザーがログインできないのも確認済み。

### 対応
- developではうまくいっている。
	- `elsif current_office && !admin_mode?`に分岐するのは意図した挙動か？
	- developではそもそもその分岐にいかない。
- `if current_user.has_valqua_role? || current_user.has_owner_manage_role? || current_user.has_owner_operator_role?`では`owner_operator`のユーザーが正しく分岐している。
- 根本の解決`has_construction_requester_group?`を参照できるようにするしかない？



### 実態
sidebarのslimが616のコミットと全然違う内容になっている。正しく入れられていない。

[issue#2204](https://github.com/Bee2B/eneos-spm/pull/2204)に