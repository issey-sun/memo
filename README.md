# README
## users テーブル

| Column              | Type  | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| encrypted_password | string | null: false |

## memos テーブル
| Column     | Type       | Options           |
| ---------- | ---------- | ----------------- |
| title      | text       | null: false       |
| introduce  | text       |                   |
| image      |            |                   |
| day        | date       | foreign_key: true |
| user       | references | foreign_key: true |

## comments テーブル
| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             |
| memo      | references |             |