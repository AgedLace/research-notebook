---
Type: MOC
Parent: [[Home]]
Tags: MOC/Inbox
---

## 'LOST' Notes

```dataview
table WITHOUT ID file.name AS Title
from "Input Notes" and !outgoing([[]])
where file.folder != "Templates"
sort file.name asc
```

- Start organizing 'LOST' Notes; for example ...

	- ### People
	- ### Places
	- ### Concepts



NOTE - when you add a link anywhere else in this Note, it will disappear from the "LOST" Notes dataview listing.  It's no longer "LOST".

---

## Inbox Index

```dataview
table WITHOUT ID file.name AS "Title"
from "Input Notes"
sort file.name asc
```

