# 実装メモ

## BE

### 設計について

現在日常保全 or 要求票工事はflagで管理しているが、勧告工事をいれるためにflagではなくintegerでのenumerizeを使用する。カラムを追加し、rakeによってflagからの移行を行う。

### 追加カラム

- construction_category（仮）

- 0：日常保全（default）

- 1：要求票工事

- 2：勧告工事

### 対応内容

- カラム追加

- 使用カラムの変更に伴うコード修正

- 勧告工事のときのバリデーション追加

## FE

### 対応内容

- ラジオボタンの実装

- 使用カラムの変更に伴うコード修正

- useSafetyChecklistFlag（boolean） → constructionCategory（integer）

- ホーム画面からconservation_reportを新規作成する際の `日常保全` or `日常保全以外`によるラジオボタンのデフォルト値の変更

- B画面（新規作成時）に`分類/種別`の選択によってラジオボタンの入力値を変更

- 勧告工事の場合に、B画面 > `工事内容`を空欄にする



# 各項目
- 工事優先度
	- construction_priority_id
- 着工日連絡期日
	- starting_type_id
- 着工前打合せ
	- meeting_type_id
- 施工容量
- 残存リスク