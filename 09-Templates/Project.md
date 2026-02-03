---
title: "{{title}}"
type: project
status: 💡 idée | 🎯 planifié | 🚧 en cours | ⏸️ en pause | ✅ complété | ❌ abandonné
priority: 🔴 haute | 🟠 moyenne | 🟢 basse
date_created: {{date}}
date_start:
date_deadline:
date_completed:
area:
tags:
  - project
---

# 🚀 {{title}}

## 📋 Aperçu

| | |
|---|---|
| **Statut** | {{status}} |
| **Priorité** | {{priority}} |
| **Domaine** | {{area}} |
| **Deadline** | {{date_deadline}} |

## 🎯 Objectif
> Quel est le résultat final attendu ?



## 💡 Pourquoi ce projet ?


## ✅ Critères de succès
- [ ]
- [ ]
- [ ]

## 📊 Progression

```dataview
TASK
FROM "03-Projects/{{title}}"
GROUP BY completed
```

### Jalons
- [ ] 🏁 Jalon 1 - Date:
- [ ] 🏁 Jalon 2 - Date:
- [ ] 🏁 Jalon finale - Date:

## 📝 Tâches

### À faire
- [ ]

### En cours
- [ ]

### Complété
- [x]

## 📅 Timeline
```mermaid
gantt
    title Timeline du projet
    dateFormat  YYYY-MM-DD
    section Phase 1
    Tâche 1           :a1, 2026-01-01, 7d
    section Phase 2
    Tâche 2           :a2, after a1, 5d
```

## 📁 Ressources
-

## 👥 Personnes impliquées
-

## 📝 Notes


## 💭 Réflexions / Retours


## 🔗 Liens
- [[04-Areas/{{area}}|Domaine associé]]

## 🏷️ Tags
#project #{{area}} #{{status}}
