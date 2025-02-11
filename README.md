<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite Especial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffb6c1;
            padding: 50px;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            margin: 0 10px;
        }
        #nao {
            position: absolute;
        }
        .hidden {
            display: none;
        }
        .gif-container {
            margin-top: 20px;
        }
        #player {
            display: none; /* Esconde o player do YouTube */
        }
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...</h1>
    <h2>Será que um encontro com você poderia dar mais sentido a tudo?</h2>
    <img src="aceita-sushi.jpg" alt="">
    <div class="buttons">
        <button id="sim">Sim</button>
        <button id="nao">Não</button>
    </div>
    <div class="gif-container hidden" id="gif-container">
        <img src="dancing.gif" alt="">
    </div>

    <!-- Player do YouTube (escondido) -->
    <iframe id="player" width="0" height="0" src="https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&enablejsapi=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const gifContainer = document.getElementById('gif-container');
        const player = document.getElementById('player');

        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        simButton.addEventListener('click', () => {
            gifContainer.classList.remove('hidden'); // Mostra o GIF
            document.body.style.backgroundImage = "url('fogos.gif')"; // Muda o fundo
            player.style.display = 'block'; // Toca o vídeo (áudio)
        });
    </script>
</body>
</html>
