---
# An instance of the Contact widget.
# Documentation: https://docs.hugoblox.com/getting-started/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: "💬 Let's Connect"
subtitle: "새로운 기회와 협업을 기다리고 있습니다 ✨"

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
    gradient_start: "#4facfe"
    gradient_end: "#00f2fe"
    gradient_direction: "135deg"
    text_color_light: true
    image: ""
    image_darken: 0.3
    image_size: "cover"
    image_position: "center"
    image_parallax: false
  spacing:
    padding: ["40px", "0", "40px", "0"]
  card:
    background_color: "rgba(255, 255, 255, 0.1)"
    border_radius: "20px"
    border: "1px solid rgba(255, 255, 255, 0.2)"
    box_shadow: "0 8px 32px rgba(0, 0, 0, 0.1)"
---

<div style="margin-top: 30px; text-align: center;">
  <h3 style="color: white; margin-bottom: 20px; font-size: 1.5rem; font-weight: 600;">📍 전북대학교 위치</h3>
  <div style="border-radius: 20px; overflow: hidden; margin: 0 auto; max-width: 800px; position: relative; padding-bottom: 56.25%; height: 0; box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);">
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3234.079611835235!2d127.13184297699142!3d35.8470513725341!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x35702330fa358b0f%3A0x27af04f87d1e88f2!2z7KCE67aB64yA7ZWZ6rWQIOqzteqzvOuMgO2VmTbtmLjqtIA!5e0!3m2!1sko!2skr!4v1760879158980!5m2!1sko!2skr"
      style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade">
    </iframe>
  </div>
</div>