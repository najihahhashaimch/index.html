# index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101c2c">
<title>TravelMate AI</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 font-family:Arial,sans-serif;
 background:#f4f6fa;
 color:#152238;
}
header{
 background:#101c2c;
 color:white;
 padding:22px;
 border-radius:0 0 24px 24px;
}
.logo{font-size:22px;font-weight:bold}
.logo span{color:#64c8ff}
.tagline{font-size:11px;color:#b6c6da;margin-top:5px}
.container{max-width:900px;margin:auto;padding:18px}
h2{font-size:19px}
.trip{
 background:linear-gradient(120deg,#173e68,#277dc0);
 color:white;padding:22px;border-radius:18px;
 margin:20px 0;
}
.trip h1{margin:10px 0}
.grid{
 display:grid;
 grid-template-columns:repeat(2,1fr);
 gap:12px;
}
.card{
 background:white;
 padding:18px;
 border-radius:16px;
 border:1px solid #e7ebf1;
 cursor:pointer;
}
.card:active{transform:scale(.97)}
.card .icon{font-size:28px;margin-bottom:10px}
.card strong{display:block;font-size:14px}
.card small{color:#758196;font-size:11px}
.page{display:none}
.page.active{display:block}
.back{
 padding:10px 15px;
 border:0;border-radius:9px;
 background:#e5edf8;
 margin-bottom:15px;
}
input,textarea,select{
 width:100%;padding:13px;
 margin:7px 0;border:1px solid #ddd;
 border-radius:10px;font-size:14px;
}
.action{
 background:#246bce;color:white;
 border:0;padding:13px 20px;
 border-radius:10px;
}
.item{
 background:white;padding:13px;
 margin:8px 0;border-radius:11px;
}
.bottom{
 position:sticky;bottom:0;
 background:white;
 display:flex;justify-content:space-around;
 padding:13px 4px;
 border-top:1px solid #eee;
}
.bottom button{
 border:0;background:none;
 font-size:11px;color:#64748b;
}
.bottom span{display:block;font-size:20px}
@media(min-width:650px){
 .grid{grid-template-columns:repeat(3,1fr)}
}
</style>
</head>

<body>

<header>
 <div class="logo">🌍 TRAVELMATE <span>AI</span></div>
 <div class="tagline">YOUR UNIVERSAL TRAVEL COMPANION</div>
</header>

<main class="container">

<section id="home" class="page active">

<h2>Hello, Traveller! 👋</h2>
<p style="color:#758196;font-size:13px">
Plan intelligently. Navigate confidently. Travel together.
</p>

<div class="trip">
 <small>YOUR ACTIVE TRIP</small>
 <h1>🇨🇳 China</h1>
 Guangzhou • Shenzhen
 <p>November 2026 · 5D4N</p>
</div>

<h2>Travel Modes</h2>

<div class="grid">

<div class="card" onclick="openPage('discover')">
 <div class="icon">🌏</div>
 <strong>Discover</strong>
 <small>Explore destinations</small>
</div>

<div class="card" onclick="openPage('plan')">
 <div class="icon">🗓️</div>
 <strong>Plan</strong>
 <small>Itinerary and bookings</small>
</div>

<div class="card" onclick="openPage('prepare')">
 <div class="icon">🎒</div>
 <strong>Prepare</strong>
 <small>Packing and documents</small>
</div>

<div class="card" onclick="openPage('navigation')">
 <div class="icon">🗺️</div>
 <strong>Smart Navigation</strong>
 <small>Map and metro routes</small>
</div>

<div class="card" onclick="openPage('adapt')">
 <div class="icon">🔄</div>
 <strong>Adapt</strong>
 <small>Travel problem solving</small>
</div>

<div class="card" onclick="openPage('reflect')">
 <div class="icon">📸</div>
 <strong>Reflect</strong>
 <small>Travel memories</small>
</div>

</div>

<h2>Travel Tools</h2>

<div class="grid">

<div class="card" onclick="openPage('ai')">
 🤖 <strong>AI Chat</strong>
</div>

<div class="card" onclick="openPage('shopping')">
 🛍️ <strong>Shopping List</strong>
</div>

<div class="card" onclick="openPage('expenses')">
 💰 <strong>Expenses</strong>
</div>

<div class="card" onclick="openPage('packing')">
 🧳 <strong>Packing List</strong>
</div>

<div class="card" onclick="openPage('weather')">
 🌤️ <strong>Weather</strong>
</div>

<div class="card" onclick="openPage('currency')">
 💱 <strong>Currency</strong>
</div>

</div>
</section>

<script>
function openPage(id){
 document.querySelectorAll('.page')
 .forEach(p=>p.classList.remove('active'));
 document.getElementById(id).classList.add('active');
 window.scrollTo(0,0);
}
</script>
</main>

<nav class="bottom">
<button onclick="openPage('home')"><span>🏠</span>Home</button>
<button onclick="openPage('plan')"><span>🗓️</span>Trips</button>
<button onclick="openPage('navigation')"><span>🗺️</span>Map</button>
<button onclick="openPage('ai')"><span>🤖</span>AI Chat</button>
</nav>

</body>
</html>
