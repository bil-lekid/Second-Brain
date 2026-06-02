---
tags:
  - MOC
  - TagIndex
---
## Tag: Sales

```dataview
LIST FROM #Sales
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

