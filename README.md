# README
## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false, unique: true|

### Association
- has_many :groups_users
- has_many :groups, through : :groups_users
- has_many :messages

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user|string|null: false|

### Association
- has_many :groups_users
- has_many :groups, through : :groups_users
- has_many :messages

## messageテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|
|image|text|
|group|references|null: false, foreign_key: true|
|user|references|null: false, foreign_key: true|


### Association
belongs_to :user
belongs_to :group
