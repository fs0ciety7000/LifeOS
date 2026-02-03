---
cssclasses:
  - wide-page
---

# MediaDB

> Ma base de donnees personnelle pour tracker films, series, jeux, livres et musique.

---

## Vue d'ensemble

| 🎬 Films | 📺 Series | 🎮 Jeux | 📚 Livres |
|:--------:|:---------:|:-------:|:---------:|
| `$= dv.pages('"07-MediaDB/Films"').length` | `$= dv.pages('"07-MediaDB/Séries"').length` | `$= dv.pages('"07-MediaDB/Jeux"').length` | `$= dv.pages('"07-MediaDB/Livres"').length` |

---

## 🎬 Films

### A voir
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  year as "Annee",
  genre as "Genre"
FROM "07-MediaDB/Films"
WHERE status = "🎬 à voir" OR status = "👀 en cours"
SORT date_added DESC
```

### Recemment vus
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  rating + "/10" as "Note",
  date_watched as "Vu le"
FROM "07-MediaDB/Films"
WHERE status = "✅ vu"
SORT date_watched DESC
LIMIT 5
```

---

## 📺 Series

### En cours
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  "S" + current_season + "E" + current_episode as "Progress",
  platform as "Plateforme"
FROM "07-MediaDB/Séries"
WHERE status = "👀 en cours"
SORT file.mtime DESC
```

### Terminees recemment
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  rating + "/10" as "Note",
  seasons + " saisons" as "Saisons"
FROM "07-MediaDB/Séries"
WHERE status = "✅ terminee"
SORT date_finished DESC
LIMIT 5
```

---

## 🎮 Jeux

### En cours
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  playtime + "h" as "Temps",
  completion + "%" as "Completion"
FROM "07-MediaDB/Jeux"
WHERE status = "🎮 en cours"
SORT playtime DESC
```

### Completes
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  rating + "/10" as "Note",
  playtime + "h" as "Temps total"
FROM "07-MediaDB/Jeux"
WHERE status = "✅ termine"
SORT date_finished DESC
LIMIT 5
```

---

## 📚 Livres

### En lecture
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  author as "Auteur",
  current_page + "/" + pages as "Pages"
FROM "07-MediaDB/Livres"
WHERE status = "👀 en cours"
SORT file.mtime DESC
```

### Lus recemment
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  author as "Auteur",
  rating + "/10" as "Note"
FROM "07-MediaDB/Livres"
WHERE status = "✅ lu"
SORT date_finished DESC
LIMIT 5
```

---

## ⭐ Top Rated (9+/10)

```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  type as "Type",
  rating + "/10" as "Note"
FROM "07-MediaDB"
WHERE rating >= 9
SORT rating DESC
LIMIT 10
```

---

## Quick Add

| | | | |
|:---:|:---:|:---:|:---:|
| [[09-Templates/Film\|🎬 Film]] | [[09-Templates/Série\|📺 Serie]] | [[09-Templates/Jeu\|🎮 Jeu]] | [[09-Templates/Livre\|📚 Livre]] |

### Raccourcis QuickAdd
- `Ctrl+Shift+A` puis `Film` - Ajouter un film
- `Ctrl+Shift+A` puis `Serie` - Ajouter une serie
- `Ctrl+Shift+A` puis `Livre` - Ajouter un livre
- `Ctrl+Shift+A` puis `Jeu` - Ajouter un jeu
