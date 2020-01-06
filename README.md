<<<<<<< Updated upstream
# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
=======
# CHAT-SPACE DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :messages
- has_many :users_groups
- has_many :groups, through: : users_groups

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|text||
|user|reference|null: false, foreign_key: true|
|group|reference|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association
- has_many :massages
- has_many :users_groups
- has_many  :users,  through:  : users_groups

## users_groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
<<<<<<< Updated upstream
- belongs_to :group

=======
- belongs_to :group
>>>>>>> Stashed changes
>>>>>>> Stashed changes
