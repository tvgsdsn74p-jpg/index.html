<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>section {
    display: none;
    padding: 20px;
    opacity: 0;
    transition: opacity 0.5s;
}

.active {
    display: block;
    opacity: 1;
}
body {
    font-family: Arial;
    margin: 0;
    background: linear-gradient(to right, #ffe6f0, #ffffff);
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
    text-align: center;
}

img {
    margin-bottom: 10px;
}
</style>

<script>
function mostrar(secao) {
    let secoes = document.querySelectorAll("section");
    secoes.forEach(s => s.classList.remove("active"));
    document.getElementById(secao).classList.add("active");
}

function verificar() {
    let pontos = 0;

    let q1 = document.querySelector('input[name="q1"]:checked');
    let q2 = document.querySelector('input[name="q2"]:checked');
    let q3 = document.querySelector('input[name="q3"]:checked');

    if (!q1 || !q2 || !q3) {
        alert("Responda todas as perguntas!");
        return;
    }

    if (q1.value == "certo") pontos++;
    if (q2.value == "certo") pontos++;
    if (q3.value == "certo") pontos++;

    if (pontos == 3) {
        alert("🎉 Parabéns! Você acertou tudo!");
    } else if (pontos == 2) {
        alert("👍 Muito bem!");
    } else {
        alert("⚠️ Revise o conteúdo!");
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
<button onclick="mostrar('quando')">Médico</button>
<button onclick="mostrar('quiz')">Quiz</button>
</nav>

<section id="inicio" class="active"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/2913/2913465.png" width="90">
<h2>Bem-vinda 💖</h2>

<img src="https://cdn-icons-png.flaticon.com/512/4333/4333609.png" width="100">

<p>Este projeto foi criado para ajudar mulheres a entender melhor seu corpo e sua saúde.</p>

<p>Aqui você encontrará informações simples, seguras e importantes sobre cuidados íntimos, prevenção de doenças e quando procurar ajuda médica.</p>
</div>
</section>

<section id="cuidados"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/2966/2966488.png" width="90">
<h2>Cuidados básicos</h2>
<p>✔ Lave a região íntima diariamente com água e sabonete neutro</p>
<p>✔ Prefira roupas íntimas de algodão</p>
<p>✔ Evite roupas muito apertadas</p>
<p>✔ Troque absorventes com frequência</p>
<p>✔ Evite duchas internas</p>
<p>✔ Beba bastante água</p>
</section>

<section id="sintomas"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/1828/1828843.png" width="90">
<h2>Sinais de alerta</h2>
<p>⚠ Corrimento com cor diferente (amarelo, verde)</p>
<p>⚠ Cheiro forte ou desagradável</p>
<p>⚠ Coceira intensa</p>
<p>⚠ Ardência ao urinar</p>
<p>⚠ Dor durante relação</p>

<p><b>Esses sintomas podem indicar infecções e devem ser avaliados.</b></p>
</section>

<section id="mitos"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/565/565547.png" width="90">
<h2>Mitos e Verdades</h2>
<p><b>Mito:</b> Corrimento sempre é normal</p>
<p><b>Verdade:</b> Depende da cor e cheiro</p>
</div>
</section>

<section id="quando"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/3209/3209265.png" width="90">
<h2>Quando ir ao médico?</h2>
<p>👉 Dor persistente</p>
<p>👉 Sangramento fora do normal</p>
<p>👉 Dúvidas</p>
</div>
</section>

<section id="quiz"><button onclick="mostrar('inicio')">⬅ Voltar</button>
<div class="card">
<img src="https://cdn-icons-png.flaticon.com/512/1828/1828884.png" width="90">
<h2>Quiz</h2>

<p>Corrimento com cheiro forte é normal?</p>
<input type="radio" name="q1" value="errado"> Sim<br>
<input type="radio" name="q1" value="certo"> Não<br><br>

<p>Higiene íntima é importante?</p>
<input type="radio" name="q2" value="certo"> Sim<br>
<input type="radio" name="q2" value="errado"> Não<br><br>

<p>Deve ir ao médico só com dor?</p>
<input type="radio" name="q3" value="errado"> Sim<br>
<input type="radio" name="q3" value="certo"> Não<br><br>

<button onclick="verificar()">Ver resultado</button>

</div>
</section>

</body>
</html>
