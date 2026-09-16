<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TRUMUXI - The Future Crypto Coin</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0a0a0a;
      color: #fff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }

    /* Header */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 20px;
      background: rgba(0, 0, 0, 0.85);
      border-bottom: 1px solid #333;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 1.5rem;
      font-weight: bold;
      color: #ffd700;
    }

    .logo-circle {
      width: 40px;
      height: 40px;
      background: linear-gradient(135deg, #ffd700, #ffaa00);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #000;
      font-weight: bold;
      font-size: 1.4rem;
    }

    nav a {
      color: #ccc;
      text-decoration: none;
      margin: 0 12px;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #ffd700;
    }

    .tmx-btn {
      background: #ffd700;
      color: #000;
      padding: 8px 16px;
      border-radius: 20px;
      font-weight: bold;
      text-decoration: none;
    }

    /* Hero */
    .hero {
      text-align: center;
      padding: 50px 20px 30px;
      background: radial-gradient(ellipse at center, #1a1a2e 0%, #0a0a0a 70%);
    }

    .hero h1 {
      font-size: 3.2rem;
      color: #ffd700;
      text-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
      margin-bottom: 8px;
    }

    .hero .tagline {
      font-size: 1.3rem;
      color: #ffd700;
      margin-bottom: 4px;
    }

    .hero .subtitle {
      color: #aaa;
      margin-bottom: 25px;
    }

    .explore-btn {
      background: linear-gradient(90deg, #ffd700, #ffaa00);
      color: #000;
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      font-size: 1.1rem;
      font-weight: bold;
      cursor: pointer;
    }

    /* Live Market - 10 Coins */
    .live-market {
      background: rgba(20, 20, 30, 0.95);
      border: 1px solid #333;
      border-radius: 16px;
      padding: 20px;
      margin: 30px auto;
      max-width: 420px;
    }

    .live-market h3 {
      color: #ffd700;
      margin-bottom: 15px;
      font-size: 1.15rem;
    }

    .coin-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 9px 0;
      border-bottom: 1px solid #222;
    }

    .coin-row:last-child {
      border-bottom: none;
    }

    .coin-info {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .coin-icon {
      width: 26px;
      height: 26px;
      border-radius: 50%;
      background: #333;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      font-weight: bold;
    }

    .green { color: #00ff88; }
    .red { color: #ff5555; }

    /* Leaders */
    .leaders {
      display: flex;
      justify-content: center;
      gap: 18px;
      flex-wrap: wrap;
      margin: 35px 0;
    }

    .leader-card {
      text-align: center;
      width: 130px;
    }

    .leader-img {
      width: 90px;
      height: 90px;
      border-radius: 50%;
      border: 3px solid #ffd700;
      margin: 0 auto 8px;
      background: #222;
    }

    .leader-name {
      font-weight: bold;
      color: #ffd700;
    }

    .leader-token {
      font-size: 0.8rem;
      color: #aaa;
    }

    /* Price Card */
    .price-card {
      background: linear-gradient(145deg, #1a1a2e, #0f0f1a);
      border: 2px solid #ffd700;
      border-radius: 20px;
      padding: 25px;
      text-align: center;
      max-width: 300px;
      margin: 0 auto 40px;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.25);
    }

    .price-card .coin {
      font-size: 2.8rem;
      color: #ffd700;
      margin-bottom: 8px;
    }

    .price-card h2 {
      color: #ffd700;
      margin-bottom: 4px;
    }

    .price-card .price {
      font-size: 2rem;
      font-weight: bold;
      margin: 10px 0 5px;
    }

    .price-card .supply {
      color: #ffd700;
      font-size: 0.95rem;
      margin-top: 8px;
      font-weight: 600;
    }

    .price-card .start {
      color: #aaa;
      font-size: 0.9rem;
    }

    /* Bottom Grid */
    .bottom-grid {
      display: grid;
      grid-template-columns: 1fr 1.6fr 1fr;
      gap: 20px;
      margin: 40px 0;
    }

    @media (max-width: 900px) {
      .bottom-grid {
        grid-template-columns: 1fr;
      }
      nav { display: none; }
    }

    .card {
      background: rgba(20, 20, 30, 0.95);
      border: 1px solid #333;
      border-radius: 15px;
      padding: 20px;
    }

    .card h3 {
      color: #ffd700;
      margin-bottom: 15px;
      font-size: 1.1rem;
    }

    .social-btn {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: none;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
      text-align: center;
      text-decoration: none;
      color: #fff;
    }

    .telegram { background: #0088cc; }
    .twitter { background: #1da1f2; }

    .chart-box {
      height: 220px;
      position: relative;
    }

    .visitors {
      text-align: center;
      font-size: 2.4rem;
      color: #ffd700;
      font-weight: bold;
      margin-top: 20px;
    }

    .visitors span {
      display: block;
      font-size: 0.9rem;
      color: #aaa;
      font-weight: normal;
      margin-top: 5px;
    }

    footer {
      text-align: center;
      padding: 30px;
      border-top: 1px solid #333;
      color: #666;
      margin-top: 40px;
    }

    footer .socials a {
      color: #ffd700;
      margin: 0 12px;
      font-size: 1.3rem;
      text-decoration: none;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">
      <div class="logo-circle">T</div>
      TRUMUXI
    </div>
    <nav>
      <a href="#">Home</a>
      <a href="#">Market</a>
      <a href="#">Chart</a>
      <a href="#">Community</a>
    </nav>
    <a href="#" class="tmx-btn">TMX</a>
  </header>

  <!-- Hero -->
  <section class="hero">
    <h1>TRUMUXI</h1>
    <p class="tagline">Four Leaders. One Vision.</p>
    <p class="subtitle">The Future Crypto Coin</p>
    <button class="explore-btn">Explore →</button>

    <!-- Live Market - 10 Coins -->
    <div class="live-market">
      <h3>📈 Live Crypto Market</h3>

      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">₿</div><div>Bitcoin <small>BTC</small></div></div>
        <div><div>$76,971</div><small class="green">+2.4%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">Ξ</div><div>Ethereum <small>ETH</small></div></div>
        <div><div>$2,420</div><small class="green">+3.1%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">◎</div><div>Solana <small>SOL</small></div></div>
        <div><div>$99.22</div><small class="green">+4.7%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">Ð</div><div>Dogecoin <small>DOGE</small></div></div>
        <div><div>$0.084</div><small class="green">+2.9%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">BNB</div><div>BNB <small>BNB</small></div></div>
        <div><div>$612</div><small class="green">+1.8%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">XRP</div><div>XRP <small>XRP</small></div></div>
        <div><div>$0.58</div><small class="red">-0.7%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">ADA</div><div>Cardano <small>ADA</small></div></div>
        <div><div>$0.42</div><small class="green">+1.5%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">AVAX</div><div>Avalanche <small>AVAX</small></div></div>
        <div><div>$28.40</div><small class="green">+3.2%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">DOT</div><div>Polkadot <small>DOT</small></div></div>
        <div><div>$5.85</div><small class="green">+2.1%</small></div>
      </div>
      <div class="coin-row">
        <div class="coin-info"><div class="coin-icon">LINK</div><div>Chainlink <small>LINK</small></div></div>
        <div><div>$13.20</div><small class="green">+4.0%</small></div>
      </div>
    </div>
  </section>

  <div class="container">
    <!-- Leaders -->
    <div class="leaders">
      <div class="leader-card">
        <div class="leader-img" style="background: linear-gradient(45deg, #c41e3a, #002868);"></div>
        <div class="leader-name">Trump</div>
        <div class="leader-token">(TRUMP)</div>
      </div>
      <div class="leader-card">
        <div class="leader-img" style="background: linear-gradient(45deg, #0033a0, #d52b1e);"></div>
        <div class="leader-name">Putin</div>
        <div class="leader-token">(SOLANA)</div>
      </div>
      <div class="leader-card">
        <div class="leader-img" style="background: linear-gradient(45deg, #c2a633, #000);"></div>
        <div class="leader-name">Elon</div>
        <div class="leader-token">(DOGECOIN)</div>
      </div>
      <div class="leader-card">
        <div class="leader-img" style="background: linear-gradient(45deg, #de2910, #ffde00);"></div>
        <div class="leader-name">China</div>
        <div class="leader-token">(VECHAIN)</div>
      </div>
    </div>

    <!-- Price Card -->
    <div class="price-card">
      <div class="coin">Ⓣ</div>
      <h2>TRUMUXI</h2>
      <div>TMX</div>
      <div class="price">$0.01</div>
      <div class="start">Starting Price</div>
      <div class="supply">Total Supply: 21,000,000 TMX</div>
      <div style="margin-top:10px; color:#ffd700; font-size:0.95rem;">The Future Has A Name</div>
    </div>

    <!-- Bottom Grid -->
    <div class="bottom-grid">
      <!-- Community -->
      <div class="card">
        <h3>🌐 TRUMUXI Community</h3>
        <p style="color:#aaa; margin-bottom:15px; font-size:0.95rem;">Join the future crypto movement.</p>
        <a href="#" class="social-btn telegram">✈️ Telegram</a>
        <a href="#" class="social-btn twitter">𝕏 X / Twitter</a>
        <p style="margin-top:15px; color:#888; font-size:0.9rem;">7 People visited TRUMUXI</p>
      </div>

      <!-- Real Chart -->
      <div class="card">
        <h3>📊 TRUMUXI Price Chart</h3>
        <div class="chart-box">
          <canvas id="tmxChart"></canvas>
        </div>
      </div>

      <!-- Visitors -->
      <div class="card">
        <h3>👥 Website Visitors</h3>
        <div class="visitors">
          1,248
          <span>People visited TRUMUXI</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <p>© 2026 TRUMUXI — Total Supply 21,000,000 TMX</p>
    <p>The Future Has A Name</p>
    <div class="socials">
      <a href="#">✈️</a>
      <a href="#">𝕏</a>
      <a href="#">🌐</a>
    </div>
  </footer>

  <script>
    // Real Chart with Chart.js
    const ctx = document.getElementById('tmxChart').getContext('2d');
    new Chart(ctx, {
      type: 'line',
      data: {
        labels: ['Start', '1H', '2H', '3H', '4H', '5H', '6H', '7H', '8H'],
        datasets: [{
          label: 'TMX Price ($)',
          data: [0.006, 0.0075, 0.0082, 0.0091, 0.0088, 0.0095, 0.0102, 0.0098, 0.01],
          borderColor: '#ffd700',
          backgroundColor: 'rgba(255, 215, 0, 0.15)',
          borderWidth: 3,
          tension: 0.4,
          fill: true,
          pointBackgroundColor: '#ffd700',
          pointRadius: 4,
          pointHoverRadius: 6
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: { display: false }
        },
        scales: {
          y: {
            beginAtZero: false,
            grid: { color: '#222' },
            ticks: { color: '#aaa' }
          },
          x: {
            grid: { color: '#222' },
            ticks: { color: '#aaa' }
          }
        }
      }
    });
  </script>
</body>
</html>
