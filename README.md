<!DOCTYPE html>
<html lang="az">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>MyRadioStream Canlı Yayım</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    body {
      margin: 0;
      height: 100vh;
      overflow: hidden;
      background: linear-gradient(135deg, #FF7E5F, #FD3A69);
      font-family: 'Poppins', sans-serif;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      perspective: 1200px;
    }

    .background-text {
      position: absolute;
      top: 50%;
      left: 50%;
      font-size: 12vw;
      font-weight: 900;
      color: rgba(255, 255, 255, 0.07);
      user-select: none;
      transform: translate(-50%, -50%) rotate(-10deg);
      white-space: nowrap;
      animation: floatText 10s ease-in-out infinite alternate;
      letter-spacing: 0.5em;
      filter: drop-shadow(0 0 5px rgba(255, 150, 50, 0.3));
    }

    @keyframes floatText {
      0% {
        transform: translate(-50%, -50%) rotate(-10deg) translateY(0);
      }
      100% {
        transform: translate(-50%, calc(-50% + 20px)) rotate(-10deg);
      }
    }

    h1 {
      position: relative;
      font-size: 3rem;
      margin-bottom: 25px;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: #FFB86C;
      text-shadow:
        0 0 5px #FF7E5F,
        0 0 15px #FF7E5F,
        0 0 30px #FD3A69;
      animation: glow 3s ease-in-out infinite alternate;
      z-index: 10;
      user-select: none;
    }

    @keyframes glow {
      0% {
        text-shadow:
          0 0 5px #FF7E5F,
          0 0 15px #FF7E5F,
          0 0 30px #FD3A69;
      }
      100% {
        text-shadow:
          0 0 15px #FFD6A5,
          0 0 40px #FFB86C,
          0 0 70px #FF8C42;
      }
    }

    .player-container {
      position: relative;
      background: rgba(255, 140, 66, 0.2);
      border-radius: 25px;
      padding: 35px 40px;
      width: 360px;
      max-width: 90vw;
      box-shadow:
        0 0 30px rgba(255, 140, 66, 0.6),
        inset 0 0 20px rgba(255, 140, 66, 0.3);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      transition: transform 0.35s ease;
      z-index: 10;
      overflow: hidden;
    }

    .player-container:hover {
      transform: scale(1.07) rotateY(8deg);
      box-shadow:
        0 0 50px rgba(255, 160, 80, 0.9),
        inset 0 0 30px rgba(255, 160, 80, 0.6);
    }

    /* Musiqi adı yazısının üstünü örtmək üçün qatı qatırıq */
    .overlay-block {
      position: absolute;
      top: 10px; left: 0; right: 0;
      height: 30px;
      background: linear-gradient(90deg, rgba(255, 140, 66, 0.9), rgba(255, 140, 66, 0.9));
      pointer-events: none;
      z-index: 20;
      border-radius: 15px 15px 0 0;
    }

    footer {
      position: relative;
      margin-top: 30px;
      font-size: 1rem;
      font-style: italic;
      color: #FFB86C;
      text-align: center;
      user-select: none;
      z-index: 10;
      text-shadow: 0 0 8px rgba(255, 184, 108, 0.5);
    }

    @media (max-width: 400px) {
      h1 {
        font-size: 2.2rem;
      }
      .player-container {
        width: 90vw;
        padding: 25px 20px;
      }
      .background-text {
        font-size: 10vw;
      }
    }
  </style>
</head>
<body>
  <div class="background-text">SÖZ-SÜZ</div>

  <div style="text-align: center;">
    <h1>MyRadioStream</h1>

    <div class="player-container">
      <script src="//myradiostream.com/embed/adobevusal"></script>
      <div class="overlay-block"></div>
    </div>

    <footer>Canlı yayım - Dinlə və zövq al!</footer>
  </div>
</body>
</html>
