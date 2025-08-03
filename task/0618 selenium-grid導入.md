```
# テスト対象URL
TEST_URL=https://dev.valqua-spm.com/

# ログインURL
LOGIN_URL=https://dev.valqua-spm.com/user/sign_in

# オフィス画面を選択
OFFICE_SCREEN_URL=https://dev.valqua-spm.com/offices

# 同時クライアント数
EMAILS=s-nagai+test-001@beeb.co.jp,s-nagai+test-002@beeb.co.jp,s-nagai+test-003@beeb.co.jp,s-nagai+test-004@beeb.co.jp,s-nagai+test-005@beeb.co.jp,s-nagai+test-006@beeb.co.jp,s-nagai+test-007@beeb.co.jp,s-nagai+test-008@beeb.co.jp,s-nagai+test-009@beeb.co.jp,s-nagai+test-010@beeb.co.jp
PASSWORD=Sakai-1234567

E_SCREEN_URL=https://dev.valqua-spm.com/daily_maintenance/offices/45/conservation_reports/daily_reports

SELENIUM_HUB_URL=http://selenium-hub:4444/wd/hub
```

## 6/25
https://github.com/Bee2B/selenium-grid/pull/8#discussion_r2163500298
現在同期処理でひとつひとつ順に実行している状態。非同期で同時実行できるように修正をduyさんに依頼中

# TODO
- [ ] 非同期処理で同時に100ユーザーがアクセスできるような形式に修正
- [ ] EC2のメモリ使用率を監視できるようにメトリクスを追加
	- STG、本番についてはIRETに依頼
	- DEVについてはBee2Bの所有物であるため、DEVで行えるようにするにはBee2Bアカウントでのメトリクス追加が必要。永井がIAMユーザー持っていないため、メトリクスがどうなっているのか確認できない。