---
cssclasses:
  - daily
  - friday
---

# 👋 你好，小鹿

> [!quote] 每一天都是新的开始

---

## 🗂️ 快速导航

<div class="nav-grid">

[[Habits Tracker|📊 习惯追踪]]
[[Calendar/Journal/Daily/2026-04-03-00|📅 今日日记]]
[[calculus/maps test|🗺️ 知识地图]]
[[Bases/Calendar.base|🗓️ 日历]]

</div>

---

## 📝 最近笔记

```dataview
TABLE file.mtime AS "修改时间"
FROM ""
WHERE file.name != "Home"
SORT file.mtime DESC
LIMIT 8
```

---

## 📅 本周日记

```dataview
LIST
FROM "Calendar/Journal/Daily"
SORT file.name DESC
LIMIT 7
```

---

## 🔥 习惯热力

![[Habits Tracker]]
