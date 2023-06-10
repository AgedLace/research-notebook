---
Status: Unprocessed
Type: Z-Note
Tags: 
  - Obsidian/Plugins/QuickAdd
  - Obsidian/Templates/Automation
  - Obsidian/Templater/Examples
---

## Use QuickAdd to Automate Templates

Source:: [Creating a tempalter for a new note - Help - Obsidian Forum](https://forum.obsidian.md/t/creating-a-tempalter-for-a-new-note/61104)

---

Use QuickAdd to automate templates?

- Create the template file
- Use special syntax for filename prompt
	- {{VALUE:Filename}} 
- Other frontmatter prompts

```
---
someField: {{VALUE:What is somefield?}}
anotherField: {{VALUE: Another field?}}
---
```

## Example Templater General Note
#Obsidian/Plugins/Templater/Examples/General-Note

```
---
created: "<% tp.file.creation_date("YYYY-MM-DD") %>"
year: <% tp.file.creation_date("YYYY") %>
topic: <% tp.file.cursor(1) %>
tags:
  - 
aliases: []
---
<%*
//If File is untitled prompt the User to set a Title (Source: https://github.com/SilentVoid13/Templater/discussions/259)
let title = tp.file.title
if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title") ?? "Untitled";
    await tp.file.rename(`${title}`);
} %>
Last Modified: `=dateformat(this.file.mtime, "DDDD, HH:mm")`

# <% tp.file.title %> 

<% tp.file.cursor(2) %>
```

