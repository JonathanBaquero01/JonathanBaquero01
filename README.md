<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adivina el número</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        h1 {
            text-align: center;
        }
        .container {
            width: 600px;
            margin: 0 auto;
        }
        .mensaje {
            text-align: center;
            margin-bottom: 10px;
        }
        .botones {
            display: flex;
            justify-content: space-around;
        }
        .boton {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
        }
        .boton:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div id="header" align="center">
        <img src="https://img.hotimg.com/Portada-Linkedin.png" width="600">
        <div align="left">
            <img src="https://komarev.com/ghpvc/?username=JonnathanBaquero01&color=FFD700" width="200" height="35">
        </div>
        
        <h1 align="center" width="600"> Hi! <img src="https://user-images.githubusercontent.com/18350557/176309783-0785949b-9127-417c-8b55-ab5a4333674e.gif" alt="Jonathan Baquero" /> I am <a class="badge-base__link LI-simple-link" href="https://www.linkedin.com/in/jonathan-baquero-rodriguez/">Jonathan Baquero</a></h1>

    </div>
    <div id="badges" align="center">
        <a href="https://www.linkedin.com/in/jonathan-baquero-rodriguez/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
        </a>
    </div>

    <div class="container">
        <h2 align="center">Adivina el número</h2>
        <div class="mensaje">
            Piensa en un número entre 1 y 100
        </div>
        <div class="botones">
            <button class="boton" onclick="adivinar('menor')">Menor</button>
            <button class="boton" onclick="adivinar('igual')">Igual</button>
            <button class="boton" onclick="adivinar('mayor')">Mayor</button>
        </div>
    </div>

    <h2 align="center">🧑‍💻 ABOUT ME</h2>
    <h3 align="justify">
        -💻📊With a background in systems engineering and computer science, and a specialized focus on data analysis using SQL, Python, and PowerBI, I have developed versatile skills ranging from PC and IT technical support to Java programming and marketing with artificial intelligence (AI).<br><br>
        -🎓💼My experience includes roles in teaching as a lecturer and in the business sector, where I have applied my knowledge to provide technical support, teach classes, and contribute to the development of AI-driven marketing strategies. Additionally, my participation in the ORACLE NEXT EDUCATION course has provided me with additional skills in data analysis and Java programming.<br><br>
        -🎓💻At University Masters, I had the opportunity to work as a support programmer, lecturer, and collaborator on AI marketing projects. Additionally, as a freelance professional, I have worked as a technology assistant for computer teams and in AI marketing studies, thus expanding my experience and skills in various areas.<br><br>
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

    <h2 align="center">Juego de Adivinar el Número</h2>
    <p align="center">Piensa en un número entre 1 y 100 y selecciona "Menor", "Igual" o "Mayor" según corresponda.</p>
    <div align="center">
        <button class="boton" onclick="adivinar('menor')">Menor</button>
        <button class="boton" onclick="adivinar('igual')">Igual</button>
        <button class="boton" onclick="adivinar('mayor')">Mayor</button>
    </div>

    <script>
        let min = 1;
        let max = 100;

        function adivinar(resultado) {
            if (resultado === 'menor') {
                max = Math.floor((min + max) / 2);
            } else if (resultado === 'mayor') {
                min = Math.floor((min + max) / 2) + 1;
            } else if (resultado === 'igual') {
                alert('¡Adiviné tu número!');
                return;
            }

            if (min <= max) {
                document.querySelector('.mensaje').textContent = `¿Es tu número ${Math.floor((min + max) / 2)}?`;
            } else {
                alert('¡Has mentido! No
