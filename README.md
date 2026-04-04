<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher - Projeto ODS 4</title>
<style>
/* ===== Estilos Globais ===== */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #fff0f5;
    padding-bottom: 120px;
    <!-- ===== DÚVIDAS ===== -->
<div class="section" id="duvidas">
    <div class="card">
        <h2>💬 Tirar Dúvidas</h2>
        <p>Este formulário é anônimo. Envie sua dúvida com segurança 💖</p>

        <iframe 
            src="https://docs.google.com/forms/d/e/1FAIpQLScpEDQnLimCVNfT1gR5rDJN0pbk1Vz32E5c79Oc0Kg8c7SXnA/viewform?embedded=true" 
            width="100%" 
            height="600" 
            frameborder="0">
        </iframe>
    </div>
</div>
    /* espaço para menu fixo */
    line-height: 1.6;
}
h2 { color: #d81b60; margin-top:0; }
h3 { color: #ad1457; margin-bottom:5px; }
ul { margin-left: 20px; }

/* ===== Header ===== */
header {
    background: #d81b60;
    color: white;
    text-align: center;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}
header p { margin-top:5px; }

/* ===== Seções ===== */
.section {
    padding: 20px;
}
.card {
    background: white;
    margin: 20px auto;
    padding: 20px;
    border-radius: 12px;
    max-width: 900px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}
.card:hover { transform: translateY(-3px); }

/* ===== Banner ===== */
.banner {
    width: 100%;
    max-height: 250px;
    object-fit: contain;
    background: white;
    margin-bottom: 15px;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
<!-- ===== DÚVIDAS ===== -->
<div class="section" id="duvidas">
    ...
</div>
        <h2>💬 Tirar Dúvidas</h2>
        <p>Este formulário é anônimo. Envie sua dúvida com segurança 💖</p>

        <iframe 
            src="https://docs.google.com/forms/d/e/1FAIpQLScpEDQnLimCVNfT1gR5rDJN0pbk1Vz32E5c79Oc0Kg8c7SXnA/viewform?embedded=true" 
            width="100%" 
            height="600" 
            frameborder="0">
        </iframe>
    </div>
</div>
/* ===== Menu de Navegação ===== */
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
nav button span { margin-top: 2px; }

/* ===== Quiz ===== */
.quiz-option { display: block; margin: 8px 0; }
.quiz-result { margin-top: 15px; font-weight: bold; color:#ad1457; }
button:hover { opacity: 0.8; cursor:pointer; }

/* ===== Legendas de imagens ===== */
.caption { font-size: 13px; color: #555; text-align: center; margin-top:5px; }

/* ===== Estilo de listas detalhadas ===== */
ul li { margin-bottom:6px; }
</style>
<script>
/* ===== Dados do Quiz ===== */
const quizData = [
    { pergunta:"1. Qual é a função dos ovários?", opcoes:["Produzir espermatozoides","Produzir óvulos e hormônios","Armazenar sangue","Controlar digestão"], correta:1 },
    { pergunta:"2. Qual método contraceptivo é oferecido gratuitamente pelo SUS?", opcoes:["Implante hormonal","DIU hormonal","Pílula anticoncepcional","Anel vaginal particular"], correta:2 },
    { pergunta:"3. Qual tecido é recomendado para roupas íntimas?", opcoes:["Sintético","Algodão","Plástico","Lã"], correta:1 },
    { pergunta:"4. Quem tem direito aos absorventes gratuitos do SUS?", opcoes:["Pessoas inscritas no CadÚnico","Qualquer pessoa","Somente homens","Pessoas com carro próprio"], correta:0 },
    { pergunta:"5. Qual é o órgão onde o bebê se desenvolve?", opcoes:["Vagina","Útero","Ovário","Trompa de Falópio"], correta:1 },
    { pergunta:"6. Qual método protege contra ISTs?", opcoes:["Preservativo","DIU","Pílula","Implante"], correta:0 },
    { pergunta:"7. Qual é um método natural de contracepção?", opcoes:["Adesivo hormonal","Tabelinha","DIU de cobre","Injeção hormonal"], correta:1 },
    { pergunta:"8. Por que roupas apertadas podem ser prejudiciais?", opcoes:["Aumentam umidade e risco de infecção","Melhoram a circulação","Fortalecem músculos","Previnem doenças"], correta:0 },
    { pergunta:"9. O que significa dignidade menstrual?", opcoes:["Acesso a absorventes, informação e condições adequadas","Ir para escola todos os dias","Tomar banho apenas uma vez","Comprar roupas caras"], correta:0 },
    { pergunta:"10. Qual órgão transporta o óvulo até o útero?", opcoes:["Vagina","Trompa de Falópio","Ovário","Útero"], correta:1 }
];

/* ===== Função para gerar quiz ===== */
function gerarQuiz(){
    const container=document.getElementById("quiz-container");
    quizData.forEach((q,i)=>{
        const div=document.createElement("div");
        div.className="card";
        const pergunta=document.createElement("h3");
        pergunta.textContent=q.pergunta;
        div.appendChild(pergunta);
        q.opcoes.forEach((op,idx)=>{
            const label=document.createElement("label");
            label.className="quiz-option";
            const input=document.createElement("input");
            input.type="radio";
            input.name="q"+i;
            input.value=idx;
            label.appendChild(input);
            label.appendChild(document.createTextNode(" "+op));
            div.appendChild(label);
        });
        container.appendChild(div);
    });
    const btn=document.createElement("button");
    btn.textContent="Verificar Respostas";
    btn.onclick=verificarQuiz;
    container.appendChild(btn);
    const resultado=document.createElement("div");
    resultado.id="resultado";
    resultado.className="quiz-result";
    container.appendChild(resultado);
}

/* ===== Função para checar respostas ===== */
function verificarQuiz(){
    let score=0;
    quizData.forEach((q,i)=>{
        const selecionado=document.querySelector('input[name="q'+i+'"]:checked');
        if(selecionado && parseInt(selecionado.value)===q.correta){ score++; }
    });
    document.getElementById("resultado").textContent="Você acertou "+score+" de "+quizData.length+" perguntas.";
}
</script>
</head>
<body onload="gerarQuiz()">

<!-- ===== HEADER ===== -->
<header>
    <h1>🌸 Saúde da Mulher</h1>
    <p>Projeto Educativo - ODS 4 | Educação de Qualidade</p>
</header>

<!-- ===== INÍCIO ===== -->
<div class="section">
    <img class="banner" src="https://img.freepik.com/vetores-gratis/conceito-de-sistema-reprodutivo-feminino_52683-45450.jpg?semt=ais_hybrid&w=740&q=80" alt="Sistema reprodutor feminino ilustrado">
    <div class="card">
        <p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher, abordando temas importantes como prevenção, cuidados íntimos, métodos contraceptivos e acesso a serviços de saúde.</p>
        <p>As informações são apresentadas de forma clara e acessível, contribuindo para o conhecimento, autonomia e bem-estar.</p>
        <h3>Sobre a autora</h3>
        <p>Meu nome é Beatriz Dias, tenho 21 anos, sou formada como técnica de enfermagem e atualmente estudante da área de Tecnologia da Informação. Minha formação em enfermagem me proporciona conhecimento sólido sobre saúde feminina, garantindo que o conteúdo apresentado seja confiável, relevante e fundamentado em práticas de cuidado real.</p>
        <p>Este trabalho foi desenvolvido como atividade acadêmica, com foco em educação e impacto social, e está alinhado com a ODS 4 (Educação de Qualidade), incentivando o acesso à informação e à conscientização sobre a saúde feminina.</p>
    </div>
</div>

<!-- ===== CUIDADOS ÍNTIMOS ===== -->
<div class="section">
    <img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg" alt="Cuidados Íntimos">
    <div class="card">
        <h2>Cuidados com a Saúde Íntima</h2>
        <p>A higiene íntima correta previne infecções, desconfortos e problemas urinários. Roupas de algodão, sabonetes neutros e troca regular de absorventes são essenciais.</p>
        <ul>
            <li>Evitar duchas internas exageradas.</li>
            <li>Trocar absorventes de 3 a 4 em 4 horas.</li>
            <li>Evitar roupas muito apertadas e sintéticas.</li>
            <li>Manter hidratação adequada para saúde geral.</li>
        </ul>
    </div>
</div>

<!-- ===== SISTEMA REPRODUTOR ===== -->
<div class="section">
    <img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg" alt="Sistema Reprodutor">
    <div class="card">
        <h2>Sistema Reprodutor Feminino</h2>
        <p>Composto por ovários, trompas, útero e vagina, é responsável pela reprodução, produção hormonal e ciclo menstrual.</p>
        <ul>
            <li>Ovários: produzem óvulos e hormônios.</li>
            <li>Trompas de Falópio: transporte do óvulo até o útero.</li>
            <li>Útero: desenvolvimento do bebê.</li>
            <li>Vagina: canal de parto e órgão de relação sexual.</li>
        </ul>
    </div>
</div>

<!-- ===== ABSORVENTES SUS ===== -->
<div class="section">
    <img class="banner" 
     src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSR2DIAQSmd8oja-E__rBwfevvQKLwJtIB_RJ-kywc2Eg&s=10" 
     alt="Absorventes SUS" 
     style="object-fit:contain; max-height:250px;">
    <div class="card">
        <h2>Absorventes Gratuitos pelo SUS</h2>
        <p>Disponíveis para pessoas cadastradas no CadÚnico ou em programas sociais. Garantem dignidade menstrual e acesso à saúde.</p>
        <ul>
            <li>Distribuição em escolas públicas e centros de saúde.</li>
            <li>Previnem infecções e ausências escolares.</li>
            <li>Importante para adolescentes e mulheres em vulnerabilidade social.</li>
        </ul>
    </div>
</div>

<!-- ===== MÉTODOS CONTRACEPTIVOS ===== -->
<div class="section">
    <img class="banner" src="https://static.vecteezy.com/ti/vetor-gratis/p1/6922254-contraceptivos-conjunto-controle-de-natalidade-ilustracao-para-impressao-fundos-capas-embalagem-cartoes-cartazes-adesivos-textil-e-design-sazonal-isolado-em-fundo-branco-vetor.jpg" alt="Métodos Contraceptivos">
    <div class="card">
        <h2>Métodos Contraceptivos</h2>
        <p>Existem métodos oferecidos gratuitamente pelo SUS e outros particulares. O ideal é escolher conforme saúde, idade e planejamento familiar.</p>
        <ul>
            <li>Pílulas anticoncepcionais</li>
            <li>DIU (hormonal e de cobre)</li>
            <li>Implantes hormonais</li>
            <li>Preservativos masculino e feminino</li>
            <li>Métodos naturais (tabelinha, ovulação)</li>
        </ul>
        <p>Consulta com ginecologista é fundamental para escolher o método mais adequado.</p>
    </div>
</div>

<!-- ===== ALIMENTAÇÃO ===== -->
<div class="section">
    <div class="card">
        <h2>Alimentação e Saúde Feminina</h2>
        <p>Dieta equilibrada influencia hormônios, imunidade e bem-estar menstrual.</p>
        <ul>
            <li>Ferro e vitamina C: previnem anemia.</li>
            <li>Cálcio e vitamina D: fortalecem ossos.</li>
            <li>Ômega 3: melhora saúde cardiovascular.</li>
            <li>Hidratação: essencial para equilíbrio do corpo.</li>
        </ul>
    </div>
</div>

<!-- ===== EXAMES PREVENTIVOS ===== -->
<div class="section">
    <div class="card">
        <h2>Exames Preventivos</h2>
        <p>Essenciais para prevenção de doenças e detecção precoce de problemas de saúde.</p>
        <ul>
            <li>Papanicolau: câncer de colo uterino</li>
            <li>Mamografia: câncer de mama</li>
            <li>Exames de ISTs: HIV, sífilis, hepatite</li>
            <li>Check-ups regulares com ginecologista</li>
        </ul>
    </div>
</div>

<!-- ===== GRAVIDEZ ===== -->
<div class="section">
    <div class="card">
        <h2>Gravidez e Planejamento Familiar</h2>
        <p>Pré-natal e acompanhamento médico garantem saúde materna e fetal. Planejamento familiar permite decisões conscientes sobre maternidade.</p>
        <ul>
            <li>Exames periódicos</li>
            <li>Suplementos: ácido fólico, vitaminas</li>
            <li>Alimentação saudável</li>
            <li>Apoio psicológico</li>
        </ul>
    </div>
</div>

<!-- ===== PREVENÇÃO DE ISTs ===== -->
<div class="section">
    <div class="card">
        <h2>Prevenção de ISTs</h2>
        <p>Uso correto de preservativos, vacinas e exames periódicos são essenciais.</p>
        <ul>
            <li>Preservativos masculino e feminino</li>
            <li>Vacinas: HPV, Hepatite B</li>
            <li>Exames regulares e acompanhamento médico</li>
            <li>Educação sexual e conscientização</li>
        </ul>
    </div>
</div>

<!-- ===== SAÚDE MENTAL ===== -->
<div class="section">
    <div class="card">
        <h2>Saúde Mental</h2>
        <p>Hormônios e ciclo menstrual influenciam humor e bem-estar emocional. Práticas de relaxamento, exercícios e acompanhamento psicológico são recomendados.</p>
        <ul>
            <li>Exercícios físicos regulares</li>
            <li>Técnicas de respiração e meditação</li>
            <li>Apoio psicológico quando necessário</li>
            <li>Diário do ciclo menstrual</li>
        </ul>
    </div>
</div>

<!-- ===== QUIZ ===== -->
<div class="section" id="quiz">
    <div id="quiz-container">
        <h2>Quiz - Teste seus conhecimentos</h2>
        <p>Responda as 10 perguntas sobre saúde da mulher, métodos contraceptivos e cuidados íntimos.</p>
    </div>
</div>

<!-- ===== MENU FIXO ===== -->
<nav>
    <button onclick="window.scrollTo(0,0)">🏠<span>Início</span></button>
    <button onclick="document.querySelectorAll('.section')[1].scrollIntoView()">🧼<span>Cuidados</span></button>
    <button onclick="document.querySelectorAll('.section')[2].scrollIntoView()">🧬<span>Sistema</span></button>
    <button onclick="document.querySelectorAll('.section')[3].scrollIntoView()">🩸<span>SUS</span></button>
    <button onclick="document.querySelectorAll('.section')[4].scrollIntoView()">💊<span>Métodos</span></button>
    <button onclick="document.querySelectorAll('.section')[5].scrollIntoView()">🥗<span>Alimentação</span></button>
    <button onclick="document.querySelectorAll('.section')[6].scrollIntoView()">🧪<span>Exames</span></button>
    <button onclick="document.querySelectorAll('.section')[7].scrollIntoView()">🤰<span>Gravidez</span></button>
    <button onclick="document.querySelectorAll('.section')[8].scrollIntoView()">🛡️<span>ISTs</span></button>
    <button onclick="document.querySelectorAll('.section')[9].scrollIntoView()">🧠<span>Mental</span></button>
    <button onclick="document.querySelectorAll('.section')[10].scrollIntoView()">❓<span>Quiz</span></button>    
</nav>
<button id="abrir-duvidas" class="btn-duvidas">💬 Tirar Dúvida</button>

<script>
document.getElementById("abrir-duvidas").onclick = function() {
    document.getElementById("duvidas").scrollIntoView({ behavior: "smooth" });
};
</script>
</body>
</html>
