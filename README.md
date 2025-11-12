<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calma e Equilíbrio</title>
    <style>
        body {
            font-family: "Poppins", sans-serif;
            background: linear-gradient(135deg, #89f7fe, #66a6ff);
            color: #fff;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        header {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            font-size: 24px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        main {
            padding: 40px 20px;
        }

        .mensagem {
            font-size: 20px;
            margin: 30px 0;
        }

        button {
            background-color: #ffffff;
            color: #3a7bd5;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background-color: #dfe9f3;
        }

        .respiracao {
            margin-top: 40px;
        }

        #contador {
            font-size: 32px;
            margin-top: 20px;
        }

        footer {
            margin-top: 50px;
            font-size: 14px;
            opacity: 0.8;
        }
    </style>
</head>
<body>

    <header>💙 Calma e Equilíbrio</header>

    <main>
        <p class="mensagem" id="mensagem">Respire fundo. Você está seguro(a) agora.</p>

        <button onclick="novaMensagem()">Nova mensagem de apoio</button>

        <div class="respiracao">
            <h2>Exercício de Respiração</h2>
            <p>Siga o ritmo: inspire, segure e expire lentamente.</p>
            <button onclick="iniciarRespiracao()">Iniciar exercício</button>
            <div id="contador"></div>
        </div>
    </main>

    <footer>© 2025 Calma e Equilíbrio | Feito com ❤️ para cuidar da mente</footer>

    <script>
        const mensagens = [
            "Você é mais forte do que imagina.",
            "Tudo bem sentir ansiedade, ela não define quem você é.",
            "Acalme sua mente, um passo de cada vez.",
            "Lembre-se: respirar é o primeiro passo para retomar o controle.",
            "Você merece paz e tranquilidade.",
            "Aceite o momento presente sem julgamentos."
        ];

        function novaMensagem() {
            const msg = mensagens[Math.floor(Math.random() * mensagens.length)];
            document.getElementById("mensagem").textContent = msg;
        }

        function iniciarRespiracao() {
            const contador = document.getElementById("contador");
            let etapas = ["Inspire profundamente", "Segure...", "Expire devagar"];
            let i = 0;

            contador.textContent = "Prepare-se...";
            let intervalo = setInterval(() => {
                contador.textContent = etapas[i];
                i++;
                if (i >= etapas.length) {
                    i = 0;
                }
            }, 4000);
        }
    </script>

</body>
</html>
