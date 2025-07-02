# vibenest
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>VibeNest</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #0f0f0f, #1f1f1f);
      color: #fff;
      margin: 0;
      padding: 0;
    }

    header {
      text-align: center;
      padding: 2rem;
      background: #121212;
      box-shadow: 0 2px 10px rgba(0,0,0,0.7);
    }

    header h1 {
      font-size: 2.5rem;
      color: #f75bff;
    }

    .playlist-section {
      padding: 2rem;
    }

    h2 {
      border-bottom: 1px solid #f75bff;
      padding-bottom: 0.5rem;
      margin-bottom: 1rem;
    }

    iframe {
      width: 100%;
      max-width: 100%;
      height: 450px;
      border-radius: 10px;
      margin-bottom: 2rem;
      border: none;
    }

    .follow-btn {
      display: inline-block;
      padding: 0.7rem 1.2rem;
      margin: 1rem 0;
      background: #f75bff;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .follow-btn:hover {
      background: #d247e6;
    }

    .followers {
      font-size: 1rem;
      color: #ccc;
    }
  </style>
</head>
<body>

  <header>
    <h1>🎶 VibeNest</h1>
    <button class="follow-btn" onclick="follow()">+ Follow</button>
    <p class="followers" id="followerCount">Followers: 0</p>
  </header>

  <div class="playlist-section">
    <h2>Deep End</h2>
    <iframe allow="autoplay *; encrypted-media *;" frameborder="0" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-top-navigation-by-user-activation"
      src="https://embed.music.apple.com/za/playlist/deep-end/pl.u-gxblVM0Tb7oa1m1"></iframe>

    <h2>Brick Talk</h2>
    <iframe src="https://embed.music.apple.com/za/playlist/brick-talk-2-0/pl.u-GgA54PbfoAKYg6g"></iframe>
    <iframe src="https://embed.music.apple.com/za/playlist/brick-talk-2-5/pl.u-GgA545auoAKYg6g"></iframe>
    <iframe src="https://embed.music.apple.com/za/playlist/brick-talk-3-0/pl.u-2aoqRP6sGxg0MrM"></iframe>
  </div>

  <script>
    // Simple follow button counter (local)
    let count = localStorage.getItem('followers') || 0;
    const display = document.getElementById('followerCount');
    display.innerText = `Followers: ${count}`;

    function follow() {
      count++;
      localStorage.setItem('followers', count);
      display.innerText = `Followers: ${count}`;
      alert("Thanks for following!");
    }
  </script>

</body>
</html>
