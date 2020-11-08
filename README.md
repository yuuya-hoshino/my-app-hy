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
|from_user_id|integer|null: false|
|status|integer|null: false|


## chat_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|chat_room_id|integer|null: false,foreign_key: true|
|user_id|integer|null: false,foreign_key: true|
|messge|text||
|image|string||

## chat_roomsテーブル

|Column|Type|Options|
|------|----|-------|

## chat_room_usersテーブル

|Column|Type|Options|
|------|----|-------|
|chat_room_id|integer|null: false,foreign_key: true|
|user_id|integer|null: false,foreign_key: true|