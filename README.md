# meal_record

```
@startuml

entity "登録日" {
+ 日付 [PK]
--
}

entity "献立" {
+ 献立ID [PK]
--
献立名
# 日付 [FK]
}

entity "料理" {
+ 料理ID [PK]
--
料理名
メモ
# 献立ID [FK]
}

entity "食材" {
+ 食材ID [PK]
--
食材名
# 料理ID [FK]
}

登録日 -|{ 献立
献立 -|{ 料理
料理 -o{ 食材

@enduml
```
