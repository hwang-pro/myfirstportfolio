---
title: 홈
type: landing
sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      username: admin
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      count: 5
      filters:
        folders:
          - project
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      offset: 0
      order: desc
    design:
      view: card
      columns: '2'
---