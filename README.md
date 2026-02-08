<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CloudVPS - Thuê VPS Giá Rẻ</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
body{background:#0f172a;color:#fff}
header{
    background:linear-gradient(135deg,#2563eb,#9333ea);
    padding:80px 20px;
    text-align:center;
}
header h1{font-size:42px;font-weight:700}
header p{margin-top:15px;font-size:18px;opacity:.9}
.btn{
    display:inline-block;
    margin-top:25px;
    padding:12px 30px;
    background:#fff;
    color:#000;
    border-radius:30px;
    font-weight:600;
    text-decoration:none;
    transition:.3s;
}
.btn:hover{transform:scale(1.05)}

.section{
    padding:70px 20px;
    text-align:center;
}
.section h2{font-size:32px;margin-bottom:40px}

.pricing{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
    max-width:1100px;
    margin:auto;
}
.card{
    background:#1e293b;
    padding:30px;
    border-radius:15px;
    transition:.3s;
}
.card:hover{transform:translateY(-10px)}
.price{
    font-size:30px;
    margin:20px 0;
    font-weight:700;
}
.card ul{
    list-style:none;
    margin:20px 0;
}
.card ul li{margin:10px 0;opacity:.8}

footer{
    background:#020617;
    padding:25px;
    text-align:center;
    font-size:14px;
    opacity:.7;
}
</style>
</head>
<body>

<header>
    <h1>CloudVPS</h1>
    <p>Thuê VPS tốc độ cao - SSD NVMe - Giá chỉ từ 99K/tháng</p>
    <a href="#pricing" class="btn">Xem Bảng Giá</a>
</header>

<section class="section" id="pricing">
    <h2>Bảng Giá VPS</h2>
    <div class="pricing">
        
        <div class="card">
            <h3>VPS Basic</h3>
            <div class="price">99.000đ</div>
            <ul>
                <li>1 CPU</li>
                <li>2GB RAM</li>
                <li>30GB SSD NVMe</li>
                <li>1TB Bandwidth</li>
            </ul>
            <a href="#" class="btn">Thuê Ngay</a>
        </div>

        <div class="card">
            <h3>VPS Pro</h3>
            <div class="price">199.000đ</div>
            <ul>
                <li>2 CPU</li>
                <li>4GB RAM</li>
                <li>60GB SSD NVMe</li>
                <li>3TB Bandwidth</li>
            </ul>
            <a href="#" class="btn">Thuê Ngay</a>
        </div>

        <div class="card">
            <h3>VPS Business</h3>
            <div class="price">399.000đ</div>
            <ul>
                <li>4 CPU</li>
                <li>8GB RAM</li>
                <li>120GB SSD NVMe</li>
                <li>Unlimited Bandwidth</li>
            </ul>
            <a href="#" class="btn">Thuê Ngay</a>
        </div>

    </div>
</section>

<footer>
© 2026 CloudVPS - Hosting & Cloud Solutions
</footer>

</body>
</html>
