---
Title: Writing A Newsletter
Alias: 
Created: Friday, June 09, 2023 23:57 pm
Last-Modified: Friday, June 09, 2023 11:57 pm
Source: 
Status: Unprocessed
Type: Source Note
Tags: Workflow/Newsletter/Create-A-System
---

# Writing A Newsletter
Created: Friday, June 09, 2023 23:57 pm
LastMmodified: Friday, June 09, 2023 11:57 pm
Source: https://bagerbach.com/blog/how-i-write-my-newsletter-with-obsidian

---

## System Requirements

- remember what you want to include
- get an overview of notes / thoughts you might write about
- keep track of things already shared (DRY)

## Plugins 

- Minimal Theme
- Dataview
- Contextual Typography for cards view

## Sample Card Template

```
---
cssClasses: cards table-wide
alias: Newsletter
---

# Weekly Newsletter

	```
	TABLE WITHOUT ID
		(link(file.path, title)) as Newsletter, file.outlinks as Links
	FROM #out/newsletter AND !"bins/templates"
	SOURT file.ctime DESC
	```
```

- `'cards` is necessary to display the Dataview table as cards
- `table-wide` makes the table wider than the note
- the query 
	- searches for all notes that have the `out/newsletter` tag
	- excludes notes that are in the "bins/templates" folder
	- sorts by note creation time, most recent first
	- `file.link as Newsletter` links newsletter note in the card
	- `file.outlinks as Links` links to outgoing links from the note in the card; keeps track of what is already written / shared
