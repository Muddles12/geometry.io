<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Five Nights at Freddy's - Fullscreen</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    html, body {
      margin: 0;
      padding: 0;
      background: #000;
      height: 100%;
      overflow: hidden;
    }

    #gameFrame {
      position: absolute;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      border: none;
    }

    #loader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: #000;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-family: sans-serif;
      font-size: 1.5rem;
      z-index: 9999;
    }

    .spinner {
      width: 48px;
      height: 48px;
      border: 6px solid #444;
      border-top: 6px solid #ff004f;
      border-radius: 50%;
      animation: spin 1s linear infinite;
      margin-right: 1rem;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }
  </style>
</head>
<body>

  <div id="loader">
    <div class="spinner"></div>
    Loading FNaF...
  </div>

  <iframe
    id="gameFrame"
    src="https://wellsousaaa.github.io/Five-Nights-at-Freddys-Web/"
    allowfullscreen
    onload="document.getElementById('loader').style.display='none';">
  </iframe>

</body>
</html>
