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
}

.banner {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.card {
    background: white;
    margin: 15px;
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
    let msg = pontos >= 7 ? "Muito bem! 👏" : "Precisa melhorar 😊";
    document.getElementById("res").innerHTML = "Pontuação: " + pontos + "/10 <br>" + msg;
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
<button onclick="mostrar('sintomas')">Sintomas</button>
<button onclick="mostrar('prevencao')">Prevenção</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio">
<img class="banner" src="https://images.unsplash.com/photo-1584515933487-779824d29309">
<div class="card">
<h2>Bem-vinda 💖</h2>
<p>Informação é essencial para o cuidado com a saúde da mulher.</p>
</div>
</section>

<section id="cuidados">
<img class="banner" src="https://images.unsplash.com/photo-1588776814546-1ffcf47267a5">
<div class="card">
<h2>Cuidados básicos</h2>
<p>✔ Higiene íntima adequada</p>
<p>✔ Uso de roupas confortáveis</p>
<p>✔ Hidratação</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="sintomas">
<img class="banner" src="https://images.unsplash.com/photo-1607746882042-944635dfe10e">
<div class="card">
<h2>Sintomas</h2>
<p>⚠ Corrimento</p>
<p>⚠ Coceira</p>
<p>⚠ Dor</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="prevencao">
<img class="banner" src="https://images.unsplash.com/photo-1576091160550-2173dba999ef">
<div class="card">
<h2>Prevenção</h2>
<p>✔ Uso de preservativo</p>
<p>✔ Consultas regulares</p>
<p>✔ Exames</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="quiz">
<img class="banner" src="https://images.unsplash.com/photo-1584697964190-7383cde1d19c">
<div class="card">
<h2>Quiz</h2>

<p>1. Higiene é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>2. Água ajuda na saúde?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>3. Automedicação é correta?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>4. Preservativo previne doenças?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>5. Coceira pode ser sinal de problema?</p>
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
