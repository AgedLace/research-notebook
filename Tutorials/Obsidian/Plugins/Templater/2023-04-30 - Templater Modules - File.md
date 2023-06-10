---
title: Templater Modules - File
created: Sunday, April 30, 2023 18:17 pm
last-modified: Sunday, April 30, 2023 06:17 pm
source: 
status: Processed
type: Tutorial
tags: Tutorials/Obsidian/Plugins/Templater/Internal-Functions/Modules/File
---

# Templater Modules - File
Created: Sunday, April 30, 2023 18:17 pm
Last-modified: Sunday, April 30, 2023 06:17 pm
Source: [tp.file - Templater](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html)
---

## Documentation


* `tp.file.content`
	* Retrieves file's content
	
* `tp.file.create_new(template: TFile | string, filename?: string, open_new: boolean = false, folder?: TFolder)`
	* Creates new file using specified template / content
	* Arguments
		* `filename` of new file
		* `folder` to put new file into
		* `open_new` whether to open the new file or not
		* `template` to be used

* `tp.file.creation_date(format: string = "YYYY-MM-DD HH:mm")`
	* Retrieves file's creation date
	* Arguments
		* `format` of date

* `tp.file.cursor(order?: number)`
	* Sets the cursor to the location after template has been inserted
	* Arguments
		* `order` of different cursors jump

* `tp.file.cursor_append(content: string)`
	* Appends content after active cursor in file
	* Arguments
		* `content` to be appended

* `tp.file.exists(filename: string)`
	* Name of file we want to check existence of
	* Arguments
		* `filename` of file to be checked

* `tp.file.find_tfile(filename: string)`
	* Search for file and return its `TFile` instance
	* Arguments
		* `filename` to search and resolve as a `TFile`

* `tp.file.folder(relative: boolean = false)`
	* Retrieves file's folder name
	* Argument
		* `relative` set to true, appends vault relative path to folder name

* `tp.rile.include(include_link: string | TFile)`
	* Search for file and returns its `TFile` instance
	* Arguments
		* `filename` we want to search and resolve

* `tp.file.folder(relative: boolean = false)`
	* Retrieves file's folder name
	* Arguments
		* `relative` set to true, appends vault relative path to folder name

* `tp.file.include(include_link: string | TFile)`
	* Includes file's link content; templates in the included content will be resolved
	* Arguments
		* `include_link` to the file to include

* `tp.file.last_modified_date(Format: string = "YYYY-MM-DED HH:mm")`
	* Retrieves file's last modification date
	* Arguments
		* `format`

* `tp.file.move(new_path: string, file_to_move?: TFile)`
	* Moves file to desired vault location
	* Arguments
		* `new_path` relative to file w/o file extension; needs to include folder and file name, *i.e.* /Notes/MyNote

* `tp.file.path(relative: boolean = false)`
	* Retrieves file's absolute path on the system
	* Arguments
		* `relative` set to true; only retrieves vault's relative path

* `tp.file.rename(new_title: string)`
	* Renames the file
	* Arguments
		* `new_title`

* `tp.file.selection()`
	* Retrieves the active file's text selection

* `tp.file.tags`
	* Retrieves file's tags (array of string)

* `tp.file.title`
	* Retrieves file's title.

![[2023-04-29 - Templater Examples#Templater Modules File Examples]]
