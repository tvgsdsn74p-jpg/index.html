<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher - Projeto ODS 4</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #fff0f5;
}

header {
    background: #e91e63;
    color: white;
    text-align: center;
    padding: 20px;
}

nav {
    background: #f06292;
    text-align: center;
    padding: 10px;
}

nav button {
    margin: 5px;
    padding: 10px;
    border-radius: 20px;
    border: none;
    cursor: pointer;
    background: white;
}

section {
    display: none;
}

.banner {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card {
    background: white;
    margin: 20px;
    padding: 20px;
    border-radius: 15px;
    line-height: 1.6;
}

h2 {
    color: #e91e63;
}

button {
    margin-top: 10px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    background: #e91e63;
    color: white;
}
</style>

<script>
function mostrar(secao){
    document.querySelectorAll("section").forEach(s => s.style.display="none");
    document.getElementById(secao).style.display="block";
}

let pontos = 0;

function responder(correta){
    if(correta){
        pontos++;
    }
}

function resultado(){
    let msg = "";

    if(pontos <= 4){
        msg = "Você precisa reforçar seus conhecimentos 😢";
    } else if(pontos <= 7){
        msg = "Você tem um bom conhecimento 👍";
    } else {
        msg = "Excelente! Você domina o assunto 👏💖";
    }

    document.getElementById("res").innerHTML =
    "Pontuação: " + pontos + "/10 <br>" + msg;
}
</script>

</head>

<body onload="mostrar('inicio')">

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Projeto Educativo - ODS 4</p>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('sintomas')">Sintomas</button>
<button onclick="mostrar('prevencao')">Prevenção</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio">
<img class="banner" src="https://images.unsplash.com/photo-1584515933487-779824d29309">
<div class="card">
<h2>Bem-vinda</h2>
<p>Este projeto tem como objetivo promover a educação em saúde da mulher, contribuindo para o conhecimento, prevenção de doenças e melhoria da qualidade de vida.</p>

<p>A informação é uma das principais ferramentas para o autocuidado. Muitas doenças podem ser evitadas ou tratadas precocemente quando a mulher conhece seu próprio corpo e reconhece sinais de alerta.</p>
</div>
</section>

<section id="cuidados">
<img class="banner" src="https://images.unsplash.com/photo-1588776814546-1ffcf47267a5">
<div class="card">
<h2>Cuidados com a saúde</h2>

<p>A higiene íntima deve ser feita diariamente, utilizando produtos adequados e evitando exageros, pois o excesso também pode causar desequilíbrio.</p>

<p>O uso de roupas leves e de algodão ajuda a evitar infecções, pois permite melhor ventilação da região íntima.</p>

<p>Beber água e manter uma alimentação saudável também são fatores importantes para o funcionamento do organismo.</p>

<p>Evitar roupas muito apertadas e permanecer muito tempo com roupas úmidas são cuidados essenciais.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="sintomas">
<img class="banner" src="https://images.unsplash.com/photo-1607746882042-944635dfe10e">
<div class="card">
<h2>Sintomas de alerta</h2>

<p>Alguns sinais indicam que algo pode não estar bem:</p>

<p>⚠ Corrimento com cor ou odor diferente</p>
<p>⚠ Coceira intensa</p>
<p>⚠ Ardência ao urinar</p>
<p>⚠ Dor durante relações</p>

<p>Esses sintomas podem indicar infecções ou outras condições que precisam de avaliação profissional.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="prevencao">
<img class="banner" src="https://images.unsplash.com/photo-1576091160550-2173dba999ef">
<div class="card">
<h2>Prevenção</h2>

<p>A prevenção é a melhor forma de cuidar da saúde.</p>

<p>O uso de preservativo é essencial para evitar infecções sexualmente transmissíveis.</p>

<p>Consultas regulares ao ginecologista ajudam na detecção precoce de doenças.</p>

<p>Exames como o preventivo (Papanicolau) são fundamentais para a saúde feminina.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="quiz">
<img class="banner" src="https://images.unsplash.com/photo-1584697964190-7383cde1d19c">
<div class="card">
<h2>Quiz Educativo</h2>

<p>1. Higiene íntima é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>2. Automedicação é recomendada?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>3. Beber água ajuda na saúde?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>4. Corrimento diferente é normal?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>5. Dor ao urinar é sinal de alerta?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>6. Preservativo previne doenças?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>7. Consultar médico é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>8. Coceira pode indicar problema?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>9. Roupas apertadas podem prejudicar?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>10. Prevenção é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<br><br>
<button onclick="resultado()">Ver resultado</button>

<p id="res"></p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

</body>
</html>
