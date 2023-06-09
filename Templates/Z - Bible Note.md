<%*
let Title = await tp.system.prompt("Note Title")
await tp.file.title
await tp.file.move("/Z - Permanent Notes/Bible Passages/" + Title);
-%>
---
Title: <% Title %>
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Z - Bible Passages
Tags:  Z-/Bible-Passages/Passage
---

**NOTE - SET YOUR TAGS!!!**


# <% Title %>
Created:: <% tp.date.now("dddd, MMMM DD, YYYY hh:mm a") %>
Last-Modified:: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>

---


### Footnotes



### Parallel Passages



### Word Studies



### Tags


