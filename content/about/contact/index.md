---
# An instance of the Contact widget.
# Documentation: https://docs.hugoblox.com/getting-started/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 50

title: "📞 연락처"
subtitle: "언제든지 연락주세요! 함께 소통하고 성장해요 🚀"

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Contact details
  email: "curry2478@naver.com"
  phone: "+82-10-3519-2478"
  address:
    street: "전북대학교"
    city: "전주시"
    region: "전라북도"
    country: "대한민국"
    country_code: "KR"
  
  
  # Contact form
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Social media links
  social:
    - icon: github
      icon_pack: fab
      link: "https://github.com/hwang-pro"
      label: "GitHub"
    - icon: instagram
      icon_pack: fab
      link: "https://www.instagram.com/hwangpercy/"
      label: "Instagram"
    - icon: envelope
      icon_pack: fas
      link: "mailto:curry2478@naver.com"
      label: "Email"

  # Map settings
  map:
    provider: "openstreetmap"
    latitude: 35.8242
    longitude: 127.1480
    zoom: 15
    marker:
      latitude: 35.8242
      longitude: 127.1480
      title: "전북대학교"
      description: "전주 최고의 대학"

design:
  columns: '2'
  background:
    color: "#f8f9fa"
    gradient_start: "#667eea"
    gradient_end: "#764ba2"
    gradient_direction: "135deg"
    image: ""
    image_darken: 0.5
    image_size: "cover"
    image_position: "center"
    image_parallax: false
    text_color_light: true
  spacing:
    padding: ["20px", "0", "20px", "0"]
---
