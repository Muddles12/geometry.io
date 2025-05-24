<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Five Nights at Freddy's | Play Now</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #0d0d0d;
      --surface: #1a1a1a;
      --primary: #ff004f;
      --text: #f0f0f0;
      --muted: #888;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      padding: 2rem 1rem 1rem;
      text-align: center;
    }

    header h1 {
      font-size: 2.5rem;
      font-weight: 600;
      background: linear-gradient(to right, #ff004f, #ff8800);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .game-wrapper {
      position: relative;
      flex-grow: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 1rem;
    }

    .game-frame-container {
      position: relative;
      width: 100%;
      max-width: 1280px;
      height: 720px;
      background: #000;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 0 40px rgba(255, 0, 79, 0.15);
    }

    iframe {
      width: 100%;
      height: 100%;
      border: none;
    }

    .loader {
      position: absolute;
      inset: 0;
      background: #000;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 10;
    }

    .spinner {
      width: 50px;
      height: 50px;
      border: 6px solid #333;
      border-top: 6px solid var(--primary);
      border-radius: 50%;
      animation: spin 1s linear infinite;
      margin-bottom: 1rem;
    }

    .loading-text {
      color: var(--text);
      font-size: 1rem;
      opacity: 0.8;
    }

    footer {
      text-align: center;
      padding: 1rem;
      font-size: 0.9rem;
      color: var(--muted);
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }

    @media (max-width: 768px) {
      .game-frame-container {
        width: 100%;
        height: 60vh;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Five Nights at Freddy's</h1>
  </header>

  <main class="game-wrapper">
    <div class="game-frame-container">
      <div class="loader" id="loader">
        <div class="spinner"></div>
        <div class="loading-text">Loading Freddy’s systems...</div>
      </div>
      <iframe
        src="https://wellsousaaa.github.io/Five-Nights-at-Freddys-Web/"
        allowfullscreen
        onload="document.getElementById('loader').style.display='none';">
      </iframe>
    </div>
  </main>

  <footer>
    <p>© 2025 FNaF Game Portal. All rights reserved.</p>
  </footer>

</body>
</html>
