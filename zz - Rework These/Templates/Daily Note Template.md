---
Title: <% tp.file.title %>
Aliases:
Created: <% tp.date.now("YYYY-MM-DD hh:mm a") %>
Last-Modified :  
Type: Capture
MOC: [[Daily Logs]]
Status: [[Unprocessed]]
Tags: 
Links: 
---

# <% tp.file.title %>

# Notes
- <% tp.file.cursor() %>

---
### Notes created today

```dataview
List
FROM "" 
WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") 
SORT file.ctime asc 
```

### Notes last touched today

```dataview
List 
FROM "" 
WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") 
SORT file.mtime asc
```

