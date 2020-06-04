# README

## usersテーブル

|column|Type|Options|
|------|----|-------|
|username|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :tweets

## users_groupsテーブル

|column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|column|Type|Options|
|------|----|-------|
|group|string|null: false|

### Association
- has_many :tweets

## tweetsテーブル

|column|Type|Options|
|------|----|-------|
|tweet|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|ingeter|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

* ...
