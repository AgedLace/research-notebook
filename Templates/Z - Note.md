<%*
let Title = await tp.system.prompt("Note Title")
await tp.file.title
await tp.file.move("/Z - Permanent Notes/" + Title);
-%>
---
Title: <% Title %>
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Z- Note
Tags:  Z-Note/Note-Name
---

**NOTE - SET YOUR TAGS!!!**


# <% Title %>
Created:: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified:: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>

---

