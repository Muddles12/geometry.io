<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Five Nights at Freddy's | Play Now</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0d0d0d;
      --surface: #1a1a1a;
      --primary: #ff004f;
      --text: #f0f0f0;
      --muted: #888;
      --radius: 16px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(160deg, #0d0d0d 0%, #121212 100%);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      padding: 2rem 1rem 1rem;
      text-align: center;
      animation: fadeIn 1s ease-in-out;
    }

    header h1 {
      font-size: 2.8rem;
      font-weight: 600;
      background: linear-gradient(to right, #ff004f, #ff8800);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    main {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 1rem;
    }

    .game-container {
      width: 100%;
      max-width: 960px;
      background: var(--surface);
      padding: 1.5rem;
      border-radius: var(--radius);
      box-shadow: 0 20px 50px rgba(255, 0, 79, 0.1);
      position: relative;
    }

    .iframe-wrapper {
      position: relative;
      width: 100%;
      padding-bottom: 56.25%;
      height: 0;
      border-radius: 12px;
      background: #000;
    }

    iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: none;
      border-radius: 12px;
    }

    .loader {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #000;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 10;
      border-radius: 12px;
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
      font-size: 1.1rem;
      opacity: 0.8;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    footer {
      text-align: center;
      padding: 2rem 1rem 1rem;
      font-size: 0.9rem;
      color: var(--muted);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Five Nights at Freddy's</h1>
  </header>

  <main>
    <div class="game-container">
      <div class="iframe-wrapper">
        <div class="loader" id="loader">
          <div class="spinner"></div>
          <div class="loading-text">Loading...</div>
        </div>
        <iframe 
          src="https://wellsousaaa.github.io/Five-Nights-at-Freddys-Web/" 
          allowfullscreen 
          onload="document.getElementById('loader').style.display='none';">
        </iframe>
      </div>
    </div>
  </main>

  <footer>
    <p>© 2025 YourGameSite. All rights reserved. Play responsibly.</p>
  </footer>

</body>
</html>
