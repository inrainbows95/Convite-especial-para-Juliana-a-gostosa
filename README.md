<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite para Juliana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-image: url('fundo.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 50px;
            margin: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }
        img {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
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
            background-color: #ff6f61;
            color: white;
            transition: background-color 0.3s;
        }
        .buttons button:hover {
            background-color: #ff3b2f;
        }
        #nao {
            position: absolute;
        }
        .hidden {
            display: none;
        }
        #confirmacao {
            margin-top: 20px;
            font-size: 1.5em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...</h1>
    <h1>Será que um sushi com você poderia dar mais sentido a tudo?</h1>
    <img src="shadow-sush.gif" alt="Sushi Animado">
    <div class="buttons">
        <button id="sim">Sim</button>
        <button id="nao">Não</button>
    </div>
    <div id="confirmacao" class="hidden">Certeza?</div>

    <!-- Vídeo do YouTube (oculto) -->
    <iframe id="youtube-audio" width="0" height="0" src="https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&loop=1&playlist=pfcSqId5Ce4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const confirmacao = document.getElementById('confirmacao');
        const youtubeAudio = document.getElementById('youtube-audio');

        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Ao clicar em "Sim", exibe a confirmação e toca a música
        simButton.addEventListener('click', () => {
            confirmacao.classList.remove('hidden');
            youtubeAudio.src += "?autoplay=1"; // Força o vídeo a tocar
        });
    </script>
</body>
</html>
