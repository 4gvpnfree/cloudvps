<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Buffet Bún Đậu 79K</title>
  <meta name="description" content="Buffet Bún Đậu 79K — Ngon sạch, phục vụ nhanh. Đặt bàn ngay!">

  <style>
    :root{
      --bg:#0b1020;
      --surface: rgba(255,255,255,.06);
      --surface2: rgba(255,255,255,.09);
      --line: rgba(255,255,255,.14);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.70);
      --shadow: 0 18px 55px rgba(0,0,0,.35);
      --radius: 18px;
      --max: 1120px;

      --a: #ffb703;     /* vàng ấm */
      --b: #fb7185;     /* hồng đỏ */
      --c: #22c55e;     /* xanh */
    }

    *{ box-sizing: border-box; }
    html{ scroll-behavior: smooth; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
      color: var(--text);
      background:
        radial-gradient(1100px 700px at 10% 15%, rgba(255,183,3,.18), transparent 58%),
        radial-gradient(900px 600px at 90% 15%, rgba(251,113,133,.18), transparent 58%),
        radial-gradient(900px 600px at 60% 90%, rgba(34,197,94,.16), transparent 60%),
        linear-gradient(180deg, #070a14 0%, var(--bg) 58%, #050712 100%);
      min-height:100vh;
      overflow-x:hidden;
    }
    a{ color: inherit; text-decoration:none; }
    button,input,textarea{ font-family: inherit; }

    /* Header */
    header{
      position: sticky;
      top:0;
      z-index: 1000;
      backdrop-filter: blur(14px);
      background: rgba(11,16,32,.60);
      border-bottom: 1px solid var(--line);
    }
    .nav{
      max-width: var(--max);
      margin: 0 auto;
      padding: 14px 16px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 12px;
    }
    .brand{
      display:flex;
      align-items:center;
      gap: 10px;
      font-weight: 900;
      letter-spacing: .2px;
    }

    /* Logo text */
    .logo-brand{
      display:flex;
      align-items:center;
      gap:8px;
      font-weight:900;
      font-size:20px;
      letter-spacing:-0.5px;
    }
    .brand-text{
      background: linear-gradient(90deg,#ffffff,#dbeafe);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .brand-price{
      padding:4px 10px;
      border-radius:8px;
      background: linear-gradient(135deg,#fbbf24,#fb7185);
      color:white;
      font-weight:900;
      box-shadow:0 6px 18px rgba(251,113,133,.4);
    }

    nav[aria-label="Điều hướng"]{
      display:flex;
      align-items:center;
      gap: 12px;
      color: var(--muted);
      font-weight: 800;
      font-size: 14px;
    }
    nav a{
      padding: 8px 10px;
      border-radius: 12px;
      transition: background .2s, color .2s;
    }
    nav a:hover{ background: rgba(255,255,255,.06); color: rgba(255,255,255,.92); }

    .actions{ display:flex; align-items:center; gap: 10px; }

    .btn{
      border: 1px solid var(--line);
      background: rgba(255,255,255,.04);
      color: rgba(255,255,255,.92);
      padding: 10px 12px;
      border-radius: 14px;
      font-weight: 900;
      font-size: 14px;
      cursor:pointer;
      transition: transform .15s, background .2s, border-color .2s, box-shadow .2s;
      display:inline-flex;
      align-items:center;
      gap: 8px;
    }
    .btn:hover{
      background: rgba(255,255,255,.07);
      border-color: rgba(255,255,255,.20);
      transform: translateY(-1px);
    }
    .btn.primary{
      border: none;
      background: linear-gradient(135deg, var(--a), var(--b));
      box-shadow: 0 18px 55px rgba(251,113,133,.12);
    }
    .btn.primary:hover{ box-shadow: 0 22px 65px rgba(251,113,133,.16); }

    .hamburger{
      display:none;
      width: 42px;
      height: 42px;
      border-radius: 14px;
      border: 1px solid var(--line);
      background: rgba(255,255,255,.04);
      cursor:pointer;
      align-items:center;
      justify-content:center;
      gap: 5px;
      flex-direction: column;
    }
    .hamburger span{
      width: 18px; height: 2px;
      background: rgba(255,255,255,.85);
      border-radius: 2px;
    }

    /* Drawer */
    .drawer{
      position: fixed; inset: 0;
      background: rgba(0,0,0,.55);
      display:none;
      z-index: 2000;
    }
    .drawer.open{ display:block; }
    .panel{
      position:absolute;
      right: 12px; top: 12px;
      width: min(92vw, 360px);
      background: rgba(15,20,40,.92);
      border: 1px solid rgba(255,255,255,.12);
      border-radius: 18px;
      box-shadow: var(--shadow);
      padding: 14px;
      backdrop-filter: blur(16px);
    }
    .panel .row{
      display:flex; align-items:center; justify-content:space-between;
      gap: 10px; margin-bottom: 10px;
    }
    .panel a{
      display:block;
      padding: 12px 12px;
      border-radius: 14px;
      color: rgba(255,255,255,.90);
      font-weight: 900;
      border: 1px solid transparent;
    }
    .panel a:hover{
      background: rgba(255,255,255,.06);
      border-color: rgba(255,255,255,.12);
    }
    .logo-nav span{
      background: linear-gradient(90deg,#fbbf24,#fb7185);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    /* Layout */
    .wrap{ max-width: var(--max); margin: 0 auto; padding: 0 16px; }
    .section{ padding: 60px 0; }
    .grid{ display:grid; gap: 16px; }

    .reveal{
      opacity:0;
      transform: translateY(10px);
      transition: opacity .55s ease, transform .55s ease;
    }
    .reveal.show{ opacity:1; transform: translateY(0); }

    /* Hero */
    .hero{ padding: 58px 0 30px; }
    .hero-grid{
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 18px;
      align-items:center;
    }
    .badge{
      display:inline-flex;
      align-items:center;
      gap: 10px;
      padding: 8px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.04);
      color: rgba(255,255,255,.82);
      font-weight: 900;
      font-size: 13px;
    }
    .dot{
      width: 9px; height: 9px;
      border-radius: 99px;
      background: var(--c);
      box-shadow: 0 0 0 6px rgba(34,197,94,.16);
    }

    h1{
      font-size: 45px;
      font-weight: 800;
      line-height: 1.05;
      letter-spacing: -1px;
      background: linear-gradient(90deg,#ffffff,#e0e7ff,#c7d2fe);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 10px 40px rgba(59,130,246,0.25);
      margin: 14px 0 10px;
    }

    .lead{
      margin: 0 0 18px;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.75;
      max-width: 56ch;
    }
    .hero-actions{ display:flex; gap: 10px; flex-wrap: wrap; }
    .mini{ margin-top: 12px; color: rgba(255,255,255,.62); font-size: 13px; }

    /* Rating badge */
    .rating-badge{
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 10px 14px;
      margin-top: 14px;
      border-radius: 999px;
      background: rgba(255,255,255,.06);
      border: 1px solid rgba(255,255,255,.10);
      backdrop-filter: blur(10px);
      color: rgba(255,255,255,.92);
      font-size: 14px;
    }
    .rating-badge b{ color:#fff; }
    .rating-badge .star{
      width: 22px;
      height: 22px;
      display: grid;
      place-items: center;
      border-radius: 999px;
      background: rgba(251,191,36,.16);
    }
    .rating-badge .dot{
      opacity: .6;
      box-shadow: none;
      background: transparent;
      width: auto;
      height: auto;
    }

    /* Hero contact pills */
    .hero-contact{
      display:flex;
      align-items:center;
      flex-wrap:wrap;
      gap:12px;
      margin-top:16px;
    }
    .pill{
      display:inline-flex;
      align-items:center;
      gap:6px;
      padding:8px 14px;
      border-radius:999px;
      background: rgba(255,255,255,.07);
      border:1px solid rgba(255,255,255,.12);
      color:#fff;
      text-decoration:none;
      font-size:13px;
      white-space:nowrap;
      transition:all .2s ease;
    }
    .pill:hover{
      background: rgba(255,255,255,.12);
      transform: translateY(-1px);
    }

    /* Hero right card */
.hero-card{
  border-radius: 22px;
  border: 1px solid rgba(255,255,255,.14);
  background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
  box-shadow: var(--shadow);
  overflow:hidden;
  position: relative;
  min-height: 320px;

  /* ✅ thêm để hover mượt */
  transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease, background .25s ease;
}

/* ✅ Hover sáng lên */
.hero-card:hover{
  transform: translateY(-8px);
  border-color: rgba(255,158,11,.55);
  background: linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.04));
  box-shadow:
    0 18px 50px rgba(0,0,0,.45),
    0 0 36px rgba(255,158,11,.28),
    0 0 80px rgba(255,0,150,.12);
}

/* ✅ KPI sáng lên nhẹ khi hover (tuỳ chọn, đẹp hơn) */
.hero-card:hover .kpi{
  color: rgba(255,158,11,1);
  transition: color .25s ease;
}
.hero-card .card{
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.hero-card .card:hover{
  transform: translateY(-4px);
  border-color: rgba(255,158,11,.35);
  box-shadow: 0 12px 30px rgba(0,0,0,.35), 0 0 22px rgba(255,158,11,.18);
}
.hero-top{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding: 14px 16px;
  border-bottom: 1px solid rgba(255,255,255,.12);
  color: rgba(255,255,255,.78);
  font-weight: 900;

  /* ✅ FIX lỗi chữ bị trôi/đè viền */
  height: 44px;
  box-sizing: border-box;
}

.hero-top > div:last-child{
  line-height: 1;
  margin: 0;
  padding: 0;
}

    /* ✅ đổi 3 chấm thành win-dot để KHÔNG đụng .pill */
    .win-dot{ width: 9px; height: 9px; border-radius: 99px; background: rgba(255,255,255,.18); }
    .win-dot:nth-child(1){ background: rgba(239,68,68,.85); }
    .win-dot:nth-child(2){ background: rgba(245,158,11,.90); }
    .win-dot:nth-child(3){ background: rgba(34,197,94,.90); }

    .hero-body{ padding: 14px; display:grid; gap: 12px; }
    .card{
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.05);
      border-radius: 16px;
      padding: 14px;
      box-shadow: 0 14px 35px rgba(0,0,0,.18);
    }
    .kpi{
      margin:0;
      font-weight: 950;
      font-size: 26px;
      letter-spacing: -0.5px;
    }
    .sub{ margin: 6px 0 0; color: rgba(255,255,255,.66); font-size: 13px; line-height:1.55; }
    .row2{ display:grid; grid-template-columns: 1fr 1fr; gap: 12px; }

    /* Section title */
    .title{
      display:flex;
      align-items:flex-end;
      justify-content:space-between;
      gap: 10px;
      margin-bottom: 16px;
    }
    .title h2{ margin:0; font-size: 26px; letter-spacing: -0.4px; }
    .title p{ margin:0; color: var(--muted); font-size: 14px; }

    /* Specials */
    .specials{ grid-template-columns: repeat(3, 1fr); }
    .food{
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.05);
      border-radius: 18px;
      overflow:hidden;
      transition: transform .2s, border-color .2s, background .2s;
    }
    .food:hover{
      transform: translateY(-2px);
      border-color: rgba(255,255,255,.20);
      background: rgba(255,255,255,.07);
    }
    .food .img{
      height: 150px;
      background:
        radial-gradient(220px 140px at 25% 30%, rgba(255,183,3,.45), transparent 60%),
        radial-gradient(260px 160px at 70% 30%, rgba(251,113,133,.40), transparent 60%),
        linear-gradient(135deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      border-bottom: 1px solid rgba(255,255,255,.10);
    }
    .food .body{ padding: 14px; }
    .food h3{ margin:0 0 6px; font-size: 16px; }
    .food p{ margin:0; color: var(--muted); font-size: 14px; line-height:1.6; }
    .chip{
      display:inline-flex;
      padding: 6px 10px;
      border-radius: 999px;
      font-size: 12px;
      font-weight: 950;
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.12);
      color: rgba(255,255,255,.84);
      margin-top: 10px;
    }

    /* Pricing */
    .pricing{ grid-template-columns: repeat(3, 1fr); }
    .price{
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.05);
      border-radius: 18px;
      padding: 18px;
      position:relative;
      overflow:hidden;
    }
    .price.highlight{
      background: linear-gradient(180deg, rgba(255,183,3,.14), rgba(251,113,133,.08));
      border-color: rgba(255,183,3,.35);
      box-shadow: 0 22px 70px rgba(255,183,3,.12);
    }
    .tag{
      display:inline-flex;
      padding: 6px 10px;
      border-radius: 999px;
      font-size: 12px;
      font-weight: 950;
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.12);
      color: rgba(255,255,255,.84);
    }
    .amount{
      font-size: 38px;
      font-weight: 980;
      letter-spacing:-1px;
      margin: 10px 0 6px;
    }
    .amount span{ font-size: 13px; color: rgba(255,255,255,.62); font-weight: 900; }
    .list{ margin: 12px 0 0; padding:0; list-style:none; display:grid; gap: 8px; }
    .list li{
      display:flex; gap: 10px; align-items:flex-start;
      color: rgba(255,255,255,.74);
      font-size: 14px;
    }
    .check{
      width: 18px; height: 18px; border-radius: 8px;
      background: rgba(34,197,94,.18);
      border: 1px solid rgba(34,197,94,.35);
      display:grid; place-items:center;
      flex:0 0 auto;
      margin-top: 1px;
      font-size: 12px;
    }
    .price .btn{ width:100%; margin-top: 14px; justify-content:center; }

    /* Info */
    .info{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      align-items:start;
    }
    .map{
      border-radius: 18px;
      overflow:hidden;
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.05);
      min-height: 260px;
    }
    iframe{ width:100%; height: 260px; border:0; }

    /* Contact */
    .contact{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    .form{
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.05);
      border-radius: 18px;
      padding: 16px;
    }
    .field{ display:grid; gap: 6px; margin-bottom: 12px; }
    label{ font-size: 13px; font-weight: 950; color: rgba(255,255,255,.80); }
    input, textarea{
      width:100%;
      padding: 12px 12px;
      border-radius: 14px;
      border: 1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.18);
      color: rgba(255,255,255,.90);
      outline:none;
    }
    textarea{ min-height: 110px; resize: vertical; }
    input:focus, textarea:focus{
      border-color: rgba(255,183,3,.55);
      box-shadow: 0 0 0 4px rgba(255,183,3,.18);
    }
    .note{ color: rgba(255,255,255,.62); font-size: 13px; line-height: 1.6; }

    footer{
      border-top: 1px solid rgba(255,255,255,.12);
      padding: 22px 0;
      color: rgba(255,255,255,.62);
      font-size: 13px;
    }
    .foot{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 10px;
      flex-wrap: wrap;
    }

    /* HERO brand buttons */
    .hero-btn{
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 14px;
      border-radius: 14px;
      font-weight: 900;
      border: 1px solid rgba(255,255,255,.14);
    }
    .brand-icon{
      width: 18px;
      height: 18px;
      flex: 0 0 auto;
    }
    .zalo-hero{
      background: #0068ff;
      border-color: rgba(255,255,255,.10);
      color: #fff;
    }
    .zalo-hero:hover{ filter: brightness(1.05); }

    .fb-hero{
      background: #1877f2;
      border-color: rgba(255,255,255,.10);
      color: #fff;
    }
    .fb-hero:hover{ filter: brightness(1.05); }

    /* Floating actions (CHỈ 1 BLOCK) */
    .float{
      position: fixed;
      right: 16px;
      bottom: 16px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      z-index: 9999;
    }
    .fab{
      width: 52px;
      height: 52px;
      border-radius: 18px;
      display: grid;
      place-items: center;
      border: 1px solid rgba(255,255,255,.14);
      box-shadow: 0 14px 40px rgba(0,0,0,.25);
      backdrop-filter: blur(10px);
      transition: transform .15s, filter .2s;
    }
    .fab:hover{
      transform: translateY(-4px);
      filter: brightness(1.06);
    }

    .fab.call-btn{ background:#22c55e !important; }
    .fab.zalo-btn{ background:#0068ff !important; }
    .fab.messenger-btn{ background: linear-gradient(135deg, #00b2ff, #006aff) !important; }
    .fab.fb-btn{ background:#1877f2 !important; }

    .zalo-btn img{
      width: 26px;
      height: 26px;
      object-fit: contain;
    }

    /* Responsive */
    @media (max-width: 980px){
      .hero-grid{ grid-template-columns: 1fr; }
      .specials{ grid-template-columns: 1fr; }
      .pricing{ grid-template-columns: 1fr; }
      .info{ grid-template-columns: 1fr; }
      .contact{ grid-template-columns: 1fr; }
    }
    @media (max-width: 760px){
      nav[aria-label="Điều hướng"], .actions .btn.primary{ display:none; }
      .hamburger{ display:flex; }
    }
        /* ============================= */
/* 🔥 GLOW DÙNG CHUNG TOÀN WEB  */
/* ============================= */

.glow{
  position: relative;
  transition: transform .25s ease,
              box-shadow .25s ease,
              border-color .25s ease,
              filter .25s ease;
  will-change: transform;
}

/* Hover phát sáng */
.glow:hover{
  transform: translateY(-6px);
  border-color: rgba(255,158,11,.55) !important;
  box-shadow:
    0 18px 50px rgba(0,0,0,.45),
    0 0 36px rgba(255,158,11,.25),
    0 0 80px rgba(255,0,150,.12) !important;
  filter: brightness(1.04);
}

/* Nếu glow bị cắt bởi overflow của cha */
.glow{ overflow: visible; }
.hero-card, .card, .food, .price, .form, .map{
  border-color: rgba(255,255,255,.12);
}
.hero-card:hover, .card:hover, .food:hover, .price:hover, .form:hover, .map:hover{
  box-shadow:
    0 18px 50px rgba(0,0,0,.45),
    0 0 36px rgba(255,158,11,.22),
    0 0 80px rgba(255,0,150,.10);
  border-color: rgba(255,158,11,.45);
}
/* ============================= */
/* 🔥 GLOW DÙNG CHUNG TOÀN WEB  */
/* ============================= */

/* wrapper glow: chịu trách nhiệm NỔI + ĐỔ BÓNG */
.glow{
  position: relative;
  display: block;
  border-radius: inherit; /* ăn theo bo góc của card bên trong */
  transition: transform .25s ease, box-shadow .25s ease, filter .25s ease;
  will-change: transform;
}

/* khi hover: NỔI LÊN + glow */
.glow:hover{
  transform: translate3d(0,-10px,0);
  z-index: 50; /* nổi lên trên các card khác */
  filter: brightness(1.04);
  box-shadow:
    0 18px 50px rgba(0,0,0,.45),
    0 0 36px rgba(255,158,11,.25),
    0 0 80px rgba(255,0,150,.12);
}

/* chữ sáng hơn (tuỳ chọn) */
.glow:hover .kpi{
  background: linear-gradient(90deg,#ffb703,#fb7185,#ffb703);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: glowMove 2s linear infinite;
}
@keyframes glowMove{
  to { background-position: 200% center; }
}
/* ============================= */
/* ✨ Hover đổi màu chữ trong card */
/* ============================= */

/* 1) Món nổi bật (food) */
.food{ transition: transform .2s, border-color .2s, background .2s; }
.food h3, .food p, .food .chip{ transition: color .25s ease, opacity .25s ease, filter .25s ease; }

.food:hover h3{
  color: #ffb703;                 /* vàng */
  text-shadow: 0 0 18px rgba(255,183,3,.25);
}
.food:hover p{
  color: rgba(255,255,255,.92);   /* sáng hơn */
}
.food:hover .chip{
  color: #fff;
  border-color: rgba(255,183,3,.45);
  background: rgba(255,183,3,.12);
}

/* 2) Giá buffet (price) */
.price h3, .price .amount, .price li, .price .tag{
  transition: color .25s ease, text-shadow .25s ease, border-color .25s ease, background .25s ease;
}

.price:hover h3,
.price:hover .amount{
  color: #ffb703;
  text-shadow: 0 0 20px rgba(255,183,3,.22);
}
.price:hover li{
  color: rgba(255,255,255,.92);
}
.price:hover .tag{
  border-color: rgba(255,183,3,.45);
  background: rgba(255,183,3,.12);
  color: #fff;
}

/* 3) Card thường (áp dụng cho các .card ngoài hero) */
.card p, .card .sub, .card b{ transition: color .25s ease, text-shadow .25s ease; }
.card:hover p:first-child{
  color: #ffb703;
  text-shadow: 0 0 18px rgba(255,183,3,.22);
}
.card:hover .sub{ color: rgba(255,255,255,.92); }
/* ============================= */
/* ✨ Hover đẹp cho khu Đặt bàn (#contact) */
/* ============================= */

#contact .card{
  transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease, filter .25s ease;
  position: relative;
}

#contact .card p,
#contact .card b{
  transition: color .25s ease, text-shadow .25s ease;
}

/* Hover card nổi + viền vàng + glow */
#contact .card:hover{
  transform: translateY(-8px);
  border-color: rgba(255,183,3,.45);
  box-shadow:
    0 18px 50px rgba(0,0,0,.45),
    0 0 36px rgba(255,158,11,.22),
    0 0 80px rgba(255,0,150,.10);
  filter: brightness(1.04);
  z-index: 5;
}

/* Dòng tiêu đề (p đầu tiên) đổi vàng + phát sáng */
#contact .card:hover p:first-child{
  color: #ffb703;
  text-shadow: 0 0 18px rgba(255,183,3,.28);
}

/* Nội dung sáng hơn */
#contact .card:hover p,
#contact .card:hover b{
  color: rgba(255,255,255,.95);
}
/* ===== Mobile: giả lập hover khi chạm ===== */

/* Card: chạm (active) + khi có focus bên trong (focus-within) */
@media (hover: none) and (pointer: coarse){
  #contact .card:active,
  #contact .card:focus-within{
    transform: translateY(-8px);
    border-color: rgba(255,183,3,.45);
    box-shadow:
      0 18px 50px rgba(0,0,0,.45),
      0 0 36px rgba(255,158,11,.22),
      0 0 80px rgba(255,0,150,.10);
    filter: brightness(1.04);
    z-index: 5;
  }

  #contact .card:active p:first-child,
  #contact .card:focus-within p:first-child{
    color: #ffb703;
    text-shadow: 0 0 18px rgba(255,183,3,.28);
  }

  #contact .card:active p,
  #contact .card:focus-within p,
  #contact .card:active b,
  #contact .card:focus-within b{
    color: rgba(255,255,255,.95);
  }
}

