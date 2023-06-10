---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/structure/
Status: Processed
Type: Tutorial
Tags:
  - Obsidian/Plugins/Dataview/Types
---

### Choose An Output Format

-  Dataview-Query/Types/LIST
-  Dataview-Query/Types/TABLE
-  Dataview-Query/Types/TASK
-  Dataview-Query/Types//CALENDAR

#### **List All Pages As Bullet Point List**

```
	```dataview 
	LIST 
	```
```

#### **List All Tasks - Completed Or Not**

```
	```dataview 
	TASK 
	```
```

#### **Render a Calendar View Where Each Page Is Represented As A Dot On Its Creation Date**

```
	```dataview 
	CALENDAR file.cday 
	```
```

#### **Show a Table With ALL Vault Pages, Their Due Dates, Tags and Average of Values of Multi-Value Field 'Working-Hours'**

```
	```dataview 
	TABLE due, file.tags AS "tags", average(working-hours) 
	```
```
