---
Status: Unprocessed
Source: 
  - (https: //blacksmithgu.github.io/obsidian-dataview/queries/structure/)
  - https: //blacksmithgu.github.io/obsidian-dataview/queries/query-types/
Tags:
	- DataQuery/Structure
  - DataQuery/Examples
  - DataQuery/Types
---

## ![[Dataview Query Structure]]

## Examples

### Choose An Output Format

- [[Dataview Query Output Formats]]
	-  [[Dataview Query Type - LIST]]
	- [[Dataview Query Type - TABLE]]
	- [[Dataview Query Type - TASK]]
	- [[Dataview Query Type - CALENDAR]]


## More Examples

```
	TASK
```

```
	TABLE recipe-type AS "type", portions, length
	FROM #recipes
```

```
	LIST
	FROM #assignments
	WHERE status = 'open'
```

```
	TABLE file.ctime, appointment.type, appointment.time, follow-ups
	FROM "30 Protocols/32 Management"
	WHERE follow-ups
	SORT appointment.time
```

```
	TABLE L.text AS "My lists"
	FROM "dailys"
	FLATTEN file.lists AS L
	WHERE contains(L.author, "Surname")
```

```
	LIST rows.c
	WHERE typeof(contacts) = "array" AND contains(contacts, [[Mr. L]])
	SORT length(contacts)
	FLATTEN contacts as c
	SORT link(c).age ASC
```

### **Show all games in the games folder, sorted by rating, with some metadata:**

```
	TABLE
  time-played AS "Time Played",
  length AS "Length",
  rating AS "Rating"
FROM "games"
SORT rating DESC
```

### **List games which are MOBAs or CRPGs.**

```
	LIST FROM #games/mobas OR #games/crpg
```

### **List all tasks in un-completed projects:**

```
	TASK FROM "dataview"
```

### **List all of the files in the `books` folder, sorted by the last time you modified the file:**

```
	TABLE file.mtime AS "Last Modified"
FROM "books"
SORT file.mtime DESC
```

### **List all files which have a date in their title (of the form `yyyy-mm-dd`), and list them by date order.**

```
	LIST file.day WHERE file.day SORT file.day DESC
```

