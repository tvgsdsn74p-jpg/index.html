<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Saúde da Mulher - Projeto ODS 4</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #fff0f5;
            padding-bottom: 100px;
        }
        header {
            background: #d81b60;
            color: white;
            text-align: center;
            padding: 20px;
        }
        nav {
            display: flex;
            overflow-x: auto;
            background: #fff;
            border-top: 2px solid #eee;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
            z-index: 10;
        }
        nav button {
            background: none;
            border: none;
            font-size: 12px;
            color: #d81b60;
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
            min-width: 80px;
            margin: 0 5px;
        }
        nav button span {
            margin-top: 2px;
        }
        section {
            display: none;
            padding: 20px;
            animation: fade 0.3s;
        }
        section.ativo {
            display: block;
        }
        .banner {
            width: 100%;
            max-height: 220px;
            object-fit: contain;
            background: white;
        }
        .card {
            background: white;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            max-width: 900px;
            line-height: 1.6;
        }
        h2 {
            color: #d81b60;
        }
        @keyframes fade { from {opacity:0;} to {opacity:1;} }
        .menu-spacer { height: 100px; }
        button {
            margin-top: 10px;
            padding: 10px;
            border-radius: 10px;
            border: none;
            background: #d81b60;
            color: white;
            cursor: pointer;
        }
        .quiz-option {
            display: block;
            margin: 8px 0;
        }
        .quiz-result {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
    <script>
        function mostrar(secao) {
            document.querySelectorAll("section").forEach(s => s.classList.remove("ativo"));
            document.getElementById(secao).classList.add("ativo");
            window.scrollTo(0,0);
        }

        // Quiz
        const quizData = [
            {
                pergunta: "1. Qual é a função dos ovários?",
                opcoes: ["Produzir espermatozoides", "Produzir óvulos e hormônios", "Armazenar sangue", "Controlar digestão"],
                correta: 1
            },
            {
                pergunta: "2. Qual método contraceptivo é oferecido gratuitamente pelo SUS?",
                opcoes: ["Implante hormonal", "DIU hormonal", "Pílula anticoncepcional", "Anel vaginal particular"],
                correta: 2
            },
            {
                pergunta: "3. Qual tecido é recomendado para roupas íntimas?",
                opcoes: ["Sintético", "Algodão", "Plástico", "Lã"],
                correta: 1
            },
            {
                pergunta: "4. Quem tem direito aos absorventes gratuitos do SUS?",
                opcoes: ["Pessoas inscritas no CadÚnico", "Qualquer pessoa", "Somente homens", "Pessoas com carro próprio"],
                correta: 0
            },
            {
                pergunta: "5. Qual é o órgão onde o bebê se desenvolve?",
                opcoes: ["Vagina", "Útero", "Ovário", "Trompa de Falópio"],
                correta: 1
            },
            {
                pergunta: "6. Qual método protege contra ISTs?",
                opcoes: ["Preservativo", "DIU", "Pílula", "Implante"],
                correta: 0
            },
            {
                pergunta: "7. Qual é um método natural de contracepção?",
                opcoes: ["Adesivo hormonal", "Tabelinha", "DIU de cobre", "Injeção hormonal"],
                correta: 1
            },
            {
                pergunta: "8. Por que roupas apertadas podem ser prejudiciais?",
                opcoes: ["Aumentam umidade e risco de infecção", "Melhoram a circulação", "Fortalecem músculos", "Previnem doenças"],
                correta: 0
            },
            {
                pergunta: "9. O que significa dignidade menstrual?",
                opcoes: ["Acesso a absorventes, informação e condições adequadas", "Ir para escola todos os dias", "Tomar banho apenas uma vez", "Comprar roupas caras"],
                correta: 0
            },
            {
                pergunta: "10. Qual órgão transporta o óvulo até o útero?",
                opcoes: ["Vagina", "Trompa de Falópio", "Ovário", "Útero"],
                correta: 1
            }
        ];

        function gerarQuiz() {
            const container = document.getElementById("quiz-container");
            container.innerHTML = "";
            quizData.forEach((q, i) => {
                const div = document.createElement("div");
                div.className = "card";
                const pergunta = document.createElement("h3");
                pergunta.textContent = q.pergunta;
                div.appendChild(pergunta);
                q.opcoes.forEach((op, idx) => {
                    const label = document.createElement("label");
                    label.className = "quiz-option";
                    const input = document.createElement("input");
                    input.type = "radio";
                    input.name = "q" + i;
                    input.value = idx;
                    label.appendChild(input);
                    label.appendChild(document.createTextNode(" " + op));
                    div.appendChild(label);
                });
                container.appendChild(div);
            });
            const btn = document.createElement("button");
            btn.textContent = "Verificar Respostas";
            btn.onclick = verificarQuiz;
            container.appendChild(btn);
            const resultado = document.createElement("div");
            resultado.id = "resultado";
            resultado.className = "quiz-result";
            container.appendChild(resultado);
        }

        function verificarQuiz() {
            let score = 0;
            quizData.forEach((q, i) => {
                const selecionado = document.querySelector('input[name="q'+i+'"]:checked');
                if(selecionado && parseInt(selecionado.value) === q.correta){
                    score++;
                }
            });
            document.getElementById("resultado").textContent = "Você acertou " + score + " de " + quizData.length + " perguntas.";
        }
    </script>
</head>
<body onload="mostrar('inicio')">

<header>
    <h1>🌸 Saúde da Mulher</h1>
    <p>Projeto Educativo - ODS 4</p>
</header>

<div class="menu-spacer"></div>

<!-- SEÇÕES EXISTENTES -->
<section id="inicio" class="ativo">
    <img class="banner" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRBhQYX5n2q73o_FDwZDA_hXSvAHox4jDzWxZF05kF3RVnXOFWtMLDQ-gaD&s" alt="Mulher">
    <div class="card">
        <h2>Sobre o Projeto</h2>
        <p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher, abordando temas importantes como prevenção, cuidados íntimos, métodos contraceptivos e acesso a serviços de saúde.</p>
        <p>As informações são apresentadas de forma clara e acessível, contribuindo para o conhecimento, autonomia e bem-estar.</p>
        <h3>Sobre a autora</h3>
        <p>Meu nome é Beatriz Dias, tenho 21 anos, sou formada como técnica de enfermagem e atualmente estudante da área de Tecnologia da Informação. Minha formação em enfermagem me proporciona conhecimento sólido sobre saúde feminina, garantindo que o conteúdo apresentado seja confiável, relevante e fundamentado em práticas de cuidado real.</p>
    </div>
</section>

<section id="cuidados">
    <img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg" alt="Cuidados Íntimos">
    <div class="card">
        <h2>Cuidados com a Saúde Íntima</h2>
        <p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região.</p>
        <p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções.</p>
        <p>Evitar roupas muito apertadas é importante para não aumentar o calor e a umidade, reduzindo risco de infecções.</p>
        <p>Manter alimentação equilibrada e boa hidratação contribui para o bom funcionamento do organismo.</p>
    </div>
</section>

<section id="sistema">
    <img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg" alt="Sistema Reprodutor">
    <div class="card">
        <h2>Sistema Reprodutor Feminino</h2>
        <p>O sistema reprodutor feminino é composto por órgãos responsáveis pela reprodução, produção de hormônios e funcionamento do ciclo menstrual.</p>
    </div>
</section>

<section id="sus">
    <img class="banner" src="https://img.freepik.com/vetores-gratis/conceito-de-sistema-reprodutivo-feminino_52683-45450.jpg?semt=ais_hybrid&w=740&q=80" alt="Absorventes SUS">
    <div class="card">
        <h2>Absorventes Gratuitos pelo SUS</h2>
        <p>O acesso a absorventes é um direito ligado à saúde, higiene e dignidade. No Brasil, o governo garante distribuição gratuita para pessoas em situação de vulnerabilidade.</p>
    </div>
</section>

<section id="contraceptivos">
    <img class="banner" src="https://static.vecteezy.com/ti/vetor-gratis/p1/6922254-contraceptivos-conjunto-controle-de-natalidade-ilustracao-para-impressao-fundos-capas-embalagem-cartoes-cartazes-adesivos-textil-e-design-sazonal-isolado-em-fundo-branco-vetor.jpg" alt="Métodos Contraceptivos">
    <div class="card">
        <h2>Métodos Contraceptivos</h2>
        <p>Os métodos contraceptivos são formas de evitar a gravidez e, em alguns casos, também ajudam na prevenção de ISTs.</p>
    </div>
</section>

<!-- QUIZ -->
<section id="quiz">
    <div class="card" id="quiz-container">
        <h2>Quiz - Teste seus conhecimentos</h2>
        <p>Responda as 10 perguntas sobre saúde da mulher, métodos contraceptivos e cuidados íntimos.</p>
    </div>
</section>

<nav>
    <button onclick="mostrar('inicio')">🏠<span>Início</span></button>
    <button onclick="mostrar('cuidados')">🧼<span>Cuidados</span></button>
    <button onclick="mostrar('sistema')">🧬<span>Sistema</span></button>
    <button onclick="mostrar('sus')">🩸<span>SUS</span></button>
    <button onclick="mostrar('contraceptivos')">💊<span>Métodos</span></button>
    <button onclick="mostrar('quiz'); gerarQuiz();">❓<span>Quiz</span></button>
</nav>

</body>
</html>
