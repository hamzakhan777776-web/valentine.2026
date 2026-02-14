# valentine.2026
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Will You Be My Valentine?</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <audio id="bgMusic" autoplay loop>
    <source src="music.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <h1>Will You Be My Valentine, Arzoo? 💖</h1>
    <div class="buttons">
      <button id="yesBtn">Yes 💖</button>
      <button id="noBtn">No 😏</button>
    </div>
    <p id="response"></p>
  </div>
  
  <!-- Floating lilies -->
  <div id="flowers"></div>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Valentine’s Day!</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <audio id="bgMusic" autoplay loop>
    <source src="music.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <h1>Happy Valentine’s Day, Arzoo! 💖</h1>
    <p>Here’s a little surprise just for you 🌸</p>
    <button onclick="location.href='page3.html'">See Surprise 🎁</button>
  </div>

  <!-- Floating lilies -->
  <div id="flowers"></div>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Surprise 💐</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <audio id="bgMusic" autoplay loop>
    <source src="music.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <h1>For My Sweet Arzoo 💖</h1>
    <p>I may not be there, but my heart is always with you 🌸</p>
    <img src="lily.png" alt="Lilies" class="center-img">
  </div>

  <!-- Floating lilies -->
  <div id="flowers"></div>

  <script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  padding: 0;
  font-family: 'Cursive', sans-serif;
  background: linear-gradient(#ffd6e7, #ffeef5);
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
}

h1 {
  font-size: 2.5em;
  color: #ff1a75;
  margin-bottom: 20px;
}

p {
  font-size: 1.2em;
  color: #ff4d94;
}

button {
  padding: 10px 25px;
  margin: 10px;
  font-size: 18px;
  cursor: pointer;
  border: none;
  border-radius: 12px;
  background: #ff4d94;
  color: white;
  transition: transform 0.2s;
}

button:hover {
  transform: scale(1.1);
  background: #ff1a75;
}

.center-img {
  width: 200px;
  margin-top: 20px;
}

/* Floating lilies */
.floating-lily {
  position: absolute;
  width: 50px;
  animation: floatUp linear infinite;
  opacity: 0.8;
}

@keyframes floatUp {
  0% { transform: translateY(100vh) rotate(0deg); }
  100% { transform: translateY(-100px) rotate(360deg); }
}
// Buttons on index.html
const yesBtn = document.getElementById('yesBtn');
const noBtn = document.getElementById('noBtn');
const response = document.getElementById('response');

if (yesBtn && noBtn && response) {
  yesBtn.onclick = () => {
    window.location.href = 'page2.html';
  };

  noBtn.onclick = () => {
    response.textContent = "Oops! You have no other choice 😏";
  };
}

// Floating lilies
const flowersContainer = document.getElementById('flowers');
const numberOfLilies = 15;

if (flowersContainer) {
  for (let i = 0; i < numberOfLilies; i++) {
    const lily = document.createElement('img');
    lily.src = 'lily.png';
    lily.className = 'floating-lily';
    lily.style.left = Math.random() * window.innerWidth + 'px';
    lily.style.animationDuration = 5 + Math.random() * 5 + 's';
    flowersContainer.appendChild(lily);
  }
}

