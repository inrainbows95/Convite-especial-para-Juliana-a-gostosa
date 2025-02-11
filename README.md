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
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-image: url('fundo.jpg'); /* Imagem de fundo */
            background-size: cover;
            background-position: center;
            color: black; /* Cor do texto */
        }
        .container {
            background-color: rgba(255, 255, 255, 0.8); /* Fundo semi-transparente */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        h1 {
            font-size: 24px;
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
            background-color: #ffb6c1;
            color: black;
        }
        #nao {
            position: absolute;
        }
        .hidden {
            display: none;
        }
        #certeza {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>A sintaxe da minha vida anda meio confusa...<br>Será que um sushi com você poderia dar mais sentido a tudo?</h1>
        <div class="buttons">
            <button id="sim">Sim</button>
            <button id="nao">Não</button>
        </div>
        <div id="certeza" class="hidden">
            <button id="confirmar">Certeza?</button>
        </div>
    </div>

    <!-- Vídeo do YouTube (oculto) -->
    <iframe id="youtube-audio" width="0" height="0" src="https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&loop=1&playlist=pfcSqId5Ce4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const certezaDiv = document.getElementById('certeza');
        const confirmarButton = document.getElementById('confirmar');
        const youtubeAudio = document.getElementById('youtube-audio');

        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Ao clicar em "Sim", exibe o botão "Certeza?"
        simButton.addEventListener('click', () => {
            certezaDiv.classList.remove('hidden');
        });

        // Ao clicar em "Certeza?", toca a música do YouTube
        confirmarButton.addEventListener('click', () => {
            youtubeAudio.src += "?autoplay=1"; // Força o vídeo a tocar
        });
    </script>
</body>
</html>
