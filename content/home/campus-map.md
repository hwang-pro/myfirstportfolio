---
widget: blank
headless: true
weight: 15          
title: "캠퍼스 위치"
subtitle: "전북대학교 공대 7호관 근처"


---

<div id="map" style="height:420px; width:100%; border-radius:12px; overflow:hidden;"></div>


<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>


<link rel="stylesheet" href="https://unpkg.com/leaflet-geosearch/dist/geosearch.css" />
<script src="https://unpkg.com/leaflet-geosearch/dist/bundle.min.js"></script>

<script>

  const map = L.map('map').setView([35.8467, 127.1257], 15);


  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '&copy; OpenStreetMap'
  }).addTo(map);


  L.marker([35.8467, 127.1257]).addTo(map)
    .bindPopup('<b>전북대학교</b><br>공대 7호관 근처')
    .openPopup();


  const provider = new window.GeoSearch.OpenStreetMapProvider();
  const searchControl = new window.GeoSearch.GeoSearchControl({
    provider,
    style: 'bar',
    showMarker: true,
    showPopup: true,
    autoClose: true,
  });
  map.addControl(searchControl);
</script>
