---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#group-by
Status: Processed
Type: Tutorial
Tags:
  - Obsidian/Plugins/Dataview/Commands/GROUP-BY
---

## **Group All Results On A Field**

- Yields one row per unique field value, which has 2 properties
	- one corresponding to the field being grouped on
	- a `rows` array field which contains all of the pages that matched

```
	GROUP BY field
	GROUP BY (computed_field) AS name
```

- In order to make working with with the `rows` easier, Dataview supports field "swizzling".

### **To Have The Field  `test` From Every Object In `rows` Arrray, `rows.test` Will Automatically Fetch The `test` Field From Every Object In `rows`, Yielding A New Array.

- You can then apply aggregation operators like `sum` or `flat` over the resulting array