## School MOC

---

### TODOs

- [ ] Create a Dataview Query to Show All Schools
- [ ] Create a Dataview Query to Show All Classes Per School
- [ ] Create a Dataview Query to Track Status of All Assignments Per Class
- [ ] Create a Dataview Query to Track Reading Notes or other Resources

Sample Dataview Query #Dataview-Query/Literature-Notes 

```
```dataview
LIST
FROM "History of Rome"
WHERE !contains(file.name, "Lecture")
```


Sample School MOC Template #Dataview-Query/Templates/MOC

```
Year: [[School MOC]]
Course: [[]]
Date: {{date}}
Lecture {{title}}

## Main Points
- 

## Related Books
- 

## Things to Memorize
- 

## Assignments
-

```

Sample Course Template #Dataview-Query/Templates/School/Course

```
# History of Rome MOC

## Themes

```dataview
LIST
FROM "History of Rome"
WHERE !contains(file.name, "Lecture")
```
```
```

Sample Lecture / Lesson Template #Dataview-Query/Templates/School/Course/Lesson

```
## Lecture Notes

```dataview
LIST
FROM "History of Rome"
WHERE contains(file.name, "Lecture")
```

When you write lecture / lesson notes, include the word "Lecture" or "Lesson" in the title.
