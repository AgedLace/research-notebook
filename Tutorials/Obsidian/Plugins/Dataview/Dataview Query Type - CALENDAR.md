---
Status: Processed
Type: Tutorial
Source: 
  - (https: //blacksmithgu.github.io/obsidian-dataview/queries/structure/)
  - https: //blacksmithgu.github.io/obsidian-dataview/queries/query-types/
Tags:
  - Obsidian/Plugins/Dataview/Types/CALENDAR
---

## Monthly Based Calendar

- every result is depicted as a dot on it's referring date
- the ONLY [[Dataview Query Types | Query Type]] that requires additional information
- this additional information *needs to be a date (or unset)* on ALL queries pages

```
CALENDAR file.ctime
```

- It is possible to use `SORT` and `GROUP BY`, **It has no affect**
- the query will not render if the meta data field contains something other than a valid *DATE* (it CAN be empty)
- to ensure only valid pages, filter for valid meta data
```
	CALENDAR due
	WHERE typeof(due) = "date"
```

