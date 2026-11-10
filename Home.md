---
cssclass: home
---

# 🏠 Mon Vault — Œuvres

> [!info] Bienvenue
> Tableau de bord de mon suivi d'œuvres (anime, manga, manhwa, manhua).

## 📊 Tableau de bord
👉 [[DATAVIEW]]

## 📺 À voir / En cours
👉 [[A VOIR-REGARDER]]

## 🗂️ Par type
- [[oeuvres/anime/]] — Anime
- [[oeuvres/manga/]] — Manga
- [[oeuvres/manhwa/]] — Manhwa
- [[oeuvres/manhua/]] — Manhua

## 🎭 Par genre
```dataview
list from "genres"
sort file.name asc
```

## 🔥 Favoris
```dataview
list from "oeuvres"
where favori = true
sort rating desc
limit 10
```
