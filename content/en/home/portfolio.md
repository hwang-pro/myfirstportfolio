---
# A section created with the Portfolio widget.
widget: portfolio
headless: true
weight: 20
title: ''
subtitle: ''

content:
  # Page type to display
  page_type: project
  # Default filter index
  filter_default: 0
  # Filter toolbar
  filter_button:
    - name: All
      tag: '*'
    - name: Web Study
      tag: web
    - name: Web Hacking Study
      tag: webhack
    - name: CTF/WARGAME Writeups
      tag: dreamhack

design:
  view: masonry
  columns: "1"
  image:
    fit: cover
    width: 70%
---