<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background-color: #fff0f5;
}

header {
    background-color: #d63384;
    color: white;
    padding: 20px;
    text-align: center;
}

nav {
    background-color: #f8c1d9;
    padding: 10px;
    text-align: center;
}

nav button {
    margin: 5px;
    padding: 10px;
    border: none;
    background-color: white;
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
    padding: 15px;
    margin: 10px 0;
    border-radius: 10px;
}
</style>

<script>
function mostrar(secao) {
    let secoes = document.querySelectorAll("section");
    secoes.forEach(s => s.classList.remove("active"));
    document.getElementById(secao).classList.add("active");
}

function verificar() {
    let resposta = document.querySelector('input[name="q1"]:checked');
    if (resposta) {
        if (resposta.value == "certo") {
            alert("Resposta correta!");
        } else {
            alert("Resposta errada!");
        }
    } else {
        alert("Escolha uma resposta!");
    }
}
</script>

</head>

<body>

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Educação e autocuidado</p>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('sintomas')">Sintomas</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio" class="active">
<div class="card">
<h2>Bem-vinda!</h2>
<p>Este site foi criado para orientar mulheres sobre saúde íntima, prevenção e autocuidado.</p>
</div>
</section>

<section id="cuidados">
<div class="card">
<h2>Cuidados básicos</h2>
<p>✔ Higiene íntima diária</p>
<p>✔ Usar roupas confortáveis</p>
<p>✔ Evitar produtos agressivos</p>
</div>
</section>

<section id="sintomas">
<div class="card">
<h2>Sinais de atenção</h2>
<p>⚠ Corrimento com cheiro forte</p>
<p>⚠ Ardência ao urinar</p>
<p>⚠ Coceira intensa</p>
<p>Procure um profissional de saúde.</p>
</div>
</section>

<section id="quiz">
<div class="card">
<h2>Quiz rápido</h2>

<p>Corrimento com cheiro forte é normal?</p>

<input type="radio" name="q1" value="errado"> Sim<br>
<input type="radio" name="q1" value="certo"> Não<br><br>

<button onclick="verificar()">Responder</button>

</div>
</section>

</body>
</html>
