<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>ORION</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Orbitron', sans-serif;
      background: radial-gradient(ellipse at center, #001100 0%, #000000 100%);
      color: #0f0;
      text-shadow: 0 0 5px #0f0;
      animation: pulse 5s infinite;
      overflow-x: hidden;
    }

    @keyframes pulse {
      0% { background-color: #001100; }
      50% { background-color: #002200; }
      100% { background-color: #001100; }
    }

    @keyframes flicker {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.98; }
    }

    header {
      background: #000;
      border-bottom: 2px solid #0f0;
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      color: #0f0;
    }

    .marquee {
      background: #003300;
      color: #0f0;
      padding: 5px;
      font-size: 14px;
      border-top: 1px solid #0f0;
      border-bottom: 1px solid #0f0;
    }

    .terminal-message {
      background-color: rgba(0, 255, 0, 0.1);
      border: 1px solid #0f0;
      padding: 10px;
      margin: 20px;
      font-family: monospace;
    }

    .online-counter {
      position: absolute;
      top: 10px;
      right: 20px;
      background: #002200;
      padding: 5px 10px;
      border: 1px solid #0f0;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">ORION</div>
    <div class="online-counter">Онлайн: <span id="onlineCount">...</span></div>
  </header>

  <div class="marquee">
    <marquee behavior="scroll" direction="left">
      ⚡ Турнир начинается в пятницу! 🕹️ Успей зарегистрироваться! 🛡️
    </marquee>
  </div>

  <div class="terminal-message">
    [BOT] Турнир начнется через 3 дня. Будь готов!
  </div>

  <script>
    // Простой рандомный онлайн-счетчик
    function updateOnlineCounter() {
      const online = Math.floor(Math.random() * 100) + 20;
      document.getElementById("onlineCount").textContent = online;
    }
    setInterval(updateOnlineCounter, 3000);
    updateOnlineCounter();
  </script>
</body>
</html>
