---
title: Templater Modules - Date
created: Sunday, April 30, 2023 14:38 pm
last-modified: Sunday, April 30, 2023 02:37 pm
source: 
status: Unprocessed
tags: Tutorials/Obsidian/Plugins/Templater/Internal-Functions/Modules/Date
---

# Templater Modules - Date
Created: Sunday, April 30, 2023 14:38 pm
Last-modified: Sunday, April 30, 2023 02:37 pm
Source: [tp.date - Templater](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/date-module.html)
---

## Documentation

* `tp.date.now(format: string = "YYYY-MM-DD", offset?: number⎮string, reference?: string, reference_format?: string)`
	* Retrieves date
	* Arguments
		* `format`
		* `offset` for the day (-7 for last week's date)
		* `reference` - date referential - *i.e.* set to the note's title
		* `reference_format` - date reference format

* `tp.date.tomorrow(format: string = "YYYY-MM-DD")`
	* Retrieves tomorrow's date
	* Arguments
		* `format`

* `tp.date.weekday(format: string = "YYYY-MM-DD", weekday: number, reference?: string, reference_format?: string)`
	* Arguments
		* `format`
		* `reference`
		* `reference_format`
		* `weekday`

* `tp.date.yesterday(format: string = "YYYY-MM-DD")`
	* Retrieves yesterday's date
	* Arguments
		* `format`

* `Moment.js`
	* access to the `moment` object,  with all it's functionalities
	* Source - [Moment.js | Docs](https://momentjs.com/docs/#/displaying/)

## Examples

![[2023-04-29 - Templater Examples#Moment.js Examples]]

