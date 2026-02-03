# 🚀 Projects

> Projets actifs avec un objectif et une deadline définis.

## 🎯 Projets en cours
```dataview
TABLE WITHOUT ID
  file.link as "Projet",
  status as "Statut",
  priority as "Priorité",
  date_deadline as "Deadline"
FROM "03-Projects"
WHERE (status = "🚧 en cours" OR status = "🎯 planifié") AND file.name != "README"
SORT priority ASC
```

## 💡 Idées de projets
```dataview
LIST
FROM "03-Projects"
WHERE status = "💡 idée" AND file.name != "README"
SORT file.ctime DESC
```

## ✅ Récemment complétés
```dataview
TABLE WITHOUT ID
  file.link as "Projet",
  date_completed as "Complété le"
FROM "03-Projects"
WHERE status = "✅ complété" AND file.name != "README"
SORT date_completed DESC
LIMIT 5
```

## 📝 Créer un nouveau projet
Utilise le template `Project.md` ou le raccourci `Ctrl+Shift+P`
