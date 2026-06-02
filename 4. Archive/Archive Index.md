---
tags:
  - Archive
  - MOC
---

# 📦 Archive Index

Tempat penyimpanan project, task, dan notes yang sudah selesai atau tidak lagi diperlukan.

## 📂 Struktur Archive

### Deprecated Projects
Project yang sudah selesai, tidak diperlukan, atau tidak berlanjut.

```dataview
LIST
FROM "4. Archive/Deprecated Projects"
SORT file.mtime desc
```

### Inactive Projects
Project yang masih dalam status inbox atau belum dikembangkan.

```dataview
LIST
FROM "4. Archive"
WHERE file.name != "Archive Index" 
AND !contains(file.path, "Deprecated Projects/")
SORT file.mtime desc
```

---

## 📊 Statistik
- Total file di Archive: `=this.file.folder.length`
- Last updated: `=date(now).format("YYYY-MM-DD HH:mm")`

## 🔗 Quick Links
- [[0. Fleeting|← Kembali ke Fleeting]]
- [[1. Projects|← Ke Projects]]
