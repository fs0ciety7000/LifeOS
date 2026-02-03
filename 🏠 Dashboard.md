---
cssclasses:
  - dashboard
  - wide-page
---

# 🌟 Life OS

> *"La vie n'est pas ce qui nous arrive, mais ce que nous en faisons."*

---

## ⚡ Actions rapides

| | | | |
|:---:|:---:|:---:|:---:|
| [[09-Templates/Daily Note\|📅 Daily Note]] | [[09-Templates/Quick Capture\|📥 Capture]] | [[09-Templates/Journal Perso\|📔 Journal]] | [[09-Templates/Project\|🚀 Projet]] |
| [[09-Templates/Film\|🎬 Film]] | [[09-Templates/Série\|📺 Série]] | [[09-Templates/Livre\|📚 Livre]] | [[09-Templates/Research Note\|🔬 Research]] |

---

## 📅 Aujourd'hui

```dataview
LIST WITHOUT ID "[[" + file.name + "]]"
FROM "01-Daily"
WHERE file.day = date(today)
```

### ✅ Tâches du jour
```dataview
TASK
FROM "01-Daily" OR "03-Projects"
WHERE !completed AND (due = date(today) OR scheduled = date(today))
LIMIT 10
```

### 📆 Agenda
```dataview
TABLE WITHOUT ID
  file.link as "Événement",
  time as "Heure"
FROM "03-Projects" OR "04-Areas"
WHERE type = "meeting" AND date = date(today)
SORT time ASC
```

---

## 📊 Vue d'ensemble

### 📥 Inbox à traiter
```dataview
LIST WITHOUT ID "[[" + file.name + "|" + file.name + "]]"
FROM "00-Inbox"
WHERE processed = false
SORT file.ctime DESC
LIMIT 5
```

### 🚀 Projets actifs
```dataview
TABLE WITHOUT ID
  file.link as "Projet",
  status as "Statut",
  priority as "Priorité",
  date_deadline as "Deadline"
FROM "03-Projects"
WHERE status = "🚧 en cours" OR status = "🎯 planifié"
SORT priority ASC
LIMIT 7
```

### ✅ Tâches en retard
```dataview
TASK
FROM "03-Projects" OR "04-Areas"
WHERE !completed AND due < date(today)
LIMIT 5
```

---

## 📔 Journal récent

### 📝 Dernières entrées perso
```dataview
TABLE WITHOUT ID
  file.link as "Date",
  mood as "Humeur"
FROM "02-Journal/Perso"
SORT file.ctime DESC
LIMIT 3
```

### 💑 Dernières entrées couple
```dataview
TABLE WITHOUT ID
  file.link as "Date",
  quality as "Connexion"
FROM "02-Journal/Couple"
SORT file.ctime DESC
LIMIT 3
```

---

## 🎬 MediaDB

### 📊 Statistiques
```dataview
TABLE WITHOUT ID
  "🎬 Films" as "Type",
  length(filter(rows, (r) => r.status = "✅ vu")) as "Complétés",
  length(filter(rows, (r) => r.status = "👀 en cours")) as "En cours",
  length(filter(rows, (r) => r.status = "🎬 à voir")) as "À voir"
FROM "07-MediaDB/Films"
GROUP BY true
```

```dataview
TABLE WITHOUT ID
  "📺 Séries" as "Type",
  length(filter(rows, (r) => r.status = "✅ terminée")) as "Complétées",
  length(filter(rows, (r) => r.status = "👀 en cours")) as "En cours",
  length(filter(rows, (r) => r.status = "📺 à voir")) as "À voir"
FROM "07-MediaDB/Séries"
GROUP BY true
```

### 👀 En cours
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  type as "Type",
  choice(type = "serie", current_episode, choice(type = "livre", current_page + "/" + pages, choice(type = "jeu", completion + "%", ""))) as "Progression"
FROM "07-MediaDB"
WHERE status = "👀 en cours"
SORT file.mtime DESC
LIMIT 5
```

### ⭐ Récemment terminés (Top rated)
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  type as "Type",
  rating as "Note"
FROM "07-MediaDB"
WHERE status = "✅ vu" OR status = "✅ terminée" OR status = "✅ lu" OR status = "✅ terminé"
SORT date_finished DESC
LIMIT 5
```

---

## 🔬 Recherche & Études

### 📚 Recherches actives
```dataview
TABLE WITHOUT ID
  file.link as "Sujet",
  domain as "Domaine",
  status as "Statut"
FROM "08-Research"
WHERE status = "🔬 exploration" OR status = "📝 en cours"
SORT file.mtime DESC
LIMIT 5
```

---

## 📈 Habitudes (Cette semaine)

| Habitude | L | M | M | J | V | S | D |
|:---------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 💧 Hydratation | | | | | | | |
| 🏃 Exercice | | | | | | | |
| 📚 Lecture | | | | | | | |
| 🧘 Méditation | | | | | | | |
| 😴 Sommeil 8h | | | | | | | |

---

## 🔗 Navigation rapide

### 📁 Dossiers
| | | |
|:---:|:---:|:---:|
| [[00-Inbox/\|📥 Inbox]] | [[01-Daily/\|📅 Daily]] | [[02-Journal/\|📔 Journal]] |
| [[03-Projects/\|🚀 Projects]] | [[04-Areas/\|🏠 Areas]] | [[05-Resources/\|📚 Resources]] |
| [[06-Archive/\|📦 Archive]] | [[07-MediaDB/\|🎬 MediaDB]] | [[08-Research/\|🔬 Research]] |

### 📊 Reviews
| | | |
|:---:|:---:|:---:|
| [[Weekly Review\|📅 Weekly]] | [[Monthly Review\|📆 Monthly]] | [[Yearly Review\|📅 Yearly]] |

---

## 💡 Citation du jour

> *Ajoutez vos citations préférées ici et utilisez le plugin "Random Quote" pour les afficher aléatoirement.*

---

<center>

**🌟 Life OS v1.0** | Made with 💜 in Obsidian

</center>
