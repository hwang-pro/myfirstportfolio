---
# An instance of the About widget.
# Documentation: https://docs.hugoblox.com/page-builder/
widget: about

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 10

title: 👋 Hello!

# Choose the user profile to display
# This should be the username (folder name) of a profile in your `content/authors/` folder.
# See https://docs.hugoblox.com/get-started/#introduce-yourself
author: admin
---

<!-- SEO Meta Tags -->
<meta name="description" content="Introduction of Hwang Kyung-jae, a student at Jeonbuk National University's Department of Industrial Information Systems Engineering. A student growing as an information security and web hacking expert.">
<meta name="keywords" content="Hwang Kyung-jae, JBNU, introduction, information security, web hacking, student, portfolio">

<style>
.wg-about .portrait-title h2,
.wg-about .portrait-title h3 {
  text-align: center !important;
}

.wg-about .portrait-title h2 {
  font-size: 1.4rem !important;
  color: #2c3e50 !important;
  margin-bottom: 0.5rem !important;
  font-weight: 600 !important;
}

.wg-about .portrait-title h3 {
  font-size: 1.1rem !important;
  color: #7f8c8d !important;
  font-weight: 400 !important;
  margin-bottom: 1rem !important;
}

.wg-about .network-icon {
  text-align: center !important;
  margin-top: 1rem !important;
}

.wg-about .network-icon .big-icon {
  margin: 0.4rem !important;
  transition: transform 0.3s ease !important;
}

.wg-about .network-icon .big-icon:hover {
  transform: scale(1.1) !important;
}

/* Profile card styling */
.wg-about {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%) !important;
  border-radius: 20px !important;
  padding: 2rem !important;
  margin-bottom: 2rem !important;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1) !important;
}

.wg-about .portrait-title h2 {
  color: white !important;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3) !important;
}

.wg-about .portrait-title h3 {
  color: rgba(255, 255, 255, 0.9) !important;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3) !important;
}

/* Dark mode styles */
.dark .wg-about {
  background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%) !important;
}

.dark .wg-about .portrait-title h2 {
  color: #ecf0f1 !important;
}

.dark .wg-about .portrait-title h3 {
  color: rgba(236, 240, 241, 0.8) !important;
}
</style>

<div style="text-align: center; margin-top: 2rem; padding: 1.5rem; background: rgba(255, 255, 255, 0.1); border-radius: 15px; backdrop-filter: blur(10px);">
  <h4 style="color: white; margin-bottom: 1rem; font-size: 1.2rem;">🚀 Current Activities</h4>
  <div style="display: flex; justify-content: center; flex-wrap: wrap; gap: 1rem;">
    <span style="background: rgba(255, 255, 255, 0.2); padding: 0.5rem 1rem; border-radius: 20px; color: white; font-size: 0.9rem;">🎓 Studying at JBNU</span>
    <span style="background: rgba(255, 255, 255, 0.2); padding: 0.5rem 1rem; border-radius: 20px; color: white; font-size: 0.9rem;">🛡️ Learning Information Security</span>
    <span style="background: rgba(255, 255, 255, 0.2); padding: 0.5rem 1rem; border-radius: 20px; color: white; font-size: 0.9rem;">💻 Researching Web Hacking</span>
    <span style="background: rgba(255, 255, 255, 0.2); padding: 0.5rem 1rem; border-radius: 20px; color: white; font-size: 0.9rem;">👥 Student Council Activities</span>
  </div>
</div>