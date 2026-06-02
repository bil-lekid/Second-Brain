---
tags:
  - MOC
  - TagIndex
---
## Tag: Relationship

```dataview
LIST FROM #Relationship
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

