<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #fff0f5;
}

/* MENU */
.menu {
    position: fixed;
    top: 0;
    width: 100%;
    background: white;
    display: flex;
    overflow-x: auto;
    padding: 10px;
    z-index: 1000;
}

.menu button {
    background: none;
    border: none;
    color: #d81b60;
    font-size: 13px;
    margin: 0 8px;
}

/* SEÇÕES */
.section {
    padding: 80px 20px;
}

.card {
    background: white;
    padding: 15px;
    border-radius: 10px;
}

/* ACORDEÃO */
.acordeao {
    background: #f8bbd0;
    border: none;
    padding: 10px;
    width: 100%;
    margin-top: 5px;
}

.painel {
    display: none;
    padding: 10px;
    background: #fff;
}

/* BOTÃO DÚVIDA */
.btn-duvidas {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #d81b60;
    color: white;
    border: none;
    padding: 15px;
    border-radius: 50px;
}

/* QUIZ */
.quiz-pergunta {
    margin-bottom: 15px;
}
</style>
</head>

<body>

<!-- MENU -->
<nav class="menu">
<button onclick="ir('inicio')">Início</button>
<button onclick="ir('cuidados')">Cuidados</button>
<button onclick="ir('sistema')">Sistema</button>
<button onclick="ir('sus')">SUS</button>
<button onclick="ir('quiz')">Quiz</button>
</nav>

<!-- INÍCIO -->
<div class="section" id="inicio">
<div class="card">
<h2>Projeto</h2>
<p>Este projeto foi criado com o objetivo de promover a educação em saúde da mulher...</p>
</div>
</div>

<!-- SISTEMA REPRODUTOR -->
<div class="section" id="sistema">
<div class="card">
<h2>Sistema Reprodutor Feminino</h2>

<button class="acordeao">Ovários</button>
<div class="painel"><p>Produzem óvulos...</p></div>

<button class="acordeao">Útero</button>
<div class="painel"><p>Desenvolvimento do bebê...</p></div>

</div>
</div>

<!-- SUS -->
<div class="section" id="sus">
<div class="card">
<h2>Dignidade Menstrual</h2>
<p>O programa garante absorventes gratuitos...</p>
</div>
</div>

<!-- QUIZ -->
<div class="section" id="quiz">
<div class="card">
<h2>Quiz</h2>

<div class="quiz-pergunta">
<p>1. Onde ocorre a fecundação?</p>
<label><input type="radio" name="q1" value="0"> Útero</label><br>
<label><input type="radio" name="q1" value="1"> Trompas</label>
</div>

<button onclick="corrigirQuiz()">Finalizar</button>

<p id="resultado"></p>

</div>
</div>

<!-- DÚVIDAS -->
<div class="section" id="duvidas">
<div class="card">
<h2>Dúvidas</h2>
<p>Formulário aqui...</p>
</div>
</div>

<button class="btn-duvidas" onclick="ir('duvidas')">💬</button>

<script>
// MENU
function ir(secao){
document.getElementById(secao).scrollIntoView({behavior:'smooth'});
}

// ACORDEÃO
document.querySelectorAll(".acordeao").forEach(btn=>{
btn.onclick=function(){
let painel=this.nextElementSibling;
painel.style.display = painel.style.display=="block"?"none":"block";
}
});

// QUIZ
function corrigirQuiz(){
let pontos=0;
if(document.querySelector('input[name="q1"]:checked')?.value=="1") pontos++;
document.getElementById("resultado").innerText="Acertos: "+pontos;
}
</script>

</body>
</html>
