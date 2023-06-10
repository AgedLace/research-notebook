<%*
let NoteTitle = await tp.system.prompt("Note Title")
titleName = tp.date.now("YYYY-MM-DD") + " " + "-" + " " + NoteTitle 
await tp.file.rename(titleName)
await tp.file.move("/Input Notes/" + titleName);
-%>
---
Title: <% NoteTitle %>
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Brain Dump
Tags:  Brain-Dump/Date
---

**NOTE - SET YOUR TAGS!!!**


# <% NoteTitle %>
Created:: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified:: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>

---

### What's On My Mind?



### What Do I Need To Do?



### What Problems Do I Have?



### What People Do I Need To Focus On?



### What Work Do I Need To Do?



### What Hobbies or Other Activities Do I Want To Address?



### What Do I Want In My Future?

### What's On My Bucket List?



---

### Separate items into ...

	* Actionable
	* Non-Actionable

