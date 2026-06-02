---
tags:
  - MOC
  - TagIndex
---
## Tag: Job

```dataview
LIST FROM #Job
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

