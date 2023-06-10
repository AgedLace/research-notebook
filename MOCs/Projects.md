---
Type: MOC
Links:
MOC: 
  - [[MOCs]]
  - [[Home]]
---

## Active Projects

```dataview
table standing, priority
from #Project/Active AND "Projects"
sort priority desc
```

## Ongoing Projects

```dataview 
table standing 
from #Project/Ongoing 
where !"Templates"
sort file.name asc 
```

## Upcoming Projects

```dataview
table standing
from #project/soon
where !"Templates"
sort file.name asc
```

## Archived Projects

```dataview
list
from #project/archive
sort file.mtime asc
where !"Templates"
limit 15
```