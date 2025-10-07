[ENEOS_SPM_KASHIMA-589](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-589) 鹿島 ユーザリスト 役職が設定されていないユーザは同じく役職が登録されていないユーザでしか検索できない

## ざっと方針
1. user.rbに役職なしのユーザーを追加するscopeを追加
	1. office_roleは存在するが、役職が未設定のユーザーを追加
2. users_controller.rbのfilter_usersに作成したscopeを適応
