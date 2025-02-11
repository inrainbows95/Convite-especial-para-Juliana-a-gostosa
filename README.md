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
            background-color: #ffb6c1; /* Fundo rosa */
            padding: 50px;
            margin: 0;
            overflow: hidden;
        }
        h1 {
            font-size: 2.5rem;
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
        .fogos {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        .fogos img {
            position: absolute;
            width: 120px;
            animation: fogos 2s infinite;
        }
        @keyframes fogos {
            0% { transform: translateY(0) rotate(0); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }
        #aceita-sushi {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-top: 20px;
            z-index: 2;
            position: relative;
        }
        iframe {
            display: none;
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
    <img id="aceita-sushi" src="aceita-sushi.jpg" alt="Sushi" class="hidden">

    <!-- Fogos de artifício -->
    <div class="fogos hidden" id="fogos">
        <img src="fogo1.gif" alt="Fogos" style="left: 10%; top: 20%;">
        <img src="fogo2.gif" alt="Fogos" style="right: 10%; top: 30%;">
        <img src="fogo3.gif" alt="Fogos" style="left: 50%; top: 40%;">
    </div>

    <!-- Áudio do YouTube (inicialmente oculto) -->
    <iframe id="youtube-audio" width="0" height="0" src="https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&loop=1&playlist=pfcSqId5Ce4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const aceitaSushi = document.getElementById('aceita-sushi');
        const fogos = document.getElementById('fogos');
        let firstClick = true;

        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const maxX = window.innerWidth - naoButton.offsetWidth - 20;
            const maxY = window.innerHeight - naoButton.offsetHeight - 20;
            const x = Math.random() * maxX;
            const y = Math.random() * maxY;
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Ao clicar em "Sim", exibe a imagem e os fogos, e toca a música
        simButton.addEventListener('click', () => {
            aceitaSushi.classList.remove('hidden');
            fogos.classList.remove('hidden');

            if (firstClick) {
                // Força o áudio a tocar
                const audioIframe = document.createElement('iframe');
                audioIframe.width = "0";
                audioIframe.height = "0";
                audioIframe.src = "https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1";
                audioIframe.allow = "autoplay";
                document.body.appendChild(audioIframe);
                firstClick = false;
            }
        });
    </script>
</body>
</html>