/* Cho card nhận focus khi bấm (tốt cho mobile + accessibility) */
#contact .card{ outline: none; }
#contact .card{ -webkit-tap-highlight-color: transparent; }
/* ✅ GLOW dùng chung: PC hover + Mobile tap (active/focus) */
.glow{
  position: relative;
  transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease, filter .25s ease;
  will-change: transform;
}

/* PC có hover thật */
@media (hover:hover){
  .glow:hover{ 
    transform: translateY(-10px);
    z-index: 5;
    border-color: rgba(255,158,11,.45);
    box-shadow:
      0 18px 50px rgba(0,0,0,.45),
      0 0 36px rgba(255,158,11,.22),
      0 0 80px rgba(255,0,150,.10);
    filter: brightness(1.04);
  }
}

/* Mobile: chạm/nhấn => active (nhấn giữ) + focus-within (giữ hiệu ứng) */
@media (hover:none){
  .glow:active,
  .glow:focus-within,
  .glow.is-active{
    transform: translateY(-10px);
    z-index: 5;
    border-color: rgba(255,158,11,.45);
    box-shadow:
      0 18px 50px rgba(0,0,0,.45),
      0 0 36px rgba(255,158,11,.22),
      0 0 80px rgba(255,0,150,.10);
    filter: brightness(1.04);
  }
}

