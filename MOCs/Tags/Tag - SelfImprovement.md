---
tags:
  - MOC
  - TagIndex
---
## Tag: SelfImprovement

```dataview
LIST FROM #SelfImprovement
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

