<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Guia de Saúde Feminina</title>

<style>

/* ===== ESTILO GERAL ===== */
body {
    font-family: Arial;
    margin: 0;
    background: #fff0f5;
    padding-bottom: 80px;
}

.section {
    padding: 20px;
}

.card {
    background: white;
    padding: 15px;
    border-radius: 10px;
}

/* ===== MENU INFERIOR ===== */
nav {
    position: fixed;
    bottom: 0;
    width: 100%;
    background: #d81b60;
    display: flex;
    overflow-x: auto;
    z-index: 1000;
}

nav button {
    flex: 1;
    border: none;
    background: transparent;
    color: white;
    padding: 10px;
    font-size: 12px;
}

/* ===== BOTÃO DÚVIDA ===== */
.btn-duvidas {
    position: fixed;
    bottom: 70px;
    right: 15px;
    background: #d81b60;
    color: white;
    border: none;
    padding: 12px;
    border-radius: 30px;
}

/* ===== ACORDEÃO ===== */
.acordeao {
    background: #f8bbd0;
    padding: 10px;
    border: none;
    width: 100%;
    margin-top: 5px;
}

.painel {
    display: none;
    background: white;
    padding: 10px;
}

</style>
</head>

<body>

<!-- ===== INÍCIO ===== -->
<div class="section" id="inicio">
<div class="card">
<h2>Guia de Saúde Feminina</h2>
<p>Seu conteúdo inicial permanece aqui</p>
</div>
</div>

<!-- ===== CUIDADOS ===== -->
<div class="section" id="cuidados">
<div class="card">
<h2>Cuidados</h2>
<p>Seu conteúdo completo aqui</p>
</div>
</div>

<!-- ===== SUS / DIGNIDADE MENSTRUAL ===== -->
<div class="section" id="sus">
<div class="card">
<h2>Dignidade Menstrual (SUS)</h2>
<p>COLE AQUI seu conteúdo completo do SUS (não apague nada)</p>
</div>
</div>

<!-- ===== MÉTODOS ===== -->
<div class="section" id="metodos">
<div class="card">
<h2>Métodos</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== ALIMENTAÇÃO ===== -->
<div class="section" id="alimentacao">
<div class="card">
<h2>Alimentação</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== EXAMES ===== -->
<div class="section" id="exames">
<div class="card">
<h2>Exames</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== GRAVIDEZ ===== -->
<div class="section" id="gravidez">
<div class="card">
<h2>Gravidez</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== IST ===== -->
<div class="section" id="ist">
<div class="card">
<h2>IST</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== SAÚDE MENTAL ===== -->
<div class="section" id="mental">
<div class="card">
<h2>Saúde Mental</h2>
<p>Seu conteúdo completo</p>
</div>
</div>

<!-- ===== QUIZ ===== -->
<div class="section" id="quiz">
<div class="card">
<h2>Quiz</h2>
<p>Seu quiz já corrigido continua aqui</p>
</div>
</div>

<!-- ===== DÚVIDAS ===== -->
<div class="section" id="duvidas">
<div class="card">
<h2>Dúvidas</h2>
<p>Seu formulário aqui</p>
</div>
</div>

<!-- BOTÃO DÚVIDA -->
<button class="btn-duvidas" id="btnDuvida">Dúvidas</button>

<!-- ===== MENU ===== -->
<nav>
<button onclick="ir('inicio')">🏠</button>
<button onclick="ir('cuidados')">🧼</button>
<button onclick="ir('sus')">🏥</button>
<button onclick="ir('metodos')">💊</button>
<button onclick="ir('alimentacao')">🥗</button>
<button onclick="ir('exames')">🧪</button>
<button onclick="ir('gravidez')">🤰</button>
<button onclick="ir('ist')">⚠️</button>
<button onclick="ir('mental')">🧠</button>
<button onclick="ir('quiz')">❓</button>
</nav>

<script>

/* ===== FUNÇÃO DE NAVEGAÇÃO ===== */
function ir(secao){
    document.getElementById(secao).scrollIntoView({behavior:"smooth"});
}

/* ===== BOTÃO DÚVIDA ===== */
document.getElementById("btnDuvida").onclick=function(){
    ir("duvidas");
};

/* ===== ACORDEÃO ===== */
var acc = document.getElementsByClassName("acordeao");
for (var i = 0; i < acc.length; i++) {
    acc[i].onclick = function() {
        var painel = this.nextElementSibling;
        painel.style.display = painel.style.display === "block" ? "none" : "block";
    }
}

</script>

</body>
</html>
