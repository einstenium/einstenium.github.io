<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>einstenium | Bio</title>
  
  <!-- Fontes originais do estilo do ServerSadzz -->
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
      --bg: #0a0a0c;
      --surface: rgba(255,255,255,0.03);
      --surface-hover: rgba(255,255,255,0.06);
      --border: rgba(255,255,255,0.08);
      --border-bright: rgba(255,255,255,0.18);
      --t: rgba(255,255,255,0.65);
      --td: rgba(255,255,255,0.3);
      --b: #f0ede6;
      --accent: #c9a96e;
      --accent-dim: rgba(201,169,110,0.15);
    }

    body {
      background: var(--bg);
      color: var(--t);
      font-family: var(--mono);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── VIDEO BG (O fundo animado do ServerSadzz) ── */
    .video-bg {
      position: fixed; inset: 0; z-index: -2; overflow: hidden;
    }
    .video-bg video {
      width: 100%; height: 100%; object-fit: cover;
      filter: brightness(0.35) saturate(0.6);
    }
    .video-bg::after {
      content: '';
      position: absolute; inset: 0;
      background:
        radial-gradient(ellipse 80% 60% at 50% 0%, rgba(10,10,12,0) 0%, rgba(10,10,12,0.7) 70%, rgba(10,10,12,1) 100%),
        linear-gradient(to bottom, rgba(10,10,12,0.3) 0%, rgba(10,10,12,0.6) 100%);
    }

    /* ── GRAIN (Efeito de estática/filme antigo) ── */
    .grain {
      position: fixed; inset: 0; z-index: -1; pointer-events: none;
      opacity: 0.04;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    }

    /* ── LAYOUT CONTAINER ── */
    .wrap {
      max-width: 440px; margin: 0 auto;
      padding: 72px 18px 80px;
      display: flex; flex-direction: column; gap: 10px;
    }

    /* ── PROFILE ── */
    .profile {
      display: flex; flex-direction: column; align-items: center;
      gap: 12px; padding: 32px 0 20px; text-align: center;
    }
    .avatar-wrap {
      position: relative; width: 88px; height: 88px;
    }
    .avatar {
      width: 100%; height: 100%;
      border-radius: 50%; object-fit: cover;
      border: 1px solid var(--border-bright);
    }
    .avatar-ring-deco {
      position: absolute; inset: -4px;
      border-radius: 50%;
      border: 1px solid var(--accent);
      opacity: 0.5;
      animation: ringPulse 3s ease-in-out infinite;
    }
    @keyframes ringPulse {
      0%,100% { transform: scale(1); opacity: 0.3; }
      50% { transform: scale(1.04); opacity: 0.6; }
    }
    .profile-name {
      font-family: var(--serif);
      font-size: 30px; font-weight: 400; font-style: italic;
      color: var(--b); letter-spacing: -0.5px;
    }

    /* ── CARD ── */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 20px 22px;
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
      transition: border-color 0.3s;
    }
    .card:hover { border-color: var(--border-bright); }

    .section-label {
      font-size: 9px; letter-spacing: 3.5px; text-transform: uppercase;
      color: var(--accent); font-weight: 500;
      margin-bottom: 14px; display: flex; align-items: center; gap: 8px;
    }
    .section-label::after {
      content: ''; flex: 1; height: 1px;
      background: linear-gradient(to right, var(--border-bright), transparent);
    }

    /* ── ABOUT ── */
    .tagline {
      font-family: var(--serif);
      font-size: 15px; font-style: italic; font-weight: 400;
      color: var(--b); line-height: 1.6;
    }

    /* ── LINKS ── */
    .lnk {
      display: flex; align-items: center; gap: 14px;
      padding: 12px 4px;
      text-decoration: none; color: var(--t);
      border-bottom: 1px solid var(--border);
      font-size: 13px; font-weight: 400; letter-spacing: 0.3px;
      transition: color 0.2s;
      position: relative; overflow: hidden;
    }
    .lnk::before {
      content: '';
      position: absolute; left: 0; top: 0; bottom: 0;
      width: 2px; background: currentColor;
      transform: scaleY(0); transform-origin: center;
      transition: transform 0.2s ease;
      opacity: 0.6;
    }
    .lnk:hover::before { transform: scaleY(1); }
    .lnk:last-child { border-bottom: none; }
    .lnk-platform { font-family: var(--serif); font-style: italic; color: var(--b); font-size: 14px; min-width: 64px; }
    .lnk-handle { flex: 1; color: var(--td); font-size: 12px; }
    .lnk-arrow { font-size: 11px; color: var(--td); }
    .lnk.dc:hover { color: #5865F2; }

    /* ── MUSIC PLAYER ── */
    .player {
      display: flex; flex-direction: column; gap: 14px;
    }
    .player-track {
      display: flex; gap: 14px; align-items: center;
    }
    .player-art {
      width: 52px; height: 52px; border-radius: 8px;
      object-fit: cover;
      border: 1px solid var(--border);
      flex-shrink: 0;
      transition: transform 0.3s;
    }
    .player-art.spinning {
      animation: vinylSpin 8s linear infinite;
    }
    @keyframes vinylSpin {
      to { transform: rotate(360deg); border-radius: 50%; }
    }
    .player-info { flex: 1; overflow: hidden; }
    .player-title {
      font-family: var(--serif); font-style: italic;
      font-size: 15px; color: var(--b); font-weight: 400;
      white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
      margin-bottom: 3px;
    }
    .player-artist {
      font-size: 11px; color: var(--td); letter-spacing: 1px;
      text-transform: uppercase;
    }
    .player-controls {
      display: flex; align-items: center; gap: 10px;
    }
    .ctrl-btn {
      background: var(--surface); border: 1px solid var(--border);
      color: var(--t); padding: 8px 18px;
      border-radius: 99px; cursor: pointer;
      font-family: var(--mono); font-size: 11px; letter-spacing: 1px;
      text-transform: uppercase;
      transition: background 0.2s, border-color 0.2s, color 0.2s;
    }
    .ctrl-btn:hover { background: var(--surface-hover); border-color: var(--border-bright); color: var(--b); }
    .ctrl-btn.primary {
      background: var(--accent-dim); border-color: rgba(201,169,110,0.3); color: var(--accent);
    }
    .ctrl-btn.primary:hover { background: rgba(201,169,110,0.25); }
    .player-progress {
      position: relative; height: 2px; background: var(--border); border-radius: 2px;
      cursor: pointer; overflow: hidden;
    }
    .player-progress-fill {
      position: absolute; left: 0; top: 0; bottom: 0;
      background: linear-gradient(to right, var(--accent), rgba(201,169,110,0.5));
      border-radius: 2px; width: 0%;
      transition: width 0.1s linear;
    }
    .player-time {
      display: flex; justify-content: space-between;
      font-size: 10px; color: var(--td); letter-spacing: 0.5px;
      margin-top: 5px;
    }
  </style>
</head>
<body>

<!-- Grain background overlay[cite: 1] -->
<div class="grain"></div>

<!-- Background Video original do ServerSadzz[cite: 1] -->
<div class="video-bg">
  <video id="bg-video" loop playsinline preload="auto" muted>
    <source src="https://files.catbox.moe/3xm2ia.mp4" type="video/mp4">
  </video>
</div>

<div class="wrap" id="wrap">

  <!-- Profile Area -->
  <div>
    <div class="profile">
      <div class="avatar-wrap">
        <div class="avatar-ring-deco"></div>
        <img src="93481932.webp" alt="einstenium" class="avatar">
      </div>
      <div class="profile-name">einstenium</div>
    </div>
  </div>

  <!-- About Card -->
  <div class="card">
    <div class="section-label">Sobre</div>
    <p class="tagline">"Imagination is more important than knowledge. For knowledge is limited, whereas imagination embraces the entire world."</p>
  </div>

  <!-- Links Card -->
  <div class="card">
    <div class="section-label">Links</div>
    <div>
      <a href="discord://~/users/118335032822700032" class="lnk dc">
        <span class="lnk-platform">Meu Discord</span>
        <span class="lnk-handle">@eistenium</span>
        <span class="lnk-arrow">↗</span>
      </a>
    </div>
  </div>

  <!-- Music Player Card (Música configurada: Ark Patrol - Let Go) -->
  <div class="card">
    <div class="section-label">Música</div>
    <div class="player">
      <div class="player-track">
        <img id="player-art" class="player-art" src="93481932.webp" alt="Album art">
        <div class="player-info">
          <div class="player-title" id="player-title">Let Go</div>
          <div class="player-artist" id="player-artist">Ark Patrol</div>
        </div>
      </div>
      <div>
        <div class="player-progress" id="progress-bar">
          <div class="player-progress-fill" id="progress-fill"></div>
        </div>
        <div class="player-time">
          <span id="time-cur">0:00</span>
          <span id="time-tot">0:00</span>
        </div>
      </div>
      <div class="player-controls">
        <button class="ctrl-btn primary" id="play-btn">Play</button>
      </div>
    </div>
  </div>

</div>

<script>
  // Script original adaptado do ServerSadzz para funcionar perfeitamente com a Let Go[cite: 1]
  const bgVideo = document.getElementById('bg-video');
  if (bgVideo) { bgVideo.play().catch(()=>{}); }

  // Configuração direta do arquivo funcional de Let Go
  const audio = new Audio("https://pub-c06a9289a2444db8867a54a01c3bf680.r2.dev/Let%20Go.mp3");
  audio.loop = true;

  let playing = false;
  const playBtn  = document.getElementById('play-btn');
  const artImg   = document.getElementById('player-art');
  const progFill = document.getElementById('progress-fill');
  const timeCur  = document.getElementById('time-cur');
  const timeTot  = document.getElementById('time-tot');
  const progBar  = document.getElementById('progress-bar');

  function fmt(s) {
    const m = Math.floor(s/60), sec = Math.floor(s%60);
    return m+':'+(sec<10?'0':'')+sec;
  }

  function togglePlay() {
    if (playing) {
      audio.pause(); 
      playing = false;
      playBtn.textContent = 'Play';
      artImg.classList.remove('spinning');
    } else {
      audio.play().then(() => {
        playing = true; 
        playBtn.textContent = 'Pause';
        artImg.classList.add('spinning');
      }).catch((e)=>console.log("Erro ao tocar:", e));
    }
  }

  audio.addEventListener('timeupdate', () => {
    if (!audio.duration) return;
    const pct = (audio.currentTime / audio.duration) * 100;
    progFill.style.width = pct + '%';
    timeCur.textContent = fmt(audio.currentTime);
    timeTot.textContent = fmt(audio.duration);
  });

  progBar.addEventListener('click', e => {
    if (!audio.duration) return;
    const rect = progBar.getBoundingClientRect();
    audio.currentTime = ((e.clientX - rect.left) / rect.width) * audio.duration;
  });

  playBtn.addEventListener('click', togglePlay);
</script>

</body>
</html>