/* ✅ Hover/tap đổi màu chữ (áp cho tiêu đề + số + text phụ) */
.glow:is(:hover,:active,:focus-within,.is-active) h3,
.glow:is(:hover,:active,:focus-within,.is-active) .kpi,
.glow:is(:hover,:active,:focus-within,.is-active) p,
.glow:is(:hover,:active,:focus-within,.is-active) .sub{
  color: rgba(255,183,3,1);
  text-shadow: 0 0 18px rgba(255,183,3,.28);
}

/* ✅ Nếu bạn muốn KPI chạy gradient như bạn thích */
.glow:is(:hover,:active,:focus-within,.is-active) .kpi{
  background: linear-gradient(90deg,#ffb703,#fb7185,#ffb703);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: glowMove 2s linear infinite;
}
@keyframes glowMove{ to { background-position: 200% center; } }

/* ✅ Tránh bị "cắt glow" do overflow của cha */
.hero-card{ overflow: visible; } /* đừng để hidden nếu muốn glow tràn ra */
  </style>
</head>

<body>
  <header>
    <div class="nav wrap">
      <a class="brand" href="#top" aria-label="Về đầu trang">
        <div class="logo-brand">
          <span class="brand-text">Buffet</span>
          <span class="brand-price">79K</span>
        </div>
      </a>

      <nav aria-label="Điều hướng">
        <a href="#specials">Món nổi bật</a>
        <a href="#pricing">Giá buffet</a>
        <a href="#info">Giờ mở cửa</a>
        <a href="#contact">Đặt bàn</a>
      </nav>

      <div class="actions">
        <a class="btn" href="tel:0888800740" aria-label="Gọi đặt bàn">📞 Gọi</a>
        <a class="btn primary" href="#contact">Đặt bàn ngay</a>
        <button class="hamburger" type="button" id="open" aria-label="Mở menu">
          <span></span><span></span><span></span>
        </button>
      </div>
    </div>
  </header>

  <!-- Drawer mobile -->
  <div class="drawer" id="drawer" aria-hidden="true">
    <div class="panel" role="dialog" aria-label="Menu">
      <div class="row">
        <div class="brand">
          <div class="logo-nav">
            Buffet <span>79K</span>
          </div>
        </div>
        <button class="btn" type="button" id="close">Đóng</button>
      </div>
      <a href="#specials" onclick="closeDrawer()">Món nổi bật</a>
      <a href="#pricing" onclick="closeDrawer()">Giá buffet</a>
      <a href="#info" onclick="closeDrawer()">Giờ mở cửa</a>
      <a href="#contact" onclick="closeDrawer()">Đặt bàn</a>
      <div style="display:grid; gap:10px; margin-top:10px;">
        <a class="btn primary" href="#contact" onclick="closeDrawer()" style="justify-content:center;">Đặt bàn ngay</a>
      </div>
    </div>
  </div>

  <main id="top" class="wrap">
    <!-- HERO -->
    <section class="hero section">
      <div class="hero-grid">
        <div class="reveal">
          <span class="badge"><span class="dot"></span> Ngon sạch • Phục vụ nhanh • Giá dễ chịu</span>

          <h1>Buffet Bún Đậu 79K<br/>Ăn thả ga — no căng bụng</h1>

          <div class="rating-badge" aria-label="Đánh giá khách hàng">
            <span class="star" aria-hidden="true">⭐</span>
            <span><b>4.9/5</b> (320+ đánh giá)</span>
            <span class="dot" aria-hidden="true">•</span>
            <span>Ăn sạch – lên món nhanh</span>
          </div>

          <p class="lead">
            Chỉ 79K/người – ăn uống thả ga không giới hạn, topping phong phú, lên món liên tục đến khi no căng bụng.
          </p>

          <div class="hero-actions">
            <a class="btn primary" href="#contact">🍽️ Đặt bàn ngay</a>
            <a class="btn" href="tel:0888800740">📞 Gọi đặt bàn</a>
            <button class="btn" type="button" onclick="copyAddress()">📍 Copy địa chỉ</button>

            <a class="btn hero-btn zalo-hero"
               href="https://zalo.me/0888800740"
               target="_blank" rel="noopener noreferrer"
               aria-label="Zalo đặt bàn">
              <img class="brand-icon"
                   src="https://upload.wikimedia.org/wikipedia/commons/9/91/Icon_of_Zalo.svg"
                   alt="Zalo">
              Zalo
            </a>

            <a class="btn hero-btn fb-hero"
               href="https://www.facebook.com/Foliwindstore"
               target="_blank" rel="noopener noreferrer"
               aria-label="Facebook fanpage">
              <svg class="brand-icon" viewBox="0 0 24 24" aria-hidden="true" fill="white">
                <path d="M22 12a10 10 0 10-11.63 9.87v-6.99H7.9V12h2.47V9.8
                c0-2.44 1.45-3.8 3.68-3.8 1.07 0 2.2.19 2.2.19v2.42h-1.24
                c-1.22 0-1.6.76-1.6 1.54V12h2.72l-.43 2.88h-2.29v6.99A10
                10 0 0022 12z"/>
              </svg>
              Facebook
            </a>
          </div>

          <div class="hero-contact">
            <a class="pill" href="https://maps.app.goo.gl/UUtTDULgwM2CRdXY9?g_st=ic" target="_blank" rel="noopener noreferrer">
              📍 Tắc Cậu, Kiên Giang
            </a>
            <a class="pill" href="tel:0888800740">
              📞 0888800740
            </a>
            <a class="pill" href="https://zalo.me/0888800740" target="_blank" rel="noopener noreferrer">
              💬 Zalo
            </a>
          </div>
        </div>

          <div class="hero-card reveal glow" tabindex="0" aria-label="Khung thông tin nhanh">
          <div class="hero-top">
            <div class="pills" aria-hidden="true">
              <span class="win-dot"></span><span class="win-dot"></span><span class="win-dot"></span>
            </div>
            <div style="font-size:13px;">Thông tin nhanh</div>
          </div>
          <div class="hero-body">
            <div class="row2">
              <div class="card">
                <p class="kpi">79K</p>
                <p class="sub">Buffet tiết kiệm • phù hợp nhóm bạn</p>
              </div>
              <div class="card">
                <p class="kpi">10K</p>
                <p class="sub">Nước uống thả ga</p>
              </div>
            </div>

            <div class="card">
              <p style="margin:0; font-weight:950;">Combo nổi bật</p>
              <p class="sub" style="margin-top:6px;">Chả cốm, nem chua rán, thịt luộc, dồi… (tùy ngày)</p>
              <span class="chip">✅ Có chỗ ngồi nhóm</span>
              <span class="chip" style="margin-left:6px;">✅ In hóa đơn / QR</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SPECIALS -->
    <section id="specials" class="section">
      <div class="title">
        <div>
          <h2>Món nổi bật</h2>
          <p>Gợi ý menu — bạn sửa tên món theo quán của bạn.</p>
        </div>
      </div>

      <div class="grid specials">
        <article class="food reveal glow" tabindex="0">
          <div class="img" aria-hidden="true"></div>
          <div class="body">
            <h3>Mẹt bún đậu đầy đủ</h3>
            <p>Thịt luộc, chả cốm, nem rán, rau dưa…</p>
            <span class="chip">🔥 Best seller</span>
          </div>
        </article>

        <article class="food reveal glow" tabindex="0">
          <div class="img" aria-hidden="true"></div>
          <div class="body">
            <h3>Chả cốm / Nem rán</h3>
            <p>Giòn thơm, chấm mắm tôm cực cuốn.</p>
            <span class="chip">✨ Giòn ngon</span>
          </div>
        </article>

        <article class="food reveal glow" tabindex="0">
          <div class="img" aria-hidden="true"></div>
          <div class="body">
            <h3>Nước giải khát</h3>
            <p>Trà tắc, nước ngọt, nước suối…</p>
            <span class="chip">🧊 Mát lạnh</span>
          </div>
        </article>
      </div>
    </section>

    <!-- PRICING -->
    <section id="pricing" class="section">
      <div class="title">
        <div>
          <h2>Giá buffet</h2>
          <p>Rõ ràng — dễ chọn — dễ quyết.</p>
        </div>
      </div>

      <div class="grid pricing">
        <div class="price reveal glow" tabindex="0">
          <span class="tag">Trẻ em</span>
          <h3>Buffet Trẻ Em</h3>
          <div class="amount">49K <span>/ suất</span></div>
          <ul class="list">
            <li><span class="check">✓</span> Phần buffet phù hợp với bé</li>
            <li><span class="check">✓</span> Ăn uống thả ga</li>
            <li><span class="check">✓</span> Topping đa dạng</li>
          </ul>
          <a class="btn" href="#contact" style="justify-content:center;">Đặt bàn</a>
        </div>

        <div class="price highlight reveal">
          <span class="tag">Phổ biến</span>
          <h3>Buffet Người Lớn + Nước</h3>
          <div class="amount">89K <span>/ suất</span></div>
          <ul class="list">
            <li><span class="check">✓</span> Ăn thả ga — no đã</li>
            <li><span class="check">✓</span> Topping phong phú</li>
            <li><span class="check">✓</span> Nhóm đông càng vui</li>
          </ul>
          <a class="btn primary" href="#contact" style="justify-content:center;">🍽️ Đặt bàn ngay</a>
        </div>

        <div class="price reveal glow" tabindex="0">
          <span class="tag">Tùy chọn</span>
          <h3>Nước giải khát</h3>
          <div class="amount">10K <span>/ món</span></div>
          <ul class="list">
            <li><span class="check">✓</span> Nước sâm / Nước mía</li>
            <li><span class="check">✓</span> Trà tắc / Nước ngọt</li>
            <li><span class="check">✓</span> Mát lạnh</li>
          </ul>
          <a class="btn" href="#contact" style="justify-content:center;">Đặt bàn</a>
        </div>
      </div>
    </section>

    <!-- INFO -->
    <section id="info" class="section">
      <div class="title">
        <div>
          <h2>Giờ mở cửa & Địa chỉ</h2>

          <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px;">
            <a class="btn primary"
              href="https://maps.app.goo.gl/UUtTDULgwM2CRdXY9?g_st=ic"
              target="_blank"
              rel="noopener noreferrer">
              🗺️ Xem Google Maps
            </a>

            <a class="btn primary"
              href="https://www.google.com/maps/dir/?api=1&destination=T%E1%BA%AFc%20C%E1%BA%ADu%2C%20Ki%C3%AAn%20Giang"
              target="_blank"
              rel="noopener noreferrer">
              🧭 Chỉ đường đến quán
            </a>
          </div>
        </div>
      </div>

      <div class="info">
        <div class="grid" style="gap:12px;">
          <div class="card reveal glow" tabindex="0">
            <p style="font-weight:950; margin:0;">⏰ Giờ mở cửa</p>
            <p class="sub" style="margin-top:8px;">
              Thứ 2 – CN: <b>15:00 – 22:00</b>
            </p>
          </div>

          <div class="card reveal glow" tabindex="0">
            <p style="font-weight:950; margin:0;">📍 Địa chỉ</p>
            <p class="sub" style="margin-top:8px;">
              <b>Tắc Cậu, Kiên Giang</b><br/>
              SDT / Zalo: <b>0888800740</b>
            </p>
            <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px;">
              <a class="btn" href="tel:0888800740">📞 Gọi</a>
              <a class="btn" href="#contact">🧾 Đặt bàn</a>
              <a class="btn primary" href="https://maps.app.goo.gl/UUtTDULgwM2CRdXY9?g_st=ic" target="_blank" rel="noopener noreferrer">🗺️ Mở Maps</a>
            </div>
          </div>

          <div class="card reveal">
            <p style="font-weight:950; margin:0;">⭐ Vì sao khách thích?</p>
            <p class="sub" style="margin-top:8px;">
              Ngon sạch, mẹt đầy, phục vụ nhanh, giá hợp lý.
              Đi nhóm bạn/ gia đình đều tiện.
            </p>
          </div>
        </div>

        <div class="map reveal glow" tabindex="0" aria-label="Bản đồ">
          <iframe
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3919.0000000000005!2d106.00000000000001!3d10.800000000000002!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0000000000000000%3A0x0000000000000000!2zR29vZ2xlIE1hcHM!5e0!3m2!1svi!2s!4v0000000000000"
            aria-label="Google Maps">
          </iframe>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section">
      <div class="title">
        <div>
          <h2>Đặt bàn nhanh</h2>
          <br />
          <p>🔥 <b>Đặt bàn qua Zalo hoặc gọi ngay</b></p>
        </div>
      </div>

      <div class="contact">
        <div class="form reveal glow" tabindex="0">
          <form id="bookingForm">
            <div class="field">
              <label for="name">Tên khách</label>
              <input id="name" name="name" placeholder="VD: Huy Hoang" required />
            </div>

            <div class="field">
              <label for="phone">Số điện thoại</label>
              <input id="phone" name="phone" inputmode="tel" placeholder="VD: 0888800740" required />
            </div>

            <div class="field">
              <label for="people">Số người</label>
              <input id="people" name="people" type="number" min="1" value="2" required />
            </div>

            <div class="field">
              <label for="time">Giờ đến</label>
              <input id="time" name="time" type="time" required />
            </div>

            <div class="field">
              <label for="note">Ghi chú</label>
              <textarea id="note" name="note" placeholder="VD: cần bàn 6 người, có trẻ em..."></textarea>
            </div>
              <button 
  class="btn primary" 
  type="button"
  style="justify-content:center; width:100%;"
  onclick="window.open('https://zalo.me/0888800740?text=Tôi muốn đặt bàn Buffet 79K','_blank')">
  ✅ Xác nhận đặt bàn
</button>

            <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px;">
              <button class="btn primary" type="button" onclick="bookViaZalo()"
                      style="justify-content:center; flex:1; min-width:180px;">
                ✅ Đặt bàn qua Zalo
              </button>
              <button class="btn" type="button" onclick="bookViaMessenger()"
                      style="justify-content:center; flex:1; min-width:180px;">
                ✅ Đặt bàn qua Messenger
              </button>
            </div>

            <p class="note" style="margin-top:10px;">
              * Khi bấm, hệ thống sẽ <b>copy nội dung</b> đặt bàn và mở Zalo/Messenger để bạn <b>dán & gửi</b>.
            </p>
          </form>
        </div>

        <div class="grid" style="gap:12px;">
          <div class="card reveal glow" tabindex="0">
            <p style="margin:0; font-weight:950;"> 🎁 Ưu đãi</p>
            <p class="sub" style="margin-top:8px;">
              Giảm <b>10% cho 3 ngày khai trương </b>
              <p>🎁 Đi càng đông – Giảm càng sâu</p>
            </p>
          </div>

          <div class="card reveal glow" tabindex="0">
            <p style="margin:0; font-weight:950;">🧾 Thanh toán tiện</p>
            <p class="sub" style="margin-top:8px;">
              Nhận chuyển khoản, quét QR, in hóa đơn nhanh.
            </p>
          </div>

          <div class="card reveal glow" tabindex="0">
            <p style="margin:0; font-weight:950;">📞 Liên hệ nhanh</p>
            <p class="sub" style="margin-top:8px;">
              SDT / Zalo: <b>0888800740</b><br/>
              Địa chỉ: <b>Tắc Cậu, Kiên Giang</b>
            </p>
            <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px;">
              <a class="btn" href="tel:0888800740">📞 Gọi</a>
              <a class="btn" href="mailto:you@example.com">✉️ Email</a>

              <!-- ✅ Facebook button fixed (không lồng thẻ a) -->
              <a class="btn primary"
                 href="https://www.facebook.com/Foliwindstore"
                 target="_blank"
                 rel="noopener noreferrer">
                <svg viewBox="0 0 24 24" width="20" height="20" fill="white" style="margin-right:8px;">
                  <path d="M22 12a10 10 0 10-11.63 9.87v-6.99H7.9V12h2.47V9.8
                    c0-2.44 1.45-3.8 3.68-3.8 1.07 0 2.2.19 2.2.19v2.42h-1.24
                    c-1.22 0-1.6.76-1.6 1.54V12h2.72l-.43 2.88h-2.29v6.99A10
                    10 0 0022 12z"/>
                </svg>
                Facebook
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div class="wrap foot">
        <div>© <span id="year"></span> Buffet Bún Đậu 79K. All rights reserved.</div>
        <div style="display:flex; gap:12px; flex-wrap:wrap;">
          <a href="#specials">Món nổi bật</a>
          <a href="#pricing">Giá buffet</a>
          <a href="#contact">Đặt bàn</a>
        </div>
      </div>
    </footer>
  </main>

  <!-- ✅ Floating actions: CHỈ 1 BLOCK -->
  <div class="float" aria-label="Hành động nhanh">
    <!-- CALL -->
    <a class="fab call-btn"
       href="tel:0888800740"
       title="Gọi"
       aria-label="Gọi">
      <svg viewBox="0 0 24 24" width="22" height="22" fill="white" aria-hidden="true">
        <path d="M6.62 10.79a15.91 15.91 0 006.59 6.59l2.2-2.2a1 1 0 011-.24
        11.36 11.36 0 003.56.57 1 1 0 011 1v3.5a1 1 0 01-1 1A17.93
        17.93 0 012 4a1 1 0 011-1h3.5a1 1 0 011 1 11.36 11.36 0
        00.57 3.56 1 1 0 01-.25 1z"/>
      </svg>
    </a>

    <!-- ZALO -->
    <a class="fab zalo-btn"
       href="https://zalo.me/0888800740"
       target="_blank"
       rel="noopener noreferrer"
       title="Zalo"
       aria-label="Zalo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Icon_of_Zalo.svg" alt="Zalo">
    </a>

    <!-- MESSENGER -->
    <a class="fab messenger-btn"
       href="https://m.me/Foliwindstore"
       target="_blank"
       rel="noopener noreferrer"
       title="Messenger"
       aria-label="Messenger">
      <svg viewBox="0 0 24 24" width="22" height="22" fill="white" aria-hidden="true">
        <path d="M12 2C6.48 2 2 6.03 2 10.5c0 2.54 1.63 4.8 4.09 6.28V22l4.02-2.21c.62.17
        1.27.26 1.94.26 5.52 0 10-4.03 10-8.5S17.52 2 12 2zm1.12
        11.47l-2.55-2.72-4.96 2.72 5.45-5.78 2.57 2.72
        4.94-2.72-5.45 5.78z"/>
      </svg>
    </a>

    <!-- FACEBOOK -->
    <a class="fab fb-btn"
       href="https://www.facebook.com/Foliwindstore"
       target="_blank"
       rel="noopener noreferrer"
       title="Facebook"
       aria-label="Facebook">
      <svg viewBox="0 0 24 24" width="22" height="22" fill="white" aria-hidden="true">
        <path d="M22 12a10 10 0 10-11.63 9.87v-6.99H7.9V12h2.47V9.8
        c0-2.44 1.45-3.8 3.68-3.8 1.07 0 2.2.19 2.2.19v2.42h-1.24
        c-1.22 0-1.6.76-1.6 1.54V12h2.72l-.43 2.88h-2.29v6.99A10
        10 0 0022 12z"/>
      </svg>
    </a>
  </div>
  <script>
    // Reveal on scroll
    const reveals = Array.from(document.querySelectorAll(".reveal"));
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          e.target.classList.add("show");
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.12 });
    reveals.forEach(el=> io.observe(el));

    // Drawer
    const drawer = document.getElementById("drawer");
    const openBtn = document.getElementById("open");
    const closeBtn = document.getElementById("close");

    function openDrawer(){
      drawer.classList.add("open");
      drawer.setAttribute("aria-hidden","false");
    }
    function closeDrawer(){
      drawer.classList.remove("open");
      drawer.setAttribute("aria-hidden","true");
    }
    openBtn.addEventListener("click", openDrawer);
    closeBtn.addEventListener("click", closeDrawer);
    drawer.addEventListener("click", (e)=>{ if(e.target === drawer) closeDrawer(); });

    // Toast
    let toastTimer = null;
    function toast(msg){
      let t = document.getElementById("toast");
      if(!t){
        t = document.createElement("div");
        t.id = "toast";
        t.style.position = "fixed";
        t.style.left = "50%";
        t.style.bottom = "18px";
        t.style.transform = "translateX(-50%)";
        t.style.padding = "10px 12px";
        t.style.borderRadius = "14px";
        t.style.background = "rgba(15,20,40,.92)";
        t.style.border = "1px solid rgba(255,255,255,.14)";
        t.style.color = "rgba(255,255,255,.92)";
        t.style.backdropFilter = "blur(14px)";
        t.style.boxShadow = "0 18px 55px rgba(0,0,0,.35)";
        t.style.zIndex = "99999";
        t.style.fontWeight = "900";
        t.style.fontSize = "13px";
        document.body.appendChild(t);
      }
      t.textContent = msg;
      t.style.opacity = "1";
      if(toastTimer) clearTimeout(toastTimer);
      toastTimer = setTimeout(()=>{ t.style.opacity="0"; }, 2000);
    }

    // Copy address
    async function copyAddress(){
      const text = "Buffet Bún Đậu 79K - Tắc Cậu, Kiên Giang";
      try{
        await navigator.clipboard.writeText(text);
        toast("✅ Đã copy địa chỉ!");
      }catch{
        toast("Không copy được (trình duyệt chặn).");
      }
    }

    // Booking demo
    document.getElementById("bookingForm").addEventListener("submit", (e)=>{
      e.preventDefault();
      const name = document.getElementById("name").value.trim() || "bạn";
      toast(`✅ Đã nhận đặt bàn cho ${name} (demo)!`);
      e.target.reset();
    });

    // Year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Booking via Zalo/Messenger
    const ZALO_PHONE = "0888800740";
    const MESSENGER_PAGE = "Foliwindstore";

    function buildBookingMessage(){
      const name = document.getElementById("name")?.value.trim();
      const phone = document.getElementById("phone")?.value.trim();
      const people = document.getElementById("people")?.value;
      const time = document.getElementById("time")?.value;
      const note = document.getElementById("note")?.value.trim();

      return (
`ĐẶT BÀN - Buffet Bún Đậu 79K
- Tên: ${name || "(chưa nhập)"}
- SĐT: ${phone || "(chưa nhập)"}
- Số người: ${people || "(chưa nhập)"}
- Giờ đến: ${time || "(chưa nhập)"}
- Ghi chú: ${note || "(không)"}

Xin xác nhận giúp em ạ.`
      );
    }

    async function copyThenOpen(url){
      const msg = buildBookingMessage();
      try{
        await navigator.clipboard.writeText(msg);
        window.open(url, "_blank", "noopener,noreferrer");
        alert("✅ Đã copy nội dung đặt bàn. Mở app và DÁN để gửi nhé!");
      }catch(e){
        window.open(url, "_blank", "noopener,noreferrer");
        alert("Mình đã mở app. Bạn copy & gửi nội dung đặt bàn theo thông tin đã nhập nhé!");
      }
    }

    function bookViaZalo(){
      const url = `https://zalo.me/${ZALO_PHONE}`;
      copyThenOpen(url);
    }

    function bookViaMessenger(){
      const url = `https://m.me/${MESSENGER_PAGE}`;
      copyThenOpen(url);
    }
    // ✅ Mobile: tap để bật/tắt glow (giữ hiệu ứng)
document.querySelectorAll('.glow').forEach(el => {
  el.addEventListener('click', (e) => {
    // tắt các thẻ khác
    document.querySelectorAll('.glow.is-active').forEach(x => { if (x !== el) x.classList.remove('is-active'); });
    // bật/tắt thẻ hiện tại
    el.classList.toggle('is-active');
    e.stopPropagation();
  });
});

// tap ra ngoài thì tắt
document.addEventListener('click', () => {
  document.querySelectorAll('.glow.is-active').forEach(x => x.classList.remove('is-active'));
});

  </script>
</body>
</html>
