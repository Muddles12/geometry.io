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
      overflow-x: hidden;
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
      animation: fadeUp 1s ease-out;
    }

    iframe {
      width: 100%;
      height: 720px;
      border: none;
      border-radius: 12px;
      background: #000;
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

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 768px) {
      iframe {
        height: 500px;
      }

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
      <iframe src="https://wellsousaaa.github.io/Five-Nights-at-Freddys-Web/" allowfullscreen></iframe>
    </div>
  </main>

  <footer>
    <p>© 2025 YourGameSite. All rights reserved. Play responsibly.</p>
  </footer>

</body>
</html>
