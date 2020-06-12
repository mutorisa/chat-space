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
|name_id|string|null: false|
|email_id|string|null: false, unique: true|
|password_id|string|null: false, unique: true|

### Association
- belongs_to :name
- belongs_to :email
  belongs_to :password
