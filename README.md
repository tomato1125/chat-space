# README

## usersテーブル

|column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :tweets
- has_many :groups, through :users_groups
- has_many :users_groups

## groups_usersテーブル

|column|Type|Options|
|------|----|-------|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|column|Type|Options|
|------|----|-------|
|name|string|null: false|

### Association
- has_many :tweets
- has_many :users, through :users_groups
- has_many :users_groups

## messagesテーブル

|column|Type|Options|
|------|----|-------|
|content|string|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

* ...
