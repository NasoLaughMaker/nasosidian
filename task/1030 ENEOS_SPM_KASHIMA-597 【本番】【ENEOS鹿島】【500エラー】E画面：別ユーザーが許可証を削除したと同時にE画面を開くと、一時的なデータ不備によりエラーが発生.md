[ENEOS_SPM_KASHIMA-597](https://vqit.backlog.com/view/ENEOS_SPM_KASHIMA-597) 【本番】【ENEOS鹿島】【500エラー】E画面：別ユーザーが許可証を削除したと同時にE画面を開くと、一時的なデータ不備によりエラーが発生

# 対応方針

count_task_by_approval_status_nctメソッド内で、taskが定義されたあとに以下を入れるだけで良い？

```

next if task.nil?

```
