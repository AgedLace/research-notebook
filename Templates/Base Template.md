---
Title: {{NAME}}
Alias: 
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: Note
Tags: {{VALUE:<tags>}}
---

# {{NAME}}
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
LastMmodified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 

---

<% tp.file.cursor() %>