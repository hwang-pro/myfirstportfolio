---
# Display name
title: 황경재

# Is this the primary user of the site?
superuser: true

# Role/position
role: '전북대 산업정보시스템공학과, 컴퓨터인공지능학부'

# Status emoji
status:
  icon: ☕️

# Short bio
bio: 정보보안/웹해킹에 관심이 있습니다.

social:
  - icon: comments
    icon_pack: fas
    link: "/myfirstportfolio/kakao_profile.jpg"   
  - icon: github
    icon_pack: fab
    link: "https://github.com/hwang-pro/myfirstportfolio"
  - icon: instagram
    icon_pack: fab
    link: "https://www.instagram.com/hwangpercy/"
---

<!-- 🗺️ 학과명 옆 지도 아이콘 -->
<div style="text-align:center; margin-top:8px;">
  <strong>전북대 산업정보시스템공학과 · 컴퓨터인공지능학부</strong>
  <button id="jbnu-map-toggle"
          title="전북대학교 지도 보기"
          style="border:none; background:none; cursor:pointer; font-size:1.3rem; margin-left:8px;">
    🗺️
  </button>
</div>

<!-- 부드러운 토글 효과 -->
<style>
#jbnu-map-wrap { 
  transition: all 0.3s ease-in-out; 
  opacity: 0; 
  display: none; 
}
#jbnu-map-wrap.active { 
  display: block; 
  opacity: 1; 
}
#map-search {
  width: 75%; 
  max-width: 450px; 
  padding: 8px 12px; 
  margin-bottom: 12px; 
  border-radius: 8px; 
  border: 1px solid #555; 
  background-color: #111; 
  color: #eee; 
  outline: none;
}
#map-search-btn {
  padding: 8px 12px;
  border-radius: 8px;
  border: none;
  background-color: #ff8c00;
  color: white;
  font-weight: bold;
  cursor: pointer;
  transition: 0.2s ease;
}
#map-search-btn:hover {
  background-color: #ffb347;
}
</style>

<!-- 지도 영역 -->
<div id="jbnu-map-wrap" style="margin-top:18px;">
  <input id="map-search" type="text" placeholder="장소 또는 주소 검색..." />
  <button id="map-search-btn">🔍</button>
  <div id="jbnu-map"
       style="height:400px; width:90%; max-width:900px; margin:12px auto; border-radius:12px; overflow:hidden; box-shadow:0 8px 25px rgba(0,0,0,0.35);">
  </div>
</div>

<!-- Leaflet CSS & JS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
  (function() {
    const btn   = document.getElementById("jbnu-map-toggle");
    const wrap  = document.getElementById("jbnu-map-wrap");
    const input = document.getElementById("map-search");
    const searchBtn = document.getElementById("map-search-btn");
    let map, marker, mapInited = false;

    function initMap() {
      const jbnu = [35.8467, 127.1257]; // 전북대 위치
      map = L.map("jbnu-map").setView(jbnu, 15);
      L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
        maxZoom: 19,
        attribution: '&copy; OpenStreetMap contributors'
      }).addTo(map);
      marker = L.marker(jbnu).addTo(map)
        .bindPopup("<b>전북대학교</b><br>공대 7호관 근처").openPopup();
    }

    // 지도 토글
    btn.addEventListener("click", () => {
      wrap.classList.toggle("active");
      if (wrap.classList.contains("active") && !mapInited) {
        setTimeout(initMap, 100);
        mapInited = true;
      }
      if (wrap.classList.contains("active")) {
        wrap.scrollIntoView({ behavior: "smooth", block: "center" });
      }
    });

    // 검색 기능 (Enter + 버튼 클릭)
    async function handleSearch() {
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

    input.addEventListener("keypress", e => {
      if (e.key === "Enter") {
        e.preventDefault();
        handleSearch();
      }
    });

    searchBtn.addEventListener("click", handleSearch);
  })();
</script>

---

Alice Wu is a professor of artificial intelligence at the Stanford AI Lab. Her research interests include distributed robotics, mobile computing and programmable matter. She leads the Robotic Neurobiology group, which develops self-reconfiguring robots, systems of self-organizing robots, and mobile sensor networks.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.

{{< icon name="download" pack="fas" >}} {{< staticref "uploads/resume.pdf" "newtab" >}}Download{{< /staticref >}} my resumé as a PDF.
