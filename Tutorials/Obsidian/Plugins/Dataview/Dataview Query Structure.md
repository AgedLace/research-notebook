---
Status: Processed
Type: Tutorial
Source: (https://blacksmithgu.github.io/obsidian-dataview/queries/structure/)
Tags:
  - Obsidian/Plugins/Dataview/Structure
  - Obsidian/Plugins/Dataview/Types
---

## Basic Query Output Structure

```
	```dataview 
	<QUERY-TYPE> <fields> 
	FROM <source> 
	<DATA-COMMAND> <expression> 
	<DATA-COMMAND> <expression> 
	...
```

- One of the 4 `Query Type` outputs (listed below) is the only mandatory part of the structure
	- TABLE
	- LIST
	- TASK
	- CALENDAR
