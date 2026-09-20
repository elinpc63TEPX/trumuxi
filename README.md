<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>TRUMUXI | The Future Has A Name</title>

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
font-family:Arial,sans-serif;
background:radial-gradient(circle at top,#513508,#050505 60%);
color:white;
}
nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:18px 5%;
background:#050505;
border-bottom:1px solid #dcae36;
}
.logo{color:#ffd34d;font-size:22px;font-weight:bold}
.logo span{
display:inline-flex;
align-items:center;
justify-content:center;
background:linear-gradient(135deg,#fff19a,#c88900);
color:#111;
border-radius:50%;
width:30px;height:30px;
margin-right:5px;
}
nav a{color:#e8cd75;text-decoration:none;margin:0 8px;font-size:12px}
.btn{
background:linear-gradient(135deg,#fff19a,#dcae36);
color:#111;
border:0;
border-radius:25px;
padding:11px 20px;
font-weight:bold;
cursor:pointer;
}
.hero{
width:92%;
max-width:1200px;
margin:25px auto;
display:grid;
grid-template-columns:1.4fr .8fr;
gap:18px;
}
.hero-main{
position:relative;
overflow:hidden;
min-height:360px;
padding:35px 28px;
border:1px solid #79551b;
border-radius:22px;
background:radial-gradient(circle at 75% 50%,#8c570b,#17130d 35%,#04080c 75%);
}
.hero-main h1{
font-size:clamp(42px,7vw,80px);
font-style:italic;
color:#ffe18a;
text-shadow:3px 4px 0 #70440c;
margin:25px 0 12px;
}
.hero-main p{color:#ead9a5;line-height:1.8}
.orb{
position:absolute;
right:8%;
bottom:25px;
width:185px;height:185px;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
font-size:100px;
font-weight:bold;
color:#ffe18a;
background:radial-gradient(circle,#fff19a,#bd7b08 45%,#241605 70%);
box-shadow:0 0 30px #ffbf3b,0 0 90px #ffbf3b55;
}
.market{
padding:18px;
border:1px solid #4a3819;
border-radius:22px;
background:#070c12;
}
.title{
display:flex;
justify-content:space-between;
align-items:center;
color:#f6d778;
font-weight:bold;
margin-bottom:14px;
}
.live{color:#55e58b;font-size:11px}
.market-item{
display:flex;
justify-content:space-between;
align-items:center;
padding:13px 10px;
margin:8px 0;
border:1px solid #29323a;
border-radius:12px;
background:#0b1118;
}
.market-item small{display:block;color:#8a96a4;margin-top:5px}
.price{text-align:right;font-size:12px}
.up{color:#55e58b;font-size:11px;margin-top:4px}
.people{
width:92%;
max-width:1200px;
margin:18px auto;
display:grid;
grid-template-columns:repeat(4,1fr);
gap:12px;
}
.person{
text-align:center;
padding:20px 8px;
border:1px solid #61471b;
border-radius:18px;
background:linear-gradient(#251a0b,#080b10);
}
.face{
width:85px;height:85px;
display:flex;
align-items:center;
justify-content:center;
margin:auto auto 10px;
border-radius:50%;
font-size:38px;
background:radial-gradient(circle,#ffe49a,#87580e 55%,#111);
border:2px solid #dcae36;
}
.person h3{color:#ffe18a;font-size:15px}
.person small{display:block;color:#aeb4bd;margin-top:5px;font-size:11px}
.badge{
display:inline-block;
margin-top:12px;
padding:5px 10px;
border-radius:20px;
background:#111c28;
border:1px solid #354452;
color:#e9cf7a;
font-size:11px;
}
.dashboard{
width:92%;
max-width:1200px;
margin:18px auto;
display:grid;
grid-template-columns:.7fr 1.5fr .7fr;
gap:14px;
}
.panel{
padding:18px;
border:1px solid #293542;
border-radius:18px;
background:linear-gradient(#09121b,#05090e);
}
.panel h3{color:#f4d675;font-size:16px;margin-bottom:14px}
.panel p{color:#9faab6;font-size:12px;line-height:1.7}
.social{
display:block;
text-align:center;
margin-top:12px;
padding:10px;
border-radius:24px;
background:linear-gradient(135deg,#fff0a0,#d99a21);
color:#211500;
font-weight:bold;
font-size:12px;
text-decoration:none;
}
.chart{
width:100%;
height:220px;
background:#07121c;
border:1px solid #20384b;
border-radius:12px;
}
.visitors{text-align:center}
.visitor-number{
font-size:35px;
font-weight:bold;
color:#ffe18a;
margin:25px 0 8px;
}
.muted{font-size:11px;color:#8995a2}
.coins{
width:92%;
max-width:1200px;
margin:25px auto 35px;
}
.grid{
display:grid;
grid-template-columns:repeat(5,1fr);
gap:12px;
}
.card{
padding:15px;
border:1px solid #293542;
border-radius:16px;
background:linear-gradient(#0b141e,#05080c);
}
.card:hover{border-color:#c99b37}
.icon{
width:38px;height:38px;
display:flex;
align-items:center;
justify-content:center;
border-radius:50%;
font-size:22px;
background:#172332;
border:1px solid #465466;
}
.top{display:flex;align-items:center;gap:8px}
.card h4{font-size:13px}
.card small{color:#8593a3;font-size:10px}
.coin-price{
font-size:15px;
font-weight:bold;
color:#ffe18a;
margin-top:14px;
}
.change{color:#55e58b;font-size:11px;margin-top:6px}
.card button{
width:100%;
margin-top:12px;
padding:8px;
border:1px solid #74551d;
border-radius:20px;
background:#16130c;
color:#f4d675;
cursor:pointer;
}
footer{
text-align:center;
padding:25px;
border-top:1px solid #2c2518;
color:#87909b;
font-size:11px;
}
.modal{
display:none;
position:fixed;
inset:0;
z-index:50;
align-items:center;
justify-content:center;
padding:20px;
background:#000c;
}
.modal-box{
width:min(500px,100%);
padding:25px;
border:1px solid #c69a37;
border-radius:18px;
background:#08111a;
}
.modal-box h2{color:#ffe18a;margin-bottom:15px}
.modal-box p{color:#b7c0ca;line-height:1.8;font-size:13px}
.close{
float:right;
background:none;
border:0;
color:white;
font-size:25px;
cursor:pointer;
}
@media(max-width:850px){
.hero{grid-template-columns:1fr}
.people{grid-template-columns:repeat(2,1fr)}
.dashboard{grid-template-columns:1fr}
.grid{grid-template-columns:repeat(2,1fr)}
.orb{width:130px;height:130px;font-size:70px;opacity:.65}
}
@media(max-width:420px){
nav{padding:12px 3%}
.logo{font-size:17px}
nav a{margin:0 3px;font-size:10px}
.hero-main{padding:25px 18px}
.hero-main h1{font-size:43px}
.grid{gap:8px}
.card{padding:11px}
}
</style>
</head>

<body>

<nav>
<div class="logo"><span>T</span>TRUMUXI</div>
<div>
<a href="#home">Home</a>
<a href="#market">Market</a>
<a href="#coins">Coins</a>
<a href="#community">Community</a>
</div>
<a class="btn" href="#coins">◉ TRMX</a>
</nav>

<main id="home">

<section class="hero">

<div class="hero-main">
<div style="color:#ffd34d;font-weight:bold;font-size:12px">
THE FUTURE OF DIGITAL CURRENCY
</div>

<h1>TRUMUXI</h1>

<p>
Four Leaders. One Vision.<br>
The Future Crypto Coin.
</p>

<button class="btn" style="margin-top:22px"
onclick="document.getElementById('coins').scrollIntoView({behavior:'smooth'})">
Explore →
</button>

<div class="orb">T</div>
</div>

<div class="market" id="market">
<div class="title">
<span>📊 Live Crypto Market</span>
<span class="live">● LIVE</span>
</div>
<div id="marketList"></div>
</div>

</section>

<section class="people">

<div class="person">
<div class="face">🇺🇸</div>
<h3>Trump</h3>
<small>TRUMP</small>
<span class="badge">TRUMP TOKEN</span>
</div>

<div class="person">
<div class="face">🇷🇺</div>
<h3>Putin</h3>
<small>SOLANA</small>
<span class="badge">SOL</span>
</div>

<div class="person">
<div class="face">🚀</div>
<h3>Elon</h3>
<small>DOGECOIN</small>
<span class="badge">DOGE</span>
</div>

<div class="person">
<div class="face">🇨🇳</div>
<h3>China</h3>
<small>VECHAIN</small>
<span class="badge">VET</span>
</div>

</section>

<section class="dashboard">

<div class="panel" id="community">
<h3>🌐 TRUMUXI Community</h3>
<p>Join the future crypto movement and follow TRUMUXI updates.</p>

<a class="social" href="#" onclick="alert('Add Telegram link');return false">
➤ Telegram
</a>

<a class="social" href="#" onclick="alert('Add X/Twitter link');return false">
𝕏 X / Twitter
</a>
</div>

<div class="panel">
<h3>📊 TRUMUXI Analytics</h3>

<div class="title">
<span style="font-size:12px">TRUMUXI Price Chart</span>
<span style="font-size:11px">TMX $0.01</span>
</div>

<canvas id="chart" class="chart" width="700" height="300"></canvas>

<div style="display:flex;justify-content:space-between;color:#8794a3;font-size:10px;margin-top:8px">
<span>Start</span>
<span>1H</span>
<span>2H</span>
<span>3H</span>
<span>4H</span>
</div>
</div>

<div class="panel visitors">
<h3>👁 Website Visitors</h3>
<div class="visitor-number" id="visitorNumber">0</div>
<div class="muted">People visited<br>TRUMUXI</div>
</div>

</section>

<section class="coins" id="coins">

<div class="title">
<span>🔥 Top 10 Crypto Market</span>
<span class="muted">Online Data</span>
</div>

<div class="grid" id="coinGrid"></div>

</section>

</main>

<footer>
© 2026 TRUMUXI · The Future Has A Name
</footer>

<div class="modal" id="modal">
<div class="modal-box">
<button class="close" onclick="closeModal()">×</button>
<h2 id="modalTitle"></h2>
<p id="modalText"></p>
</div>
</div>

<script>

const coins=[
{id:'bitcoin',name:'Bitcoin',symbol:'BTC',icon:'₿',price:67967},
{id:'ethereum',name:'Ethereum',symbol:'ETH',icon:'◆',price:2420.03},
{id:'solana',name:'Solana',symbol:'SOL',icon:'≋',price:99.22},
{id:'dogecoin',name:'Dogecoin',symbol:'DOGE',icon:'Ð',price:.083927},
{id:'tether',name:'Tether',symbol:'USDT',icon:'₮',price:1},
{id:'binancecoin',name:'BNB',symbol:'BNB',icon:'◆',price:600},
{id:'ripple',name:'XRP',symbol:'XRP',icon:'✕',price:2.45},
{id:'cardano',name:'Cardano',symbol:'ADA',icon:'₳',price:.85},
{id:'avalanche-2',name:'Avalanche',symbol:'AVAX',icon:'A',price:28.4},
{id:'chainlink',name:'Chainlink',symbol:'LINK',icon:'⬡',price:22.1}
];

function formatPrice(n){
return n<1?n.toFixed(6):n.toLocaleString('en-US',{minimumFractionDigits:2,maximumFractionDigits:2});
}

function renderCoins(){

document.getElementById('coinGrid').innerHTML=coins.map((c,i)=>`

<article class="card">

<div class="top">
<div class="icon">${c.icon}</div>
<div>
<h4>${c.name}</h4>
<small>${c.symbol}</small>
</div>
</div>

<div class="coin-price" id="price-${c.id}">
$${formatPrice(c.price)}
</div>

<div class="change" id="change-${c.id}">
+${(1.2+i*.37).toFixed(2)}%
</div>

<button onclick="showCoin('${c.name}','${c.symbol}',${c.price})">
View Details →
</button>

</article>

`).join('');

}

function renderMarket(){

document.getElementById('marketList').innerHTML=coins.slice(0,4).map((c,i)=>`

<div class="market-item">

<div>
<strong>${c.icon} ${c.name}</strong>
<small>${c.symbol}</small>
</div>

<div class="price">
$${formatPrice(c.price)}
<div class="up">+${(2.4+i*.7).toFixed(1)}%</div>
</div>

</div>

`).join('');

}

function showCoin(name,symbol,price){

document.getElementById('modalTitle').textContent=name+' ('+symbol+')';

document.getElementById('modalText').textContent=
'Reference price: $'+formatPrice(price)+
'. Online market data may be loaded through the CoinGecko public API. TRMX display price is $0.01 and is not a verified market price.';

document.getElementById('modal').style.display='flex';

}

function closeModal(){
document.getElementById('modal').style.display='none';
}

async function loadOnlinePrices(){

try{

const ids=coins.map(c=>c.id).join(',');

const response=await fetch(
'https://api.coingecko.com/api/v3/simple/price?ids='+
ids+'&vs_currencies=usd&include_24hr_change=true'
);

if(!response.ok)return;

const data=await response.json();

coins.forEach(c=>{

if(data[c.id]&&data[c.id].usd){

const price=document.getElementById('price-'+c.id);
const change=document.getElementById('change-'+c.id);

price.textContent='$'+formatPrice(data[c.id].usd);

const value=data[c.id].usd_24h_change||0;

change.textContent=(value>=0?'+':'')+value.toFixed(2)+'%';

change.style.color=value>=0?'#55e58b':'#ff7474';

}

});

}catch(error){

console.log('Online prices unavailable');

}

}

function drawChart(){

const canvas=document.getElementById('chart');
const ctx=canvas.getContext('2d');

const w=canvas.width;
const h=canvas.height;

ctx.clearRect(0,0,w,h);

ctx.strokeStyle='#263b4d';
ctx.lineWidth=1;

for(let i=1;i<5;i++){

let y=i*h/5;

ctx.beginPath();
ctx.moveTo(25,y);
ctx.lineTo(w-20,y);
ctx.stroke();

}

const values=[.006,.008,.009,.0102,.0093,.0095,.0115];

const min=.005;
const max=.0125;

const points=values.map((v,i)=>({

x:25+i*(w-55)/(values.length-1),

y:h-25-(v-min)/(max-min)*(h-50)

}));

ctx.beginPath();

points.forEach((p,i)=>{

if(i===0)ctx.moveTo(p.x,p.y);
else ctx.lineTo(p.x,p.y);

});

ctx.lineTo(points[points.length-1].x,h-25);
ctx.lineTo(points[0].x,h-25);
ctx.closePath();

ctx.fillStyle='rgba(220,174,54,.12)';
ctx.fill();

ctx.beginPath();

points.forEach((p,i)=>{

if(i===0)ctx.moveTo(p.x,p.y);
else ctx.lineTo(p.x,p.y);

});

ctx.strokeStyle='#ffd34d';
ctx.lineWidth=4;
ctx.stroke();

points.forEach(p=>{

ctx.beginPath();
ctx.arc(p.x,p.y,5,0,Math.PI*2);
ctx.fillStyle='#fff0a0';
ctx.fill();

});

}

function visitorCounter(){

let count=Number(localStorage.getItem('trumuxiVisitors')||'0');

if(!sessionStorage.getItem('trumuxiSession')){

count++;

localStorage.setItem('trumuxiVisitors',String(count));

sessionStorage.setItem('trumuxiSession','1');

}

document.getElementById('visitorNumber').textContent=count.toLocaleString();

}

renderCoins();
renderMarket();
drawChart();
visitorCounter();
loadOnlinePrices();

setInterval(loadOnlinePrices,60000);

window.addEventListener('resize',drawChart);

</script>

</body>
</html>
