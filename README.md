# Rec.html.css
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Empatia e Cooperação: Pilares do Futuro</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- RESET E VARIÁVEIS (DESIGN EMPÁTICO) --- */
        :root {
            --bg-principal: #f4f7f6;
            --texto-escuro: #0080ff;
            --cor-empatia: #1c135f; /* Roxo suave - escuta, profundidade */
            --cor-cooperacao: #04ffcd; /* Verde-água - união, crescimento */
            --cor-card-bg: #ffffff;
            --transicao: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-principal);
            color: var(--texto-escuro);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- HEADER --- */
        header {
            background-color: transparent;
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: absolute;
            width: 100%;
            z-index: 10;
        }

        .logo {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--texto-escuro);
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            background: linear-gradient(135deg, rgba(108, 92, 231, 0.1) 0%, rgba(0, 114, 148, 0.1) 100%);
            position: relative;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 15px;
            color: var(--texto-escuro);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 30px;
            color: #556779;
        }

        .btn-cta {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--cor-empatia);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(108, 92, 231, 0.3);
            transition: var(--transicao);
        }

        .btn-cta:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(108, 92, 231, 0.5);
            background-color: #5b4bc4;
        }

        /* --- SEÇÃO DE CARDS (GRID E COOPERAÇÃO VISUAL) --- */
        .conceitos {
            max-width: 1100px;
            margin: -60px auto 60px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            position: relative;
            z-index: 2;
        }

        .card {
            background-color: var(--cor-card-bg);
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: var(--transicao);
            border-top: 5px solid transparent;
        }

        .card-empatia { border-top-color: var(--cor-empatia); }
        .card-cooperacao { border-top-color: var(--cor-cooperacao); }

        /* Efeito de Cooperação Visual: Quando passa o mouse em um card, a seção inteira reage */
        .conceitos:hover .card {
            opacity: 0.7;
            transform: scale(0.98);
        }

        .conceitos .card:hover {
            opacity: 1;
            transform: scale(1.03) translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* --- SEÇÃO INTERATIVA (MINI-GAME/QUIZ) --- */
        .interativo {
            max-width: 800px;
            margin: 0 auto 80px auto;
            padding: 40px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.03);
            text-align: center;
        }

        .interativo h2 {
            margin-bottom: 20px;
        }

        .cenario {
            background: #f8fafd;
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 25px;
            border-left: 4px solid var(--cor-empatia);
            text-align: left;
        }

        .opcoes {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .btn-opcao {
            padding: 15px 20px;
            border: 2px solid #e2e8f0;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            font-family: inherit;
            font-size: 1rem;
            text-align: left;
            transition: var(--transicao);
        }

        .btn-opcao:hover {
            border-color: #cbd5e1;
            background: #f8fafc;
        }

        /* Classes de feedback manipuladas pelo JavaScript */
        .btn-opcao.sucesso {
            border-color: var(--cor-cooperacao);
            background-color: rgba(0, 184, 148, 0.1);
            color: #006b54;
            font-weight: 600;
        }

        .btn-opcao.erro {
            border-color: #ff7675;
            background-color: rgba(255, 118, 117, 0.1);
            color: #c0392b;
        }

        .feedback-mensagem {
            margin-top: 25px;
            padding: 15px;
            border-radius: 10px;
            font-weight: 500;
            display: none;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --- FOOTER --- */
        footer {
            text-align: center;
            padding: 30px;
            background-color: #2c3e50;
            color: #a0aec0;
            font-size: 0.9rem;
        }

        /* Responsividade */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .conceitos { margin-top: 20px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">Conexão Humana</div>
    </header>

    <section class="hero">
        <h1>Empatia & Cooperação</h1>
        <p>Entender a perspectiva do outro é o primeiro passo. Agir juntos em direção a um objetivo comum é o que transforma o mundo.</p>
        <a href="#agir" class="btn-cta">Testar Atitude</a>
    </section>

    <section class="conceitos">
        <div class="card card-empatia">
            <h3>👁️ Empatia</h3>
            <p>Não é apenas sentir pena, mas ter a capacidade psicológica de se colocar no lugar do outro, compreender seus sentimentos e motivações sem julgamentos prévios.</p>
        </div>
        <div class="card card-cooperacao">
            <h3>🤝 Cooperação</h3>
            <p>O ato de operar junto. É quando indivíduos combinam seus talentos, esforços e recursos para alcançar um resultado que beneficia a coletividade.</p>
        </div>
    </section>

    <section class="interativo" id="agir">
        <h2>O que você faria?</h2>
        <p style="color: #718096; margin-bottom: 20px;">Coloque seus valores à prova na situação abaixo:</p>
        
        <div class="cenario">
            <strong>Cenário:</strong> Um colega de equipe sumiu do grupo nas últimas semanas e não entregou a parte dele do projeto final, que vale grande parte da nota. O prazo termina amanhã.
        </div>

        <div class="opcoes">
            <button class="btn-opcao" onclick="verificarEscolha(this, 'errada')">A) Tirar o nome dele do trabalho imediatamente e reclamar com o professor.</button>
            <button class="btn-opcao" onclick="verificarEscolha(this, 'errada')">B) Ignorar a situação, fazer apenas a sua parte e deixar a dele em branco.</button>
            <button class="btn-opcao" onclick="verificarEscolha(this, 'correta')">C) Mandar uma mensagem privada perguntando se está tudo bem, ouvir o lado dele e oferecer ajuda para finalizar o que falta a tempo.</button>
        </div>

        <div id="feedback" class="feedback-mensagem"></div>
    </section>

    <footer>
        <p>&copy; 2026 - Desenvolvido com Empatia e Cooperação.</p>
    </footer>

    <script>
        function verificarEscolha(elemento, tipo) {
            // Limpa escolhas anteriores
            const botoes = document.querySelectorAll('.btn-opcao');
            botoes.forEach(btn => btn.className = 'btn-opcao');
            
            const feedbackDiv = document.getElementById('feedback');
            feedbackDiv.style.display = 'block';

            if (tipo === 'correta') {
                elemento.classList.add('sucesso');
                feedbackDiv.style.backgroundColor = 'rgba(0, 184, 148, 0.15)';
                feedbackDiv.style.color = '#006b54';
                feedbackDiv.innerHTML = '✨ <strong>Excelente escolha!</strong> Ao demonstrar empatia, você descobriu que ele estava passando por um problema sério. Cooperando, vocês entregaram o projeto e fortaleceram um laço humano de valor inestimável.';
            } else {
                elemento.classList.add('erro');
                feedbackDiv.style.backgroundColor = 'rgba(255, 118, 117, 0.15)';
                feedbackDiv.style.color = '#c0392b';
                feedbackDiv.innerHTML = '❌ <strong>Essa atitude isola em vez de unir.</strong> Agir de forma individualista pode resolver o problema imediato, mas quebra a confiança e perde a oportunidade de ajudar alguém que poderia estar precisando de apoio.';
            }
        }
    </script>
</body>
</html>