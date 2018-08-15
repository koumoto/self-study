# DynamoDBについて

## 概要
- フルマネージドのNoSQL
- 開発者はAPI経由で利用
- DBの容量追加は自動
- スキーマレス
- トランザクションは無し

## 主キー
- Hash Type Primary Key
- Hash and Range Type Primary Key

## ローカル・セカンダリ・インデックス

- クエリのためのインデックス
- 従来のレンジキーの代替
- 後からインデックス作成は不可

## CRUD
- PutItem 作成/置換
- UpdateItem 全部/部分更新
- DeleteItem 削除
- GetItem 取得

## データ型
- String型
- Number型
- Binary型