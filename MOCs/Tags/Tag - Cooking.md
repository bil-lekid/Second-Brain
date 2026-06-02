---
tags:
  - MOC
  - TagIndex
---
## Tag: Cooking

```dataview
LIST FROM #Cooking
WHERE !contains(file.path, "MOCs/Tags") AND !contains(file.path, "_codex_backups") AND !contains(file.path, "_imports")
SORT file.mtime desc
```

