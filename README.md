# Brenda---anivers-rio-

<!DOCTYPE html><html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Contagem para o Aniversário da Brenda</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to top, #e0f7fa, #ffffff);
      color: #333;
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      padding: 2rem;
      border-radius: 20px;
      background: rgba(255, 255, 255, 0.95);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      max-width: 90%;
      animation: fadeIn 1.5s ease-in-out;
    }
    h1 {
      color: #d32f2f;
      font-size: 2.2rem;
    }
    p {
      font-size: 1.2rem;
      margin: 1rem 0;
    }
    .countdown {
      font-size: 1.5rem;
      margin-top: 1rem;
      color: #1565c0;
    }
    .hidden {
      color: #999;
      font-size: 0.9rem;
      margin-top: 1rem;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(15px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Contagem para o Aniversário da Brenda 🎉</h1>
    <div class="countdown" id="contador"></div>
    <p id="mensagemDia"></p>
    <div class="hidden" id="declaracaoEscondida"></div>
  </div>  <script>
    const hoje = new Date();
    const aniversario = new Date(hoje.getFullYear(), 7, 27); // 27 de agosto (mês 7)
    if (hoje > aniversario) aniversario.setFullYear(aniversario.getFullYear() + 1);

    const diff = Math.ceil((aniversario - hoje) / (1000 * 60 * 60 * 24));
    const contador = document.getElementById("contador");
    contador.textContent = `Faltam ${diff} dia${diff > 1 ? 's' : ''} para o grande dia!`;

    const mensagens = [
      "Você é mais forte do que imagina e mais amada do que pensa.",
      "Cultive sua luz. O mundo precisa dela.",
      "Cada passo seu inspira quem te admira.",
      "Nunca se esqueça do quanto você é especial.",
      "Sua presença é um presente para o mundo.",
      "Ame-se com a mesma intensidade que deseja ser amada.",
      "Não há nada mais bonito do que alguém que brilha sendo quem é."
    ];

    const segredo = [
      "Entre as linhas, escondo algo só seu...",
      "...cada página dessa espera tem um pouco de mim.",
      "O que não digo em voz alta, escrevo aqui com carinho.",
      "Se você chegou até aqui, saiba que penso em você todos os dias.",
      "A contagem é só desculpa para te lembrar o quanto você é importante.",
      "E quando o dia chegar, talvez eu finalmente diga tudo...",
      "...porque você é, desde já, meu motivo favorito."
    ];

    const diaIndex = (7 - diff) >= 0 ? (7 - diff) : 0;
    document.getElementById("mensagemDia").textContent = mensagens[diaIndex] || mensagens[0];
    document.getElementById("declaracaoEscondida").textContent = segredo[diaIndex] || "";
  </script></body>
</html>
