---
Source: https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#from
Status: Unprocessed
Tags:
  - Obsidian/Plugins/Dataview/Commands/FROM
  - Obsidian/Plugins/Dataview/Sources
  - Obsidian/Plugins/Dataview/Sources/Combined
---

## Restrict Dataview Queries with 'FROM'

- `FROM` takes a source, or a combination of sources as an argument
- See [[Dataview Query Sources]] and [[Dataview Query Combining Sources]]

### `FROM` Sources are one or more of ...

- Tags
			- Use `FROM #tag`
- Folders
	- Use `FROM "folder"`
- Single Files
	- Use `FROM path/to/file`
- Links
	- TO a file
	- FROM a file
	- ALL links
		- All pages TO a file
			- Use `FROM [[note]]`
		- All pages FROM a file
			- Use `FROM outgoing([[note]])`

You can compound these filters using `AND` and `OR`.

#### **Return All Pages in `"folder"` with `#tag` , *i.e.*

```
	FROM #tag AND "folder"
```

#### **Return All Pages Which Link to `[[food]]` `OR` `[[Exercise]]`**

```
	FROM [[Food]] or [[Exercise]]
```

#### **Exclude Files Which Have `#tag`**

```
	FROM -#tag
```

#### **Only Include Files Tagged With `#tag` Which Are NOT in `folder`**

```
	FROM #tag and -"folder"
```

#### **List All Pages Inside Folder 'Books' and It's Sub Folders**

```
	```dataview 
	LIST 
	FROM "Books" 
	```
```

#### **List All Pages That Include Tag `#status/open` or `#status/wip`**

```
	```dataview
	LIST
	FROM #status/open OR #status/wip
```

#### **List All Pages That Have Either The Tag `#assignment` And Are Inside Folder `"30 School"` (Or Its Sub Folders), Or Are Inside Folder `"30 School/32 Homeworks"` And Are Linked On Page `School Dashboard Current To Dos`**

```
	LIST 
	FROM (#assignment AND "30 School") OR ("30 School/32 Homeworks" AND outgoing([[School Dashboard Current To Dos]])) 
	```
```

