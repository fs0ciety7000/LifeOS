# 🎬 MediaDB

> Ta base de données personnelle pour films, séries, jeux, livres et musique.

## 📊 Vue d'ensemble

### 🎬 Films
```dataview
TABLE WITHOUT ID
  file.link as "Film",
  rating as "Note",
  status as "Statut",
  year as "Année"
FROM "07-MediaDB/Films"
SORT rating DESC
LIMIT 10
```

### 📺 Séries
```dataview
TABLE WITHOUT ID
  file.link as "Série",
  rating as "Note",
  status as "Statut",
  current_episode as "Épisode"
FROM "07-MediaDB/Séries"
WHERE status = "👀 en cours"
SORT file.mtime DESC
```

### 🎮 Jeux
```dataview
TABLE WITHOUT ID
  file.link as "Jeu",
  rating as "Note",
  status as "Statut",
  playtime as "Temps joué"
FROM "07-MediaDB/Jeux"
SORT rating DESC
LIMIT 10
```

### 📚 Livres
```dataview
TABLE WITHOUT ID
  file.link as "Livre",
  author as "Auteur",
  rating as "Note",
  status as "Statut"
FROM "07-MediaDB/Livres"
SORT rating DESC
LIMIT 10
```

## 📈 Statistiques

### Par statut
```dataview
TABLE WITHOUT ID
  length(rows) as "Total"
FROM "07-MediaDB"
WHERE file.name != "README"
GROUP BY status
```

## 🏷️ Raccourcis
- `Ctrl+Shift+F` - Ajouter un film
- `Ctrl+Shift+S` - Ajouter une série
- `Ctrl+Shift+L` - Ajouter un livre
- `Ctrl+Shift+G` - Ajouter un jeu
