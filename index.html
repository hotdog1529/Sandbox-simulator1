<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Sandbox Simulator (Mobile)</title>
<style>
    body {
        margin: 0;
        background: #222;
        display: flex;
        height: 100vh;
        justify-content: center;
        align-items: center;
    }
    canvas {
        border: 2px solid white;
        image-rendering: pixelated;
        touch-action: none; /* Prevent scrolling when touching canvas */
    }
</style>
</head>
<body>

<canvas id="canvas"></canvas>

<script>
// GRID CONFIG
const CELL = 4;
const W = 150;
const H = 150;

const canvas = document.getElementById("canvas");
canvas.width = W * CELL;
canvas.height = H * CELL;
const ctx = canvas.getContext("2d");

const EMPTY = 0;
const SAND = 1;
let grid = new Array(W * H).fill(EMPTY);

function id(x, y) { return y * W + x; }

// PLACE PARTICLE
function placeSand(clientX, clientY) {
    const rect = canvas.getBoundingClientRect();
    const x = Math.floor((clientX - rect.left) / CELL);
    const y = Math.floor((clientY - rect.top) / CELL);
    if (x >= 0 && x < W && y >= 0 && y < H) {
        grid[id(x, y)] = SAND;
    }
}

// MOUSE SUPPORT
canvas.addEventListener("mousemove", e => {
    if (e.buttons === 1) placeSand(e.clientX, e.clientY);
});
canvas.addEventListener("mousedown", e => {
    placeSand(e.clientX, e.clientY);
});

// TOUCH SUPPORT
canvas.addEventListener("touchstart", e => {
    e.preventDefault();
    for (let t of e.touches) placeSand(t.clientX, t.clientY);
});
canvas.addEventListener("touchmove", e => {
    e.preventDefault();
    for (let t of e.touches) placeSand(t.clientX, t.clientY);
});

// SIMULATION
function step() {
    for (let y = H - 2; y >= 0; y--) {
        for (let x = 0; x < W; x++) {
            if (grid[id(x, y)] === SAND) {
                if (grid[id(x, y + 1)] === EMPTY) {
                    grid[id(x, y + 1)] = SAND;
                    grid[id(x, y)] = EMPTY;
                } else if (x > 0 && grid[id(x - 1, y + 1)] === EMPTY) {
                    grid[id(x - 1, y + 1)] = SAND;
                    grid[id(x, y)] = EMPTY;
                } else if (x < W - 1 && grid[id(x + 1, y + 1)] === EMPTY) {
                    grid[id(x + 1, y + 1)] = SAND;
                    grid[id(x, y)] = EMPTY;
                }
            }
        }
    }
}

// DRAW
function draw() {
    for (let y = 0; y < H; y++) {
        for (let x = 0; x < W; x++) {
            ctx.fillStyle = (grid[id(x, y)] === SAND) ? "#FFD27F" : "#000";
            ctx.fillRect(x * CELL, y * CELL, CELL, CELL);
        }
    }
}

function loop() {
    step();
    draw();
    requestAnimationFrame(loop);
}

loop();
</script>

</body>
</html>
