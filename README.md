<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Guia de Saúde Feminina</title>
<style>
/* ===== GLOBAL ===== */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #fff0f5;
    padding-bottom: 120px;
    line-height: 1.6;
}
h2 { color: #d81b60; margin-top:0; }
h3 { color: #ad1457; margin-bottom:5px; }
ul { margin-left: 20px; }
ul li { margin-bottom:6px; }
button:hover { opacity: 0.8; cursor:pointer; }

/* ===== HEADER ===== */
header {
    background: #d81b60;
    color: white;
    text-align: center;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}
header p { margin-top:5px; }

/* ===== SEÇÕES ===== */
.section { padding: 20px; scroll-margin-bottom: 120px; }
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
.banner {
    width: 100%;
    max-height: 250px;
    object-fit: contain;
    background: white;
    margin-bottom: 15px;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
.caption { font-size: 13px; color: #555; text-align: center; margin-top:5px; }

/* ===== ACORDEÃO ===== */
.acordeao {
    background: #f8bbd0;
    color: #880e4f;
    cursor: pointer;
    padding: 12px;
    width: 100%;
    border: none;
    text-align: left;
    margin-top: 8px;
    border-radius: 8px;
    font-weight: bold;
}
.painel {
    display: none;
    background: #fff;
    padding: 10px;
    border-radius: 8px;
    margin-top: 5px;
}

/* ===== MENU FIXO ===== */
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

/* ===== BOTÃO DE DÚVIDA ===== */
.btn-duvidas {
    position: fixed;
    bottom: 80px;
    right: 15px;
    background: #d81b60;
    color: white;
    border: none;
    padding: 12px 15px;
    border-radius: 30px;
    z-index: 999;
}

/* ===== QUIZ ===== */
.quiz-option { display: block; margin: 8px 0; }
.quiz-result { margin-top: 15px; font-weight: bold; color:#ad1457; }
</style>
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
        <p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher...</p>
        <h3>Sobre a autora</h3>
        <p>Meu nome é Beatriz Dias, tenho 21 anos, sou técnica de enfermagem e estudante de TI. Minha formação em enfermagem garante que o conteúdo seja confiável e fundamentado.</p>
    </div>
</div>

<!-- ===== CUIDADOS ÍNTIMOS ===== -->
<div class="section">
    <img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg" alt="Cuidados Íntimos">
    <div class="card">
        <h2>Cuidados com a Saúde Íntima</h2>
        <ul>
            <li>Evitar duchas internas exageradas.</li>
            <li>Trocar absorventes de 3 a 4 em 4 horas.</li>
            <li>Evitar roupas muito apertadas e sintéticas.</li>
            <li>Manter hidratação adequada.</li>
        </ul>
    </div>
</div>

<!-- ===== SISTEMA REPRODUTOR ===== -->
<div class="section">
    <img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg" alt="Sistema Reprodutor">
    <div class="card">
        <h2>Sistema Reprodutor Feminino</h2>
        <p>Clique em cada parte para aprender mais 👇</p>

        <button class="acordeao">Ovários</button>
        <div class="painel"><p>Os ovários produzem os óvulos e hormônios como estrogênio e progesterona. São responsáveis pela ovulação em cada ciclo menstrual.</p></div>

        <button class="acordeao">Trompas de Falópio</button>
        <div class="painel"><p>Transportam o óvulo até o útero e é onde geralmente ocorre a fecundação.</p></div>

        <button class="acordeao">Útero</button>
        <div class="painel"><p>Órgão onde ocorre o desenvolvimento do bebê. O endométrio é eliminado na menstruação quando não há gravidez.</p></div>

        <button class="acordeao">Vagina</button>
        <div class="painel"><p>Canal que liga o útero ao exterior. Atua na menstruação, relação sexual e parto.</p></div>

        <button class="acordeao">Clitóris</button>
        <div class="painel"><p>Órgão altamente sensível responsável pelo prazer sexual. Possui milhares de terminações nervosas.</p></div>

        <button class="acordeao">Hímen</button>
        <div class="painel"><p>Membrana fina na entrada da vagina. Pode variar de forma e elasticidade e não define virgindade.</p></div>
    </div>
</div>

<!-- ===== ABSORVENTES SUS ===== -->
<div class="section" id="sus">
    <img class="banner" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSR2DIAQSmd8oja-E__rBwfevvQKLwJtIB_RJ-kywc2Eg&s=10" alt="Programa de Dignidade Menstrual SUS">
    <div class="card">
        <h2>Absorventes Gratuitos pelo SUS</h2>
        <p>O Programa de Proteção e Promoção da Saúde Menstrual garante acesso gratuito a absorventes higiênicos para pessoas em situação de vulnerabilidade social.</p>

        <h3>📅 Quando começou?</h3>
        <p>Instituído pela Lei nº 14.214/2021 e implementado nacionalmente a partir de 2023 pelo SUS.</p>

        <h3>👩‍⚕️ Quem tem direito?</h3>
        <ul>
            <li>Pessoas menstruantes em situação de vulnerabilidade social</li>
            <li>Inscritas no CadÚnico</li>
            <li>Estudantes da rede pública de baixa renda</li>
            <li>Pessoas em situação de rua</li>
            <li>Pessoas privadas de liberdade ou em medidas socioeducativas</li>
        </ul>

        <h3>📍 Onde retirar?</h3>
        <ul>
            <li>Unidades Básicas de Saúde (UBS)</li>
            <li>Farmácias credenciadas</li>
            <li>Escolas públicas participantes</li>
            <li>Centros de Referência de Assistência Social (CRAS)</li>
        </ul>

        <h3>📲 Como conseguir?</h3>
        <ul>
            <li>Apresentar CPF ou Cartão do SUS</li>
            <li>Estar inscrita no CadÚnico (quando necessário)</li>
            <li>Solicitar diretamente na unidade participante</li>
            <li>Em alguns casos, cadastro ou autorização via aplicativo/unidade de saúde</li>
        </ul>

        <h3>💡 Por que isso é importante?</h3>
        <ul>
            <li>Combate à pobreza menstrual</li>
            <li>Reduz riscos de infecções</li>
            <li>Diminui evasão escolar</li>
            <li>Promove dignidade e igualdade</li>
            <li>Garante acesso à higiene básica</li>
        </ul>

        <h3>⚠️ O que é pobreza menstrual?</h3>
        <p>Falta de acesso a produtos de higiene menstrual, saneamento básico e informação adequada, afetando saúde física, emocional e social.</p>

        <h3>🏥 Papel do SUS</h3>
        <p>Distribui absorventes, promove educação menstrual, prevenção de doenças e acolhimento.</p>

        <h3>📚 Informação também é cuidado</h3>
        <p>O programa incentiva ações educativas sobre saúde menstrual, higiene íntima e autocuidado, especialmente para adolescentes e jovens.</p>
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
            <li>Ferro e vitamina C: previnem anemia</li>
            <li>Cálcio e vitamina D: fortalecem ossos</li>
            <li>Ômega 3: melhora saúde cardiovascular</li>
            <li>Hidratação: essencial para equilíbrio do corpo</li>
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
        <p>Pré-natal e acompanhamento médico garantem saúde materna e fetal.</p>
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

<!-- ===== DÚVIDAS ===== -->
<div class="section" id="duvidas">
    <div class="card">
        <h2>💬 Tirar Dúvidas</h2>
        <p>Este formulário é anônimo. Envie sua dúvida com segurança 💖</p>
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScpEDQnLimCVNfT1gR5rDJN0pbk1Vz32E5c79Oc0Kg8c7SXnA/viewform?embedded=true" width="100%" height="600"></iframe>
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
/* ===== ACORDEÃO ===== */
var acc = document.getElementsByClassName("acordeao");
for (var i = 0; i < acc.length; i++) {
    acc[i].onclick = function() {
        this.classList.toggle("ativo");
        var painel = this.nextElementSibling;
        painel.style.display = (painel.style.display === "block") ? "none" : "block";
    };
}

/* ===== BOTÃO DÚVIDAS ===== */
document.getElementById("abrir-duvidas").onclick = function() {
    document.getElementById("duvidas").scrollIntoView({ behavior: "smooth" });
};

/* ===== QUIZ ===== */
/* ===== QUIZ ===== */
const quizData = [
    {
        pergunta:"1. Qual é a função dos ovários?",
        opcoes:["Produzir espermatozoides","Produzir óvulos e hormônios","Armazenar sangue","Filtrar toxinas"],
        resposta:1
    },
    {
        pergunta:"2. De quanto em quanto tempo deve trocar o absorvente?",
        opcoes:["1 vez ao dia","A cada 12 horas","A cada 3 a 4 horas","Só quando estiver cheio"],
        resposta:2
    },
    {
        pergunta:"3. O que previne ISTs?",
        opcoes:["Pílula","DIU","Preservativo","Chá natural"],
        resposta:2
    },
    {
        pergunta:"4. Qual exame previne câncer do colo do útero?",
        opcoes:["Mamografia","Ultrassom","Papanicolau","Raio-x"],
        resposta:2
    },
    {
        pergunta:"5. O SUS oferece absorventes gratuitos?",
        opcoes:["Não","Sim","Só em hospitais privados","Apenas para idosos"],
        resposta:1
    },
    {
        pergunta:"6. O útero tem qual função?",
        opcoes:["Digestão","Respiração","Gestação","Filtração"],
        resposta:2
    },
    {
        pergunta:"7. Qual vitamina ajuda na prevenção da anemia?",
        opcoes:["Vitamina C","Vitamina D","Ferro + Vitamina C","Magnésio"],
        resposta:2
    },
    {
        pergunta:"8. O que é pobreza menstrual?",
        opcoes:["Falta de renda apenas","Falta de acesso a higiene menstrual","Doença infecciosa","Tipo de anemia"],
        resposta:1
    },
    {
        pergunta:"9. Qual método contraceptivo é mais seguro contra ISTs?",
        opcoes:["DIU","Pílula","Preservativo","Tabelinha"],
        resposta:2
    },
    {
        pergunta:"10. A saúde mental pode influenciar o ciclo menstrual?",
        opcoes:["Não","Sim","Só em casos raros","Apenas em adolescentes"],
        resposta:1
    }
];

function gerarQuiz(){
    const container = document.getElementById("quiz-container");

    quizData.forEach((q, index)=>{
        let div = document.createElement("div");
        div.innerHTML = `<p><
