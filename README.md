<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: linear-gradient(#ffe6f0, #ffffff);
}

header {
    background: #ff4d88;
    color: white;
    padding: 20px;
    text-align: center;
}

nav {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    background: #ff80aa;
}

nav button {
    margin: 5px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    background: white;
    cursor: pointer;
    font-weight: bold;
}

section {
    display: none;
    padding: 20px;
    opacity: 0;
    transition: 0.5s;
}

.active {
    display: block;
    opacity: 1;
}

.card {
    background: white;
    padding: 20px;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

button {
    margin-top: 10px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    background: #ff4d88;
    color: white;
    cursor: pointer;
}

.progress {
    height: 10px;
    background: #ddd;
    border-radius: 10px;
    margin: 10px 0;
}

.progress-bar {
    height: 10px;
    background: #ff4d88;
    width: 0%;
    border-radius: 10px;
}
</style>

<script>
function mostrar(secao){
    document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
    document.getElementById(secao).classList.add("active");
}

let pontos = 0;
let respondidas = 0;

function responder(btn, correta){
    if(btn.classList.contains("clicado")) return;

    btn.classList.add("clicado");

    if(correta){
        pontos++;
        btn.style.background = "green";
    } else {
        btn.style.background = "red";
    }

    respondidas++;
    atualizarBarra();
}

function atualizarBarra(){
    let progresso = (respondidas / 10) * 100;
    document.getElementById("barra").style.width = progresso + "%";
}

function resultado(){
    let texto = "";

    if(pontos <= 4){
        texto = "Você precisa aprender mais 😢";
    } else if(pontos <= 7){
        texto = "Você sabe o básico 👍";
    } else {
        texto = "Excelente! 👏💖";
    }

    document.getElementById("resultado").innerHTML =
    "Pontuação: " + pontos + "/10 <br>" + texto;
}
</script>

</head>

<body>

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Educação e prevenção</p>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio" class="active">
<div class="card">
<h2>Bem-vinda 💖</h2>
<p>Este projeto promove educação sobre saúde da mulher.</p>
<p>Conhecimento ajuda na prevenção e cuidado.</p>
</div>
</section>

<section id="cuidados">
<div class="card">
<h2>Cuidados</h2>
<p>✔ Higiene adequada</p>
<p>✔ Roupas leves</p>
<p>✔ Hidratação</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="quiz">
<div class="card">
<h2>Quiz</h2>

<div class="progress">
<div id="barra" class="progress-bar"></div>
</div>

<p>1. Higiene diária é importante?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>2. Automedicação é recomendada?</p>
<button onclick="responder(this,false)">Sim</button>
<button onclick="responder(this,true)">Não</button>

<p>3. Corrimento estranho é normal?</p>
<button onclick="responder(this,false)">Sim</button>
<button onclick="responder(this,true)">Não</button>

<p>4. Água ajuda na saúde?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>5. Preservativo previne doenças?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>6. Dor ao urinar é sinal de alerta?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>7. Roupas apertadas ajudam?</p>
<button onclick="responder(this,false)">Sim</button>
<button onclick="responder(this,true)">Não</button>

<p>8. Consultar médico é importante?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>9. Coceira pode indicar problema?</p>
<button onclick="responder(this,true)">Sim</button>
<button onclick="responder(this,false)">Não</button>

<p>10. Higiene íntima deve ser evitada?</p>
<button onclick="responder(this,false)">Sim</button>
<button onclick="responder(this,true)">Não</button>

<br><br>
<button onclick="resultado()">Ver resultado</button>

<p id="resultado"></p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

</body>
</html>
