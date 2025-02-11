
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
            background-image: url('shadow-gif.gif'); /* Substitua pelo nome do seu GIF */
            background-size: cover;
            background-position: center;
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
    </style>
</head>
<body>
    <h1>A sintaxe da minha vida anda meio confusa...</h1>
    <h2>Será que um sushi com você poderia dar mais sentido a tudo?</h2>
    <div class="buttons">
        <button id="sim">Sim, com certeza!</button>
        <button id="nao">Não</button>
    </div>
    
    <script>
        const simButton = document.getElementById('sim');
        const naoButton = document.getElementById('nao');
        
        // Faz o botão "Não" fugir do cursor
        naoButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - naoButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - naoButton.offsetHeight);
            naoButton.style.left = `${x}px`;
            naoButton.style.top = `${y}px`;
        });

        // Ao clicar em "Sim", exibe a confirmação e depois abre o link
        simButton.addEventListener('click', () => {
            const certeza = confirm("Certeza?");
            if (certeza) {
                window.location.href = "https://youtube.com/shorts/pfcSqId5Ce4?si=SAkh1lX7b2D62J1m";
            }
        });
    </script>
</body>
</html>
