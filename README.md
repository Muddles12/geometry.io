<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Five Nights at Freddy's - Web Version</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    html, body {
      margin: 0;
      padding: 0;
      background: #000;
      color: #fff;
      font-family: 'Segoe UI', sans-serif;
      height: 100%;
    }

    header {
      text-align: center;
      padding: 1.5rem 1rem;
      background-color: #111;
      font-size: 2rem;
      font-weight: bold;
      color: #ff004f;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 1rem;
      gap: 1rem;
    }

    .ad {
      width: 160px;
      height: 600px;
      background-color: #1a1a1a;
      border: 2px dashed #444;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.9rem;
      color: #888;
    }

    .game-wrapper {
      flex: 1;
      max-width: 1024px;
      aspect-ratio: 16 / 9;
      background-color: #000;
      border: 3px solid #222;
      border-radius: 8px;
      overflow: hidden;
      position: relative;
    }

    iframe {
      width: 100%;
      height: 100%;
      border: none;
      display: block;
    }

    #loader {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: #000;
      z-index: 10;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 1.2rem;
      color: #fff;
    }

    .spinner {
      width: 40px;
      height: 40px;
      border: 5px solid #333;
      border-top: 5px solid #ff004f;
      border-radius: 50%;
      animation: spin 1s linear infinite;
      margin-right: 1rem;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }

    .fullscreen-btn {
      position: absolute;
      bottom: 10px;
      right: 10px;
      background: #222;
      border: 1px solid #555;
      padding: 6px 12px;
      color: white;
      font-size: 14px;
      cursor: pointer;
      border-radius: 4px;
      z-index: 20;
    }

    @media (max-width: 900px) {
      .ad {
        display: none;
      }

      .container {
        flex-direction: column;
        align-items: center;
      }

      .game-wrapper {
        width: 100%;
        max-width: 100%;
      }
    }
  </style>
</head>
<body>

  <header>
    Five Nights at Freddy's
  </header>

  <div class="container">
    <div class="ad">Ad Space</div>

    <div class="game-wrapper" id="gameContainer">
      <div id="loader">
        <div class="spinner"></div>
        Loading game...
      </div>
      <iframe
        id="gameFrame"
        src="https://wellsousaaa.github.io/Five-Nights-at-Freddys-Web/"
        allowfullscreen
        onload="hideLoader()">
      </iframe>
      <button class="fullscreen-btn" onclick="openFullscreen()">Fullscreen</button>
    </div>

    <div class="ad">Ad Space</div>
  </div>

  <script>
    function hideLoader() {
      const loader = document.getElementById('loader');
      if (loader) loader.style.display = 'none';
    }

    function openFullscreen() {
      const iframe = document.getElementById("gameFrame");
      if (iframe.requestFullscreen) {
        iframe.requestFullscreen();
      } else if (iframe.mozRequestFullScreen) {
        iframe.mozRequestFullScreen();
      } else if (iframe.webkitRequestFullscreen) {
        iframe.webkitRequestFullscreen();
      } else if (iframe.msRequestFullscreen) {
        iframe.msRequestFullscreen();
      }
    }
  </script>

</body>
</html>
