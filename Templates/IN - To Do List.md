---
Title: {{NAME}}
Alias:
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: To Do List
Tags: 
  - To-Do-List
  - {{VALUE:<Tags>}}
---

# {{NAME}}
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
Last-modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 

---

<% tp.file.cursor() %>