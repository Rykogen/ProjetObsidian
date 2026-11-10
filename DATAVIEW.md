# 📊 Dashboard

> [!info] Mon suivi
> Ce tableau de bord se met à jour tout seul à partir des en-têtes YAML de mes œuvres.

## 📖 En cours 
```dataview
table progression, total, rating
from "oeuvres"
where statut = "en-cours"
sort file.name asc
```

## 📚 Toute ma bibliothèque
```dataview
table without id
file.link as "Titre",
type as "Type",
statut as "Statut",
rating as "Note"
from "oeuvres"
sort file.name asc
```

## 🗂️ Classement par type
```dataview
table rows.file.link as "Titres"
from "oeuvres"
group by type
```

## 📂 Par dossier
```dataview
table without id
file.link as "Titre",
statut as "Statut"
from "oeuvres"
sort file.folder asc, file.name asc
```

## ⚔️ Les œuvres d'action
```dataview
list
from "oeuvres"
where contains(genre, "Action") or contains(genre, "[[Action]]")
```

## ⭐ Mes favoris
```dataview
table rating, statut
from "oeuvres"
where favori = true
sort rating desc
```

## 🆕 Dernières ajoutées
```dataview
table without id
file.link as "Titre",
file.ctime as "Ajoutée le"
from "oeuvres"
sort file.ctime desc
limit 5
```

## 📅 Calendrier
```dataview
calendar file.ctime
from "oeuvres"
```

## ✅ Ma CHECK LIST
```dataview
task
from "A VOIR-REGARDER"
where !completed
```

