<%*
let NoteTitle = await tp.system.prompt("Note Title")
titleName = tp.date.now("YYYY-MM-DD") + " " + "-" + " " + NoteTitle 
await tp.file.rename(titleName)
await tp.file.move("/" + titleName);
-%>
---
Title: <% NoteTitle %>
Alias: 
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Note
Tags: Test
---

**NOTE - SET YOUR TAGS**


# <% NoteTitle %>
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
LastMmodified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 

---

<% tp.file.cursor() %>