---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#where
Status: Unprocessed
Tags:
  - Obsidian/Plugins/Dataview/Commands/WHERE
---

## Filter Pages On Fields

- Only pages where the clause evaluates to `true` will be yielded.

```
	WHERE <clause>
```

### **Obtain All Files Which Were Modified In The Last 24 Hours**

```
	LIST WHERE file.mtime >= date(today) - dur(1 day)
```

### **Find All Projects Which Are Not Marked Complete And Are More Than A Month Old**

```
	LIST FROM #projects
	WHERE !completed AND file.ctime <= date(today) - dur(1 month)
```

### **List All Pages That Were `due` Before Today**

```
	LIST
	WHERE due AND due < date(today)
```

