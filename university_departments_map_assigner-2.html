<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>جامعة كلباء - دليل الأقسام</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@3.3.3/dist/tailwind.min.css">
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <style>
    body { font-family: 'Cairo', sans-serif; }
    #map { height: 100%; }
  </style>
</head>
<body class="bg-beige-100">
  <header class="bg-yellow-900 text-white p-4 text-2xl font-semibold">مرحبا بكم في جامعة كلباء</header>

  <section class="bg-yellow-50 p-4 text-yellow-900">
    <h2 class="text-xl font-semibold mb-2">مقدمة</h2>
    <p>يسرنا أن نقدم هذا الدليل لتسهيل الوصول إلى أقسام الجامعة بكل راحة وسهولة. يمكنكم استكشاف الأقسام ومشاهدة المسارات على الخريطة التفاعلية.</p>
    <p class="mt-2">مبادرة من الطالبة: عايشه راشد الزعابي<br>رقم الجماعي: KB2410105</p>
  </section>

  <div class="flex h-screen">
    <aside class="w-80 bg-yellow-50 p-4 shadow-md overflow-auto">
      <h3 class="text-yellow-900 text-xl font-semibold mb-2">الأقسام</h3>
      <ul id="deptsList" class="space-y-2"></ul>
    </aside>
    <main class="flex-1">
      <div id="map" class="h-full"></div>
    </main>
  </div>

  <footer class="bg-yellow-900 text-white p-2 text-center">© 2025 جامعة كلباء</footer>

  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
  <script>
    const state = {
      depts: [
        {name: 'قسم التسجيل والقبول', lat: 25.1128, lng: 56.3255},
        {name: 'قسم المالية', lat: 25.1132, lng: 56.3262},
        {name: 'قسم شؤون الطلبة', lat: 25.1124, lng: 56.3249},
        {name: 'قسم الإدارة', lat: 25.1130, lng: 56.3250},
        {name: 'قسم الموارد البشرية', lat: 25.1126, lng: 56.3258},
        {name: 'قسم المكتبة', lat: 25.1122, lng: 56.3252},
        {name: 'قسم تكنولوجيا المعلومات', lat: 25.1129, lng: 56.3247}
      ],
      markers: {},
      polyline: null,
      userMarker: null,
      userCircle: null
    };

    const deptsList = document.getElementById('deptsList');

    const map = L.map('map').setView([25.1122, 56.3245], 17);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', { maxZoom: 19, attribution: '© OpenStreetMap' }).addTo(map);

    const entrance = [25.1120, 56.3245];
    L.marker(entrance).addTo(map).bindPopup('بوابة الجامعة').openPopup();

    state.depts.forEach((d,i)=>{
      const li = document.createElement('li');
      li.className = 'p-2 bg-yellow-100 rounded cursor-pointer hover:bg-yellow-200';
      li.textContent = d.name;
      li.onclick = ()=> showRoute(i);
      deptsList.appendChild(li);
    });

    state.depts.forEach((d,i)=>{
      const marker = L.marker([d.lat,d.lng]).addTo(map).bindPopup(`<b>${d.name}</b>`);
      state.markers[i] = marker;
    });

    function showRoute(i){
      const d = state.depts[i];
      if(state.polyline){ map.removeLayer(state.polyline); }
      state.polyline = L.polyline([entrance, [d.lat,d.lng]], {color:'#8B4513', weight:5, opacity:0.7}).addTo(map);
      map.fitBounds(state.polyline.getBounds());
      state.markers[i].openPopup();
    }

    map.locate({watch: true, setView: true, maxZoom: 18});

    map.on('locationfound', function(e){
      const radius = e.accuracy / 2;
      if(!state.userMarker){
        state.userMarker = L.marker(e.latlng).addTo(map).bindPopup('أنت هنا').openPopup();
      } else {
        state.userMarker.setLatLng(e.latlng);
      }
      if(!state.userCircle){
        state.userCircle = L.circle(e.latlng, radius).addTo(map);
      } else {
        state.userCircle.setLatLng(e.latlng).setRadius(radius);
      }
    });

    map.on('locationerror', function(e){ alert('تعذر الحصول على الموقع: ' + e.message); });
  </script>
</body>
</html>
