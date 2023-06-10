---
Source: (https://www.thoughtasylum.com/2021/07/24/the-basics-of-templater-for-obsidian/)
Status: Processed
Type: Tutorial
Tags:
  - Obsidian/Plugins/Templater/Examples
---

## Example Templates

---

### **Daily Quote**

```
<% tp.web.daily_quote() %>
```

### **Tomorrow Link**

```
[[<% tp.date.now("YYYY-MM-DD", 1) %>]]
```

---

[[Use QuickAdd to Automate Templates]]
