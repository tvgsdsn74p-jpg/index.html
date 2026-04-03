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

.card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
}

img {
    width: 100px;
    margin: 10px;
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
    let msg = "";

    if(pontos <= 4){
        msg = "Você precisa aprender mais 😢";
    } else if(pontos <= 7){
        msg = "Você sabe o básico 👍";
    } else {
        msg = "Excelente! 👏💖";
    }

    document.getElementById("res").innerHTML =
    "Pontuação: " + pontos + "/10 <br>" + msg;
}
</script>

</head>

<body onload="mostrar('inicio')">

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Educação e prevenção</p>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('sintomas')">Sintomas</button>
<button onclick="mostrar('prevencao')">Prevenção</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio">
<div class="card">
<h2>Bem-vinda 💖</h2>
<img src="https://cdn-icons-png.flaticon.com/512/4333/4333609.png">
<p>Este site educativo ajuda mulheres a entender melhor sua saúde.</p>
<p>A informação é essencial para prevenção de doenças e bem-estar.</p>
</div>
</section>

<section id="cuidados">
<div class="card">
<h2>Cuidados básicos</h2>
<img src="https://cdn-icons-png.flaticon.com/512/2966/2966488.png">
<p>✔ Higiene íntima diária</p>
<p>✔ Uso de roupas de algodão</p>
<p>✔ Evitar roupas apertadas</p>
<p>✔ Trocar absorventes regularmente</p>
<p>✔ Beber bastante água</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="sintomas">
<div class="card">
<h2>Sintomas</h2>
<img src="https://cdn-icons-png.flaticon.com/512/1828/1828843.png">
<p>⚠ Corrimento diferente</p>
<p>⚠ Mau cheiro</p>
<p>⚠ Coceira</p>
<p>⚠ Ardência ao urinar</p>
<p>⚠ Dor durante relação</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="prevencao">
<div class="card">
<h2>Prevenção</h2>
<img src="https://cdn-icons-png.flaticon.com/512/2921/2921822.png">
<p>✔ Uso de preservativo</p>
<p>✔ Consultas regulares</p>
<p>✔ Exames preventivos</p>
<p>✔ Evitar automedicação</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<section id="quiz">
<div class="card">
<h2>Quiz</h2>

<p>1. Higiene íntima é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>2. Automedicação é recomendada?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>3. Beber água ajuda na saúde?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>4. Corrimento estranho é normal?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>5. Dor ao urinar é sinal de alerta?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>6. Usar preservativo previne doenças?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>7. Roupas apertadas ajudam?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>8. Consultar médico é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>9. Coceira pode indicar problema?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>10. Higiene deve ser evitada?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<br><br>
<button onclick="resultado()">Ver resultado</button>

<p id="res"></p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

</body>
</html>
