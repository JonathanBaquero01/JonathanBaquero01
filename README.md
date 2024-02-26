<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tetris Game</title>
    <style>
        #tetris {
            margin-top: 20px;
            display: flex;
            justify-content: center;
        }

        canvas {
            border: 1px solid #000;
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
    <h2 align="center">🧑‍💻 ABOUT ME </h2>
    <h3 align="justify">
        -💻📊With a background in systems engineering and computer science, and a specialized focus on data analysis using SQL, Python, and PowerBI, I have developed versatile skills ranging from PC and IT technical support to Java programming and marketing with artificial intelligence (AI).<br>
        -🎓💼My experience includes roles in teaching as a lecturer and in the business sector, where I have applied my knowledge to provide technical support, teach classes, and contribute to the development of AI-driven marketing strategies. Additionally, my participation in the ORACLE NEXT EDUCATION course has provided me with additional skills in data analysis and Java programming.<br>
        -🎓💻At University Masters, I had the opportunity to work as a support programmer, lecturer, and collaborator on AI marketing projects. Additionally, as a freelance professional, I have worked as a technology assistant for computer teams and in AI marketing studies, thus expanding my experience and skills in various areas.<br>
        -🚀📈I am excited to continue my professional journey, exploring new opportunities and contributing to the success of innovative projects in the fields of technology and data analysis.
    </h3>
    <h2 align="center">🛠️ Languages and Tools</h2>
    <div class="image-container" align="center">
        <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="50" height="50">&nbsp;
        <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python" width="50" height="50">&nbsp;
        <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="My SQL" alt="My SQL" width="50" height="50">&nbsp;
        <img src="https://github.com/devicons/devicon/blob/master/icons/java/java-original-wordmark.svg" title="Java" alt="Java" width="50" height="50">&nbsp;
        <img src="https://github.com/devicons/devicon/blob/master/icons/windows11/windows11-original.svg" title="Windows" alt="Windows" width="50" height="50">&nbsp;
        <img src="https://img.hotimg.com/PowerBi.png" title="PowerBI" alt="PowerBI" width="70" height="50">&nbsp;
    </div>
    <div id="tetris" align="center">
        <canvas id="tetrisCanvas" width="240" height="400"></canvas>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const canvas = document.getElementById('tetrisCanvas');
            const context = canvas.getContext('2d');

            // Escalar el tamaño del canvas para que cada bloque tenga 20x20 píxeles
            context.scale(20, 20);

            // Función para limpiar el canvas
            function clearCanvas() {
                context.fillStyle = '#000';
                context.fillRect(0, 0, canvas.width, canvas.height);
            }

            // Función para dibujar un bloque
            function drawBlock(x, y, color) {
                context.fillStyle = color;
                context.fillRect(x, y, 1, 1);
                context.strokeStyle = '#000';
                context.strokeRect(x, y, 1, 1);
            }

            // Representación del tablero de juego (10x20)
            const board = [];
            for (let row = 0; row < 20; row++) {
                board[row] = [];
                for (let col = 0; col < 10; col++) {
                    board[row][col] = '#000';
                }
            }

            // Función para dibujar el tablero de juego
            function drawBoard() {
                clearCanvas();
                board.forEach((row, y) => {
                    row.forEach((color, x) => {
                        drawBlock(x, y, color);
                    });
                });
            }

            drawBoard();
        });
    </script>
    <div align="center">
        <img src="https://readme-jokes.vercel.app/api" alt="Jokes Card">
    </div>
</body>
</html>
