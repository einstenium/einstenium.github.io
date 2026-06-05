
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>einstenium | Bio</title>
  
  <!-- Fontes Gringas e Minimalistas -->
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
      --bg: #000000; /* Fundo todo preto puro como pediu */
      --surface: rgba(255, 255, 255, 0.02);
      --surface-hover: rgba(255, 255, 255, 0.05);
      --border: rgba(255, 255, 255, 0.05);
      --border-bright: rgba(255, 255, 255, 0.15);
      --t: rgba(255, 255, 255, 0.6);
      --td: rgba(255, 255, 255, 0.3);
      --b: #f0ede6;
      --accent: #c9a96e;
    }

    /* Reset total para sumir com qualquer linha azul ou margem do GitHub */
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

    /* Grão estático bem sutil de fundo */
    .grain {
      position: fixed; inset: 0; z-index: 1; pointer-events: none;
      opacity: 0.02;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    }

    /* Container Principal com animação de entrada */
    .wrap {
      width: 100%;
      max-width: 450px; 
      padding: 40px 16px;
      display: flex; flex-direction: column; gap: 14px;
      position: relative;
      z-index: 2;
      animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Banner do Einstein no Topo */
    .banner-container {
      width: 100%;
      border-radius: 16px;
      overflow: hidden;
      border: 1px solid var(--border);
      position: relative;
      aspect-ratio: 16 / 10;
    }
    .banner-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform 0.5s ease;
    }
    .banner-container:hover .banner-img {
      transform: scale(1.03);
    }

    /* Card de Conteúdo */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 22px;
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      transition: border-color 0.3s ease, background 0.3s ease;
    }
    .card:hover { 
      border-color: var(--border-bright); 
      background: var(--surface-hover);
    }

    .section-label {
      font-size: 9px; letter-spacing: 4px; text-transform: uppercase;
      color: var(--accent); font-weight: 500;
      margin-bottom: 12px; display: flex; align-items: center; gap: 8px;
    }
    .section-label::after {
      content: ''; flex: 1; height: 1px;
      background: linear-gradient(to right, var(--border-bright), transparent);
    }

    /* Frase de Respeito */
    .tagline {
      font-family: var(--serif);
      font-size: 16px; font-style: italic; font-weight: 400;
      color: var(--b); line-height: 1.6;
    }

    /* Links Estilo Botão Clean com Animação Smooth */
    .lnk {
      display: flex; align-items: center; justify-content: space-between;
      padding: 16px;
      text-decoration: none; color: var(--t);
      background: rgba(255,255,255,0.01);
      border: 1px solid var(--border);
      border-radius: 12px;
      font-size: 13px; 
      transition: all 0.3s cubic-bezier(0.25, 1, 0.5, 1);
    }
    .lnk:hover {
      border-color: var(--b);
      color: var(--b);
      transform: translateY(-2px);
      background: rgba(255,255,255,0.03);
      box-shadow: 0 10px 20px rgba(0,0,0,0.5);
    }
    .lnk-platform { font-family: var(--serif); font-style: italic; color: var(--b); font-size: 15px; }
    .lnk-handle { color: var(--td); font-size: 12px; transition: color 0.3s; }
    .lnk:hover .lnk-handle { color: var(--t); }
    .lnk-arrow { font-size: 12px; color: var(--td); transition: transform 0.3s; }
    .lnk:hover .lnk-arrow { transform: translate(2px, -2px); color: var(--b); }

    /* Nome do perfil minimalista embaixo do banner */
    .profile-title {
      font-family: var(--serif);
      font-size: 26px; font-style: italic;
      color: var(--b); text-align: center;
      margin: 6px 0;
    }
  </style>
</head>
<body>

<div class="grain"></div>

<div class="wrap">

  <!-- Banner Novo (Suxando direto o arquivo do seu GitHub) -->
  <div class="banner-container">
    <img src="▷ Frases Bonitas de los Mejores Autores.jpg" alt="einstenium" class="banner-img">
  </div>

  <div class="profile-title">einstenium</div>

  <!-- Frase Atualizada -->
  <div class="card">
    <div class="section-label">Pensamento</div>
    <p class="tagline">"Procure ser uma pessoa de valor, em vez de procurar ser uma pessoa de sucesso."</p>
  </div>

  <!-- Links Secundários -->
  <div class="card">
    <div class="section-label">Conectar</div>
    <a href="discord://~/users/118335032822700032" class="lnk">
      <span class="lnk-platform">Discord</span>
      <span class="lnk-handle">@eistenium</span>
      <span class="lnk-arrow">↗</span>
    </a>
  </div>

</div>

</body>
</html>
