<!-- ---
title: Teaching
summary: My courses
type: landing

cascade:
  - _target:
      kind: page
    params:
      show_breadcrumb: true

sections:
  - block: collection
    id: teaching
    content:
      title: Teaching
      filters:
        folders:
          - teaching
    design:
      view: article-grid
      columns: 2
--- -->
---
title: Research
summary: My research projects and publications
type: landing  # 这个字段保持不变，确保使用正确的布局
cascade:
  - _target:
      kind: page
    params:
      show_breadcrumb: true

sections:
  - block: collection
    id: research
    content:
      title: Research Projects
      filters:
        folders:
          - research  # 确保文件夹路径正确
    design:
      view: article-grid
      columns: 2
---
