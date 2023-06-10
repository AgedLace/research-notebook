---
Status: Processed
Type: Tutorial
Source: 
  - (https: //blacksmithgu.github.io/obsidian-dataview/queries/structure/)
  - https: //blacksmithgu.github.io/obsidian-dataview/queries/query-types/
Tags:
  - Obsidian/Plugins/Dataview/Types/TASK
---

## Interactive Task Lists

- [[Dataview Query Commands]] operate on the Task level so you can filter them
- Dataview Queries are the only possibility to *manipulate your files*; normally Dataview does not touch the content of your files
	- If you check a TASK in Dataview, it will be checked in your file, too

```
	TASK
```

### **Use [[Dataview Query Commands]] to refine your query**

```
	TASK
	WHERE !completed AND contains(tags, "#shopping")
```

### **Group Tasks By Their Originating File**

```
	TASK
	WHERE !completed
	GROUP BY file.link
```

## Child Tasks

- belong to their parent task
	- you'll get child tasks as part of the parent **as long as the parent matches the query**
	- you'll get individual children back **if the child matches your predicate but the parent does not**
- are not counted separately
- behave differently on filtering
- a task is a 'child' task if ...
	- it is indented by a tab
	- AND is below an unindented task

```
	TASK
```

```
	TASK
	WHERE !completed
```

```
TASK
WHERE urgent
```

