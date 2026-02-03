# 🔬 Research & Études

> Espace dédié à la recherche, l'apprentissage et les études approfondies.

## 📚 Recherches actives
```dataview
TABLE WITHOUT ID
  file.link as "Sujet",
  domain as "Domaine",
  status as "Statut",
  file.mtime as "Modifié"
FROM "08-Research"
WHERE (status = "🔬 exploration" OR status = "📝 en cours") AND file.name != "README"
SORT file.mtime DESC
```

## 📂 Organisation

### Notes/
Notes de recherche individuelles, concepts, définitions.

### Sources/
Références bibliographiques, articles, papers.

### Projects/
Projets de recherche plus conséquents (thèse, mémoire, etc.)

## 🔗 Méthode Zettelkasten

Cette section peut être utilisée avec la méthode Zettelkasten:
1. **Notes éphémères** → Inbox
2. **Notes de littérature** → Sources
3. **Notes permanentes** → Notes (avec liens)

## 📝 Créer une note de recherche
Utilise le template `Research Note.md` ou `Ctrl+Shift+R`
