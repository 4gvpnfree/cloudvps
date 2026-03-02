<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shop Tài Khoản Premium</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: #0f172a;
      color: #fff;
    }
    header {
      background: linear-gradient(90deg, #6366f1, #22c55e);
      padding: 16px;
      text-align: center;
      font-size: 22px;
      font-weight: bold;
    }
    .container {
      max-width: 1100px;
      margin: auto;
      padding: 20px;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }
    .card {
      background: #1e293b;
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
      transition: 0.25s;
    }
    .card:hover {
      transform: translateY(-5px);
    }
    .card h3 {
      margin-top: 0;
    }
    .price {
      font-size: 22px;
      color: #22c55e;
      font-weight: bold;
      margin: 10px 0;
    }
    .btn {
      display: block;
      text-align: center;
      padding: 10px;
      border-radius: 10px;
      background: #6366f1;
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: 0.2s;
    }
    .btn:hover {
      background: #4f46e5;
    }
    footer {
      text-align: center;
      padding: 20px;
      opacity: 0.7;
      font-size: 14px;
    }
    .topbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
      flex-wrap: wrap;
      gap: 10px;
    }
    input {
      padding: 10px;
      border-radius: 8px;
      border: none;
      width: 250px;
    }
  </style>
</head>
<body>

<header>
  🚀 Shop Tài Khoản Premium
</header>

<div class="container">
  <div class="topbar">
    <div><i class="fa-solid fa-shield"></i> Tài khoản uy tín • Giao tự động</div>
    <input type="text" id="search" placeholder="Tìm sản phẩm..." />
  </div>

  <div class="grid" id="productList">

    <div class="card" data-name="youtube premium">
      <h3><i class="fa-brands fa-youtube"></i> YouTube Premium</h3>
      <div>Không quảng cáo • Xem nền</div>
      <div class="price">29.000đ / tháng</div>
      <a class="btn" href="#" onclick="buy('YouTube Premium')">Mua ngay</a>
    </div>

    <div class="card" data-name="netflix">
      <h3><i class="fa-solid fa-film"></i> Netflix Premium</h3>
      <div>4K • Xem đa thiết bị</div>
      <div class="price">49.000đ / tháng</div>
      <a class="btn" href="#" onclick="buy('Netflix Premium')">Mua ngay</a>
    </div>

    <div class="card" data-name="chatgpt plus">
      <h3><i class="fa-solid fa-robot"></i> ChatGPT Plus</h3>
      <div>GPT-4 • Tốc độ cao</div>
      <div class="price">99.000đ / tháng</div>
      <a class="btn" href="#" onclick="buy('ChatGPT Plus')">Mua ngay</a>
    </div>

    <div class="card" data-name="canva pro">
      <h3><i class="fa-solid fa-palette"></i> Canva Pro</h3>
      <div>Thiết kế không giới hạn</div>
      <div class="price">39.000đ / tháng</div>
      <a class="btn" href="#" onclick="buy('Canva Pro')">Mua ngay</a>
    </div>

  </div>
</div>

<footer>
  © 2026 Shop Premium • Hỗ trợ Telegram/Zalo của bạn
</footer>

<script>
  function buy(product) {
    alert("Bạn đã chọn mua: " + product + "\nLiên hệ admin để nhận tài khoản.");
  }

  // tìm kiếm
  const search = document.getElementById('search');
  search.addEventListener('input', function() {
    const keyword = this.value.toLowerCase();
    document.querySelectorAll('.card').forEach(card => {
      const name = card.dataset.name;
      card.style.display = name.includes(keyword) ? 'block' : 'none';
    });
  });
</script>

</body>
</html>
