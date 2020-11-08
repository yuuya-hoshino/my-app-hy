# README

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false,unique: true|
|password|string|null: false|
|each_split|string|null: false|

### Association

- has_many : chat_room_user
- has_many : reaction
- has_many : groups_user


## reactionsテーブル

|Column|Type|Options|
|------|----|-------|
|to_user_id|integer|null: false|
|from_user_id|integer|null: false|
|status|integer|null: false|

### Association

- belongs_to : user

## chat_messagesテーブル

|Column|Type|Options|
|------|----|-------|
|chat_room_id|integer|null: false,foreign_key: true|
|user_id|integer|null: false,foreign_key: true|
|messge|text||
|image|string||

### Association

- belongs_to : user
- belongs_to : chat_room

## chat_roomsテーブル

|Column|Type|Options|
|------|----|-------|

- has_many : chat_room_user
- has_many : groups_user

## chat_room_usersテーブル

|Column|Type|Options|
|------|----|-------|
|chat_room_id|integer|null: false,foreign_key: true|
|user_id|integer|null: false,foreign_key: true|

### Association

- belongs_to : user
- belongs_to : chat_room