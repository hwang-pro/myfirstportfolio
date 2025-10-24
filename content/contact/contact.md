---
# An instance of the Contact widget.
# Documentation: https://docs.hugoblox.com/getting-started/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

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
  
  # Business hours
  appointment_url: ""
  
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
    - icon: university
      icon_pack: fas
      link: "https://ise.jbnu.ac.kr/ise/index.do"
      label: "전북대 정보시스템공학과"
    - icon: robot
      icon_pack: fas
      link: "https://csai.jbnu.ac.kr/csai/index.do"
      label: "전북대 컴퓨터인공지능학부"
    - icon: blog
      icon_pack: fas
      link: "https://blog.naver.com/curry2478"
      label: "네이버 블로그"

design:
  columns: '2'
  background:
    gradient_start: "#667eea"
    gradient_end: "#764ba2"
    gradient_direction: "135deg"
    text_color_light: true
  spacing:
    padding: ["20px", "0", "20px", "0"]
---
<div style="border-radius:16px; overflow:hidden; margin-top: 20px; position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3234.079611835235!2d127.13184297699142!3d35.8470513725341!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x35702330fa358b0f%3A0x27af04f87d1e88f2!2z7KCE67aB64yA7ZWZ6rWQIOqzteqzvOuMgO2VmTbtmLjqtIA!5e0!3m2!1sko!2skr!4v1760879158980!5m2!1sko!2skr"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>
</div>