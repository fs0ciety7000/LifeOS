---
cssclasses:
  - dashboard
  - wide-page
banner: "99-Attachments/banner.png"
banner_y: 0.5
---

<div class="dashboard-header">
<div class="profile-section">

![[avatar.png|150]]

</div>
<div class="clock-section">

# Dashboard 2026

```dataviewjs
const now = new Date();
const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
const dateStr = now.toLocaleDateString('fr-FR', options);
dv.paragraph(`**${dateStr.charAt(0).toUpperCase() + dateStr.slice(1)}**`);
```

</div>
</div>

> [!quote|clean] 🎯 *2026's Plans and Milestones* 🚀

---

## Main Hub

> [!multi-column]
>
>> [!note|green] 💚 Health
>> - 🛏️ [[Sleep Log|Sleep]]
>> - 🥗 [[Nutrition|Diet]]
>> - 💪 [[Fitness Tracker|Fitness]]
>> - 🧠 [[Mental Health|Mind]]
>> - 🩺 [[Medical Timeline]]
>
>> [!note|yellow] 🏠 Homes
>> - 🏡 [[Home]]
>> - 📋 [[Life OS Home]]
>> - 🎯 [[Goals 2026]]
>> - 📅 [[Weekly Planning]]
>> - 🗂️ [[Archive Home]]
>
>> [!note|cyan] 🔬 ADHD & Mind
>> - 📊 [[Weekly Research]]
>> - 💡 [[ADHD Tips]]
>> - 🧪 [[My ADHD]]
>> - 📚 [[Learning Hub]]
>
>> [!note|purple] 🗺️ Road Maps
>> - 🐍 [[Python for AI]]
>> - 🎯 [[Career Roadmap]]
>> - ♟️ [[Chess Roadmap]]
>> - 🧠 [[Machine Learning]]
>> - 💭 [[Philosophy Path]]

---

> [!multi-column]
>
>> [!note|orange] 📊 Tracking
>> - 📚 [[Bookshelf]]
>> - 🎬 [[Movies]]
>> - 📺 [[TV Shows]]
>> - 🎮 [[Games]]
>> - 🎵 [[Music]]
>
>> [!note|pink] 💭 Philosophy
>> - 📜 [[Philosophical Views]]
>> - 🙏 [[Philosophy & Religion]]
>> - 💫 [[Life Philosophy]]
>> - 🌱 [[Seeds of Doubt]]
>
>> [!note|blue] 🎨 Content Creation
>> - 📝 [[Blog Ideas]]
>> - 🎥 [[Video Projects]]
>> - 💻 [[Dev Projects]]
>> - *Soon...*

---

## Vault Info

> [!multi-column]
>
>> [!note|gray] 📄 Recent file updates
>> ```dataview
>> LIST WITHOUT ID file.link
>> FROM ""
>> WHERE file.name != "🏠 Dashboard" AND !contains(file.path, "09-Templates")
>> SORT file.mtime DESC
>> LIMIT 8
>> ```
>
>> [!note|teal] 🏷️ Tagged
>> ```dataview
>> LIST WITHOUT ID file.link
>> FROM #favorite OR #priority
>> LIMIT 6
>> ```
>
>> [!note|indigo] 📈 Stats
>> - 📁 **Files:** `$= dv.pages().length`
>> - 📔 **Daily Notes:** `$= dv.pages('"01-Daily"').length`
>> - 🎬 **Media Logged:** `$= dv.pages('"07-MediaDB"').length`
>> - 📚 **Books:** `$= dv.pages('"07-MediaDB/Livres"').length`
>> - 🔬 **Research:** `$= dv.pages('"08-Research"').length`

---

## 📅 On Today

