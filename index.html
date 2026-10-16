
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ade Hery Nuriana Game</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    background: #070b20;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
}

header {
    padding: 20px 10px;
    background: linear-gradient(90deg, #071a48, #541a82);
    box-shadow: 0 0 20px #00d9ff55;
}

h1 {
    margin: 5px;
    color: #50eaff;
    text-shadow: 0 0 15px #00bfff;
    font-size: clamp(23px, 6vw, 36px);
}

header p {
    color: #d5caff;
}

#info {
    display: flex;
    justify-content: center;
    gap: 25px;
    padding: 12px;
    font-weight: bold;
    color: #ffe66d;
}

#game {
    position: relative;
    width: min(94vw, 420px);
    height: 440px;
    margin: 10px auto;
    overflow: hidden;
    border: 2px solid #38eaff;
    border-radius: 16px;
    background:
        radial-gradient(circle at 50% 20%, #24245b, #080b1e 75%);
    box-shadow: 0 0 25px #00cfff55;
}

#player {
    position: absolute;
    bottom: 12px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 38px;
    z-index: 2;
    user-select: none;
}

.item {
    position: absolute;
    top: -35px;
    font-size: 27px;
    user-select: none;
}

#overlay {
    position: absolute;
    inset: 0;
    z-index: 5;
    background: #050819eF;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 25px;
}

#overlay h2 {
    color: #5cecff;
}

button {
    padding: 12px 20px;
    margin: 5px;
    border: 0;
    border-radius: 25px;
    background: linear-gradient(90deg, #00cfff, #9b5cff);
    color: white;
    font-weight: bold;
    font-size: 15px;
    cursor: pointer;
}

.controls {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin: 15px;
}

.controls button {
    width: 85px;
    height: 55px;
    font-size: 25px;
    touch-action: none;
}

#note {
    color: #b6c9ff;
    font-size: 13px;
    padding: 10px;
}
</style>
</head>

<body>

<header>
    <h1>ADE HERY NURIANA</h1>
    <p>⚡ NEON COIN CHALLENGE ⚡</p>
</header>

<div id="info">
    <span>🪙 Skor: <span id="score">0</span></span>
    <span>❤️ Nyawa: <span id="lives">3</span></span>
</div>

<div id="game">
    <div id="player">🧑‍🚀</div>

    <div id="overlay">
        <h2>🚀 ADE GAME</h2>
        <p>
            Kumpulkan koin 🪙 sebanyak mungkin!<br>
            Hindari bom 💣 agar tidak kehilangan nyawa.
        </p>
        <button onclick="startGame()">MULAI GAME ▶</button>
    </div>
</div>

<div class="controls">
    <button id="left">⬅️</button>
    <button id="right">➡️</button>
</div>

<p id="note">
    Gunakan tombol panah atau tombol di layar untuk bergerak.
</p>

<script>
const game = document.getElementById("game");
const player = document.getElementById("player");
const overlay = document.getElementById("overlay");
const scoreText = document.getElementById("score");
const livesText = document.getElementById("lives");

let x = 50;
let score = 0;
let lives = 3;
let running = false;
let objects = [];
let spawnTimer;
let animationFrame;
let lastTime = 0;
let keys = { left: false, right: false };

function movePlayer() {
    if (keys.left) x -= 0.9;
    if (keys.right) x += 0.9;

    x = Math.max(5, Math.min(95, x));
    player.style.left = x + "%";
}

function startGame() {
    clearInterval(spawnTimer);
    cancelAnimationFrame(animationFrame);

    objects.forEach(o => o.el.remove());
    objects = [];

    score = 0;
    lives = 3;
    x = 50;
    lastTime = 0;
    keys.left = false;
    keys.right = false;

    scoreText.textContent = score;
    livesText.textContent = lives;
    player.style.left = x + "%";

    overlay.style.display = "none";
    running = true;

    spawnTimer = setInterval(createItem, 750);
    animationFrame = requestAnimationFrame(loop);
}

function createItem() {
    if (!running) return;

    const el = document.createElement("div");
    el.className = "item";

    const bomb = Math.random() < 0.28;
    el.textContent = bomb ? "💣" : "🪙";

    const pos = Math.random() * 88 + 6;
    el.style.left = pos + "%";
    game.appendChild(el);

    objects.push({
        el: el,
        x: pos,
        y: -35,
        speed: 1.5 + Math.random() * 1.5,
        bomb: bomb
    });
}

function loop(time) {
    if (!running) return;

    const dt = lastTime ? Math.min(time - lastTime, 32) : 16;
    lastTime = time;

    movePlayer();

    const gameHeight = game.clientHeight;
    const playerTop = gameHeight - 62;

    for (let i = objects.length - 1; i >= 0; i--) {
        const o = objects[i];
        o.y += o.speed * dt / 16;

        o.el.style.top = o.y + "px";

        const hitX = Math.abs(o.x - x) < 9;
        const hitY = o.y > playerTop - 20 &&
                     o.y < playerTop + 35;

        if (hitX && hitY) {
            if (o.bomb) {
                lives--;
                livesText.textContent = lives;
            } else {
                score += 10;
                scoreText.textContent = score;
            }

            o.el.remove();
            objects.splice(i, 1);

            if (lives <= 0) {
                endGame();
                return;
            }

            continue;
        }

        if (o.y > gameHeight) {
            o.el.remove();
            objects.splice(i, 1);
        }
    }

    animationFrame = requestAnimationFrame(loop);
}

function endGame() {
    running = false;
    clearInterval(spawnTimer);
    cancelAnimationFrame(animationFrame);

    overlay.style.display = "flex";
    overlay.innerHTML = `
        <h2>GAME OVER 💥</h2>
        <p>Hebat, Ade Hery Nuriana!</p>
        <p>Skor akhir kamu: <strong>${score}</strong></p>
        <button onclick="startGame()">MAIN LAGI 🔄</button>
    `;
}

function setKey(direction, value) {
    keys[direction] = value;
}

document.addEventListener("keydown", e => {
    if (e.key === "ArrowLeft" || e.key === "a") {
        keys.left = true;
        e.preventDefault();
    }
    if (e.key === "ArrowRight" || e.key === "d") {
        keys.right = true;
        e.preventDefault();
    }
});

document.addEventListener("keyup", e => {
    if (e.key === "ArrowLeft" || e.key === "a") {
        keys.left = false;
    }
    if (e.key === "ArrowRight" || e.key === "d") {
        keys.right = false;
    }
});

function bindButton(id, direction) {
    const button = document.getElementById(id);

    button.addEventListener("pointerdown", e => {
        e.preventDefault();
        setKey(direction, true);
    });

    ["pointerup", "pointerleave", "pointercancel"].forEach(event => {
        button.addEventListener(event, () => {
            setKey(direction, false);
        });
    });
}

bindButton("left", "left");
bindButton("right", "right");
</script>

</body>
</html>
