<!DOCTYPE html>
<html lang="ja">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>気分で行き先を決めるマップ（徒歩15分以内）</title>

 <link
   rel="stylesheet"
   href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
 />

 <style>
   body {
     margin: 0;
     font-family: sans-serif;
     text-align: center;
     line-height: 1.6;
   }

   h1 {
     margin: 12px;
     font-size: clamp(18px, 4vw, 24px);
   }

   .buttons {
     display: flex;
     flex-wrap: wrap;
     justify-content: center;
     gap: 8px;
     padding: 0 10px;
   }

   button {
     padding: 12px 16px;
     font-size: clamp(14px, 3.5vw, 16px);
     cursor: pointer;
     border: 1px solid #ccc;
     border-radius: 6px;
     background: #f8f8f8;
     flex: 1 1 200px;
     max-width: 280px;
   }

   button:hover {
     background: #eee;
   }

   #message {
     margin: 10px;
     font-size: clamp(14px, 3.5vw, 16px);
   }

   #map {
     height: 70vh;
     width: 100%;
   }

   @media (min-width: 768px) {
     #map {
       height: 75vh;
     }
   }
 </style>
</head>
<body>

 <h1>今の気分で行き先を決めるマップ（徒歩15分以内）</h1>

 <div class="buttons">
   <button onclick="showRandomSpot('calm')">📚 静かに過ごしたい</button>
   <button onclick="showRandomSpot('lively')">🎉 にぎやかな場所に行きたい</button>
   <button onclick="showRandomSpot('nature')">🌿 自然に触れたい</button>
 </div>

 <div id="message"></div>
 <div id="map"></div>

 <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

 <script>
   // 高知県立大学 永国寺キャンパス
   const campus = [33.5599, 133.5316];

   // 徒歩15分 ≒ 1200m
   const walkRadius = 1200;

   const map = L.map('map').setView(campus, 15);

   L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
     attribution: '© OpenStreetMap contributors'
   }).addTo(map);

   let circle = null;
   let marker = null;

   // 気分ごとの円の色
   const moodColors = {
     calm:   { color: 'blue',   fillColor: '#99ccff' },
     lively: { color: 'orange', fillColor: '#ffe699' },
     nature: { color: 'green',  fillColor: '#b6e3b6' }
   };

   // スポットデータ
   const spots = {
     calm: [
       { name: "永国寺図書館", lat: 33.5606, lng: 133.5307 },
       { name: "オーテピア", lat: 33.5619, lng: 133.5328 },
       { name: "高知公園", lat: 33.5590, lng: 133.5339 }
     ],
     lively: [
       { name: "帯屋町商店街", lat: 33.5604, lng: 133.5353 },
       { name: "高知駅前", lat: 33.5638, lng: 133.5430 },
       { name: "ひろめ市場", lat: 33.5595, lng: 133.5347 }
     ],
     nature: [
       { name: "桂浜", lat: 33.4976, lng: 133.5676 },
       { name: "牧野植物園", lat: 33.5796, lng: 133.5543 },
       { name: "鏡川（河川敷）", lat: 33.5558, lng: 133.5228 }
     ]
   };

   function showRandomSpot(mood) {
     if (marker) map.removeLayer(marker);
     if (circle) map.removeLayer(circle);

     // 気分に応じた色の円を表示
     circle = L.circle(campus, {
       radius: walkRadius,
       color: moodColors[mood].color,
       fillColor: moodColors[mood].fillColor,
       fillOpacity: 0.3
     }).addTo(map);

     // 徒歩15分以内のスポットだけ抽出
     const availableSpots = spots[mood].filter(place =>
       map.distance(campus, [place.lat, place.lng]) <= walkRadius
     );

     if (availableSpots.length === 0) {
       document.getElementById("message").textContent =
         "徒歩15分以内に該当する場所がありません。";
       return;
     }

     // ランダムで1か所選択
     const place = availableSpots[
       Math.floor(Math.random() * availableSpots.length)
     ];

     marker = L.marker([place.lat, place.lng])
       .addTo(map)
       .bindPopup(place.name)
       .openPopup();

     map.setView(campus, 15);

     const moodText = {
       calm: "静かに過ごしたい日におすすめ",
       lively: "にぎやかな場所で気分転換",
       nature: "自然に触れてリラックス"
     };

     document.getElementById("message").textContent =
       moodText[mood] + "： " + place.name;
   }
 </script>

</body>
</html>
