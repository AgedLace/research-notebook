<%*
let NoteTitle = await tp.system.prompt("Note Title")
titleName = tp.date.now("YYYY-MM-DD") + " " + "-" + " " + NoteTitle 
await tp.file.rename(titleName)
await tp.file.move("/Daily Notes/Daily Journal/" + titleName);
-%>
---
Title: <% NoteTitle %>
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Prayer Journal
Tags:  Prayer-Journal
---

**NOTE - SET YOUR TAGS!!!**


# <% NoteTitle %>

Created:: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified:: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>

---

## Bible Reading

> * Father God, "deal bountifully with Your servant, that I may live and keep Your Word. Open my eyes that I may see wondrous things from Your law."
	
## Passage


- **Gratitude Prayer**
	- 


- **Asking Prayer**
	- 


- **Psalm Prayer**
	- 


- **Notes**
	- 


