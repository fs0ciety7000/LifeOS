---
date: {{date}}
type: monthly
month: {{date:MMMM}}
year: {{date:YYYY}}
tags:
  - monthly
  - review
---

# 📆 Revue {{date:MMMM YYYY}}

## 🎯 Objectifs du mois

### Définis en début de mois
1.
2.
3.

### Résultats
| Objectif | Statut | Notes |
|----------|--------|-------|
| | ✅/❌/🔄 | |

## 📊 Bilan des semaines

```dataview
TABLE WITHOUT ID
  file.link as "Semaine",
  length(filter(file.tasks, (t) => t.completed)) as "✅ Complétées"
FROM "01-Daily"
WHERE type = "weekly" AND date.month = {{date:M}} AND date.year = {{date:YYYY}}
SORT date ASC
```

## 🏆 Accomplissements majeurs
1.
2.
3.

## 📚 Ce que j'ai appris


## 🎬 Médias consommés
```dataview
TABLE WITHOUT ID
  file.link as "Titre",
  type as "Type",
  rating as "Note"
FROM "07-MediaDB"
WHERE date_finished >= date({{date:YYYY-MM}}-01) AND date_finished < date({{date+1M:YYYY-MM}}-01)
SORT rating DESC
```

## 📈 Statistiques

### Habitudes (moyenne)
| Habitude | Taux |
|----------|------|
| 💧 Hydratation | % |
| 🏃 Exercice | % |
| 📚 Lecture | % |
| 🧘 Méditation | % |

### Bien-être
- Énergie moyenne: /10
- Humeur moyenne: /10

## 💰 Finances (optionnel)


## 🔮 Mois prochain

### Priorités
1.
2.
3.

### Objectifs SMART
1.

## 💭 Réflexion du mois


## 🔗 Navigation
- ⬅️ [[Monthly Review {{date-1M:YYYY-MM}}|Mois précédent]]
- ➡️ [[Monthly Review {{date+1M:YYYY-MM}}|Mois suivant]]
- 📅 [[Yearly Review {{date:YYYY}}|Année]]
