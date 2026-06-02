---
tags:
  - MOC
  - TagIndex
---
## Tag: Productivity

```dataview
LIST FROM #Productivity
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

