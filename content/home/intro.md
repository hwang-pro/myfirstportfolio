--
# Use the Intro widget of the Blog template
widget: about.avatar

# This file represents a page section.
headless: true

# Order that this section will appear in.
weight: 10
design:
    show_social: true

author: admin
#design:
#  background:
#    color: '#090a0b'
#    text_color_light: true
#    video:
#      path:  # enter filename of a video in /assets/media
#  css_class: fullscreen
---

👋 안녕하세요, 저는 전북대에 재학중인 정보보안에 관심이 있는 학생 황경재입니다!
<!-- 🗺️ 학과명 옆 지도 아이콘 + 토글 지도 -->
<div style="text-align:center; margin-top:10px;">
  <strong>전북대 산업정보시스템공학과 · 컴퓨터인공지능학부</strong>
  <button id="jbnu-map-toggle"
          title="전북대학교 지도 보기"
          style="border:none; background:none; cursor:pointer; font-size:1.3rem; margin-left:8px;">
    🗺️
  </button>
</div>

<div id="jbnu-map-wrap" style="display:none; margin-top:16px;">
  <input id="map-search" type="text" placeholder="장소 또는 주소 검색..."
         style="width:80%; max-width:500px; padding:8px 12px; margin-bottom:12px; border-radius:8px; border:1px solid #555; background-color:#111; color:#eee; outline:none;">
  <div id="jbnu-map"
       style="height:400px; width:90%; max-width:900px; margin:0 auto; border-radius:12px; overflow:hidden; box-shadow:0 8px 25px rgba(0,0,0,0.35);">
  </div>
</div>

<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
  (function() {
    const btn   = document.getElementById("jbnu-map-toggle");
    const wrap  = document.getElementById("jbnu-map-wrap");
    const input = document.getElementById("map-search");
    let map, marker, mapInited = false;

    function initMap() {
      const jbnu = [35.8467, 127.1257];
      map = L.map("jbnu-map").setView(jbnu, 15);
      L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
        maxZoom: 19,
        attribution: '&copy; OpenStreetMap contributors'
      }).addTo(map);
      marker = L.marker(jbnu).addTo(map)
        .bindPopup("<b>전북대학교</b><br>공대 7호관 근처").openPopup();
    }

    btn.addEventListener("click", () => {
      const hidden = wrap.style.display === "none";
      wrap.style.display = hidden ? "block" : "none";
      if (hidden && !mapInited) {
        setTimeout(initMap, 0);
        mapInited = true;
      }
      if (hidden) wrap.scrollIntoView({ behavior: "smooth", block: "center" });
    });

    input.addEventListener("keypress", async (e) => {
      if (e.key === "Enter") {
        e.preventDefault();
        const query = input.value.trim();
        if (!query) return;
        const res = await fetch(`https://nominatim.openstreetmap.org/search?format=json&q=${encodeURIComponent(query)}`);
        const data = await res.json();
        if (data.length > 0) {
          const { lat, lon, display_name } = data[0];
          map.setView([lat, lon], 15);
          marker.setLatLng([lat, lon])
            .bindPopup(`<b>${display_name}</b>`)
            .openPopup();
        } else {
          alert("검색 결과를 찾을 수 없습니다 😢");
        }
      }
    });
  })();
</script>

{style="font-size: 1.2rem; background: #FFB76B; background: linear-gradient(to right, #FFB76B 0%, #FFA73D 30%, #FF7C00 60%, #FF7F04 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent;"}

아직은 부족한 포토폴리오이지만,열심히 채워 나가겠습니다😍
