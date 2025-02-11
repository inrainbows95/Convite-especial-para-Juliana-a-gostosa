
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite para a Juliana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>A sintaxe da minha vida anda meio confusa...</h1>
        <h2>Será que um sushi com você poderia dar mais sentido a tudo?</h2>
        <div class="buttons">
            <button id="sim">Sim</button>
            <button id="nao">Não</button>
        </div>
        <div id="confirmacao" class="hidden">
            <p>Certeza?</p>
            <button id="confirmar-sim">Sim</button>
            <button id="confirmar-nao">Não</button>
        </div>
    </div>

    <!-- Vídeo do YouTube (oculto) -->
    <iframe id="youtube-audio" width="0" height="0" src="https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0&loop=1&playlist=pfcSqId5Ce4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

    <script src="script.js"></script>
</body>
</html> 
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-image: url('fundo.jpg');
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    text-align: center;
}

.container {
    background-color: rgba(255, 255, 255, 0.8); /* Fundo semi-transparente */
    padding: 20px;
    border-radius: 10px;
}

h1, h2 {
    margin: 10px 0;
}

.buttons {
    margin-top: 20px;
}

.buttons button, #confirmacao button {
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

#youtube-audio {
    position: absolute;
    top: -9999px;
    left: -9999px;
}
const simButton = document.getElementById('sim');
const naoButton = document.getElementById('nao');
const confirmacaoDiv = document.getElementById('confirmacao');
const confirmarSimButton = document.getElementById('confirmar-sim');
const confirmarNaoButton = document.getElementById('confirmar-nao');
const youtubeAudio = document.getElementById('youtube-audio');

// Faz o botão "Não" fugir do cursor
naoButton.addEventListener('mouseover', () => {
    const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
    const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
    naoButton.style.left = `${x}px`;
    naoButton.style.top = `${y}px`;
});

// Ao clicar em "Sim", exibe a confirmação
simButton.addEventListener('click', () => {
    confirmacaoDiv.classList.remove('hidden');
});

// Ao confirmar "Sim", toca a música
confirmarSimButton.addEventListener('click', () => {
    youtubeAudio.src += "?autoplay=1"; // Força o vídeo a tocar
    alert("É isso aí! Vamos combinar o sushi!");
});

// Ao confirmar "Não", volta para o início
confirmarNaoButton.addEventListener('click', () => {
    confirmacaoDiv.classList.add('hidden');
});
