<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #ffe6f0;
}

header {
    background: #ff4d88;
    color: white;
    text-align: center;
    padding: 15px;
}

nav {
    text-align: center;
    background: #ff80aa;
    padding: 10px;
}

nav button {
    margin: 5px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    cursor: pointer;
}

section {
    display: none;
    padding: 20px;
}

.active {
    display: block;
}

.card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
}

button {
    margin-top: 10px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    background: #ff4d88;
    color: white;
}

img {
    margin: 10px;
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
    document.getElementById("res").innerHTML =
    "Você fez " + pontos + " pontos!";
}
</script>

</head>

<body onload="mostrar('inicio')">

<header>
<h1>🌸 Saúde da Mulher</h1>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio">
<div class="card">
<h2>Bem-vinda 💖</h2>
<img src="https://cdn-icons-png.flaticon.com/512/4333/4333609.png" width="100">
<p>Informação ajuda a cuidar da sua saúde.</p>
</div>
</section>

<section id="cuidados">
<div class="card">
<h2>Cuidados</h2>
<img src="https://cdn-icons-png.flaticon.com/512/2966/2966488.png" width="100">
<p>✔ Higiene diária</p>
<p>✔ Beber água</p>
<p>✔ Evitar roupas apertadas</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="quiz">
<div class="card">
<h2>Quiz</h2>

<p>1. Higiene é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>2. Automedicação é recomendada?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>3. Água ajuda?</p>
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
