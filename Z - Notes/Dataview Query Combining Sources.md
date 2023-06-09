---
Source: https://blacksmithgu.github.io/obsidian-dataview/reference/sources/combining-sources
Status:  Unprocessed
Tags: 
  - Obsidian/Plugins/Dataview/Sources/Combined
---

## Compose Filters To Get More Advanced Sources Using `AND` and `OR`

### **Return All Pages In `folder` With `#tag`**

```
	FROM #tag AND "folder"
```

### **Return Only Pages Containing `#food` But Not `#fastfood`**

```
	FROM #food and !#fastfood
```

### **Return Any Pages Which Link to ``[[Food]] OR [[Exercise]]`**

```
	FROM [[Food]] OR [[Exercise]]
```

## Complex Queries

- use parenthesis to logically group items

```
	FROM #tag AND ("folder" OR #other-tag)
```

```
	FROM (#tag1 OR #tag2) AND (#tag3 or #tag4)
```

