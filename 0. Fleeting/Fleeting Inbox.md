---
tags:
  - Fleeting
  - MOC
---

[[SOP - Fleeting to PARA (Distill, Express, Publish)|SOP: Fleeting -> PARA]]

## What To Process Next (0. Fleeting)

```dataview
TABLE file.folder as Folder, file.mtime as Updated, tags
FROM "0. Fleeting"
WHERE file.name != "0. Fleeting" AND file.name != "Fleeting Inbox"
SORT file.mtime desc
```

## Only Fleeting Tag (Needs Categorizing)

```dataview
LIST FROM "0. Fleeting"
WHERE file.name != "0. Fleeting" AND file.name != "Fleeting Inbox"
AND contains(tags, "Fleeting")
AND length(tags) = 1
SORT file.mtime desc
```

## Fleeting Tag Outside 0. Fleeting (Potentially Processed)

```dataview
TABLE file.folder as Folder, file.mtime as Updated, tags
FROM #Fleeting
WHERE file.name != "0. Fleeting" AND file.name != "Fleeting Inbox"
AND !contains(file.path, "0. Fleeting/")
SORT file.mtime desc
```
