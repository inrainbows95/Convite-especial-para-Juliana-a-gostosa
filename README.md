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
            z-index: 2;
            position: relative;
        }
        .confirm-box {
            display: none;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
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
    <img id="aceita-sushi" src="aceita-sushi.png" alt="" class="hidden">
    
    <div class="confirm-box" id="confirm-box">
        <p>Certeza?</p>
        <button id="confirm-sim">Sim!</button>
    </div>
    
    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        const aceitaSushi = document.getElementById('aceita-sushi');
        const confirmBox = document.getElementById('confirm-box');
        const confirmSim = document.getElementById('confirm-sim');

        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Ao clicar em "Sim", aparece a confirmação
        simButton.addEventListener('click', () => {
            confirmBox.style.display = 'block';
        });

        // Quando confirma, exibe a imagem e toca a música
        confirmSim.addEventListener('click', () => {
            confirmBox.style.display = 'none';
            aceitaSushi.classList.remove('hidden');
            
            // Cria um elemento de áudio do YouTube
            const audio = document.createElement('iframe');
            audio.width = '0';
            audio.height = '0';
            audio.src = "https://www.youtube.com/embed/pfcSqId5Ce4?autoplay=1&controls=0";
            audio.frameBorder = '0';
            audio.allow = 'autoplay';
            document.body.appendChild(audio);
        });
    </script>
</body>
</html>
