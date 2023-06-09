---
Status: Reviewing
Tags: 
- Dataview-Query/MOC-Index 
- Dataview-Query/Recently-Opened-Notes
- Dataview-Query/Unprocessed-Notes
---


## MOC Index

```dataview
table from #MOC
sort file.mtime desc
```

## Recently Opened Notes 

```dataview
table from "/"
where file.name != "Home Note"
sort file.mtime desc
limit 5
```

## Unprocessed Notes


```dataview
table WITHOUT ID filename as "Title", "status" as "Status"
WHERE "Status" = "Unprocessed"
```

```dataview
table
from "" and !outgoing([[]])
where file.folder != "Templates"
sort file.name asc
```

## All Tasks In Vault

```dataview 
TASK 
```
