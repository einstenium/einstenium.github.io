
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>Bio</title>
  
  <!-- Fontes Gringas Premium (Inter + Geist Mono) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Geist+Mono:wght@300;400;500&family=Inter:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">

  <style>
    *, *::before, *::after {
      margin: 0; padding: 0;
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    /* FORÇAR SUMIR COM A BARRA AZUL/TÍTULO DO GITHUB */
    header, #header, #title_container, .title-container, #banner {
      display: none !important;
      opacity: 0 !important;
      visibility: hidden !important;
      height: 0 !important;
      padding: 0 !important;
      margin: 0 !important;
    }

    :root {
      --sans: 'Inter', sans-serif;
      --mono: 'Geist Mono', monospace;
      --bg: #000000;
      --surface: rgba(255, 255, 255, 0.02);
      --surface-hover: rgba(255, 255, 255, 0.05);
      --border: rgba(255, 255, 255, 0.06);
      --border-bright: rgba(255, 255, 255, 0.2);
      --t: rgba(255, 255, 255, 0.6);
      --td: rgba(255, 255, 255, 0.35);
      --b: #ffffff;
    }

    html, body {
      background-color: var(--bg) !important;
      margin: 0 !important;
      padding: 0 !important;
      width: 100%;
      height: 100%;
      overflow-x: hidden;
    }

    body {
      color: var(--t);
      font-family: var(--sans);
      display: flex;
      justify-content: center;
      align-items: flex-start;
    }

    /* Intro Screen */
    .intro-screen {
      position: fixed;
      inset: 0;
      background: #000000;
      z-index: 9999;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      transition: opacity 0.5s cubic-bezier(0.25, 1, 0.5, 1);
    }
    .intro-icon {
      width: 44px;
      height: 44px;
      object-fit: contain;
      filter: invert(1);
      mix-blend-mode: screen;
      opacity: 0.4;
      animation: pulseIcon 1.8s ease-in-out infinite;
      transition: transform 0.3s, opacity 0.3s;
    }
    .intro-screen:hover .intro-icon {
      transform: scale(1.08);
      opacity: 0.8;
    }
    @keyframes pulseIcon {
      0%, 100% { opacity: 0.3; transform: scale(0.95); }
      50% { opacity: 0.7; transform: scale(1.05); }
    }
    .intro-screen.hide {
      opacity: 0;
      pointer-events: none;
    }

    /* Grain */
    .grain {
      position: fixed; inset: 0; z-index: 1; pointer-events: none;
      opacity: 0.012;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    }

    /* Main Container */
    .wrap {
      width: 100%;
      max-width: 440px; 
      padding: 50px 16px;
      display: flex; flex-direction: column; gap: 14px;
      position: relative;
      z-index: 2;
      opacity: 0;
      transform: translateY(10px);
      transition: opacity 0.6s cubic-bezier(0.16, 1, 0.3, 1), transform 0.6s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .wrap.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* Banner */
    .banner-container {
      width: 100%;
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--border);
      aspect-ratio: 16 / 10;
      background: #000000;
    }
    .banner-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* Cards */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 20px;
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      transition: border-color 0.3s ease, background 0.3s ease;
    }
    .card:hover { 
      border-color: var(--border-bright); 
      background: var(--surface-hover);
    }

    .section-label {
      font-family: var(--mono);
      font-size: 9px; letter-spacing: 3px; text-transform: uppercase;
      color: var(--t); font-weight: 400; opacity: 0.6;
      margin-bottom: 12px; display: flex; align-items: center; gap: 8px;
    }
    .section-label::after {
      content: ''; flex: 1; height: 1px;
      background: linear-gradient(to right, var(--border), transparent);
    }

    /* Thought Text */
    .tagline {
      font-size: 14px;
      font-style: italic;
      font-weight: 300;
      color: var(--b);
      line-height: 1.6;
    }

    /* Links */
    .lnk {
      display: flex; align-items: center; justify-content: space-between;
      padding: 14px 16px;
      text-decoration: none; color: var(--t);
      background: rgba(255,255,255,0.002);
      border: 1px solid var(--border);
      border-radius: 10px;
      font-size: 13px;
      font-family: var(--mono);
      transition: all 0.3s cubic-bezier(0.25, 1, 0.5, 1);
    }
    .lnk:hover {
      border-color: var(--b);
      color: var(--b);
      transform: translateY(-1px);
      background: rgba(255,255,255,0.02);
    }
    .lnk-platform { color: var(--b); font-size: 13px; font-weight: 400; }
    .lnk-handle { color: var(--td); font-size: 11px; transition: color 0.3s; margin-right: auto; margin-left: 12px; }
    .lnk:hover .lnk-handle { color: var(--t); }
    .lnk-arrow { font-size: 11px; color: var(--td); transition: transform 0.3s, color 0.3s; }
    .lnk:hover .lnk-arrow { transform: translate(1px, -1px); color: var(--b); }
  </style>
</head>
<body>

<!-- Intro Screen -->
<div class="intro-screen" id="intro" onclick="enterSite()">
  <img src="1435385886551314542.webp" alt="Enter" class="intro-icon">
</div>

<div class="grain"></div>

<div class="wrap" id="main-wrap">

  <!-- Banner -->
  <div class="banner-container">
    <img src="einstein.jpg" alt="Banner" class="banner-img">
  </div>

  <!-- Thought Card -->
  <div class="card">
    <div class="section-label">Thought</div>
    <p class="tagline">"Try not to become a man of success, but rather try to become a man of value."</p>
  </div>

  <!-- Connect Card -->
  <div class="card">
    <div class="section-label">Connect</div>
    <a href="discord://~/users/118335032822700032" class="lnk">
      <span class="lnk-platform">Discord</span>
      <span class="lnk-handle">@eistenium</span>
      <span class="lnk-arrow">↗</span>
    </a>
  </div>

</div>

<script>
  function enterSite() {
    document.getElementById('intro').classList.add('hide');
    setTimeout(() => {
      document.getElementById('main-wrap').classList.add('show');
    }, 100);
  }
</script>

</body>
</html>