> [!multi-column]
>
>> [!note|clean wide-2] 📆 Recent Journal
>> ```dataview
>> TABLE WITHOUT ID
>>   file.link as "Entry",
>>   mood as "Mood"
>> FROM "02-Journal/Perso"
>> SORT file.ctime DESC
>> LIMIT 4
>> ```
>
>> [!note|clean wide-1] 🗓️ Calendar
>> ```dataviewjs
>> const today = dv.date("today");
>> dv.header(4, today.toFormat("MMMM yyyy"));
>> dv.paragraph("📍 **Today:** " + today.toFormat("EEEE, d"));
>> ```
>>
>> [[01-Daily/2026/2026-02-03|→ Today's Note]]

---

## 🚀 Active Projects

```dataview
TABLE WITHOUT ID
  file.link as "📁 Project",
  status as "📊 Status",
  priority as "🎯",
  due as "📅 Due"
FROM "03-Projects"
WHERE status != "✅ completed" AND status != "📦 archived"
SORT priority ASC
LIMIT 6
```

---

## 📚 Currently Consuming

> [!multi-column]
>
>> [!note|book] 📖 Reading
>> ```dataview
>> TABLE WITHOUT ID
>>   file.link as "Book",
>>   author as "Author",
>>   "p." + current_page + "/" + pages as "Progress"
>> FROM "07-MediaDB/Livres"
>> WHERE status = "👀 en cours"
>> LIMIT 3
>> ```
>
>> [!note|tv] 📺 Watching
>> ```dataview
>> TABLE WITHOUT ID
>>   file.link as "Show",
>>   "S" + current_season + "E" + current_episode as "Progress"
>> FROM "07-MediaDB/Séries"
>> WHERE status = "👀 en cours"
>> LIMIT 3
>> ```
>
>> [!note|game] 🎮 Playing
>> ```dataview
>> TABLE WITHOUT ID
>>   file.link as "Game",
>>   playtime + "h" as "Time"
>> FROM "07-MediaDB/Jeux"
>> WHERE status = "🎮 en cours"
>> LIMIT 3
>> ```

---

## ⭐ Recently Completed

```dataview
TABLE WITHOUT ID
  file.link as "Title",
  type as "Type",
  rating + "/10 ⭐" as "Rating",
  date_finished as "Finished"
FROM "07-MediaDB"
WHERE contains(status, "✅")
SORT date_finished DESC
LIMIT 5
```

---

## ✅ Tasks

> [!multi-column]
>
>> [!todo] 📋 Due Today
>> ```tasks
>> due today
>> not done
>> short mode
>> limit 5
>> ```
>
>> [!todo] 📅 Upcoming
>> ```tasks
>> due after today
>> due before in 7 days
>> not done
>> short mode
>> limit 5
>> ```
>
>> [!done] ✅ Done Recently
>> ```tasks
>> done after 3 days ago
>> short mode
>> limit 5
>> ```

---

## 💡 Quick Actions

| | | | |
|:---:|:---:|:---:|:---:|
| [[09-Templates/Daily Note\|📅 Daily]] | [[09-Templates/Quick Capture\|📥 Capture]] | [[09-Templates/Journal Perso\|📔 Journal]] | [[09-Templates/Project\|🚀 Project]] |
| [[09-Templates/Film\|🎬 Film]] | [[09-Templates/Série\|📺 Series]] | [[09-Templates/Livre\|📚 Book]] | [[09-Templates/Jeu\|🎮 Game]] |

---

## 🔗 Navigation

> [!multi-column]
>
>> **📁 Folders**
>> [[00-Inbox/README|📥 Inbox]] • [[01-Daily/README|📅 Daily]] • [[02-Journal/README|📔 Journal]]
>> [[03-Projects/README|🚀 Projects]] • [[04-Areas/README|🏠 Areas]] • [[07-MediaDB/README|🎬 Media]]
>
>> **📊 Reviews**
>> [[Weekly Review|📅 Weekly]] • [[Monthly Review|📆 Monthly]] • [[Yearly Review|📅 Yearly]]

---

<center>

**✨ Life OS v2.0** | Made with 💜 in Obsidian | *Inspired by SlRvb*

</center>
