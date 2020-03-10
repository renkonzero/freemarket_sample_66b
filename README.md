# README

# フリマアプリ DB設計

## Categoryテーブル
|Column|Type|Options|
|------|----|-------|
|name||string|null: false, unique: true|
### Association
- has_many :products


## Brandテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, unique: true|
### Association
- has_many :products


## Photoテーブル
|Column|Type|Options|
|------|----|-------|
|photo_id|string|
### Association
- has_many :products


##  Commentテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|comment_id|integer|null: false, foreign_key: true|
|created_at|timestamp|null: false|
### Association
- belongs_to :user
- belongs_to :product


