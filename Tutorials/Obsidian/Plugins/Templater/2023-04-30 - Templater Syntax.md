---
title: Templater Syntax
created: Sunday, April 30, 2023 09:10 am
last-modified: Sunday, April 30, 2023 09:09 am
source: 
status: Processed
type: Tutorial
tags: Tutorials/Obsidian/Plugins/Templater/Syntax
---

# Templater Syntax
Created: Sunday, April 30, 2023 09:10 am
Last-modified: Sunday, April 30, 2023 09:09 am
Source: [Syntax - Templater](https://silentvoid13.github.io/Templater/syntax.html)
---

## Function Invocation

To invoke the Function ...

	`tp.date.now()`

To invoke the Function with arguments ...

	`tp.date.now(arg1_value, arg2_value, arg3_val, ...)`

* Arguments must be passed in the correct order

*Function Arguments*

* can have different *types*
	* `string` values must be in quotes -> "value" or 'value'
	* `number` values must be integers -> 15, -5, ...
	* `boolean` values must be either `true` or `false`

* Function documentation syntax
	* `tp.<my_function>(arg1_name: type, arg2_name?: type, arg3_name: type = <default_value>, arg4_name: type1|type2, ...)`
	* Where ...
		* `arg_name` represents a *symbolic* name for the argument
		* `type` represents the expected type for the argument
	* Arguments appended with a `?` are optional
	* Default values are specified using an equal sign (=)
	* Arguments that can have different types will be specified using a pile `|`
	
	* NOTE - DON'T specify `name` or `type` or `default value` when calling a function.  *Only the value of the arguments are required.*

	* Example ...
		* `tp.date.now(format: string = "YYYY-MM-DD", offset?: number|string, reference?: string, reference_format?: string)`

	* The *valid* invocations are ...
		* 2023-05-08
		* 2023-05-15
		* 2021-04-16
			* Assuming the file name is of the format `"YYYY-MM-DD"`






