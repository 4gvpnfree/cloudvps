<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shop Data VPN Pro</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
:root{
  --dark:#2b2b2b;
  --dark2:#3a3a3a;
  --primary:#19a7ce;
}

body{
  margin:0;
  font-family:Arial,Helvetica,sans-serif;
  background:#f2f3f7;
}

.header{
  padding:15px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.menu-btn{font-size:22px;cursor:pointer}
.user-btn{font-size:20px;cursor:pointer}

.container{padding:12px 12px 80px}

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}

.card{
  background:linear-gradient(135deg,var(--dark),var(--dark2));
  color:white;
  padding:18px;
  border-radius:16px;
  display:flex;
  align-items:center;
  gap:10px;
  font-weight:bold;
  box-shadow:0 6px 14px rgba(0,0,0,.25);
  cursor:pointer;
  transition:.2s;
}

.card:hover{transform:scale(.97)}
.card.full{grid-column:span 2}
.card i{font-size:22px}

.banner{
  margin:16px 12px;
  padding:18px;
  border-radius:16px;
  color:white;
  font-size:22px;
  font-weight:bold;
  background:linear-gradient(90deg,#f6b100,#19a7ce);
  box-shadow:0 6px 14px rgba(0,0,0,.25);
}

/* sidebar */
.sidebar{
  position:fixed;
  top:0;
  left:-270px;
  width:270px;
  height:100%;
  background:white;
  transition:.3s;
  z-index:999;
  box-shadow:2px 0 10px rgba(0,0,0,.2);
  padding:15px;
}
.sidebar.active{left:0}
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
  box-shadow:0 -2px 10px rgba(0,0,0,.15);
}
.bottom-nav div{text-align:center;font-size:12px;color:#555}
.bottom-nav i{display:block;font-size:18px;margin-bottom:4px}

/* modal */
.modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.45);
  display:none;
  align-items:center;
  justify-content:center;
  z-index:2000;
}
.modal.active{display:flex}
.modal-box{
  background:white;
  width:90%;
  max-width:380px;
  border-radius:18px;
  padding:20px;
}
.modal-box h3{margin-top:0}

.input{
  width:100%;
  padding:12px;
  margin:6px 0;
  border-radius:10px;
  border:1px solid #ddd;
}

.btn{
  width:100%;
  padding:12px;
  border:none;
  border-radius:12px;
  background:var(--primary);
  color:white;
  font-weight:bold;
  margin-top:8px;
}

.toast{
  position:fixed;
  top:20px;
  left:50%;
  transform:translateX(-50%);
  background:#333;
  color:#fff;
  padding:10px 16px;
  border-radius:20px;
  display:none;
  z-index:3000;
}
</style>
</head>
<body>

<div class="toast" id="toast">Đã thêm vào giỏ</div>

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
  <b>Shop Data VPN Pro</b>
  <i class="fa fa-user user-btn" onclick="openLogin()"></i>
</div>

<!-- PRODUCTS -->
<div class="container">
  <div class="grid" id="productGrid"></div>
</div>

<div class="banner">🔥 Free VPN tốc độ cao</div>

<!-- BOTTOM NAV -->
<div class="bottom-nav">
  <div><i class="fa fa-home"></i>Trang chủ</div>
  <div><i class="fa fa-list"></i>Sản phẩm</div>
  <div><i class="fa fa-building-columns"></i>Nạp tiền</div>
  <div><i class="fa fa-cart-shopping"></i>Đơn hàng</div>
  <div><i class="fa fa-user"></i>Tài khoản</div>
</div>

<!-- LOGIN MODAL -->
<div class="modal" id="loginModal">
  <div class="modal-box">
    <h3>Đăng nhập</h3>
    <input class="input" placeholder="Tài khoản" id="user">
    <input class="input" type="password" placeholder="Mật khẩu" id="pass">
    <button class="btn" onclick="login()">Đăng nhập</button>
  </div>
</div>

<script>
const products=[
  {name:"VPN NDP (NO DATA PLAN)",icon:"fa-shield",full:true},
  {name:"VPN TDP (TIKTOK DATA PLAN)",icon:"fa-tiktok",full:true},
  {name:"ID Apple Free",icon:"fa-apple"},
  {name:"Capcut Pro",icon:"fa-crown"},
  {name:"Youtube Premium",icon:"fa-youtube",full:true},
  {name:"Netflix Premium",icon:"fa-film",full:true},
  {name:"Chat GPT Plus",icon:"fa-robot"},
  {name:"Canva Pro",icon:"fa-palette"}
];

const grid=document.getElementById("productGrid");
products.forEach(p=>{
  const div=document.createElement("div");
  div.className="card"+(p.full?" full":"");
  div.innerHTML=`<i class="fa ${p.icon}"></i>${p.name}`;
  div.onclick=()=>addCart(p.name);
  grid.appendChild(div);
});

function toggleMenu(){
  sidebar.classList.toggle("active");
}

function openLogin(){
  loginModal.classList.add("active");
}

function login(){
  const u=user.value.trim();
  const p=pass.value.trim();
  if(!u||!p) return alert("Nhập đầy đủ");
  localStorage.setItem("user",u);
  loginModal.classList.remove("active");
  showToast("Đăng nhập thành công");
}

function addCart(name){
  showToast("Đã chọn: "+name);
}

function showToast(msg){
  toast.innerText=msg;
  toast.style.display="block";
  setTimeout(()=>toast.style.display="none",2000);
}

window.onclick=e=>{
  if(e.target===loginModal) loginModal.classList.remove("active");
};
</script>

</body>
</html>
