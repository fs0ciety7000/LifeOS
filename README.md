# 🌟 Life OS - Obsidian Vault

> Un système personnel complet pour organiser ta vie, tes projets, tes médias et ta croissance personnelle.

## 📁 Structure

```
LifeOS/
├── 00-Inbox/           # 📥 Capture rapide (à traiter)
├── 01-Daily/           # 📅 Notes quotidiennes
│   ├── 2025/
│   └── 2026/
├── 02-Journal/         # 📔 Journaux
│   ├── Perso/
│   └── Couple/
├── 03-Projects/        # 🚀 Projets actifs
├── 04-Areas/           # 🏠 Domaines de vie
│   ├── Santé/
│   ├── Finances/
│   ├── Carrière/
│   ├── Développement-Personnel/
│   ├── Relations/
│   └── Maison/
├── 05-Resources/       # 📚 Ressources & références
│   ├── Articles/
│   ├── Livres/
│   ├── Cours/
│   └── Tutoriels/
├── 06-Archive/         # 📦 Archives
├── 07-MediaDB/         # 🎬 Base de données médias
│   ├── Films/
│   ├── Séries/
│   ├── Jeux/
│   ├── Livres/
│   └── Musique/
├── 08-Research/        # 🔬 Recherche & études
│   ├── Notes/
│   ├── Sources/
│   └── Projects/
├── 09-Templates/       # 📝 Modèles
└── 99-Attachments/     # 📎 Pièces jointes
```

## 🚀 Installation

### 1. Plugins essentiels à installer

Ouvre Obsidian > Settings > Community Plugins > Browse

**Indispensables :**
- **Dataview** - Requêtes dynamiques (affiche listes, tables)
- **Templater** - Templates avancés avec variables
- **QuickAdd** - Création rapide de notes
- **Calendar** - Vue calendrier
- **Periodic Notes** - Daily/Weekly/Monthly notes
- **Tasks** - Gestion des tâches avancée

**Recommandés :**
- **Kanban** - Tableaux Kanban
- **Full Calendar / Google Calendar** - Intégration calendrier
- **Banners** - Images d'en-tête
- **Style Settings** - Personnalisation du thème
- **Excalidraw** - Dessins et diagrammes
- **Charts** - Graphiques

### 2. Configuration des plugins

#### Templater
```
Settings > Templater > Template folder location: 09-Templates
```

#### Periodic Notes
```
Daily Note:
  - Format: YYYY-MM-DD
  - Location: 01-Daily/{{date:YYYY}}
  - Template: 09-Templates/Daily Note.md

Weekly Note:
  - Format: YYYY-[W]WW
  - Location: 01-Daily/{{date:YYYY}}
  - Template: 09-Templates/Weekly Review.md
```

#### QuickAdd - Macros recommandées

| Raccourci | Action |
|-----------|--------|
| `Ctrl+Shift+D` | Nouvelle Daily Note |
| `Ctrl+Shift+J` | Nouveau Journal Perso |
| `Ctrl+Shift+C` | Nouveau Journal Couple |
| `Ctrl+Shift+F` | Ajouter Film |
| `Ctrl+Shift+S` | Ajouter Série |
| `Ctrl+Shift+L` | Ajouter Livre |
| `Ctrl+Shift+G` | Ajouter Jeu |
| `Ctrl+Shift+P` | Nouveau Projet |
| `Ctrl+Shift+R` | Nouvelle Note Research |

### 3. Activer les CSS Snippets
```
Settings > Appearance > CSS Snippets > Activer:
  ✅ dashboard.css
  ✅ global-theme.css
```

## 🔄 Synchronisation Multi-Device

### Option 1: Obsidian Sync (Payant - Recommandé)
- Natif, sécurisé, synchronisation en temps réel
- Fonctionne sur toutes les plateformes
- ~$5/mois ou ~$50/an

### Option 2: Syncthing (Gratuit)

