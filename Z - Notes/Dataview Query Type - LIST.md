---
Status: Unprocessed
Source: 
  - (https: //blacksmithgu.github.io/obsidian-dataview/queries/structure/)
  - https: //blacksmithgu.github.io/obsidian-dataview/queries/query-types/
Tags:
  - Obsidian/Plugins/Dataview/Types/LIST
---

### **The simplest LIST query outputs a bullet point list of all files in your vault**

```
	LIST
```

Choose A Source
	- [[Dataview Query Sources]]

- Add Additional Information to your query by specifying it right after the `LIST` command and befoe possiby available data commands.

### **List Files and the Folders They Are In**

```
	LIST file.folder
```

- You can only add **ONE** additional information, not multiple.
- You can **specify a computered value** instead of a plain metadata field, which can contained information of multiple fields

```
	LIST "File Path: " + file.folder + " _(created: " + file.cday + ")_"
FROM "Games"
```

Filter, Sort, Group or Limit Results
- [[Dataview Query Command - FROM]]

```
	LIST 
FROM #games/mobas OR #games/crpg
```

- [[Dataview Query Command - WHERE]]
- [[Dataview Query Command - SORT]]
- [[Dataview Query Command - GROUP BY]]

- A **grouped list** shows their group keys, and only the group keys, by default

```
	LIST
	GROUP BY type
```

### **Add File Lnks to Output By Specifying Them As Additional Information**

```
	LIST rows.file.link
	GROUP BY type
```

## LIST WITHOUT ID

- Remove the file name or group key included in list view with `LIST WITHOUT ID`

```
	LIST WITHOUT ID
```

```
	LIST WITHOUT ID type
```

- Can be handy  to output computed values

```
	LIST WITHOUT ID length(rows) + " pages of type " + key
GROUP BY type
```

- [[Dataview QUery Command - FLATTEN]]
- [[Dataview Query Command - LIMIT]]

## Combination Queries

### **List All Pages that have `due` and where `due` is before today**

```
	LIST
	WHERE due AND due < date(today)
```


### **List the 10 most recently created pages that have the tag `status/open`**

```
	LIST
	FROM #status/open
	SORT file.ctime DESC
	LIMIT 10
```


### **List the 10 oldest and incompleted tasks as an interactive task list, grouped by their containing file and sorted from oldest to newest file.**

```
	TASK
	WHERE !completed
	SORT created ASC
	LIMIT 10
	GROUP BY file.link
	SORT rows.file.ctime ASC
```
