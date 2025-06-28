# site-para-camillyy
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para Camilly 💜</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Georgia&display=swap" rel="stylesheet">
  <style>
    html, body {
      min-height: 100vh;
      margin: 0;
      padding: 0;
      font-family: 'Georgia', serif;
      color: #f0d6e0;
      background: linear-gradient(120deg, #0d0d0d, #29001a, #1a001f, #ff66c4);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      overflow-x: hidden;
    }
    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }
    .particles {
      position: fixed;
      top: 0; left: 0; width: 100vw; height: 100vh;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }
    .particle {
      position: absolute;
      border-radius: 50%;
      opacity: 0.5;
      animation: float 12s linear infinite;
      background: radial-gradient(circle, #ff66c4 0%, #ff1a75 100%);
    }
    .particle:nth-child(1) { width: 60px; height: 60px; left: 10vw; top: 80vh; animation-duration: 14s; }
    .particle:nth-child(2) { width: 40px; height: 40px; left: 80vw; top: 60vh; animation-duration: 10s; }
    .particle:nth-child(3) { width: 80px; height: 80px; left: 50vw; top: 90vh; animation-duration: 18s; }
    .particle:nth-child(4) { width: 30px; height: 30px; left: 70vw; top: 95vh; animation-duration: 12s; }
    .particle:nth-child(5) { width: 100px; height: 100px; left: 20vw; top: 85vh; animation-duration: 20s; }
    @keyframes float {
      0% { transform: translateY(0) scale(1);}
      100% { transform: translateY(-110vh) scale(1.2);}
    }
    header {
      background: linear-gradient(to right, #29001a, #1a001f);
      text-align: center;
      padding: 60px 20px 30px 20px;
      position: relative;
      z-index: 1;
    }
    header h1 {
      font-family: 'Pacifico', cursive;
      font-size: 3em;
      color: #ff4da6;
      text-shadow: 0 0 10px #ff66c4, 0 0 20px #ff66c4;
      margin-bottom: 10px;
    }
    .heart-container {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-bottom: 10px;
    }
    .heart {
      width: 60px;
      height: 54px;
      position: relative;
      display: inline-block;
      animation: pulse 1.2s infinite;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      left: 30px;
      top: 0;
      width: 30px;
      height: 48px;
      background: #ff1a75;
      border-radius: 30px 30px 0 0;
      transform: rotate(-45deg);
      box-shadow: -8px -14px 10px 0 black inset;
    }
    .heart::after {
      left: 0;
      transform: rotate(45deg);
      box-shadow: -15px 10px 14px 0 black inset;
    }
    @keyframes pulse {
      0% { transform: scale(1);}
      50% { transform: scale(1.15);}
      100% { transform: scale(1);}
    }
    .audio-btn {
      background: #ff66c4;
      color: #fff;
      border: none;
      padding: 10px 24px;
      border-radius: 24px;
      cursor: pointer;
      font-size: 1.1em;
      margin-top: 10px;
      transition: background 0.3s;
      box-shadow: 0 2px 8px #1a001f44;
      z-index: 2;
      position: relative;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }
    .audio-btn:hover {
      background: #ff1a75;
    }
    section {
      padding: 40px 20px;
      max-width: 800px;
      margin: auto;
      position: relative;
      z-index: 1;
    }
    h2 {
      color: #ff66c4;
      font-family: 'Pacifico', cursive;
      border-bottom: 1px solid #ff66c4;
      padding-bottom: 10px;
      margin-top: 0;
    }
    p {
      font-size: 1.2em;
      line-height: 1.6;
    }
    footer {
      text-align: center;
      padding: 30px;
      color: #999;
      font-size: 0.9em;
      position: relative;
      z-index: 1;
    }
    @media (max-width: 600px) {
      header h1 { font-size: 2em; }
      .heart { width: 40px; height: 36px; }
      section { padding: 24px 8px; }
    }
  </style>
</head>
<body>

<!-- Fundo animado com partículas -->
<div class="particles">
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
  <div class="particle"></div>
</div>

<header>
  <h1>Para Camilly 💖</h1>
  <div class="heart-container">
    <div class="heart"></div>
  </div>
  <button class="audio-btn" id="audioBtn">
    <span id="audioIcon">▶️</span> Ouvir música especial
  </button>
  <!-- Player do YouTube oculto -->
  <div id="ytplayer" style="width:0;height:0;overflow:hidden;"></div>
</header>

<section>
  <h2>Nossa História</h2>
  <p>Nos conhecemos há alguns anos, mas foi em <strong>28/12/2024</strong> que começamos a conversar de verdade. Com o tempo, nos aproximamos cada vez mais, e no dia <strong>30/05/2025</strong> algo especial aconteceu. Desde então, você tem sido o sol na minha escuridão e a paz no meu caos.</p>
</section>

<section>
  <h2>Momentos Juntos</h2>
  <p>Cada conversa, cada olhar, cada sorriso… tudo com você é mágico. Você transforma meus dias e faz meu coração bater mais forte. Nossa conexão é única, como se as estrelas tivessem nos unido por destino.</p>
</section>

<section>
  <h2>Declaração de Amor</h2>
  <p>Camilly, eu te amo com uma intensidade que palavras não conseguem descrever. Você é meu abrigo, minha inspiração, minha razão de sorrir. Prometo te amar em cada fase, cada dia, cada noite — para sempre.</p>
</section>

<section>
  <h2>Mensagem Final</h2>
  <p>Este site é só um pedacinho do que sinto por você. Espero que ele te faça sorrir e lembre que meu coração é todo seu. 💘</p>
</section>

<footer>
  Feito com amor por alguém que nunca vai parar de te amar. 🌹
</footer>

<!-- YouTube IFrame API -->
<script src="https://www.youtube.com/iframe_api"></script>
<script>
  let player;
  let isPlaying = false;
  // ID do vídeo do YouTube fornecido
  const YT_VIDEO_ID = "EknM0uyi93M";

  function onYouTubeIframeAPIReady() {
    player = new YT.Player('ytplayer', {
      height: '0',
      width: '0',
      videoId: YT_VIDEO_ID,
      playerVars: {
        'autoplay': 0,
        'controls': 0,
        'loop': 1,
        'playlist': YT_VIDEO_ID
      },
      events: {
        'onReady': onPlayerReady,
        'onStateChange': onPlayerStateChange
      }
    });
  }

  function onPlayerReady(event) {
    // Nada a fazer aqui, só inicialização
  }

  function onPlayerStateChange(event) {
    const icon = document.getElementById('audioIcon');
    const btn = document.getElementById('audioBtn');
    if (event.data === YT.PlayerState.PLAYING) {
      icon.textContent = '⏸️';
      btn.childNodes[1].nodeValue = ' Pausar música';
      isPlaying = true;
    } else {
      icon.textContent = '▶️';
      btn.childNodes[1].nodeValue = ' Ouvir música especial';
      isPlaying = false;
    }
  }

  document.getElementById('audioBtn').addEventListener('click', function() {
    if (player) {
      if (!isPlaying) {
        player.playVideo();
      } else {
        player.pauseVideo();
      }
    }
  });
</script>
</body>
</html>
