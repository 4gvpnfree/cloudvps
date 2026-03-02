<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shop VPN</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
body{
    margin:0;
    font-family: Arial, Helvetica, sans-serif;
    background:#f2f3f7;
}

/* header */
.header{
    padding:15px;
    display:flex;
    align-items:center;
    gap:10px;
}

.menu-btn{
    font-size:22px;
    cursor:pointer;
}

/* product grid */
.container{
    padding:12px;
}

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:12px;
}

.card{
    background:linear-gradient(135deg,#2b2b2b,#3a3a3a);
    color:white;
    padding:18px;
    border-radius:14px;
    display:flex;
    align-items:center;
    gap:10px;
    font-weight:bold;
    box-shadow:0 4px 10px rgba(0,0,0,0.2);
}

.card.full{
    grid-column:span 2;
}

.card i{
    font-size:22px;
}

/* free vpn banner */
.banner{
    margin:16px 12px;
    padding:18px;
    border-radius:16px;
    color:white;
    font-size:22px;
    font-weight:bold;
    background:linear-gradient(90deg,#f6b100,#19a7ce);
    box-shadow:0 6px 14px rgba(0,0,0,0.25);
}

/* sidebar */
.sidebar{
    position:fixed;
    top:0;
    left:-260px;
    width:260px;
    height:100%;
    background:white;
    transition:0.3s;
    z-index:999;
    box-shadow:2px 0 10px rgba(0,0,0,0.2);
    padding:15px;
}

.sidebar.active{
    left:0;
}

.side-item{
    padding:14px 10px;
    border-bottom:1px solid #eee;
    display:flex;
    align-items:center;
    gap:10px;
    color:#333;
}

/* bottom nav */
.bottom-nav{
    position:fixed;
    bottom:0;
    left:0;
    width:100%;
    background:white;
    display:flex;
    justify-content:space-around;
    padding:10px 0;
    box-shadow:0 -2px 10px rgba(0,0,0,0.15);
}

.bottom-nav div{
    text-align:center;
    font-size:12px;
    color:#555;
}

.bottom-nav i{
    display:block;
    font-size:18px;
    margin-bottom:4px;
}
</style>
</head>

<body>

<!-- SIDEBAR -->
<div class="sidebar" id="sidebar">
    <div class="side-item"><i class="fa fa-home"></i> Trang chủ</div>
    <div class="side-item"><i class="fa fa-cart-shopping"></i> Sản phẩm</div>
    <div class="side-item"><i class="fa fa-building-columns"></i> Nạp tiền</div>
    <div class="side-item"><i class="fa fa-clock-rotate-left"></i> Lịch sử</div>
    <div class="side-item"><i class="fa fa-right-from-bracket"></i> Đăng xuất</div>
</div>

<!-- HEADER -->
<div class="header">
    <i class="fa fa-bars menu-btn" onclick="toggleMenu()"></i>
    <b>Shop Data VPN</b>
</div>

<!-- PRODUCTS -->
<div class="container">
    <div class="grid">

        <div class="card">
            <i class="fa fa-cart-shopping"></i>
            Tất cả sản phẩm
        </div>

        <div class="card">
            <i class="fa fa-shield-halved"></i>
            Free VPN
        </div>

        <div class="card full">
            <i class="fa fa-shield"></i>
            VPN NDP (NO DATA PLAN)
        </div>

        <div class="card full">
            <i class="fa-brands fa-tiktok"></i>
            VPN TDP (TIKTOK DATA PLAN)
        </div>

        <div class="card">
            <i class="fa-brands fa-apple"></i>
            ID Apple Free
        </div>

        <div class="card">
            <i class="fa fa-crown"></i>
            Capcut Pro
        </div>

        <div class="card full">
            <i class="fa-brands fa-youtube"></i>
            Youtube Premium
        </div>

        <div class="card full">
            <i class="fa fa-film"></i>
            Netflix Premium
        </div>

        <div class="card">
            <i class="fa fa-robot"></i>
            Chat GPT Plus
        </div>

        <div class="card">
            <i class="fa fa-palette"></i>
            Canva Pro
        </div>

    </div>
</div>

<div class="banner">
    🔥 Free VPN
</div>

<!-- BOTTOM NAV -->
<div class="bottom-nav">
    <div><i class="fa fa-home"></i>Trang chủ</div>
    <div><i class="fa fa-list"></i>Sản phẩm</div>
    <div><i class="fa fa-building-columns"></i>Nạp tiền</div>
    <div><i class="fa fa-cart-shopping"></i>Đơn hàng</div>
    <div><i class="fa fa-user"></i>Thông tin</div>
</div>

<script>
function toggleMenu(){
    document.getElementById("sidebar").classList.toggle("active");
}
</script>

</body>
</html>
