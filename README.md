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

## tweetsテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null:false|
|user|references|null: false, foreign_key: true|
|adjective|references|null: false, foreign_key: true|
|noun|references|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :adjective
- belongs_to :noun


## adjectivesテーブル

|Column|Type|Options|
|------|----|-------|
|tytle|text|null: false|

### Association
- has_many :tweets

## nounsテーブル

|Column|Type|Options|
|------|----|-------|
|tytle|text|null: false|

### Association
- has_many :tweets

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false|

### Association
- has_many :tweets