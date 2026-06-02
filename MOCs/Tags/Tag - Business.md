---
tags:
  - MOC
  - TagIndex
---
## Tag: Business

```dataview
LIST FROM #Business
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

