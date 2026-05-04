```
filters:
  or:
    - file.name.contains(this.file.name.slice(4))
    - file.ctime.toString().contains(this.file.name.slice(4))
formulas:
  # 将创建时间格式化为 YYYY-MM-DD 以便在表格中整齐展示
  created_date: file.ctime.toString().slice(0, 10)
properties:
  file.name:
    displayName: Entry
  note.categories:
    displayName: Categories
  file.ctime:
    displayName: Created
  note.tags:
    displayName: Tags
views:
  - type: table
    name: On This Day
    filters:
      and:
        - file.name != this.file.name
    order:
      - formula.created_date
      - file.name
    sort:
      # 改为按格式化后的创建时间降序排列
      - property: formula.created_date
        direction: DESC
    columnSize:
      formula.created_date: 153
      file.name: 558
```