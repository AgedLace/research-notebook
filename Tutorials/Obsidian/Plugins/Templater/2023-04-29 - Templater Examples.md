---
title: Templater Examples
source: [[https://www.thoughtasylum.com/2021/07/24/the-basics-of-templater-for-obsidian/]]
created: Saturday, April 29, 2023 21:20 pm
last-modified: Saturday, April 29, 2023 09:20 pm
status: Processed
type: Tutorial
tags: Tutorials/Obsidian/Plugins/Templater/Examples
---

# Templater Examples
created: Saturday, April 29, 2023 21:20 pm
last-modified: Saturday, April 29, 2023 09:20 pm
source: [The Basics of Templater for Obisidian | ThoughtAsylum](https://www.thoughtasylum.com/2021/07/24/the-basics-of-templater-for-obsidian/)

---

## Example Templates

### Daily Quote

`<% tp.web.daily_quote() %>`

### Tomorrow Link

`[[<% tp.date.now("YYYY-MM-DD", 1) %>]]`

### Moment.js Examples

* `Date` now -> 
	* <% tp.date.now() %>
* `Date` now with format -> 
	* `<% tp.date.now.("Do MMMM YYYY") %>

* `Last Week` ->
	* <% tp.date.now("dddd Do MMMM YYYY", -7) %>
* `Today` ->
	* <% tp.date.now("dddd Do MMMM YYYY, ddd") %>
* `Next Week` ->
	* <% tp.date.now("dddd Do MMMM YYYY", 7) %>

* `Last Month` ->
	* <% tp.date.now("YYYY-MM-DD", "P-1M") %>
* `Next Year` ->
	* <% tp.date.now("YYYY-MM-DD", "P1Y") %>

* `File's title date + 1 day` - tomorrow ->
	* <% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>
* `File's title date -1` - yesterday ->
	* <% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>

* `Date` tomorrow with format ->
	* <% tp.date.tomorrow("Do MMMM YYYY") %>

`This week's monday` ->
	<% tp.date.weekday("YYYY-MM-DD", 0) %>
`Next monday` ->
	<% tp.date.weekday("YYYY-MM-DD", 7) %>
`File's title monday` -> 
	<% tp.date.weekday("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
`File's title next monday` -> 
	<% tp.date.weekday("YYYY-MM-DD", 7, tp.file.title, "YYYY-MM-DD") %>

`Date yesterday with format` -> 
	<% tp.date.yesterday("Do MMMM YYYY") %>

### Templater Modules File Examples

`File Content` ->
	`<% tp.file.content %>` ->

`File creation date` -> 
	<% tp.file.creation_date() %>
`File creation date with format` ->
	<% tp.file.creation_date("dddd Do MMMM YYYY HH:mm") %>

`File creation` -> 
`	[[<% (await tp.file.create_new("MyFileContent", "MyFilename")).basename %>]]`

`File cursor` -> 
	<% tp.file.cursor(1) %>

`File cursor append` -> 
	<% tp.file.cursor_append("Some text") %>
    
`File existence` -> 
	<% await tp.file.exists("MyFolder/MyFile.md") %>
`File existence of current file` -> 
	<% await tp.file.exists(tp.file.folder(true)+"/"+tp.file.title+".md") %>

`File find TFile` -> 
	`<% tp.file.find_tfile("MyFile").basename %>`
    
`File Folder` -> 
	<% tp.file.folder() %>
`File Folder with relative path` -> 
	<% tp.file.folder(true) %>

`File Include` -> 
	<% tp.file.include("[[Template1]]") %>

`File Last Modif Date` -> 
	<% tp.file.last_modified_date() %>
`File Last Modif Date with format` -> 
	<% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm") %>

`File Move` -> 
	<% await tp.file.move("/A/B/" + tp.file.title) %>
`File Move + Rename` -> 
	<% await tp.file.move("/A/B/NewTitle") %>

`File Path` -> 
	<% tp.file.path() %>
`File Path with relative path` -> 
	<% tp.file.path(true) %>

`File Rename` -> 
	<% await tp.file.rename("MyNewName") %>
`Append a "2"` -> 
	<% await tp.file.rename(tp.file.title + "2") %>

`File Selection` -> 
	<% tp.file.selection() %>

`File tags` -> 
	<% tp.file.tags %>

`File title` -> 
	<% tp.file.title %>
`Strip the Zettelkasten ID of title (if space separated)` -> 
	<% tp.file.title.split(" ")[1] %>
