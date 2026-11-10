# Fantasy

## Description
> Genre : **Fantasy**

## Oeuvres

```dataview
table statut, progression, total, rating, type
from "oeuvres"
where contains(genre, this.file.link)
sort statut asc, file.name asc
```

## Favoris

```dataview
table rating, statut
from "oeuvres"
where contains(genre, this.file.link) and favori = true
sort rating desc
```

## En cours

```dataview
list from "oeuvres"
where contains(genre, this.file.link) and statut = "en-cours"
```

## Termines

```dataview
list from "oeuvres"
where contains(genre, this.file.link) and statut = "terminé"
```

## Statistiques

```dataviewjs
const pages = dv.pages('"oeuvres"').where(p => (p.genre || []).some(g => g.path === dv.current().file.path));
dv.paragraph("**Total :** " + pages.length + " | **En cours :** " + pages.where(p=>p.statut==="en-cours").length + " | **Termines :** " + pages.where(p=>p.statut==="terminé").length);
```
