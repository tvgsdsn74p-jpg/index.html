<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher - ODS 4</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #fff0f5;
}

header {
    background: #d81b60;
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
    max-height: 220px;
    object-fit: contain;
    background: white;
}

.card {
    background: white;
    margin: 20px;
    padding: 20px;
    border-radius: 15px;
    line-height: 1.6;
}

h2 {
    color: #d81b60;
}

button {
    margin-top: 10px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    background: #d81b60;
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
        msg = "Você precisa estudar mais 😢";
    } else if(pontos <= 7){
        msg = "Você está no caminho certo 👍";
    } else {
        msg = "Excelente conhecimento! 👏💖";
    }

    document.getElementById("res").innerHTML =
    "Pontuação: " + pontos + "/10 <br>" + msg;
}
</script>

</head>

<body onload="mostrar('inicio')">

<header>
<h1>🌸 Saúde da Mulher</h1>
<p>Educação em saúde - ODS 4</p>
</header>

<nav>
<button onclick="mostrar('inicio')">🏠 Início</button>
<button onclick="mostrar('cuidados')">🧼 Cuidados</button>
<button onclick="mostrar('sintomas')">⚠️ Sintomas</button>
<button onclick="mostrar('prevencao')">🛡️ Prevenção</button>
<button onclick="mostrar('quiz')">🧠 Quiz</button>
</nav>

<section id="inicio">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/4149/4149673.png">
<div class="card">
<h2>Educação em Saúde da Mulher</h2>

<p>Este projeto tem como objetivo promover a educação em saúde da mulher, alinhado à ODS 4, que busca garantir educação de qualidade para todos.</p>

<p>A saúde feminina envolve cuidados físicos, emocionais e preventivos. Ter acesso à informação permite que a mulher reconheça sinais do próprio corpo e busque ajuda quando necessário.</p>

<p>A educação em saúde é essencial para reduzir doenças, melhorar a qualidade de vida e incentivar o autocuidado.</p>

</div>
</section>

<section id="cuidados">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/3774/3774299.png">
<div class="card">
<h2>Cuidados com a saúde íntima</h2>

<p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região.</p>

<p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções.</p>

<p>É importante evitar roupas muito apertadas, pois elas aumentam o calor e a umidade, favorecendo o crescimento de microrganismos.</p>

<p>Além disso, manter uma alimentação equilibrada e boa hidratação contribui para o bom funcionamento do organismo.</p>

</div>
</section>

<section id="sintomas">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/564/564619.png">
<div class="card">
<h2>Sintomas de alerta</h2>

<p>Alguns sinais indicam possíveis problemas de saúde e não devem ser ignorados.</p>

<p>Corrimentos com cor amarelada, esverdeada ou com odor forte podem indicar infecções.</p>

<p>Coceira intensa, ardência ou dor durante a relação também são sinais importantes.</p>

<p>Ardência ao urinar pode indicar infecção urinária.</p>

<p>Ao perceber qualquer um desses sintomas, é fundamental procurar um profissional de saúde para avaliação adequada.</p>

</div>
</section>

<section id="prevencao">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/2913/2913465.png">
<div class="card">
<h2>Prevenção</h2>

<p>A prevenção é a principal forma de manter a saúde.</p>

<p>O uso de preservativo é essencial para evitar infecções sexualmente transmissíveis.</p>

<p>Consultas regulares ao ginecologista permitem a detecção precoce de doenças.</p>

<p>Exames preventivos, como o Papanicolau, são fundamentais para prevenir o câncer do colo do útero.</p>

<p>Evitar a automedicação também é muito importante, pois pode mascarar sintomas e agravar problemas.</p>

</div>
</section>

<section id="quiz">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/3135/3135755.png">
<div class="card">
<h2>Quiz Educativo</h2>

<p>Teste seus conhecimentos:</p>

<p>1. Higiene íntima é importante?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>2. Automedicação é recomendada?</p>
<button onclick="responder(false)">Sim</button>
<button onclick="responder(true)">Não</button>

<p>3. Beber água ajuda na saúde?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>4. Corrimento diferente pode indicar problema?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>5. Dor ao urinar é sinal de alerta?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>6. Preservativo previne doenças?</p>
<button onclick="responder(true)">Sim</button>
<button onclick="responder(false)">Não</button>

<p>7. Consultas médicas são importantes?</p>
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

</div>
</section>

</body>
</html>
