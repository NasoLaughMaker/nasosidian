`git config pull.rebase true`

## Github上でBaseBranchを変更した場合
1. `git checkout -b backup_branch`
2. `git checkout 元のブランチ`
3. `git reset --hard origin/ベースにしたいブランチ`
4. `git cherry-pick 取り込みたいcommit^..取り込みたいcommit`
5. `git log --oneline`
6. `git push -f origin 元のブランチ`