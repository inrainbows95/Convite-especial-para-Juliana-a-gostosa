<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite para Juliana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('WhatsApp Image 2025-02-11 at 05.59.32.jpeg') no-repeat center center/cover;
            padding: 50px;
            margin: 0;
            overflow: hidden;
        }
        h1 {
            font-size: 2rem;
            color: white;
            text-shadow: 2px 2px 4px black;
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
        #gif-container img {
            width: 200px;
            height: auto;
        }
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...<br>Será que um sushi com você poderia dar mais sentido a tudo?</h1>
    
    <div id="gif-container">
        <img src="shadow-sush.gif" alt="Sushi GIF">
    </div>
    
    <div class="buttons">
        <button id="sim">Sim</button>
        <button id="nao">Não</button>
    </div>
    
    <script>
        const naoButton = document.getElementById('nao');
        const simButton = document.getElementById('sim');

        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        simButton.addEventListener('click', () => {
            const confirmacao = confirm("Certeza?");
            if (confirmacao) {
                window.location.href = "https://youtube.com/shorts/pfcSqId5Ce4?si=SAkh1lX7b2D62J1m";
            }
        });
    </script>
</body>
</html>