#### Desktop (Bazzite Linux)
```bash
# Installation
flatpak install flathub me.kozec.syncthingtk
# ou
sudo dnf install syncthing

# Lancer et configurer
syncthing
```

#### Android (Samsung S25 Ultra)
1. Installer "Syncthing-Fork" depuis F-Droid ou Play Store
2. Ajouter le dossier du vault
3. Connecter les deux appareils via ID

#### Configuration
- Sync bidirectionnelle
- Exclure: `.obsidian/workspace.json`, `.obsidian/plugins/*/data.json`

### Option 3: Git + Working Copy (iOS) / Termux (Android)

```bash
# Sur desktop, après modifications
git add .
git commit -m "Sync $(date +%Y-%m-%d)"
git push

# Sur mobile, pull régulièrement
git pull
```

## ⌨️ Raccourcis clavier

| Raccourci | Action |
|-----------|--------|
| `Ctrl+O` | Switcher rapide |
| `Ctrl+G` | Graph View |
| `Ctrl+Shift+F` | Recherche globale |
| `Ctrl+Shift+P` | Palette de commandes |
| `Ctrl+Shift+A` | QuickAdd |
| `Ctrl+Shift+T` | Insérer template |
| `Ctrl+Enter` | Toggle checkbox |
| `Alt+←/→` | Navigation historique |

## 📱 Configuration Mobile

### Obsidian Mobile
1. Installer depuis Play Store / App Store
2. Ouvrir le vault synchronisé
3. Activer les mêmes plugins essentiels
4. Les CSS snippets fonctionnent automatiquement

### Raccourcis mobiles
- Swipe depuis la gauche → Sidebar
- Appui long sur + → Menu création rapide
- Pull-to-refresh dans les notes

## 🎨 Personnalisation du thème

Le thème inclus est optimisé pour 2026 avec:
- Glass-morphism effects
- Gradients modernes (purple/blue)
- Dark mode optimisé
- Support mobile complet

### Couleurs personnalisables
Modifie `.obsidian/snippets/global-theme.css` pour changer:
- `--interactive-accent`: Couleur principale
- `--tag-color`: Couleur des tags
- Gradients et effets néon

## 📊 Dashboard

Le fichier `🏠 Dashboard.md` est ta page d'accueil centrale.

**Fonctionnalités:**
- Vue des tâches du jour
- Projets actifs
- Inbox à traiter
- MediaDB en cours
- Statistiques d'habitudes

**Conseil:** Définis-le comme page d'accueil:
```
Settings > Core Plugins > Enable "Home" > Set to "🏠 Dashboard"
```

## 🔗 Intégration Google Calendar

### Plugin: Full Calendar ou Google Calendar

1. Créer un projet Google Cloud Console
2. Activer Calendar API
3. Créer des credentials OAuth
4. Configurer le plugin avec les credentials

Ou utiliser l'intégration ICS:
1. Obtenir l'URL ICS de ton calendrier Google
2. Configurer dans le plugin Calendar

## 📝 Workflow quotidien suggéré

### Matin (5 min)
1. Ouvrir Dashboard
2. Créer la Daily Note (`Ctrl+Shift+D`)
3. Définir les 3 priorités du jour
4. Vérifier l'agenda

### Journée
- Capturer dans Inbox (`Ctrl+Shift+A`)
- Cocher les tâches complétées
- Ajouter notes dans la Daily Note

### Soir (10 min)
1. Compléter la Daily Note
2. Journal Perso si envie
3. Tracker les habitudes
4. Prévoir demain

### Hebdomadaire (30 min)
- Weekly Review le dimanche
- Traiter l'Inbox
- Planifier la semaine

## 🆘 Support

- [Documentation Obsidian](https://help.obsidian.md)
- [Forum Obsidian](https://forum.obsidian.md)
- [Discord Obsidian](https://discord.gg/obsidianmd)

---

**Version:** 1.0
**Créé le:** Février 2026
**Licence:** MIT - Libre d'utilisation et modification
