<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite para a Juliana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffb6c1;
            padding: 50px;
            margin: 0;
            overflow: hidden;
        }
        h1 {
            font-size: 2rem;
            color: #333;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            margin: 0 10px;
            border: none;
            border-radius: 5px;
            background-color: #ff69b4;
            color: white;
        }
        #nao {
            position: absolute;
        }
        .hidden {
            display: none;
        }
        #aceita-sushi {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-top: 20px;
        }
        #certeza-box {
            display: none;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...</h1>
    <h2>Será que um sushi com você poderia dar mais sentido a tudo?</h2>
    <div class="buttons">
        <button id="sim">Sim, com certeza!</button>
        <button id="nao">Não</button>
    </div>
    <div id="certeza-box">
        <h2>Certeza?</h2>
        <button id="certeza">Sim!</button>
    </div>
    <img id="aceita-sushi" src="aceita-sushi.png" alt="Aceita Sushi" class="hidden">
    <iframe id="youtube-audio" width="0" height="0" src="" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen class="hidden"></iframe>
    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const certezaBox = document.getElementById('certeza-box');
        const certezaButton = document.getElementById('certeza');
        const aceitaSushi = document.getElementById('aceita-sushi');
        const youtubeAudio = document.getElementById('youtube-audio');
        
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });
        
        simButton.addEventListener('click', () => {
            certezaBox.style.display = 'block';
        });
        
        certezaButton.addEventListener('click', () => {
            aceitaSushi.classList.remove('hidden');
            youtubeAudio.src = "https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&loop=1";
        });
    </script>
</body>
</html>
