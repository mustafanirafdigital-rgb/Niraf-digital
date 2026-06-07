<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Home</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="preconnect" href="https://iili.io">
  <link rel="preconnect" href="https://cdn-icons-png.flaticon.com">
  <link rel="preconnect" href="https://upload.wikimedia.org">
  <link rel="preconnect" href="https://images.bukaolshop.com">
  <link rel="preconnect" href="https://vectorseek.com">
  <link rel="preconnect" href="https://logowik.com">
  
  <link href="https://fonts.googleapis.com/css2?family=Urbanist:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --accent: #F4511E;
      --soft-blue: #E6F2FF;
      --muted: #666;
      --text-dark: #333;
      --bg-light: #F2F4F6;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    html { -webkit-text-size-adjust: 100%; }

    body {
      font-family: 'Urbanist', sans-serif;
      background: #f2f2f2;
      color: var(--text-dark);
      touch-action: manipulation;
      -webkit-tap-highlight-color: transparent;
    }

    a, button {
      text-decoration: none;
      color: inherit;
      -webkit-tap-highlight-color: transparent;
    }
    a:focus, a:active, a:visited,
    button:focus, button:active {
      outline: none;
      text-decoration: none;
      color: inherit;
    }

    .icon-btn:active,
    .icon-box-top:active,
    .icon-box:active,
    .tablink:active,
    .provider-box:active,
    .ewallet-box:active,
    .driver-box:active {
      background: rgba(0,0,0,0.1) !important;
      border-radius: 10px;
      transition: background 0.1s ease;
      transform: scale(0.97);
    }

    .header {
      background: var(--accent);
      color: #fff;
      padding: 20px 16px 64px 16px;
      position: relative;
      box-shadow: 0 2px 6px rgba(0,0,0,0.15);
    }
    .header-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .header-text { display: flex; flex-direction: column; }
    .header-text .hi { font-size: 13px; opacity: 0.9; }
    .header-text .name { font-size: 16px; font-weight: 800; }

    .header-icons { display: flex; gap: 12px; }

    .icon-btn {
      width: 38px;
      height: 38px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--soft-blue);
      position: relative;
    }
    .icon-btn img { width: 20px; height: 20px; display: block; }
    .icon-btn.chat img { width: 24px; height: 24px; }
    .icon-btn.notif img {
      filter: brightness(0) saturate(100%) invert(41%) sepia(97%) saturate(3186%) hue-rotate(2deg) brightness(96%) contrast(104%);
    }
    .notif-badge {
      position: absolute;
      top: -6px;
      right: -6px;
      background: #FF0000;
      color: #fff;
      font-size: 11px;
      padding: 2px 6px;
      border-radius: 50%;
      line-height: 1;
      min-width: 20px;
      text-align: center;
      box-sizing: border-box;
    }

    .saldo-container {
      position: absolute;
      left: 16px;
      right: 16px;
      bottom: -28px;
      background: #fff;
      border-radius: 12px;
      padding: 12px;
      display: flex;
      box-shadow: 0 6px 18px rgba(0,0,0,0.1);
    }
    .saldo-box {
      flex: 1;
      padding: 0 8px;
    }
    .saldo-box + .saldo-box {
      border-left: 1px solid #eee;
    }
    .saldo-box span {
      display: block;
      font-size: 13px;
      color: var(--muted);
      text-align: left;
    }
    .saldo-box .value {
      font-weight: 800;
      font-size: 18px;
      color: var(--accent);
      margin-top: 4px;
      display: block;
      text-align: left;
    }

    .menu-aksi {
      display: flex;
      justify-content: space-around;
      background: #fff;
      margin: 50px 12px 8px;
      padding: 10px 0;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    .menu-aksi a { text-align: center; }
    .menu-aksi a span {
      font-size: 12px;
      font-weight: 600;
    }
    .icon-box-top {
      width: 47px;
      height: 47px;
      background: var(--soft-blue);
      border-radius: 11px;
      margin: 0 auto 5px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .icon-box-top img {
      width: 30px;
      height: 30px;
    }

    .banner-container {
      margin: 10px;
      border-radius: 10px;
      overflow: hidden;
      background: #fff;
    }
    .banner-container img {
      width: 100%;
      height: 170px;
      object-fit: contain;
    }

    .provider-section {
      background: #fff;
      margin: 10px;
      border-radius: 10px;
      padding: 12px 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    .provider-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 8px;
      text-align: center;
    }
    .provider-box {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
      padding: 6px 2px;
      border-radius: 10px;
    }
    .provider-icon-wrapper {
      width: 47px;
      height: 47px;
      background: var(--soft-blue);
      border-radius: 11px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      margin-bottom: 5px;
    }
    .provider-icon {
      width: 30px;
      height: 30px;
      object-fit: contain;
    }
    .provider-badge {
      position: absolute;
      top: -6px;
      right: -6px;
      padding: 2px 5px;
      border-radius: 8px;
      font-size: 8px;
      font-weight: 800;
      color: #fff;
      white-space: nowrap;
      line-height: 1;
    }
    .badge-only4u { background: #FF9800; }
    .badge-promo { background: #F44336; }
    .badge-cuanku { background: #1565C0; }
    .badge-cuanmax { background: #E91E63; }
    .provider-name {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-dark);
      line-height: 1.2;
    }

    .ewallet-section {
      background: #fff;
      margin: 10px;
      border-radius: 10px;
      padding: 14px 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    .ewallet-section-title {
      font-size: 15px;
      font-weight: 800;
      color: var(--text-dark);
      margin-bottom: 14px;
      padding-left: 4px;
    }
    .ewallet-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      text-align: center;
    }
    .ewallet-box {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
      padding: 8px 4px;
      border-radius: 10px;
    }
    .ewallet-icon-wrapper {
      width: 47px;
      height: 47px;
      background: var(--soft-blue);
      border-radius: 11px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      margin-bottom: 6px;
    }
    .ewallet-icon {
      width: 30px;
      height: 30px;
      object-fit: contain;
      border-radius: 0;
    }
    .ewallet-name {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-dark);
      line-height: 1.2;
    }

    .driver-section {
      background: #fff;
      margin: 10px;
      border-radius: 10px;
      padding: 14px 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    .driver-section-title {
      font-size: 15px;
      font-weight: 800;
      color: var(--text-dark);
      margin-bottom: 14px;
      padding-left: 4px;
    }
    .driver-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      text-align: center;
    }
    .driver-box {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
      padding: 8px 4px;
      border-radius: 10px;
    }
    .driver-icon-wrapper {
      width: 47px;
      height: 47px;
      background: var(--soft-blue);
      border-radius: 11px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      margin-bottom: 6px;
    }
    .driver-icon {
      width: 30px;
      height: 30px;
      object-fit: contain;
      border-radius: 0;
    }
    .driver-name {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-dark);
      line-height: 1.2;
    }

    .tab-container {
      background: #fff;
      margin: 10px;
      border-radius: 10px;
      padding: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    .tab-header {
      display: flex;
      justify-content: space-around;
      border-bottom: 1px solid #eee;
      margin-bottom: 8px;
    }
    .tablink {
      background: none;
      border: none;
      font-size: 14px;
      padding: 8px;
      font-weight: 800;
      color: var(--muted);
      cursor: pointer;
      font-family: 'Urbanist', sans-serif;
    }
    .tablink.active {
      color: var(--accent);
      border-bottom: 2px solid var(--accent);
    }

    .tab-content {
      display: none;
      grid-template-columns: repeat(4, 1fr);
      gap: 12px;
      text-align: center;
    }
    .tab-content.active { display: grid; }
    .tab-content a { color: var(--text-dark); }
    .icon-box {
      width: 47px;
      height: 47px;
      border-radius: 11px;
      background: var(--soft-blue);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 4px;
    }
    .icon-box img {
      width: 30px;
      height: 30px;
    }
    .tab-content span {
      font-size: 12px;
      font-weight: 600;
      display: block;
      line-height: 14px;
    }

    /* === LOGO ORBIT PERSIS GAMBAR === */
    .orbit-icon-box {
      width: 47px;
      height: 47px;
      border-radius: 14px;
      background: #E8F0FE;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 4px;
      flex-direction: column;
      gap: 1px;
    }
    .orbit-icon-box .orbit-telkomsel {
      font-size: 5.5px;
      font-weight: 700;
      color: #E60000;
      letter-spacing: 0.2px;
      line-height: 1;
    }
    .orbit-icon-box .orbit-brand {
      font-size: 15px;
      font-weight: 800;
      color: #E60000;
      line-height: 1;
      letter-spacing: -0.3px;
    }
    .orbit-label {
      font-size: 12px;
      font-weight: 600;
      display: block;
      line-height: 14px;
    }

    .security-section {
      background: #fff;
      border-radius: 12px;
      margin: 8px;
      padding: 16px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }
    .security-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;
    }
    .security-brand { display: flex; align-items: center; gap: 8px; }
    .brand-icon {
      width: 32px;
      height: 32px;
      background: var(--accent);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .brand-icon img { width: 20px; height: 20px; filter: brightness(0) invert(1); }
    .brand-text .brand-name { font-weight: 800; font-size: 14px; color: var(--text-dark); }
    .brand-text .brand-sub { font-size: 12px; color: var(--muted); }
    .security-status {
      border: 1px solid var(--accent);
      border-radius: 6px;
      padding: 4px 8px;
      display: flex;
      gap: 4px;
      font-size: 12px;
      font-weight: 600;
      color: var(--accent);
    }
    .security-warning {
      background: #f7f7f7;
      padding: 10px;
      border-radius: 8px;
      text-align: center;
      font-weight: 700;
      font-size: 13px;
      margin-bottom: 16px;
      color: var(--text-dark);
    }
    .security-features {
      display: flex;
      justify-content: space-around;
      text-align: center;
      align-items: center;
    }
    .feature-item { display: flex; flex-direction: column; align-items: center; }
    .feature-icon {
      width: 48px;
      height: 48px;
      background: var(--accent);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 6px;
    }
    .feature-icon img { width: 22px; height: 22px; filter: brightness(0) invert(1); }
    .feature-text { font-size: 12px; font-weight: 600; color: var(--text-dark); }

    .marquee-container {
      background: rgba(255,255,255,0.15);
      border-radius: 8px;
      padding: 6px 0;
      margin: 12px 0 8px;
      overflow: hidden;
      position: relative;
    }
    .marquee-track {
      display: flex;
      width: max-content;
      animation: marquee-scroll 15s linear infinite;
      will-change: transform;
      transform: translateZ(0);
    }
    .marquee-track:hover {
      animation-play-state: paused;
    }
    .marquee-text {
      font-size: 13px;
      font-weight: 600;
      color: #fff;
      white-space: nowrap;
      padding-right: 40px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .marquee-text .info-icon {
      width: 18px;
      height: 18px;
      filter: brightness(0) invert(1);
      background: rgba(255,255,255,0.25);
      border-radius: 50%;
      padding: 2px;
      flex-shrink: 0;
    }
    @keyframes marquee-scroll {
      0% { transform: translateX(0) translateZ(0); }
      100% { transform: translateX(-50%) translateZ(0); }
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="header-top">
      <div class="header-text">
        <div class="hi">Selamat Datang</div>
        <div class="name">Juragan</div>
      </div>
      <div class="header-icons">
        <a href="https://wa.me/6281373949114?text=Halo%20NIRAF%20DIGITAL,%20saya%20butuh%20bantuan" 
           class="icon-btn chat" 
           title="Chat Customer Service"
           target="_blank"
           rel="noopener noreferrer">
          <img src="https://iili.io/K1gCpgp.md.png" alt="Chat" decoding="async">
        </a>
      </div>
    </div>

    <div class="marquee-container">
      <div class="marquee-track">
        <div class="marquee-text">
          <img src="https://cdn-icons-png.flaticon.com/512/3601/3601638.png" alt="info" class="info-icon" decoding="async">
          Selamat datang di NIRAF DIGITAL — Silahkan dimaksimalkan transaksinya Juragan !
        </div>
        <div class="marquee-text">
          <img src="https://cdn-icons-png.flaticon.com/512/3601/3601638.png" alt="info" class="info-icon" decoding="async">
          Selamat datang di NIRAF DIGITAL — Silahkan dimaksimalkan transaksinya Juragan!
        </div>
      </div>
    </div>
   
    <div class="saldo-container">
      <div class="saldo-box">
        <span>Saldo Akun</span>
        <div class="value" id="saldo_user">150000</div>
      </div>
      <div class="saldo-box">
        <span>My Poin</span>
        <a href="#/akun/?page=poin" class="value" id="poin_member">250</a>
      </div>
    </div>
  </div>

  <div class="menu-aksi">
    <a href="#/akun/?page=topup"><div class="icon-box-top"><img src="https://iili.io/KENMPvS.md.png" alt="Topup" loading="lazy" decoding="async"></div><span>Topup Saldo</span></a>
    <a href="https://nirafdigital2.digitalshop.id/digital/390812"><div class="icon-box-top"><img src="https://iili.io/K5uxOxI.md.png" alt="Tarik" loading="lazy" decoding="async"></div><span>transfer bank</span></a>
    <a href="https://nirafdigital2.digitalshop.id/digital/394632"><div class="icon-box-top"><img src="https://iili.io/K5ulxWJ.th.png" alt="Transfer" loading="lazy" decoding="async"></div><span>Transfer Member</span></a>
    <a href="https://nirafdigital2.digitalshop.id/digital/389591"><div class="icon-box-top"><img src="https://iili.io/KRmUCQt.md.png" alt="Mutasi" loading="lazy" decoding="async"></div><span>Mutasi</span></a>
  </div>

  <div class="banner-container">
    <img id="bannerImage" src="https://images.bukaolshop.com/hosting/179068/3260f5698963141442.png" alt="Banner" decoding="async">
  </div>

  <div class="provider-section">
    <div class="provider-grid">
      <a href="#" class="provider-box">
        <div class="provider-icon-wrapper">
          <img src="https://portal.powertec.com.au/sites/default/files/styles/scale_square/public/2024-01/Indosat_Ooredoo_logo.png.webp" alt="Indosat" class="provider-icon" loading="lazy" decoding="async">
          <span class="provider-badge badge-only4u">Only4U</span>
        </div>
        <span class="provider-name">Indosat</span>
      </a>
      <a href="https://nirafdigital2.digitalshop.id/digital/388543" class="provider-box">
        <div class="provider-icon-wrapper">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Telkomsel_2021_icon.svg/960px-Telkomsel_2021_icon.svg.png" alt="Telkomsel" class="provider-icon" loading="lazy" decoding="async">
          <span class="provider-badge badge-promo">Promo</span>
        </div>
        <span class="provider-name">Telkomsel</span>
      </a>
      <a href="https://nirafdigital2.digitalshop.id/digital/388206" class="provider-box">
        <div class="provider-icon-wrapper">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Axis_logo_2015.svg/1280px-Axis_logo_2015.svg.png" alt="XL-Axis" class="provider-icon" loading="lazy" decoding="async">
          <span class="provider-badge badge-cuanku">CuanKu</span>
        </div>
        <span class="provider-name">XL-Axis</span>
      </a>
      <a href="https://nirafdigital2.digitalshop.id/digital/386915" class="provider-box">
        <div class="provider-icon-wrapper">
          <img src="https://upload.wikimedia.org/wikipedia/id/thumb/6/68/3-brand.svg/960px-3-brand.svg.png" alt="Tri" class="provider-icon" loading="lazy" decoding="async">
          <span class="provider-badge badge-cuanmax">CuanMAX</span>
        </div>
        <span class="provider-name">Tri</span>
      </a>
    </div>
  </div>

  <div class="tab-container">
    <div class="tab-header">
      <button class="tablink active" onclick="openTab('isiulang',this)">Pembelian</button>
      <button class="tablink" onclick="openTab('bayartagihan', this)">Bayar Tagihan</button>
      <button class="tablink" onclick="openTab('lainya', this)">Lainya</button>
    </div>

    <!-- Isi Ulang -->
    <div id="isiulang" class="tab-content active">
      <a href="https://nirafdigital2.digitalshop.id/digital/384135"><div class="icon-box"><img src="https://iili.io/KRyhBg2.md.png" alt="Pulsa" loading="lazy" decoding="async"></div><span><p></p>Pulsa</br>Reguler<p></p></span></a>
      <a href="https://nirafdigital2.digitalshop.id/digital/385020"><div class="icon-box"><img src="https://iili.io/K5uMmOB.md.png" alt="Token" loading="lazy" decoding="async"></div><span><p>Token</br>Listrik<p></p></span></a>
      <a href="https://nirafdigital2.digitalshop.id/digital/385425"><div class="icon-box"><img src="https://iili.io/KRy7Faf.md.png" alt="Data" loading="lazy" decoding="async"></div><span>Data Internet</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/K592Pxp.md.png" alt="Voucher" loading="lazy" decoding="async"></div><span>Inject Voucher</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/K5uNjkJ.md.png" alt="Pulsa" loading="lazy" decoding="async"></div><span>Games</span></a>
      <a href="https://nirafdigital2.digitalshop.id/digital/390140"><div class="icon-box"><img src="https://iili.io/K598IEX.md.png" alt="Token" loading="lazy" decoding="async"></div><span>E-Wallet bebas</span></a>
      <a href="https://nirafdigital2.digitalshop.id/digital/390843"><div class="icon-box"><img src="https://iili.io/KRy67Jn.md.png" alt="Data" loading="lazy" decoding="async"></div><span>Pulsa transfer</span></a>
      <a href="https://nirafdigital2.digitalshop.id/digital/387404"><div class="icon-box"><img src="https://iili.io/KRyGZa1.md.png" alt="Voucher" loading="lazy" decoding="async"></div><span>Telp & SMS</span></a>
      
      <!-- ORBIT: LOGO DARI CSS PERSIS GAMBAR -->
      <a href="https://nirafdigital2.digitalshop.id/digital/394926">
        <div class="orbit-icon-box">
          <span class="orbit-telkomsel">Telkomsel</span>
          <span class="orbit-brand">Orbit</span>
        </div>
        <span class="orbit-label">Orbit</span>
      </a>
    </div>

    <!-- Bayar Tagihan -->
    <div id="bayartagihan" class="tab-content">
      <a href="#"><div class="icon-box"><img src="https://iili.io/K5uMmOB.md.png" alt="Listrik" loading="lazy" decoding="async"></div><span>Listrik Bulanan</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/K1m9qiX.md.png" alt="BPJS" loading="lazy" decoding="async"></div><span>BPJS Kesehatan</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/K1mn4Lb.md.png" alt="Internet" loading="lazy" decoding="async"></div><span>Internet Bulanan</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KEGpNrN.md.png" alt="PDAM" loading="lazy" decoding="async"></div><span>Air PDAM</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KEhsnUP.md.png" alt="Listrik" loading="lazy" decoding="async"></div><span>Gas Negara</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KRyhBg2.md.png" alt="BPJS" loading="lazy" decoding="async"></div><span>Telepon Pascabayar</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/K5u1ES2.md.png" alt="Internet" loading="lazy" decoding="async"></div><span>Cicilan Bulanan</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KEjuloX.md.png" alt="PDAM" loading="lazy" decoding="async"></div><span>E-samsat</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KEjDFrx.md.png" alt="Internet" loading="lazy" decoding="async"></div><span>PBB Pajak Bumi</span></a>
      <a href="#"><div class="icon-box"><img src="https://iili.io/KEwWwwF.md.png" alt="PDAM" loading="lazy" decoding="async"></div><span>TV Bulanan</span></a>
    </div>

    <!-- Lainya -->
    <div id="lainya" class="tab-content">
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/3063/3063176.png" alt="Voucher Game" loading="lazy" decoding="async"></div><span>Voucher Game</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/1005/1005141.png" alt="Streaming" loading="lazy" decoding="async"></div><span>Streaming</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/2966/2966486.png" alt="Voucher Belanja" loading="lazy" decoding="async"></div><span>Voucher Belanja</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/2966/2966332.png" alt="Asuransi" loading="lazy" decoding="async"></div><span>Asuransi</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" alt="Pajak" loading="lazy" decoding="async"></div><span>Pajak Kendaraan</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/3135/3135768.png" alt="Samsat" loading="lazy" decoding="async"></div><span>Samsat Online</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/2920/2920277.png" alt="Donasi" loading="lazy" decoding="async"></div><span>Donasi</span></a>
      <a href="#"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/2920/2920349.png" alt="Zakat" loading="lazy" decoding="async"></div><span>Zakat</span></a>
      <a href="https://velotiket.com/konterkupay"><div class="icon-box"><img src="https://cdn-icons-png.flaticon.com/512/3125/3125848.png" alt="Tiket Pesawat" loading="lazy" decoding="async"></div><span>Tiket Pesawat</span></a>
    </div>
  </div>

  <div class="ewallet-section">
    <div class="ewallet-section-title">E-Wallet</div>
    <div class="ewallet-grid">
      <a href="https://nirafdigital2.digitalshop.id/digital/391157" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://vectorseek.com/wp-content/uploads/2023/09/Dana-E-Wallet-App-Logo-Vector.svg-.png" alt="Dana" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">Dana</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Logo_ovo_purple.svg/960px-Logo_ovo_purple.svg.png" alt="OVO" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">OVO</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://logowik.com/content/uploads/images/gopay7196.jpg" alt="GoPay" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">GoPay</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://static.vecteezy.com/system/resources/thumbnails/067/065/685/small_2x/shopeepay-colored-logo-rounded-icon-transparent-background-free-png.png" alt="ShopeePay" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">ShopeePay</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://iconlogovector.com/uploads/images/2024/03/lg-65e38a30a6a72-LinkAja.webp" alt="LinkAja" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">LinkAja</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://images.icon-icons.com/2699/PNG/512/grab_logo_icon_169071.png" alt="Grab" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">Grab</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://logowik.com/content/uploads/images/maxim2941.jpg" alt="Maxim" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">Maxim</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://zonalogo.com/api/asset-preview?url=https%3A%2F%2Fassets.zonalogo.com%2Ffinance%2Fdoku.com%2Flogo-1774502529163-749.svg&theme=dark&v=v2" alt="Doku" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">Doku</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://cdn.aptoide.com/imgs/1/7/1/17138e7527b121d4aae0c72f2583c01b_fgraphic.jpg" alt="iSaku" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">iSaku</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://kaspro.id/style/images/Logo%20KasPro.png" alt="Kaspro" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">Kaspro</span>
      </a>
      <a href="#" class="ewallet-box">
        <div class="ewallet-icon-wrapper">
          <img src="https://cdn.aptoide.com/imgs/0/e/e/0eecd0cd602eb03a2705c8bcd93928ac_icon.png" alt="AstraPay" class="ewallet-icon" loading="lazy" decoding="async">
        </div>
        <span class="ewallet-name">AstraPay</span>
      </a>
    </div>
  </div>

  <div class="driver-section">
    <div class="driver-section-title">Driver</div>
    <div class="driver-grid">
      <a href="#" class="driver-box">
        <div class="driver-icon-wrapper">
          <img src="https://iconlogovector.com/uploads/images/2023/06/lg-c59d473ed3003d93c070836a79e80a6b79.jpg" alt="Gojek Driver" class="driver-icon" loading="lazy" decoding="async">
        </div>
        <span class="driver-name">Gojek Driver</span>
      </a>
      <a href="#" class="driver-box">
        <div class="driver-icon-wrapper">
          <img src="https://cdn.iconscout.com/icon/free/png-256/free-grab-icon-svg-download-png-282266.png?f=webp" alt="Grab Driver" class="driver-icon" loading="lazy" decoding="async">
        </div>
        <span class="driver-name">Grab Driver</span>
      </a>
      <a href="#" class="driver-box">
        <div class="driver-icon-wrapper">
          <img src="https://logowik.com/content/uploads/images/maxim2941.jpg" alt="Maxim Driver" class="driver-icon" loading="lazy" decoding="async">
        </div>
        <span class="driver-name">Maxim Driver</span>
      </a>
      <a href="#" class="driver-box">
        <div class="driver-icon-wrapper">
          <img src="https://images.seeklogo.com/logo-png/40/1/shopee-pay-logo-png_seeklogo-406839.png" alt="Shopee Driver" class="driver-icon" loading="lazy" decoding="async">
        </div>
        <span class="driver-name">Shopee Driver</span>
      </a>
    </div>
  </div>

  <div class="security-section">
    <div class="security-header">
      <div class="security-brand">
        <div class="brand-icon">
          <img src="https://neropict.wordpress.com/wp-content/uploads/2025/03/1161490.png" alt="Shield" decoding="async">
        </div>
        <div class="brand-text">
          <div class="brand-name">NIRAF DIGITAL</div>
          <div class="brand-sub">Protection</div>
        </div>
      </div>
      <div class="security-status">
        <span>100%</span>
        <span>Terlindungi</span>
      </div>
    </div>
    <div class="security-warning">
      Jangan Berikan Kode OTP Kepada Siapapun
    </div>
    <div class="security-features">
      <div class="feature-item">
        <div class="feature-icon">
          <img src="https://cdn-icons-png.flaticon.com/512/483/483408.png" alt="Keuangan Aman" decoding="async">
        </div>
        <div class="feature-text">Keuangan Aman</div>
      </div>
      <div class="feature-item">
        <div class="feature-icon">
          <img src="https://cdn-icons-png.flaticon.com/512/929/929610.png" alt="Aktivitas Terlindungi" decoding="async">
        </div>
        <div class="feature-text">Aktivitas Terlindungi</div>
      </div>
    </div>
  </div>

  <script>
    function openTab(tabName, btn) {
      const allTabs = document.querySelectorAll('.tab-content');
      const allButtons = document.querySelectorAll('.tablink');
      allTabs.forEach(tab => tab.classList.remove('active'));
      allButtons.forEach(button => button.classList.remove('active'));
      document.getElementById(tabName).classList.add('active');
      btn.classList.add('active');
    }

    document.addEventListener('DOMContentLoaded', () => {
      const banners = [
        "https://images.bukaolshop.com/hosting/183180/3ebda4c2e9c4222993.png",
        "https://images.bukaolshop.com/hosting/183180/71fa94f3706a766770.png",
      ];
      const banner = document.getElementById('bannerImage');
      let index = 0;
      setInterval(() => {
        index = (index + 1) % banners.length;
        const img = new Image();
        img.src = banners[index];
        img.onload = () => {
          banner.src = banners[index];
        };
      }, 5000);
    });

    function formatRupiah(angka) {
      if (!angka) return 'Rp 0';
      return 'Rp ' + angka.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
    }

    document.addEventListener('DOMContentLoaded', () => {
      const saldo = document.getElementById('saldo_user');
      const poin = document.getElementById('poin_member');
      if (saldo) saldo.textContent = formatRupiah(saldo.textContent.replace(/[^0-9]/g, ''));
      if (poin) poin.textContent = poin.textContent;
    });
  </script>
</body>
</html>
