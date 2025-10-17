---
widget: blank
headless: true
weight: 12
title: ""
subtitle: ""
---


<div style="display:flex; align-items:center; gap:10px; flex-wrap:wrap; font-size:1.05rem;">
  <div>
    <strong>전북대 산업정보시스템공학과 · 컴퓨터인공지능학부</strong>
  </div>


  <button id="jbnu-map-toggle"
          title="전북대로 찾아오는 지도 보기"
          style="border:none; background:none; cursor:pointer; font-size:1.6rem;">
    📍
  </button>
</div>


<div id="jbnu-map-wrap" style="display:none; margin-top:12px;">
  <div id="jbnu-map"
       style="height:420px; width:100%; max-width:900px; margin:0 auto; border-radius:14px; overflow:hidden; box-shadow:0 8px 28px rgba(0,0,0,0.35);">
  </div>
</div>


<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
  (function () {
    const btn   = document.getElementById('jbnu-map-toggle');
    const wrap  = document.getElementById('jbnu-map-wrap');
    let mapInited = false;

    function initMap() {
      const center = [35.8467, 127.1257]; // 전북대 위치
      const map = L.map('jbnu-map').setView(center, 15);
      L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        attribution: '&copy; OpenStreetMap',
      }).addTo(map);
      L.marker(center).addTo(map)
        .bindPopup('<b>전북대학교</b><br>공대 7호관 근처')
        .openPopup();
      mapInited = true;
    }

    btn.addEventListener('click', function () {
      const isHidden = wrap.style.display === 'none';
      wrap.style.display = isHidden ? 'block' : 'none';
      if (isHidden && !mapInited) setTimeout(initMap, 0);
      if (isHidden) wrap.scrollIntoView({ behavior: 'smooth', block: 'center' });
    });
  })();
</script>
