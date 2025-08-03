- [ENEOS_SPM_KASHIMA-386](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-386) 【ENEOS鹿島】【本番】【500エラー】E画面>作業許可を修正中に、監督受取で絞り込むと発生するエラー
- [Issue#5462](https://github.com/Bee2B/eneos-spm/issues/5462)

# TODO
- [ ] 作業許可の修正中には監督受取バッチを非活性にする

## 内部処理
- [x] 修正ボタン押下 
- [x] approve_cancelメソッドを呼び出す。
- [x] editing = trueに変更する
- [x] 条件分岐で `permit_task_kashima_starting_approval_manager_size(count)`を変更
- [ ] count_task_by_approval_status_conrtollerを呼び出す