
 <!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: linear-gradient(to right, #ffe6f0, #fff);
}

header {
    background: #c2185b;
    color: white;
    padding: 25px;
    text-align: center;
}

nav {
    background: #f8bbd0;
    padding: 10px;
    text-align: center;
}

nav button {
    padding: 10px 15px;
    margin: 5px;
    border: none;
    border-radius: 20px;
    background: white;
    cursor: pointer;
    font-weight: bold;
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
    margin: 15px auto;
    border-radius: 15px;
    max-width: 600px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
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
    if (!resposta) {
        alert("Escolha uma resposta!");
        return;
    }

    if (resposta.value == "certo") {
        alert("✅ Correto!");
    } else {
        alert("❌ Errado!");
    }
}
</script>

</head>

<body>

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Educação, prevenção e autocuidado</p>
</header>

<nav>
<button onclick="mostrar('inicio')">Início</button>
<button onclick="mostrar('cuidados')">Cuidados</button>
<button onclick="mostrar('sintomas')">Sintomas</button>
<button onclick="mostrar('mitos')">Mitos</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio" class="active">
<div class="card">
<h2>Bem-vinda 💖</h2>
<p>Este projeto tem como objetivo ensinar de forma simples sobre saúde íntima feminina, promovendo informação e prevenção.</p>
</div>
</section>

<section id="cuidados">
<div class="card">
<h2>Cuidados básicos</h2>
<p>✔ Higiene íntima diária</p>
<p>✔ Uso de roupas confortáveis</p>
<p>✔ Evitar produtos com cheiro forte</p>
<p>✔ Beber bastante água</p>
</div>
</section>

<section id="sintomas">
<div class="card">
<h2>Sinais de alerta</h2>
<p>⚠ Corrimento com odor forte</p>
<p>⚠ Coceira intensa</p>
<p>⚠ Ardência ao urinar</p>
<p>⚠ Dor durante relação</p>
<p><b>Procure um profissional de saúde.</b></p>
</div>
</section>

<section id="mitos">
<div class="card">
<h2>Mitos e Verdades</h2>
<p><b>❌ Mito:</b> Corrimento sempre é normal</p>
<p><b>✔ Verdade:</b> Depende do cheiro e cor</p>

<p><b>❌ Mito:</b> Só precisa ir ao ginecologista com dor</p>
<p><b>✔ Verdade:</b> Consultas preventivas são essenciais</p>
</div>
</section>

<section id="quiz">
<div class="card">
<h2>Teste seu conhecimento</h2>

<p>Corrimento com cheiro forte é normal?</p>

<input type="radio" name="q1" value="errado"> Sim<br>
<input type="radio" name="q1" value="certo"> Não<br><br>

<button onclick="verificar()">Responder</button>

</div>
</section>

</body>
</html>
