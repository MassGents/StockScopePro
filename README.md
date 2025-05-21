# StockScopePro
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>StockScope Pro</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f172a;
      --card: #1e293b;
      --accent: #3b82f6;
      --text: #e2e8f0;
      --muted: #94a3b8;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Inter', sans-serif;
    }
    body {
      background-color: var(--bg);
      color: var(--text);
      padding: 2rem;
    }
    header {
      text-align: center;
      margin-bottom: 2rem;
    }
    h1 {
      color: var(--accent);
      font-size: 2.5rem;
      font-weight: 600;
    }
    nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1rem;
      margin-bottom: 2rem;
    }
    nav a {
      color: var(--text);
      text-decoration: none;
      padding: 0.5rem 1rem;
      background-color: var(--card);
      border-radius: 8px;
      transition: 0.3s;
    }
    nav a:hover {
      background-color: var(--accent);
      color: #fff;
    }
    .section {
      display: none;
      animation: fadeIn 0.3s ease-in-out;
    }
    .active {
      display: block;
    }
    .card {
      background-color: var(--card);
      padding: 1rem 1.5rem;
      border-radius: 10px;
      margin-bottom: 1.5rem;
    }
    h2 {
      margin-bottom: 1rem;
      color: var(--accent);
    }
    p {
      color: var(--muted);
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

<header>
  <h1>StockScope Pro</h1>
</header>

<nav>
  <a href="#" onclick="showSection('prices')">Prices</a>
  <a href="#" onclick="showSection('news')">News</a>
  <a href="#" onclick="showSection('portfolio')">Portfolio</a>
  <a href="#" onclick="showSection('alerts')">Alerts</a>
  <a href="#" onclick="showSection('recommendations')">Recommendations</a>
  <a href="#" onclick="showSection('about')">About</a>
</nav>

<section id="prices" class="section active">
  <div class="card">
    <h2>Live Stock Prices</h2>
    <p>This will show real-time stock data from all markets. Coming soon!</p>
  </div>
</section>

<section id="news" class="section">
  <div class="card">
    <h2>Market News</h2>
    <p>This will show the latest financial news using NewsAPI. Coming soon!</p>
  </div>
</section>

<section id="portfolio" class="section">
  <div class="card">
    <h2>My Portfolio</h2>
    <p>You’ll be able to enter stocks you own and see total performance. Coming soon!</p>
  </div>
</section>

<section id="alerts" class="section">
  <div class="card">
    <h2>Price Alerts</h2>
    <p>Track price changes and set alert triggers. Coming soon!</p>
  </div>
</section>

<section id="recommendations" class="section">
  <div class="card">
    <h2>Smart Recommendations</h2>
    <p>We’ll recommend stocks to watch based on trends and momentum. Coming soon!</p>
  </div>
</section>

<section id="about" class="section">
  <div class="card">
    <h2>About StockScope</h2>
    <p>StockScope Pro helps you stay informed, track stocks, and invest smarter — all in one place.</p>
  </div>
</section>

<script>
  function showSection(id) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }
</script>

</body>
</html>
