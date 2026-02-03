# 📥 Inbox

> Point d'entrée pour toutes les captures rapides. À traiter régulièrement.

## 🎯 Objectif
Capturer rapidement toute idée, tâche ou information sans interrompre ton flux de travail.

## 📝 Workflow
1. **Capturer** - Utilise `Ctrl+Shift+A` pour créer une note rapide
2. **Clarifier** - Lors de ta revue, détermine de quoi il s'agit
3. **Organiser** - Déplace vers le bon dossier ou supprime
4. **Objectif** - Garder l'inbox vide (ou presque)

## 📊 Notes à traiter
```dataview
LIST
FROM "00-Inbox"
WHERE file.name != "README"
SORT file.ctime DESC
```
