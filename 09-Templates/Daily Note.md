---
date: {{date}}
weekday: {{date:dddd}}
type: daily
tags:
  - daily
---

# 📅 {{date:dddd D MMMM YYYY}}

## 🌅 Intention du jour
> Quelle est mon intention principale aujourd'hui ?



## ✅ Tâches

### 🎯 Priorités (3 max)
- [ ]
- [ ]
- [ ]

### 📋 À faire
- [ ]

### ✔️ Complété
- [x]

## 📆 Agenda
```dataview
TASK
FROM "03-Projects" OR "04-Areas"
WHERE !completed AND due = date({{date:YYYY-MM-DD}})
```

## 📝 Notes du jour


## 💭 Réflexions


## 🙏 Gratitude
1.
2.
3.

## 📊 Trackers

### Habitudes
- [ ] 💧 Hydratation (8 verres)
- [ ] 🏃 Exercice
- [ ] 📚 Lecture (30 min)
- [ ] 🧘 Méditation
- [ ] 😴 8h de sommeil

### Énergie & Humeur
- Énergie: /10
- Humeur: /10
- Stress: /10

## 🔗 Liens
- ⬅️ [[{{date-1d:YYYY-MM-DD}}|Hier]]
- ➡️ [[{{date+1d:YYYY-MM-DD}}|Demain]]
- 📅 [[Weekly Review {{date:YYYY-[W]WW}}|Semaine]]
