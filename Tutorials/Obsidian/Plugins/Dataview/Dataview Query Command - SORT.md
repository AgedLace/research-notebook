---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#sort
Status: Processed
Type: Tutorial
Tags:
  - Tutorials/Obsidian/Plugins/Dataview/Commands/SORT
---

## **Sorts All Results By One Or More Fields**

```
	SORT date [ASCENDING/DESCENDING/ASC/DESC]
```

## **Sort On Multiple Fields. `SORT` Will Be Done Based On The First Field**

- IF a tie occurs, the second field will be used to sort the tied fields.  IF still a tie, the third field will resolve in, and so on.

```
	SORT field1 [ASCENDING/DESCENDING/ASC/DESC], ... fieldN [ASC/DESC]
```


