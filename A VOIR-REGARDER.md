# 📺 À VOIR / À LIRE

> [!info] Ma liste de suivi
> Œuvres marquées comme `à-voir` dans le front matter, mises à jour automatiquement.

## 🎬 À voir (statut à-voir)
```dataview
table type, genre, annee, rating
from "oeuvres"
where statut = "à-voir"
sort file.name asc
```

## ⏳ En cours
```dataview
table type, progression, total
from "oeuvres"
where statut = "en-cours"
sort progression desc
```

## ✅ Checklist manuelle
- [ ] Death note
- [ ] One piece
```