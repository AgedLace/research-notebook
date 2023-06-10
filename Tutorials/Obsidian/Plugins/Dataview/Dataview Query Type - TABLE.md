---
Status: Processed
Type: Tutorial
Source: 
  - (https: //blacksmithgu.github.io/obsidian-dataview/queries/structure/)
  - https: //blacksmithgu.github.io/obsidian-dataview/queries/query-types/
Tags:
  - Obsidian/Plugins/Dataview/Types/TABLE
---

## Table Query Types

- Can add zero to multiple meta data fields to the query as columns
	- Add them as a *comma separated list*
- Can specify calculations as columns well
- Can specify a *table header* via the `AS <header>` syntax
- Can refine results with [[Dataview Query Commands]]

```
TABLE
```

### **Specify one to multiple additional informations**

```
TABLE started, file.folder, file.etags
FROM #games
```

### **Custom Column Headers**

```
TABLE started, file.folder AS Path, file.etags AS "File Tags"
FROM #games
```

### **Using Calculations or Expressions As Column Values**

```
TABLE 
default(finished, date(today)) - started AS "Played for", 
file.folder AS Path, 
file.etags AS "File Tags"
FROM #games
```

## Table Without ID

- Removes the default "File" or "Group" as the first column's name
- Can use this if you output another identifying value

```
TABLE WITHOUT ID
steamid,
file.etags AS "File Tags"
FROM #games
```

- Can also use to *rename first column for one specific query*

```
TABLE WITHOUT ID
file.link AS "Game"
file.etags AS "File Tags"
FROM #games
```

