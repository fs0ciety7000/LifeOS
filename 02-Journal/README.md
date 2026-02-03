# 📔 Journal

> Espace personnel pour tes réflexions quotidiennes et ton journal de couple.

## 📝 Perso
Journal personnel pour tes pensées, émotions et réflexions.
- Raccourci: `Ctrl+Shift+J`
- Template: Journal Perso

## 💑 Couple
Journal pour documenter votre relation, vos moments partagés et votre communication.
- Raccourci: `Ctrl+Shift+C`
- Template: Journal Couple

## 📊 Entrées récentes

### Perso
```dataview
LIST
FROM "02-Journal/Perso"
WHERE file.name != "README"
SORT file.ctime DESC
LIMIT 5
```

### Couple
```dataview
LIST
FROM "02-Journal/Couple"
WHERE file.name != "README"
SORT file.ctime DESC
LIMIT 5
```
