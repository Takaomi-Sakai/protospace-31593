# テーブル設計

## users テーブル

| Column      | Type   | Option   |
| ----------- | ------ | -------- |
| email       | string | NOT NULL |
| password    | string | NOT NULL |
| name        | string | NOT NULL |
| profile     | text   | NOT NULL |
| occupation  | text   | NOT NULL |
| position    | text   | NOT NULL |

### Association

- has_many :comments
- has_many :prototypes

## prototypes テーブル

| Column      | Type       | Option   |
| ----------- | ---------- | -------- |
| title       | string     | NOT NULL |
| catch       | text       | NOT NULL |
| concept     | text       | NOT NULL |
| user        | references |          |

### Association

- has_many : comments


## comments テーブル

| Column      | Type       | Option   |
| ----------- | ---------- | -------- |
| text        | text       | NOT NULL |
| user        | references |          |
| prototype   | references |          |
