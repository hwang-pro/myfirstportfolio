---
widget: slider
weight: 1
active: true

design:
  # 슬라이드 높이 (px)
  slide_height: '400px'
  is_fullscreen: false
  # 자동 전환 (밀리초)
  loop: true
  interval: 3000

content:
  slides:
    - title: 정보보안 학습
      content: 체계적인 정보보안 지식 습득
      align: center
      background:
        image:
          filename: slides/slide1.jpg
          filters:
            brightness: 0.7
        position: center
        color: '#666'
    
    - title: 웹 해킹 연구
      content: 다양한 웹 취약점 분석 및 연구
      align: center
      background:
        image:
          filename: slides/slide2.jpg
          filters:
            brightness: 0.7
        position: center
        color: '#666'
    
    - title: CTF/WARGAME
      content: 실전 문제 해결 능력 향상
      align: center
      background:
        image:
          filename: slides/slide3.jpg
          filters:
            brightness: 0.7
        position: center
        color: '#666'
---
