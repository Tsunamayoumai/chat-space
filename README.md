# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation



##usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false, unipue: true|

### Association
- has_many :groups, through: :group_users
- has_many :group_users
- has_many :massages



###users table
|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|

### Association
- has_many :groups, through: :group_users
- has_many :group_users
- has_many :massages



###messages table
|Column|Type|Options|
|------|----|-------|
|user|references|foreign_key: true, null: false|
|group|references|foreign_key: true, null: false|
|content|text|
|image|string|

### Association
- belongs_to :user
- belongs_to :group


###group_users table
|Column|Type|Options|
|------|----|-------|
|user|references|foreign_key: true, null: false|
|group|references|foreign_key: true, null: false|

### Association
- belongs_to :group
- belongs_to :user


* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
