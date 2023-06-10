---
Title: {{DATE}} {{NAME}}
Alias: 
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
Last-Modified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 
Status: Unprocessed
Type: {{FIELD:<Type of File>}}
Tags: {{FIELD:<Tags>}}
---

# {{DATE}} {{NAME}}
Created: <% tp.date.now("dddd, MMMM DD, YYYY HH:mm a") %>
LastMmodified: <% tp.file.last_modified_date("dddd, MMMM DD, YYYY hh:mm a") %>
Source: 

---

<% tp.file.cursor() %>