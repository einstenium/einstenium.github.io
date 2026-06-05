<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>einstenium | Bio</title>
  
  <!-- Fontes Gringas Minimalistas -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@300;400;500&family=Playfair+Display:ital,wght@1,400;1,600&display=swap" rel="stylesheet">

  <style>
    *, *::before, *::after {
      margin: 0; padding: 0;
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    :root {
      --serif: 'Playfair Display', Georgia, serif;
      --mono: 'DM Mono', 'Courier New', monospace;
      --bg: #000000;
      --surface: rgba(255, 255, 255, 0.02);
      --surface-hover: rgba(255, 255, 255, 0.05);
      --border: rgba(255, 255, 255, 0.06);
      --border-bright: rgba(255, 255, 255, 0.2);
      --t: rgba(255, 255, 255, 0.65);
      --td: rgba(255, 255, 255, 0.35);
      --b: #ffffff; /* Branco puro no lugar do dourado/amarelo */
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
      font-family: var(--mono);
      display: flex;
      justify-content: center;
      align-items: flex-start;
    }

    /* Tela de Entrada Baseada no Ícone */
    .intro-screen {
      position: fixed;
      inset: 0;
      background: #000000;
      z-index: 9999;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      cursor: pointer;
      transition: opacity 0.6s cubic-bezier(0.25, 1, 0.5, 1), transform 0.6s cubic-bezier(0.25, 1, 0.5, 1);
    }
    .intro-icon {
      width: 42px;
      height: 42px;
      object-fit: contain;
      opacity: 0.5;
      animation: pulseIcon 2s ease-in-out infinite;
      transition: transform 0.3s, opacity 0.3s;
    }
    .intro-screen:hover .intro-icon {
      transform: scale(1.1);
      opacity: 0.9;
    }
    @keyframes pulseIcon {
      0%, 100% { opacity: 0.3; transform: scale(0.96); }
      50% { opacity: 0.8; transform: scale(1.04); }
    }
    .intro-screen.hide {
      opacity: 0;
      transform: scale(1.02);
      pointer-events: none;
    }

    /* Grão estático sutil de fundo */
    .grain {
      position: fixed; inset: 0; z-index: 1; pointer-events: none;
      opacity: 0.015;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    }

    /* Container Principal */
    .wrap {
      width: 100%;
      max-width: 440px; 
      padding: 50px 16px;
      display: flex; flex-direction: column; gap: 14px;
      position: relative;
      z-index: 2;
      opacity: 0;
      transform: translateY(10px);
      transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .wrap.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* Banner Atualizado */
    .banner-container {
      width: 100%;
      border-radius: 14px;
      overflow: hidden;
      border: 1px solid var(--border);
      aspect-ratio: 16 / 10;
      background: #050505;
    }
    .banner-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* Nome do perfil embaixo do banner */
    .profile-title {
      font-family: var(--serif);
      font-size: 25px; font-style: italic;
      color: var(--b); text-align: center;
      margin: 4px 0 2px 0;
      letter-spacing: -0.3px;
    }

    /* Cards */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 20px;
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      transition: border-color 0.3s ease, background 0.3s ease;
    }
    .card:hover { 
      border-color: var(--border-bright); 
      background: var(--surface-hover);
    }

    /* Labels sem o amarelo antigo */
    .section-label {
      font-size: 9px; letter-spacing: 4px; text-transform: uppercase;
      color: var(--t); font-weight: 500; opacity: 0.8;
      margin-bottom: 12px; display: flex; align-items: center; gap: 8px;
    }
    .section-label::after {
      content: ''; flex: 1; height: 1px;
      background: linear-gradient(to right, var(--border), transparent);
    }

    /* Frase */
    .tagline {
      font-family: var(--serif);
      font-size: 15px; font-style: italic; font-weight: 400;
      color: var(--b); line-height: 1.6;
    }

    /* Links Estilo Botão Clean Mono */
    .lnk {
      display: flex; align-items: center; justify-content: space-between;
      padding: 15px;
      text-decoration: none; color: var(--t);
      background: rgba(255,255,255,0.005);
      border: 1px solid var(--border);
      border-radius: 10px;
      font-size: 13px; 
      transition: all 0.3s cubic-bezier(0.25, 1, 0.5, 1);
    }
    .lnk:hover {
      border-color: var(--b);
      color: var(--b);
      transform: translateY(-1px);
      background: rgba(255,255,255,0.02);
    }
    .lnk-platform { font-family: var(--serif); font-style: italic; color: var(--b); font-size: 14px; }
    .lnk-handle { color: var(--td); font-size: 12px; transition: color 0.3s; }
    .lnk:hover .lnk-handle { color: var(--t); }
    .lnk-arrow { font-size: 11px; color: var(--td); transition: transform 0.3s, color 0.3s; }
    .lnk:hover .lnk-arrow { transform: translate(1px, -1px); color: var(--b); }
  </style>
</head>
<body>

<!-- Tela de Entrada Animada -->
<div class="intro-screen" id="intro" onclick="enterSite()">
  <img src="1435385886551314542.webp" alt="Entrar" class="intro-icon">
</div>

<!-- Efeito de grão discreto -->
<div class="grain"></div>

<!-- Conteúdo Principal -->
<div class="wrap" id="main-wrap">

  <!-- Banner Corrigido -->
  <div class="banner-container">
    <img src="einstein.jpg" alt="Banner" class="banner-img">
  </div>

  <div class="profile-title">einstenium</div>

  <!-- Frase -->
  <div class="card">
    <div class="section-label">Pensamento</div>
    <p class="tagline">"Procure ser uma pessoa de valor, em vez de procurar ser uma pessoa de sucesso."</p>
  </div>

  <!-- Links -->
  <div class="card">
    <div class="section-label">Conectar</div>
    <a href="discord://~/users/118335032822700032" class="lnk">
      <span class="lnk-platform">Discord</span>
      <span class="lnk-handle">@eistenium</span>
      <span class="lnk-arrow">↗</span>
    </a>
  </div>

</div>

<script>
  function enterSite() {
    // Esconde a tela do ícone
    document.getElementById('intro').classList.add('hide');
    // Mostra o site com a transição fluida
    setTimeout(() => {
      document.getElementById('main-wrap').classList.add('show');
    }, 150);
  }
</script>

</body>
</html>
