# README

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false,unique: true|
|password|string|null: false|
|each_split|string|null: false|

## reactionsテーブル

|Column|Type|Options|
|------|----|-------|
|to_user_id|integer|null: false|
|email|string|null: false,unique: true|
|password|string|null: false|
|each_split|string|null: false|