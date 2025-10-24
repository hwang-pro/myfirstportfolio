---
title: "🚀 개인 프로젝트"
subtitle: "제가 직접 개발하고 공부한 프로젝트들을 소개합니다"
type: widget_page
summary: "개인적으로 진행한 다양한 프로젝트와 학습 기록을 확인해보세요"

# Optional banner image
image:
  filename: ""
  focal_point: "Center"
  preview_only: false

# Optional header image
header:
  image: ""
  caption: ""
---

## 🎯 프로젝트 개요

안녕하세요! 저는 다양한 분야의 프로젝트를 통해 지속적으로 성장하고 있습니다. 

### 📚 주요 학습 영역
- **CTF/WARGAME**: 드림핵을 통한 보안 문제 해결
- **웹 개발**: 프론트엔드와 백엔드 기술 습득
- **웹 보안**: 웹 해킹 기법과 방어 방법 연구

각 프로젝트는 제가 배운 내용을 실제로 적용하고 실험해본 결과물들입니다. 아래 카드들을 클릭하여 자세한 내용을 확인해보세요!

---

# Portfolio Section
widget: portfolio
headless: true
weight: 10

title: '프로젝트 목록'
subtitle: ''

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
    - name: All
      tag: '*'
    - name: CTF/WARGAME
      tag: dreamhack
    - name: 웹 개발
      tag: web
    - name: 웹 보안
      tag: webhack

design:
  view: card
  columns: "2"
  image:
    fit: cover     
    width: 100%     
