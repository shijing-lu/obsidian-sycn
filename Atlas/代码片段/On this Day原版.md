```
filters:
  or:
    - file.name.contains(this.file.name.slice(4))
    - date.toString().contains(this.file.name.slice(4))
formulas:
  date: date.toString().slice(0, 10)
properties:
  file.name:
    displayName: Entry
  note.categories:
    displayName: Categories
  note.created:
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
      - file.basename
      - file.name
      - formula.date
    sort:
      - property: file.basename
        direction: DESC
    columnSize:
      formula.date: 153
      file.name: 558

```
