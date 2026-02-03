# 📅 Daily Notes

> Notes quotidiennes, weekly et monthly reviews.

## 🗓️ Cette semaine
```dataview
LIST
FROM "01-Daily"
WHERE file.day >= date(today) - dur(7 days) AND type = "daily"
SORT file.day DESC
```

## 📊 Reviews récentes
```dataview
TABLE WITHOUT ID
  file.link as "Review",
  type as "Type"
FROM "01-Daily"
WHERE type = "weekly" OR type = "monthly"
SORT file.ctime DESC
LIMIT 5
```

## ⌨️ Raccourcis
- `Ctrl+Shift+D` - Nouvelle Daily Note
- Plugin Calendar pour navigation visuelle
