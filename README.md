<!DOCTYPE html>
<html lang="en">
<head>
  <meta name='admaven-placement' content=BqdY6rTr8>
  <meta charset="UTF-8" />
  <title>Unblocked Games</title>
  <h1>Trouble loading?  Try refreshing the page</h1>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- ✅ Google AdSense Script -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-4623021982506157"
     crossorigin="anonymous"></script>

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

    .game-column {
      display: flex;
      flex-direction: column;
      align-items: center;
      flex: 1;
      max-width: 1024px;
    }

    .game-wrapper {
      width: 100%;
      background-color: #000;
      border: 3px solid #222;
      border-radius: 8px;
      overflow: hidden;
      position: relative;
      max-width: 100%;
    }

    iframe {
      width: 100%;
      height: 500px;
      border: none;
      display: block;
    }

    .fullscreen-btn {
      margin-top: 0.75rem;
      padding: 10px 20px;
      background-color: black;
      color: white;
      border: 2px solid white;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .fullscreen-btn:hover {
      background-color: #111;
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
    Mini Football - Unblocked
  </header>

  <div class="container">
    <div class="ad">Ad Space</div>

    <div class="game-column">
      <div class="game-wrapper" id="gameContainer">
        <iframe
          id="gameFrame"
          src="https://ubg98.github.io/super-liquid-soccer-unblockedz.html"
          allow="fullscreen"
          allowfullscreen
          allowtransparency="true">
        </iframe>

      </div>

      <button class="fullscreen-btn" onclick="openFullscreen()">
        Open Fullscreen
      </button>
    </div>

    <div class="ad">Ad Space</div>
  </div>

  <script>
    function openFullscreen() {
      const iframe = document.getElementById('gameFrame');
      if (iframe.requestFullscreen) {
        iframe.requestFullscreen();
      } else if (iframe.mozRequestFullScreen) {
        iframe.mozRequestFullScreen();
      } else if (iframe.webkitRequestFullscreen) {
        iframe.webkitRequestFullscreen();
      } else if (iframe.msRequestFullscreen) {
        iframe.msRequestFullscreen();
      } else {
        // fallback: open in new tab
        window.open(iframe.src, '_blank');
      }
    }
  </script>

</body>
</html>
