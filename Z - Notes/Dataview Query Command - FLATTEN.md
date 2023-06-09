---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#flatten
Status: Unprocessed
Tags:
  - Obsidian/Plugins/Dataview/Commands/FLATTEN
---

## **Flatten An Array In Every Row, Yielding One Result Row Per Entry In The Array**

```
	FLATTEN field
	FLATTEN (computed_field) AS name
```

## **Flatten The `authors` Field In Each Literature Note To Give One Row Per Author**

```
	TABLE authors FROM #LiteratureNote
	FLATTEN authors
```

- A good use would be when there is a deeply nested list that you want to use more easily.
- `file.lists` or `file.tasks`
	- Notice the simpler query
	- Though the end results are slightly different (grouped vs non-grouped)
	- You can use a `GROUP BY file.link` to achieve identical results but would need to use `rows.T.text`.

```
	table T.text as "Tazsk Text"
	from "Scratchpad"
	flatten file.tasks as T
	where T.text
```

```
	table filter (file.tasks.text, (t) => t) as "Task Text"
	from "Scratchpad"
	where file.tasks.text
```

- `FLATTEN` makes it easier to operate on nested lists since you can then use simpler where conditions on them as opposed to using functions like `map()` or `filter()`.
- 