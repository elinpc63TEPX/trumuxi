<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="TRUMUXI — a cinematic crypto concept inspired by four global names and the future of digital assets.">
<meta name="theme-color" content="#070912">
<title>TRUMUXI — The Future Has a Name</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
:root{
  --bg:#060812;--card:rgba(18,22,38,.72);--line:rgba(255,255,255,.11);
  --text:#f7f8ff;--muted:#9da5bd;--gold:#ffd45a;--cyan:#5ee7ff;
  --purple:#9d6cff;--green:#63f5b0;--danger:#ff6d86;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:Inter,Arial,sans-serif;background:radial-gradient(circle at 50% -10%,#25204b 0,#0b0d19 35%,var(--bg) 70%);color:var(--text);overflow-x:hidden}
body:before{content:"";position:fixed;inset:0;pointer-events:none;opacity:.18;background-image:linear-gradient(rgba(255,255,255,.03) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,.03) 1px,transparent 1px);background-size:55px 55px;mask-image:linear-gradient(to bottom,#000,transparent 75%)}
a{color:inherit;text-decoration:none}
.container{width:min(1120px,92%);margin:auto}
.nav{position:fixed;z-index:20;top:14px;left:50%;transform:translateX(-50%);width:min(1100px,94%);padding:12px 16px;border:1px solid var(--line);border-radius:22px;background:rgba(5,7,16,.72);backdrop-filter:blur(18px);display:flex;align-items:center;justify-content:space-between}
.brand{font-weight:900;letter-spacing:3px;font-size:18px}.brand span{color:var(--gold)}
.navlinks{display:flex;gap:20px;font-size:13px;color:#cbd0df}.navlinks a:hover{color:var(--gold)}
.btn{display:inline-flex;align-items:center;justify-content:center;padding:13px 20px;border-radius:13px;border:1px solid var(--line);font-weight:800;font-size:13px;transition:.25s;cursor:pointer}
.btn.primary{background:linear-gradient(135deg,var(--gold),#ff9f43);color:#17120a;border:0;box-shadow:0 10px 35px rgba(255,191,72,.2)}
.btn:hover{transform:translateY(-2px)}
.hero{min-height:850px;display:grid;place-items:center;text-align:center;padding:150px 0 90px;position:relative}
.orb{position:absolute;width:460px;height:460px;border-radius:50%;background:radial-gradient(circle,rgba(157,108,255,.26),transparent 65%);filter:blur(10px);animation:pulse 5s infinite alternate}
@keyframes pulse{to{transform:scale(1.15);opacity:.7}}
.coin{position:relative;width:190px;height:190px;margin:0 auto 35px;border-radius:50%;display:grid;place-items:center;background:radial-gradient(circle at 35% 25%,#fff4bd,#ffc94e 22%,#8f4d13 70%,#241507);box-shadow:0 0 0 8px rgba(255,212,90,.08),0 0 90px rgba(255,186,56,.3),inset 0 0 35px rgba(255,255,255,.35);animation:float 4s ease-in-out infinite}
.coin:after{content:"T";font-size:105px;font-weight:1000;color:#211404;text-shadow:3px 3px 0 rgba(255,255,255,.22)}
@keyframes float{50%{transform:translateY(-10px) rotate(2deg)}}
.kicker{color:var(--gold);font-size:12px;letter-spacing:5px;font-weight:900;margin-bottom:14px}
h1{font-size:clamp(52px,12vw,112px);line-height:.86;letter-spacing:-5px;background:linear-gradient(90deg,#fff,#ffd45a,#fff);-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p{max-width:700px;margin:25px auto;color:var(--muted);font-size:17px;line-height:1.8}
.actions{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-top:25px}
.ticker{border-top:1px solid var(--line);border-bottom:1px solid var(--line);padding:15px 0;overflow:hidden;white-space:nowrap;color:#b9c0d3;font-size:12px}
.ticker span{margin-right:45px}.up{color:var(--green)}
section{padding:100px 0}.section-head{display:flex;align-items:end;justify-content:space-between;gap:25px;margin-bottom:30px}
.eyebrow{color:var(--cyan);font-size:11px;font-weight:900;letter-spacing:3px;text-transform:uppercase;margin-bottom:10px}
h2{font-size:clamp(32px,6vw,58px);letter-spacing:-2px}.sub{color:var(--muted);line-height:1.7;max-width:650px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.card{border:1px solid var(--line);background:linear-gradient(145deg,rgba(255,255,255,.055),rgba(255,255,255,.015));border-radius:22px;padding:25px;box-shadow:0 15px 50px rgba(0,0,0,.15)}
.card:hover{border-color:rgba(255,212,90,.3);transform:translateY(-3px);transition:.25s}
.stat{font-size:32px;font-weight:900;margin:10px 0}.label{color:var(--muted);font-size:12px}
.people{grid-template-columns:repeat(4,1fr)}
.person{min-height:210px;display:flex;flex-direction:column;justify-content:end;overflow:hidden;position:relative}
.person:before{content:"";position:absolute;inset:0;background:radial-gradient(circle at 70% 25%,rgba(255,212,90,.22),transparent 35%),linear-gradient(145deg,#161b35,#080a12)}
.person>*{position:relative}.person .letter{font-size:55px;font-weight:1000;color:var(--gold);opacity:.8}.person h3{font-size:21px}.person p{color:var(--muted);font-size:12px;margin-top:5px}
.tokenomics{display:grid;grid-template-columns:1.1fr .9fr;gap:18px}
.bar{height:12px;border-radius:99px;background:#20253a;overflow:hidden;margin:10px 0 22px}.fill{height:100%;background:linear-gradient(90deg,var(--purple),var(--gold));border-radius:99px}
.row{display:flex;justify-content:space-between;gap:15px;color:#d9ddec;font-size:13px;margin-bottom:9px}
.roadmap{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}.phase{min-height:220px}.phase b{display:inline-block;color:#080a12;background:var(--gold);padding:6px 9px;border-radius:8px;font-size:11px}.phase h3{margin:18px 0 10px}.phase li{list-style:none;color:var(--muted);font-size:13px;line-height:1.8}
.cta{padding:55px;text-align:center;border:1px solid rgba(255,212,90,.22);border-radius:28px;background:radial-gradient(circle at center,rgba(157,108,255,.18),transparent 65%),rgba(255,255,255,.025)}
footer{padding:45px 0;border-top:1px solid var(--line);color:var(--muted);font-size:12px}.foot{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap}

/* Live Market & Chart styles */
.live-grid{display:grid;grid-template-columns:1fr 1.2fr;gap:20px;margin-top:30px}
.coin-list{max-height:420px;overflow-y:auto}
.coin-row{display:flex;justify-content:space-between;align-items:center;padding:11px 0;border-bottom:1px solid rgba(255,255,255,.07)}
.coin-row:last-child{border-bottom:none}
.coin-left{display:flex;align-items:center;gap:10px}
.coin-icon{width:28px;height:28px;border-radius:50%;background:#1c2138;display:grid;place-items:center;font-size:12px;font-weight:700}
.chart-box{height:320px;position:relative}

@media(max-width:800px){
  .navlinks{display:none}
  .grid,.people,.roadmap,.tokenomics,.live-grid{grid-template-columns:1fr}
  .hero{min-height:760px}
  .coin{width:145px;height:145px}
  .coin:after{font-size:80px}
}
@media(max-width:520px){
  section{padding:75px 0}
  .grid,.people,.roadmap,.tokenomics{grid-template-columns:1fr}
  .hero{padding-top:130px}
  .hero p{font-size:15px}
  h1{letter-spacing:-3px}
  .cta{padding:35px 20px}
  .section-head{display:block}
  .section-head .sub{margin-top:12px}
}
</style>
</head>
<body>
<nav class="nav">
  <a class="brand" href="#">TRU<span>MUXI</span></a>
  <div class="navlinks">
    <a href="#about">About</a>
    <a href="#market">Market</a>
    <a href="#tokenomics">Tokenomics</a>
    <a href="#roadmap">Roadmap</a>
    <a href="#community">Community</a>
  </div>
  <a class="btn primary" href="#community">Explore</a>
</nav>

<header class="hero">
  <div class="orb"></div>
  <div class="container" style="position:relative">
    <div class="coin"></div>
    <div class="kicker">A NEW CRYPTO CONCEPT</div>
    <h1>TRUMUXI</h1>
    <p>Four names. One symbol. A cinematic vision for a digital asset built around identity, technology and the future.</p>
    <div class="actions">
      <a class="btn primary" href="#about">Discover TRUMUXI</a>
      <a class="btn" href="#roadmap">View Roadmap</a>
    </div>
  </div>
</header>

<div class="ticker">
  <div class="container">
    <span>TRUMUXI <b>TMX</b></span>
    <span>TOTAL SUPPLY <b>21,000,000</b></span>
    <span>PRICE <b class="up">$0.01</b></span>
    <span>STATUS <b class="up">BUILDING</b></span>
  </div>
</div>

<main>
<!-- About -->
<section id="about">
<div class="container">
  <div class="section-head">
    <div>
      <div class="eyebrow">The origin</div>
      <h2>Four names.<br>One identity.</h2>
    </div>
    <p class="sub">TRUMUXI is a creative crypto brand concept inspired by four globally recognizable names. The website is designed to evolve as the project gains its real token, contract, community and market data.</p>
  </div>
  <div class="grid people">
    <div class="card person"><div class="letter">T</div><h3>Trump</h3><p>TRUM — the opening identity.</p></div>
    <div class="card person"><div class="letter">P</div><h3>Putin</h3><p>UX — the power and movement concept.</p></div>
    <div class="card person"><div class="letter">E</div><h3>Elon</h3><p>MU — technology and innovation.</p></div>
    <div class="card person"><div class="letter">C</div><h3>China</h3><p>XI — the final signature.</p></div>
  </div>
</div>
</section>

<!-- Dashboard -->
<section>
<div class="container">
  <div class="section-head">
    <div>
      <div class="eyebrow">Dashboard</div>
      <h2>Project snapshot</h2>
    </div>
    <p class="sub">Live project data for TRUMUXI.</p>
  </div>
  <div class="grid">
    <div class="card"><div class="label">TOKEN SYMBOL</div><div class="stat">TMX</div><div class="label">Official symbol</div></div>
    <div class="card"><div class="label">TOKEN PRICE</div><div class="stat">$0.01</div><div class="label">Starting price</div></div>
    <div class="card"><div class="label">TOTAL SUPPLY</div><div class="stat">21M</div><div class="label">21,000,000 TMX</div></div>
    <div class="card"><div class="label">MARKET CAP</div><div class="stat">$210K</div><div class="label">At starting price</div></div>
    <div class="card"><div class="label">LIQUIDITY</div><div class="stat">TBA</div><div class="label">To be announced</div></div>
    <div class="card"><div class="label">CONTRACT</div><div class="stat">TBA</div><div class="label">Add after deployment</div></div>
  </div>
</div>
</section>

<!-- Live Market + Chart -->
<section id="market">
<div class="container">
  <div class="section-head">
    <div>
      <div class="eyebrow">Live Data</div>
      <h2>Market & Chart</h2>
    </div>
    <p class="sub">Top 10 cryptocurrencies + TRUMUXI price chart.</p>
  </div>

  <div class="live-grid">
    <!-- 10 Coins -->
    <div class="card coin-list">
      <div class="eyebrow" style="margin-bottom:15px">Top 10 Cryptocurrencies</div>
      
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">₿</div><div>Bitcoin <small style="color:var(--muted)">BTC</small></div></div>
        <div style="text-align:right"><div>$76,971</div><small class="up">+2.4%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">Ξ</div><div>Ethereum <small style="color:var(--muted)">ETH</small></div></div>
        <div style="text-align:right"><div>$2,420</div><small class="up">+3.1%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">◎</div><div>Solana <small style="color:var(--muted)">SOL</small></div></div>
        <div style="text-align:right"><div>$99.22</div><small class="up">+4.7%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">Ð</div><div>Dogecoin <small style="color:var(--muted)">DOGE</small></div></div>
        <div style="text-align:right"><div>$0.084</div><small class="up">+2.9%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">BNB</div><div>BNB <small style="color:var(--muted)">BNB</small></div></div>
        <div style="text-align:right"><div>$612</div><small class="up">+1.8%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">XRP</div><div>XRP <small style="color:var(--muted)">XRP</small></div></div>
        <div style="text-align:right"><div>$0.58</div><small style="color:var(--danger)">-0.7%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">ADA</div><div>Cardano <small style="color:var(--muted)">ADA</small></div></div>
        <div style="text-align:right"><div>$0.42</div><small class="up">+1.5%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">AVAX</div><div>Avalanche <small style="color:var(--muted)">AVAX</small></div></div>
        <div style="text-align:right"><div>$28.40</div><small class="up">+3.2%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">DOT</div><div>Polkadot <small style="color:var(--muted)">DOT</small></div></div>
        <div style="text-align:right"><div>$5.85</div><small class="up">+2.1%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-left"><div class="coin-icon">LINK</div><div>Chainlink <small style="color:var(--muted)">LINK</small></div></div>
        <div style="text-align:right"><div>$13.20</div><small class="up">+4.0%</small></div>
      </div>
    </div>

    <!-- Real Chart -->
    <div class="card">
      <div class="eyebrow" style="margin-bottom:10px">TRUMUXI Price Chart</div>
      <div style="display:flex;justify-content:space-between;margin-bottom:15px">
        <div style="font-size:22px;font-weight:800;color:var(--gold)">$0.01</div>
        <div class="up">+66% from start</div>
      </div>
      <div class="chart-box">
        <canvas id="tmxChart"></canvas>
      </div>
    </div>
  </div>
</div>
</section>

<!-- Tokenomics -->
<section id="tokenomics">
<div class="container">
  <div class="section-head">
    <div>
      <div class="eyebrow">Economy</div>
      <h2>Tokenomics</h2>
    </div>
    <p class="sub">Total Supply fixed at <b style="color:var(--gold)">21,000,000 TMX</b></p>
  </div>
  <div class="tokenomics">
    <div class="card">
      <div class="row"><span>Community & Ecosystem</span><b>40%</b></div><div class="bar"><div class="fill" style="width:40%"></div></div>
      <div class="row"><span>Liquidity</span><b>25%</b></div><div class="bar"><div class="fill" style="width:25%"></div></div>
      <div class="row"><span>Marketing</span><b>15%</b></div><div class="bar"><div class="fill" style="width:15%"></div></div>
      <div class="row"><span>Development</span><b>10%</b></div><div class="bar"><div class="fill" style="width:10%"></div></div>
      <div class="row"><span>Treasury / Reserve</span><b>10%</b></div><div class="bar"><div class="fill" style="width:10%"></div></div>
    </div>
    <div class="card">
      <div class="eyebrow">Supply</div>
      <h3 style="font-size:25px;margin-bottom:15px">21,000,000 TMX</h3>
      <p class="sub">Fixed total supply. No additional minting planned.</p>
      <br>
      <a class="btn primary" href="#community">Join the build</a>
    </div>
  </div>
</div>
</section>

<!-- Roadmap -->
<section id="roadmap">
<div class="container">
  <div class="section-head">
    <div>
      <div class="eyebrow">Mission</div>
      <h2>Roadmap</h2>
    </div>
    <p class="sub">A simple four-stage path from concept to a functioning crypto project.</p>
  </div>
  <div class="roadmap">
    <div class="card phase"><b>PHASE 01</b><h3>Foundation</h3><ul><li>✓ Brand identity</li><li>✓ Website concept</li><li>• Community channels</li><li>• Whitepaper</li></ul></div>
    <div class="card phase"><b>PHASE 02</b><h3>Build</h3><ul><li>• Choose blockchain</li><li>• Smart contract</li><li>• Token verification</li><li>• Security review</li></ul></div>
    <div class="card phase"><b>PHASE 03</b><h3>Launch</h3><ul><li>• Liquidity setup</li><li>• Explorer listing</li><li>• Market tracking</li><li>• Community campaign</li></ul></div>
    <div class="card phase"><b>PHASE 04</b><h3>Expansion</h3><ul><li>• Exchange applications</li><li>• Partnerships</li><li>• Products & utilities</li><li>• Global community</li></ul></div>
  </div>
</div>
</section>

<!-- Community -->
<section id="community">
<div class="container">
  <div class="cta">
    <div class="eyebrow">TRUMUXI COMMUNITY</div>
    <h2>The future has a name.</h2>
    <p class="sub" style="margin:15px auto 25px">Total Supply: <b style="color:var(--gold)">21,000,000 TMX</b> · Starting Price: $0.01</p>
    <div class="actions">
      <a class="btn primary" href="#" onclick="alert('Replace this with your official Telegram link');return false">Telegram</a>
      <a class="btn" href="#" onclick="alert('Replace this with your official X link');return false">X / Twitter</a>
      <a class="btn" href="#" onclick="alert('Replace this with your contract link');return false">Contract</a>
    </div>
  </div>
</div>
</section>
</main>

<footer>
<div class="container foot">
  <div>© 2026 TRUMUXI · Total Supply 21,000,000 TMX</div>
  <div>The Future Has A Name</div>
</div>
</footer>

<script>
// Smooth scroll
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click',e=>{
    const id=a.getAttribute('href');
    if(id && id!=="#"){
      const el=document.querySelector(id);
      if(el){e.preventDefault();el.scrollIntoView({behavior:'smooth'});}
    }
  });
});

// Real Chart
const ctx = document.getElementById('tmxChart').getContext('2d');
new Chart(ctx, {
  type: 'line',
  data: {
    labels: ['Start','1H','2H','3H','4H','5H','6H','7H','8H'],
    datasets: [{
      label: 'TMX Price',
      data: [0.006, 0.0072, 0.0081, 0.0089, 0.0085, 0.0093, 0.0098, 0.0096, 0.01],
      borderColor: '#ffd45a',
      backgroundColor: 'rgba(255, 212, 90, 0.12)',
      borderWidth: 3,
      tension: 0.4,
      fill: true,
      pointBackgroundColor: '#ffd45a',
      pointRadius: 4,
      pointHoverRadius: 6
    }]
  },
  options: {
    responsive: true,
    maintainAspectRatio: false,
    plugins: { legend: { display: false } },
    scales: {
      y: {
        grid: { color: 'rgba(255,255,255,0.06)' },
        ticks: { color: '#9da5bd' }
      },
      x: {
        grid: { color: 'rgba(255,255,255,0.06)' },
        ticks: { color: '#9da5bd' }
      }
    }
  }
});
</script>
</body>
</html>
