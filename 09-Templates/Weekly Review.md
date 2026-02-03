---
date: {{date}}
type: weekly
week: {{date:WW}}
year: {{date:YYYY}}
tags:
  - weekly
  - review
---

# 📊 Revue Semaine {{date:WW}} - {{date:YYYY}}

> *Du {{monday:DD/MM}} au {{sunday:DD/MM}}*

## 🎯 Objectifs de la semaine

### Priorités définies
1.
2.
3.

### Résultats
- [ ] Objectif 1 -
- [ ] Objectif 2 -
- [ ] Objectif 3 -

## 📈 Bilan

### ✅ Accomplissements
```dataview
TASK
FROM "01-Daily"
WHERE completed AND file.day >= date({{monday:YYYY-MM-DD}}) AND file.day <= date({{sunday:YYYY-MM-DD}})
LIMIT 20
```

### 🎓 Ce que j'ai appris


### 💡 Insights & Idées


### 😤 Frustrations / Obstacles


## 📊 Statistiques

### Habitudes (jours complétés / 7)
| Habitude | L | M | M | J | V | S | D | Total |
|----------|---|---|---|---|---|---|---|-------|
| 💧 Hydratation | | | | | | | | /7 |
| 🏃 Exercice | | | | | | | | /7 |
| 📚 Lecture | | | | | | | | /7 |
| 🧘 Méditation | | | | | | | | /7 |

### Moyennes
- Énergie moyenne: /10
- Humeur moyenne: /10
- Heures de sommeil: h

## 🔮 Semaine prochaine

### Priorités
1.
2.
3.

### Événements importants


### À ne pas oublier


## 💭 Réflexion

### Ce qui a bien fonctionné


### Ce que je veux améliorer


### Note à moi-même


## 🔗 Navigation
- ⬅️ [[Weekly Review {{date-7d:YYYY-[W]WW}}|Semaine précédente]]
- ➡️ [[Weekly Review {{date+7d:YYYY-[W]WW}}|Semaine suivante]]
- 📅 [[Monthly Review {{date:YYYY-MM}}|Mois]]
