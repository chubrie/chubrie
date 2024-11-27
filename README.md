- 👋 Hi, I’m @chubrie
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
chubrie/chubrie is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Digital Art Portfolio</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Cursive', sans-serif;
      background: linear-gradient(to bottom, #ffe6f2, #ffcce6);
      overflow: hidden;
    }

    h1 {
      text-align: center;
      color: #ff6699;
      font-size: 3rem;
      margin-top: 20px;
    }

    .portfolio {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 20px;
    }

    .art-piece {
      width: 300px;
      height: 300px;
      border-radius: 15px;
      background-color: #fff;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      overflow: hidden;
    }

    .art-piece img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .petals {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 10;
    }

    @keyframes fall {
      from {
        transform: translateY(-10%) rotate(0deg);
      }
      to {
        transform: translateY(110%) rotate(360deg);
      }
    }

    .petal {
      position: absolute;
      width: 25px;
      height: 25px;
      background-image: url('https://www.example.com/sakura-petal.png'); /* Replace with your sakura petal image */
      background-size: contain;
      background-repeat: no-repeat;
      animation: fall 5s linear infinite;
    }
  </style>
</head>
<body>
  <div class="petals">
    <!-- Add petals dynamically -->
    <script>
      for (let i = 0; i < 50; i++) {
        const petal = document.createElement('div');
        petal.classList.add('petal');
        petal.style.left = Math.random() * 100 + '%';
        petal.style.animationDuration = Math.random() * 3 + 2 + 's';
        petal.style.animationDelay = Math.random() * 5 + 's';
        document.querySelector('.petals').appendChild(petal);
      }
    </script>
  </div>
  <h1>Welcome to My Art Portfolio</h1>
  <div class="portfolio">
    <div class="art-piece"><img src="art1.jpg" alt="Art Piece 1"></div>
    <div class="art-piece"><img src="art2.jpg" alt="Art Piece 2"></div>
    <div class="art-piece"><img src="art3.jpg" alt="Art Piece 3"></div>
  </div>
</body>
</html>
