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

<!-- TRAVELMATE AI - PART 2 -->

<section id="ai" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🤖 TravelMate AI Chat</h2>
 <p>Ask anything about your trip.</p>

 <div id="chatBox" class="item">
  <strong>TravelMate</strong>
  <p>Hi! I'm your travel companion. What do you need help with?</p>
 </div>

 <input id="chatInput" placeholder="Ask about your trip...">
 <button class="action" onclick="sendTravelMessage()">Send</button>
 <p style="font-size:11px;color:#758196">
  Demo chat interface. AI responses require a secure AI API connection.
 </p>
</section>

<section id="navigation" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🗺️ Smart Navigation</h2>
 <p>Choose your destination and open a map.</p>

 <input id="mapDestination" placeholder="Where do you want to go?">

 <button class="action" onclick="openAmap()">
  Open Amap / Gaode 🇨🇳
 </button>

 <button class="action"
 style="margin-top:10px;background:#16845b"
 onclick="openGoogleMaps()">
  Open Google Maps 🌍
 </button>

 <div class="item">
  <strong>China Travel</strong>
  <p>Use Amap / Gaode for navigation in China.</p>
  <a href="https://www.amap.com/" target="_blank">Visit Amap website ↗</a>
 </div>

 <div class="item">
  <strong>Other destinations</strong>
  <p>Use Google Maps for other countries.</p>
 </div>

 <p style="font-size:11px;color:#758196">
  Internet connection is required for live maps and directions.
 </p>
</section>

<section id="discover" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🌏 Discover</h2>
 <p>Explore places, attractions and local experiences.</p>
 <input id="discoverPlace" placeholder="Enter city or destination">
 <button class="action" onclick="searchDestination()">Explore</button>
</section>

<section id="plan" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🗓️ Trip Planner</h2>
 <input id="planTitle" placeholder="Activity or destination">
 <input id="planDate" type="date">
 <button class="action" onclick="addPlan()">Add to itinerary</button>
 <div id="planList"></div>
</section>

<section id="prepare" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🎒 Prepare</h2>
 <p>Prepare documents and travel essentials.</p>
 <div class="item">Passport</div>
 <div class="item">Flight tickets</div>
 <div class="item">Hotel booking</div>
 <div class="item">Travel insurance</div>
</section>

<section id="adapt" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🔄 Travel Help</h2>
 <p>Need help during your journey?</p>
 <div class="item">🚨 Emergency planning</div>
 <div class="item">🚆 Transport problems</div>
 <div class="item">🏨 Hotel issues</div>
 <div class="item">🍜 Find food nearby</div>
</section>

<section id="reflect" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>📸 Travel Memories</h2>
 <textarea id="memoryNote" placeholder="Write your travel memories..."></textarea>
 <button class="action" onclick="saveMemory()">Save memory</button>
 <div id="memoryList"></div>
</section>

<section id="weather" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🌤️ Weather</h2>
 <p>Check the latest weather forecast.</p>
 <a href="https://www.weather.com/" target="_blank">Open weather forecast ↗</a>
</section>

<section id="currency" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>💱 Currency Converter</h2>
 <input id="myrAmount" type="number" placeholder="Amount in MYR">
 <label>Convert to</label>
 <select id="currencyRate">
  <option value="1.55">Chinese Yuan (CNY) - sample rate</option>
  <option value="0.19">US Dollar (USD) - sample rate</option>
 </select>
 <button class="action" onclick="convertCurrency()">Convert</button>
 <div id="currencyResult" class="item"></div>
 <small>Sample rates only. Check live exchange rates before exchanging money.</small>
</section>

<section id="shopping" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🛍️ Shopping List</h2>
 <input id="shoppingItem" placeholder="Item to buy at destination">
 <button class="action" onclick="addShopping()">Add item</button>
 <div id="shoppingList"></div>
</section>

<section id="expenses" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>💰 Expense Tracker</h2>
 <input id="expenseName" placeholder="Expense description">
 <input id="expenseAmount" type="number" placeholder="Amount (RM)">
 <button class="action" onclick="addExpense()">Add expense</button>
 <div id="expenseList"></div>
 <h3 id="expenseTotal">Total: RM0.00</h3>
</section>

<section id="packing" class="page">
 <button class="back" onclick="openPage('home')">← Back</button>
 <h2>🧳 Packing List</h2>
 <input id="packingItem" placeholder="Item to bring from home">
 <button class="action" onclick="addPacking()">Add item</button>
 <div id="packingList"></div>
</section>

<script>
function sendTravelMessage(){
 const input=document.getElementById('chatInput');
 const box=document.getElementById('chatBox');
 if(!input.value.trim())return;
 box.innerHTML += '<p><strong>You:</strong> '+escapeTravel(input.value)+'</p>';
 box.innerHTML += '<p><strong>TravelMate:</strong> AI connection is not set up yet. This feature will be connected in a later stage.</p>';
 input.value='';
}

function escapeTravel(value){
 const d=document.createElement('div');
 d.textContent=value;
 return d.innerHTML;
}

function openAmap(){
 const q=document.getElementById('mapDestination').value.trim();
 window.open('https://www.amap.com/search?query='+encodeURIComponent(q),'_blank');
}

function openGoogleMaps(){
 const q=document.getElementById('mapDestination').value.trim();
 window.open('https://www.google.com/maps/search/?api=1&query='+encodeURIComponent(q),'_blank');
}

function searchDestination(){
 const q=document.getElementById('discoverPlace').value.trim();
 if(q)window.open('https://www.google.com/search?q='+encodeURIComponent(q+' travel attractions'),'_blank');
}

function addPlan(){
 const name=document.getElementById('planTitle').value.trim();
 const date=document.getElementById('planDate').value;
 if(!name)return;
 addTravelItem('planList',name+' '+date);
 document.getElementById('planTitle').value='';
}

function addShopping(){
 const v=document.getElementById('shoppingItem').value.trim();
 if(!v)return;
 addTravelItem('shoppingList','🛍️ '+v);
 document.getElementById('shoppingItem').value='';
}

function addPacking(){
 const v=document.getElementById('packingItem').value.trim();
 if(!v)return;
 addTravelItem('packingList','🧳 '+v);
 document.getElementById('packingItem').value='';
}

function addTravelItem(id,value){
 const el=document.createElement('div');
 el.className='item';
 el.textContent=value;
 document.getElementById(id).appendChild(el);
}

let travelExpenses=0;

function addExpense(){
 const name=document.getElementById('expenseName').value.trim();
 const amount=Number(document.getElementById('expenseAmount').value);
 if(!name||amount<=0)return;
 travelExpenses+=amount;
 addTravelItem('expenseList',name+' — RM'+amount.toFixed(2));
 document.getElementById('expenseTotal').textContent='Total: RM'+travelExpenses.toFixed(2);
 document.getElementById('expenseName').value='';
 document.getElementById('expenseAmount').value='';
}

function convertCurrency(){
 const amount=Number(document.getElementById('myrAmount').value);
 const rate=Number(document.getElementById('currencyRate').value);
 document.getElementById('currencyResult').textContent=
  'Estimated amount: '+(amount*rate).toFixed(2);
}

function saveMemory(){
 const v=document.getElementById('memoryNote').value.trim();
 if(!v)return;
 addTravelItem('memoryList',v);
 document.getElementById('memoryNote').value='';
}
</script>
</body>
</html>

</body>
</html>
