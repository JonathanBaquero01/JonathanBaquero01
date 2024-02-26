<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snake Game</title>
    <style>
        canvas {
            background-color: #000;
            display: block;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div id="header" align="center">
        <img src="https://img.hotimg.com/Portada-Linkedin.png" width="1200">
        <div align="left">
            <img src="https://komarev.com/ghpvc/?username=JonnathanBaquero01&color=FFD700" width="200" height="30">
        </div>
        <h1 align="center" width="1200"> Hi! <img src="https://user-images.githubusercontent.com/18350557/176309783-0785949b-9127-417c-8b55-ab5a4333674e.gif" alt="Jonathan Baquero" /> I am <a class="badge-base__link LI-simple-link" href="https://www.linkedin.com/in/jonathan-baquero-rodriguez/">Jonathan Baquero</a></h1>
    </div>
    <div id="badges" align="center">
        <a href="https://www.linkedin.com/in/ferchulobo777/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
        </a>
    </div>
    <h2 align="center">🧑‍💻 ABOUT ME</h2>
    <h3 align="justify">
        <!-- Your about me content here -->
    </h3>
    <h2 align="center">🛠️ Languages and Tools</h2>
    <div class="image-container" align="center">
        <!-- Your languages and tools content here -->
    </div>
    <div align="center">
        <canvas id="gameCanvas" width="400" height="400"></canvas>
    </div>
    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        const box = 20;
        const canvasSize = 400;
        const snake = [{ x: 10, y: 10 }];
        let food = {};
        let dx = 0;
        let dy = 0;
        let score = 0;

        function createFood() {
            food = {
                x: Math.floor(Math.random() * (canvasSize / box)) * box,
                y: Math.floor(Math.random() * (canvasSize / box)) * box
            };
        }

        function draw() {
            ctx.clearRect(0, 0, canvasSize, canvasSize);
            ctx.fillStyle = '#00FF00';
            snake.forEach((segment) => {
                ctx.fillRect(segment.x, segment.y, box, box);
            });

            ctx.fillStyle = '#FF0000';
            ctx.fillRect(food.x, food.y, box, box);

            ctx.fillStyle = '#FFFFFF';
            ctx.font = '30px Arial';
            ctx.fillText(`Score: ${score}`, 10, 30);
        }

        function moveSnake() {
            const head = { x: snake[0].x + dx, y: snake[0].y + dy };
            snake.unshift(head);

            if (head.x === food.x && head.y === food.y) {
                score += 10;
                createFood();
            } else {
                snake.pop();
            }
        }

        function checkCollision() {
            if (
                snake[0].x < 0 ||
                snake[0].x >= canvasSize ||
                snake[0].y < 0 ||
                snake[0].y >= canvasSize ||
                snake.slice(1).some((segment) => segment.x === snake[0].x && segment.y === snake[0].y)
            ) {
                clearInterval(gameLoop);
                alert(`Game Over! Your score is ${score}`);
            }
        }

        function gameLoop() {
            moveSnake();
            draw();
            checkCollision();
        }

        createFood();
        const gameLoop = setInterval(gameLoop, 100);

        document.addEventListener('keydown', (event) => {
            const keyPressed = event.key;
            if (keyPressed === 'ArrowLeft' && dx === 0) {
                dx = -box;
                dy = 0;
            } else if (keyPressed === 'ArrowRight' && dx === 0) {
                dx = box;
                dy = 0;
            } else if (keyPressed === 'ArrowUp' && dy === 0) {
                dx = 0;
                dy = -box;
            } else if (keyPressed === 'ArrowDown' && dy === 0) {
                dx = 0;
                dy = box;
            }
        });
    </script>
</body>
</html>
