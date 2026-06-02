---
tags:
  - Journal
  - MOC
---

# 📔 Daily Journal

Personal reflection, gratitude, lessons, and life events. This is a space for **processing emotions** and **recording moments**, not for actionable tasks (those go in [[0. Fleeting|Fleeting Notes]]).

## Quick Links
- [[SOP - Daily Journal Practice|How to journal effectively]]
- [[2026/May|Current month]] 
- [[2026|This year]]

## Archive by Year
```dataview
LIST
FROM "_daily_journal"
WHERE file.name != "_daily_journal"
SORT file.name desc
```

## Recent Entries
```dataview
LIST
FROM "_daily_journal/2026"
SORT file.name desc
LIMIT 10
```

---

## 🎯 Guidelines

### What Goes Here
✅ Personal reflections and feelings
✅ Lessons learned from the day
✅ Gratitude and wins (big or small)
✅ Events and moments worth remembering
✅ Mood tracking and mental health notes

### What Does NOT Go Here
❌ Task lists (→ [[0. Fleeting|Fleeting Notes]])
❌ Project updates (→ [[1. Projects|Projects]])
❌ Actionable ideas (→ [[0. Fleeting|Fleeting Notes]])
❌ Quick captures (→ [[0. Fleeting|Fleeting Notes]])

---

## 📊 Journal Statistics
- Total entries: `=length(search("tag:DailyEntry"))`
- This year: `=length(search("tag:DailyEntry AND path(_daily_journal/2026)"))`
- Current streak: `=dateformat(now(), "days") - dateformat(max(search("tag:DailyEntry").file.mtime), "days")` days

---

## 🔗 Related
- [[0. Fleeting]] — For capturing and processing
- [[3. Resources]] — For storing extracted wisdom
- [[START HERE]] — Main vault entrance
