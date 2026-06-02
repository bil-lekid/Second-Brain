---
tags:
  - MOC
  - TagIndex
---
## Tag: Blog

```dataview
LIST FROM #Blog
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

