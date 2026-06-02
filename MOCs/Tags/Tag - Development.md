---
tags:
  - MOC
  - TagIndex
---
## Tag: Development

```dataview
LIST FROM #Development
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

