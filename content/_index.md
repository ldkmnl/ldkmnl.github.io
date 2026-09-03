---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-09-01
type: landing

sections:
  - block: collection
    id: works
    content:
      title: '近期工作'
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 10
      # Filter on criteria
      filters:
        folders:
          - works
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: list
      # Reduce spacing
      spacing:
        padding: [40px, 0, 0, 0]

  - block: collection
    id: 3dprint #导航栏url跳转标签
    content:
      title: '增材制造'
      text: ''
      filters:
        folders:
          - 3dprint
        exclude_featured: false
    design:
      view: card

  - block: collection
    id: photos #导航栏url跳转标签
    content:
      title: '摄影作品'
      text: ''
      filters:
        folders:
          - photos
        exclude_featured: false
    design:
      view: card
---
