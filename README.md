
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
            margin: 10px;
            border: none;
            border-radius: 5px;
            background-color: #ff69b4;
            color: white;
        }
        #nao {
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...</h1>
    <h2>Será se um sushi com você poderia dar mais sentido a tudo?</h2>
    <div class="buttons">
        <button id="sim">Sim, com certeza!</button>
        <button id="nao">Não</button>
    </div>
    
    <script>
        const naoButton = document.getElementById('nao');
        const simButton = document.getElementById('sim');

        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Quando clica em "Sim", exibe "Certeza?"
        simButton.addEventListener('click', () => {
            const certeza = confirm("Certeza?");
            if (certeza) {
                window.location.href = "https://youtube.com/shorts/pfcSqId5Ce4?si=SAkh1lX7b2D62J1m";
            }
        });
    </script>
</body>
</html>
