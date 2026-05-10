<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🍒 Cherry Catch</title>

<style>
body{
  margin:0;
  overflow:hidden;
  font-family:Arial,sans-serif;
  background:linear-gradient(180deg,#ffeef3,#ffffff);
}

#game{
  width:100vw;
  height:100vh;
  position:relative;
}

#scoreBoard{
  position:fixed;
  top:15px;
  right:15px;
  background:white;
  padding:12px 18px;
  border-radius:18px;
  box-shadow:0 8px 20px rgba(0,0,0,.15);
  font-weight:900;
  z-index:10;
}

#lives{
  position:fixed;
  top:15px;
  left:15px;
  background:white;
  padding:12px 18px;
  border-radius:18px;
  box-shadow:0 8px 20px rgba(0,0,0,.15);
  font-weight:900;
  z-index:10;
}

#player{
  position:absolute;
  bottom:25px;
  left:50%;
  transform:translateX(-50%);
  width:90px;
  height:45px;
  background:linear-gradient(135deg,#111,#444);
  border-radius:50px;
  box-shadow:0 12px 25px rgba(0,0,0,.25);
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:28px;
}

.cherry{
  position:absolute;
  font-size:38px;
  animation:fall linear forwards;
}

@keyframes fall{
  from{
    transform:translateY(-60px);
  }
  to{
    transform:translateY(110vh);
  }
}

#startScreen,
#gameOver{
  position:fixed;
  inset:0;
  background:linear-gradient(180deg,#fff,#ffeef3);
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  z-index:99;
  text-align:center;
  padding:20px;
}

#gameOver{
  display:none;
}

.logo{
  font-size:110px;
  animation:float 2s infinite;
}

@keyframes float{
  50%{
    transform:translateY(-12px);
  }
}

h1{
  font-size:46px;
  margin:10px 0;
}

p{
  color:#555;
  font-size:17px;
}

button{
  border:0;
  background:linear-gradient(135deg,#ff4d6d,#ff758f);
  color:white;
  padding:16px 28px;
  border-radius:22px;
  font-size:18px;
  font-weight:900;
  cursor:pointer;
  box-shadow:0 10px 25px rgba(255,77,109,.35);
  margin-top:15px;
}

#controls{
  position:fixed;
  bottom:20px;
  left:0;
  right:0;
  display:flex;
  justify-content:space-between;
  padding:0 25px;
  z-index:20;
  pointer-events:none;
}

.controlBtn{
  width:75px;
  height:75px;
  border-radius:50%;
  background:rgba(0,0,0,.75);
  color:white;
  font-size:32px;
  display:flex;
  align-items:center;
  justify-content:center;
  pointer-events:auto;
  user-select:none;
}
</style>
</head>

<body>

<div id="game">

  <div id="scoreBoard">ניקוד: <span id="score">0</span></div>
  <div id="lives">חיים: <span id="lifeCount">3</span></div>

  <div id="player">🧺</div>

  <div id="controls">
    <div class="controlBtn" ontouchstart="moveLeft=true" ontouchend="moveLeft=false" onmousedown="moveLeft=true" onmouseup="moveLeft=false">⬅️</div>
    <div class="controlBtn" ontouchstart="moveRight=true" ontouchend="moveRight=false" onmousedown="moveRight=true" onmouseup="moveRight=false">➡️</div>
  </div>

</div>

<div id="startScreen">
  <div class="logo">🍒</div>
  <h1>Cherry Catch</h1>
  <p>תזוז ימינה ושמאלה ותתפוס כמה שיותר דובדבנים</p>
  <button onclick="startGame()">התחל משחק</button>
</div>

<div id="gameOver">
  <div class="logo">💔</div>
  <h1>המשחק נגמר</h1>
  <p>הניקוד שלך: <span id="finalScore">0</span></p>
  <button onclick="restartGame()">שחק שוב</button>
</div>

<script>
let score = 0;
let lives = 3;
let playerX = window.innerWidth / 2;
let moveLeft = false;
let moveRight = false;
let gameRunning = false;
let cherryInterval;
let speed = 4;

const player = document.getElementById("player");
const scoreEl = document.getElementById("score");
const livesEl = document.getElementById("lifeCount");

function startGame(){
  document.getElementById("startScreen").style.display = "none";
  gameRunning = true;

  cherryInterval = setInterval(createCherry, 900);
  requestAnimationFrame(gameLoop);
}

function restartGame(){
  document.querySelectorAll(".cherry").forEach(c => c.remove());

  score = 0;
  lives = 3;
  speed = 4;
  playerX = window.innerWidth / 2;

  scoreEl.innerText = score;
  livesEl.innerText = lives;

  document.getElementById("gameOver").style.display = "none";
  gameRunning = true;

  cherryInterval = setInterval(createCherry, 900);
  requestAnimationFrame(gameLoop);
}

function createCherry(){
  if(!gameRunning) return;

  const cherry = document.createElement("div");
  cherry.className = "cherry";
  cherry.innerText = "🍒";

  cherry.style.left = Math.random() * (window.innerWidth - 50) + "px";
  cherry.style.top = "-50px";

  document.getElementById("game").appendChild(cherry);
}

function gameLoop(){
  if(!gameRunning) return;

  if(moveLeft) playerX -= 7;
  if(moveRight) playerX += 7;

  if(playerX < 45) playerX = 45;
  if(playerX > window.innerWidth - 45) playerX = window.innerWidth - 45;

  player.style.left = playerX + "px";

  document.querySelectorAll(".cherry").forEach(cherry => {
    let y = cherry.offsetTop + speed;
    cherry.style.top = y + "px";

    const cherryRect = cherry.getBoundingClientRect();
    const playerRect = player.getBoundingClientRect();

    if(
      cherryRect.bottom >= playerRect.top &&
      cherryRect.left < playerRect.right &&
      cherryRect.right > playerRect.left
    ){
      cherry.remove();
      score++;
      scoreEl.innerText = score;

      if(score % 10 === 0){
        speed += 0.7;
      }
    }

    if(y > window.innerHeight){
      cherry.remove();
      lives--;
      livesEl.innerText = lives;

      if(lives <= 0){
        endGame();
      }
    }
  });

  requestAnimationFrame(gameLoop);
}

function endGame(){
  gameRunning = false;
  clearInterval(cherryInterval);

  document.getElementById("finalScore").innerText = score;
  document.getElementById("gameOver").style.display = "flex";
}

document.addEventListener("keydown", e => {
  if(e.key === "ArrowLeft") moveLeft = true;
  if(e.key === "ArrowRight") moveRight = true;
});

document.addEventListener("keyup", e => {
  if(e.key === "ArrowLeft") moveLeft = false;
  if(e.key === "ArrowRight") moveRight = false;
});
</script>

</body>
</html>
