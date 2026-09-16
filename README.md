<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TRUMUXI - The Future Crypto Coin</title>
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
      background: rgba(0, 0, 0, 0.8);
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
      margin: 0 15px;
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

    /* Hero Section */
    .hero {
      text-align: center;
      padding: 60px 20px;
      background: radial-gradient(ellipse at center, #1a1a2e 0%, #0a0a0a 70%);
      position: relative;
      overflow: hidden;
    }

    .hero h1 {
      font-size: 3.5rem;
      color: #ffd700;
      text-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
      margin-bottom: 10px;
    }

    .hero .tagline {
      font-size: 1.4rem;
      color: #ffd700;
      margin-bottom: 5px;
    }

    .hero .subtitle {
      color: #aaa;
      margin-bottom: 30px;
    }

    .explore-btn {
      background: linear-gradient(90deg, #ffd700, #ffaa00);
      color: #000;
      padding: 12px 30px;
      border: none;
      border-radius: 30px;
      font-size: 1.1rem;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .explore-btn:hover {
      transform: scale(1.05);
    }

    /* Live Market */
    .live-market {
      background: rgba(20, 20, 30, 0.9);
      border: 1px solid #333;
      border-radius: 15px;
      padding: 20px;
      margin: 30px auto;
      max-width: 350px;
    }

    .live-market h3 {
      color: #ffd700;
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .coin-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 0;
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
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #333;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8rem;
    }

    .green { color: #00ff88; }
    .red { color: #ff4444; }

    /* Leaders */
    .leaders {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin: 40px 0;
    }

    .leader-card {
      text-align: center;
      width: 140px;
    }

    .leader-img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 3px solid #ffd700;
      object-fit: cover;
      margin-bottom: 10px;
      background: #222;
    }

    .leader-name {
      font-weight: bold;
      color: #ffd700;
    }

    .leader-token {
      font-size: 0.85rem;
      color: #aaa;
    }

    /* Price Card */
    .price-card {
      background: linear-gradient(145deg, #1a1a2e, #0f0f1a);
      border: 2px solid #ffd700;
      border-radius: 20px;
      padding: 25px;
      text-align: center;
      max-width: 280px;
      margin: 0 auto 40px;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.2);
    }

    .price-card .coin {
      font-size: 3rem;
      color: #ffd700;
      margin-bottom: 10px;
    }

    .price-card h2 {
      color: #ffd700;
      margin-bottom: 5px;
    }

    .price-card .price {
      font-size: 2rem;
      font-weight: bold;
      margin: 10px 0;
    }

    .price-card .start {
      color: #aaa;
      font-size: 0.9rem;
    }

    /* Bottom Sections */
    .bottom-grid {
      display: grid;
      grid-template-columns: 1fr 1.5fr 1fr;
      gap: 20px;
      margin: 40px 0;
    }

    @media (max-width: 900px) {
      .bottom-grid {
        grid-template-columns: 1fr;
      }
    }

    .card {
      background: rgba(20, 20, 30, 0.9);
      border: 1px solid #333;
      border-radius: 15px;
      padding: 20px;
    }

    .card h3 {
      color: #ffd700;
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 8px;
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

    .chart-placeholder {
      height: 180px;
      background: #111;
      border-radius: 10px;
      display: flex;
      align-items: flex-end;
      padding: 10px;
      gap: 8px;
    }

    .bar {
      flex: 1;
      background: linear-gradient(to top, #ffd700, #ffaa00);
      border-radius: 4px 4px 0 0;
      transition: height 0.5s;
    }

    .visitors {
      text-align: center;
      font-size: 2.5rem;
      color: #ffd700;
      font-weight: bold;
    }

    .visitors span {
      display: block;
      font-size: 0.9rem;
      color: #aaa;
      font-weight: normal;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 30px;
      border-top: 1px solid #333;
      color: #666;
      margin-top: 40px;
    }

    footer .socials {
      margin-top: 15px;
    }

    footer .socials a {
      color: #ffd700;
      margin: 0 10px;
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

    <!-- Live Market -->
    <div class="live-market">
      <h3>📈 Live Crypto Market</h3>
      <div class="coin-row">
        <div class="coin-info">
          <div class="coin-icon">₿</div>
          <div>
            <div>Bitcoin</div>
            <small>BTC</small>
          </div>
        </div>
        <div>
          <div>$76,971</div>
          <small class="green">+2.4%</small>
        </div>
      </div>
      <div class="coin-row">
        <div class="coin-info">
          <div class="coin-icon">Ξ</div>
          <div>
            <div>Ethereum</div>
            <small>ETH</small>
          </div>
        </div>
        <div>
          <div>$2,420.03</div>
          <small class="green">+3.1%</small>
        </div>
      </div>
      <div class="coin-row">
        <div class="coin-info">
          <div class="coin-icon">◎</div>
          <div>
            <div>Solana</div>
            <small>SOL</small>
          </div>
        </div>
        <div>
          <div>$99.22</div>
          <small class="green">+4.7%</small>
        </div>
      </div>
      <div class="coin-row">
        <div class="coin-info">
          <div class="coin-icon">Ð</div>
          <div>
            <div>Dogecoin</div>
            <small>DOGE</small>
          </div>
        </div>
        <div>
          <div>$0.083927</div>
          <small class="green">+2.9%</small>
        </div>
      </div>
    </div>
  </section>

  <!-- Leaders -->
  <div class="container">
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
      <div style="margin-top:10px; color:#ffd700;">The Future Has A Name</div>
    </div>

    <!-- Bottom Grid -->
    <div class="bottom-grid">
      <!-- Community -->
      <div class="card">
        <h3>🌐 TRUMUXI Community</h3>
        <p style="color:#aaa; margin-bottom:15px;">Join the future crypto movement.</p>
        <a href="#" class="social-btn telegram">✈️ Telegram</a>
        <a href="#" class="social-btn twitter">𝕏 X / Twitter</a>
        <p style="margin-top:15px; color:#888; font-size:0.9rem;">7 People visited TRUMUXI</p>
      </div>

      <!-- Chart -->
      <div class="card">
        <h3>📊 TRUMUXI Analytics</h3>
        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
          <span>TRUMUXI Price Chart</span>
          <span style="color:#ffd700;">TMX $0.01</span>
        </div>
        <div class="chart-placeholder">
          <div class="bar" style="height:30%"></div>
          <div class="bar" style="height:45%"></div>
          <div class="bar" style="height:55%"></div>
          <div class="bar" style="height:70%"></div>
          <div class="bar" style="height:60%"></div>
          <div class="bar" style="height:75%"></div>
          <div class="bar" style="height:85%"></div>
          <div class="bar" style="height:95%"></div>
        </div>
        <div style="display:flex; justify-content:space-between; margin-top:8px; font-size:0.8rem; color:#666;">
          <span>Start</span><span>1H</span><span>2H</span><span>3H</span><span>4H</span>
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
    <p>© 2026 TRUMUXI</p>
    <p>The Future Has A Name</p>
    <div class="socials">
      <a href="#">✈️</a>
      <a href="#">𝕏</a>
      <a href="#">🌐</a>
    </div>
  </footer>

</body>
</html>
