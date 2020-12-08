# README

## users

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| nickname           | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |

has_many :books

## books

| Column           | Type       | Options                        |
| ---------------- | ---------- | ------------------------------ |
| name             | string     | null: false                    |
| title            | string     | null: false                    |
| memo             | text       | null: false                    |
| user             | references | null: false, foreign_key: true |

belongs_to :user