<%*
let NoteTitle = await tp.system.prompt("Note Title")
titleName = tp.date.now("YYYY-MM-DD") + " " + "-" + " " + NoteTitle 
await tp.file.rename(titleName)
await tp.file.move("/Daily Notes/Daily Bible Reading/" + titleName);
-%>
---
Title: <% NoteTitle %>
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Bible Reading
Tags:  Bible-Reading/Passage
---

**NOTE - SET YOUR TAGS!!!**


# <% NoteTitle %>
Created:: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified:: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>

author:: 
historical-era:: 
key-verse:: 
theme:: 

---

## Chapter
Parallel-Passages:: [[ ]]

### Heading



### Footnotes


---

