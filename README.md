<div id="header" align="center">
    <img src="https://img.hotimg.com/Portada-Linkedin.png" width="1200">
    <div align="left">
    <img src="https://komarev.com/ghpvc/?username=JonnathanBaquero01&color=FFD700" width="200" height="35">
    </div>
    
<h1 align="center" width="1200"> Hi! <img src="https://user-images.githubusercontent.com/18350557/176309783-0785949b-9127-417c-8b55-ab5a4333674e.gif" alt="Jonathan Baquero" /> I am <a class="badge-base__link LI-simple-link" href="https://www.linkedin.com/in/jonathan-baquero-rodriguez/">Jonathan Baquero</a></h1>
   
</div>
<div id="badges" align="center">
    <a href="https://www.linkedin.com/in/jonathan-baquero-rodriguez/" target="_blank">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
    </a>  
</div>
    
---

<h2 align="center">🧑‍💻 ABOUT ME</h2>

<h3 align="justify">
    
-💻📊With a background in systems engineering and computer science, and a specialized focus on data analysis using SQL, Python, and PowerBI, I have developed versatile skills ranging from PC and IT technical support to Java programming and marketing with artificial intelligence (AI).

-🎓💼My experience includes roles in teaching as a lecturer and in the business sector, where I have applied my knowledge to provide technical support, teach classes, and contribute to the development of AI-driven marketing strategies. Additionally, my participation in the ORACLE NEXT EDUCATION course has provided me with additional skills in data analysis and Java programming.

-🎓💻At University Masters, I had the opportunity to work as a support programmer, lecturer, and collaborator on AI marketing projects. Additionally, as a freelance professional, I have worked as a technology assistant for computer teams and in AI marketing studies, thus expanding my experience and skills in various areas.

-🚀📈I am excited to continue my professional journey, exploring new opportunities and contributing to the success of innovative projects in the fields of technology and data analysis.
</h3>
    
---

<h2 align="center">🛠️ Languages and Tools</h2>

<div class="image-container" align="center">
    <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="50" height="50">&nbsp;
    <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python" width="50" height="50">&nbsp;
    <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="My SQL" alt="My SQL" width="50" height="50">&nbsp;
    <img src="https://github.com/devicons/devicon/blob/master/icons/java/java-original-wordmark.svg" title="Java" alt="Java" width="50" height="50">&nbsp;
    <img src="https://github.com/devicons/devicon/blob/master/icons/windows11/windows11-original.svg" title="Windows" alt="Windows" width="50" height="50">&nbsp;
    <img src="https://img.hotimg.com/PowerBi.png" title="PowerBI" alt="PowerBI" width="70" height="50">&nbsp;
</div>

---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guess the Color</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
        }
        
        #game-container {
            text-align: center;
        }
        
        #color-box {
            width: 200px;
            height: 200px;
            margin: 20px auto;
            border: 2px solid black;
        }
        
        .color-option {
            display: inline-block;
            width: 60px;
            height: 60px;
            margin: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div id="game-container">
        <div id="color-box"></div>
        <div id="options">
            <div class="color-option" style="background-color: rgb(255, 0, 0);" onclick="checkColor('red')"></div>
            <div class="color-option" style="background-color: rgb(0, 255, 0);" onclick="checkColor('green')"></div>
            <div class="color-option" style="background-color: rgb(0, 0, 255);" onclick="checkColor('blue')"></div>
        </div>
        <div id="message"></div>
        <button onclick="newGame()">New Color</button>
    </div>  
    <script>
        function getRandomColor() {
            const r = Math.floor(Math.random() * 256);
            const g = Math.floor(Math.random() * 256);
            const b = Math.floor(Math.random() * 256);
            return `rgb(${r}, ${g}, ${b})`;
        }
        
        function newGame() {
            const color = getRandomColor();
            document.getElementById('color-box').style.backgroundColor = color;
            document.getElementById('message').textContent = '';
        }
        
        function checkColor(guess) {
            const color = document.getElementById('color-box').style.backgroundColor;
            const correctColor = color.replace(/\s/g, '');
            const result = guess === correctColor ? 'Correct!' : 'Incorrect!';
            document.getElementById('message').textContent = result;
        }
        
        newGame(); // Start a new game when the page loads
    </script>
</body>
</html>


