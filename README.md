<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #fff0f5;
    padding-bottom: 120px;
}

.section { padding:20px; }
.card {
    background:#fff;
    padding:20px;
    border-radius:12px;
    max-width:900px;
    margin:auto;
}

h2 { color:#d81b60; }

nav {
    position:fixed;
    bottom:0;
    width:100%;
    display:flex;
    background:#fff;
}
nav button {
    flex:1;
    border:none;
    background:none;
    padding:10px;
    color:#d81b60;
}

.btn-duvida {
    position:fixed;
    bottom:70px;
    right:10px;
    background:#d81b60;
    color:#fff;
    border:none;
    padding:12px;
    border-radius:50%;
}

/* acordeão */
.acordeao {
    background:#f8bbd0;
    border:none;
    padding:10px;
    width:100%;
    margin-top:5px;
}
.painel {
    display:none;
    background:#fff;
    padding:10px;
}

/* quiz */
.quiz-option { display:block; margin:5px; }
.quiz-result { font-weight:bold; }
</style>
</head>

<body>

<header style="background:#d81b60;color:white;text-align:center;padding:20px;">
<h1>🌸 Saúde da Mulher</h1>
</header>

<!-- INTRO -->
<div class="section">
<div class="card">
<p>Este projeto foi criado com o objetivo de promover a educação em saúde da mulher, apresentando informações de maneira clara e acessível, favorecendo o conhecimento, a autonomia e o bem-estar feminino.</p>

<p>Trata-se de um trabalho acadêmico voltado para a educação e o impacto social, alinhado à ODS 4 (Educação de Qualidade).</p>

<h3>Autora</h3>
<p>Beatriz Dias</p>
</div>
</div>

<!-- CUIDADOS -->
<div class="section">
<div class="card">
<h2>Cuidados Íntimos</h2>
<ul>
<li>Evitar duchas internas</li>
<li>Trocar absorventes regularmente</li>
<li>Usar roupas de algodão</li>
<li>Manter higiene adequada</li>
</ul>
</div>
</div>

<!-- DIGNIDADE MENSTRUAL COMPLETA -->
<div class="section">
<div class="card">
<h2>Dignidade Menstrual</h2>

<p>A dignidade menstrual refere-se ao direito de toda pessoa menstruante ter acesso a condições adequadas de higiene, produtos menstruais e informação de qualidade.</p>

<h3>Programa no SUS</h3>
<p>O governo federal criou o Programa de Proteção e Promoção da Saúde e Dignidade Menstrual, que garante distribuição gratuita de absorventes.</p>

<h3>Quem tem direito?</h3>
<ul>
<li>Pessoas inscritas no CadÚnico</li>
<li>Estudantes da rede pública</li>
<li>Pessoas em situação de vulnerabilidade social</li>
<li>Pessoas em situação de rua</li>
<li>Pessoas privadas de liberdade</li>
</ul>

<h3>Onde retirar?</h3>
<ul>
<li>Unidades Básicas de Saúde (UBS)</li>
<li>Farmácias credenciadas</li>
<li>CRAS</li>
<li>Escolas públicas participantes</li>
</ul>

<h3>Como funciona?</h3>
<ul>
<li>Cadastro no CadÚnico</li>
<li>Apresentação de documento</li>
<li>Retirada gratuita mensal</li>
</ul>

<h3>Importância</h3>
<ul>
<li>Previne infecções</li>
<li>Reduz evasão escolar</li>
<li>Promove dignidade e autoestima</li>
</ul>

<h3>Fonte</h3>
<p>Ministério da Saúde e Governo Federal</p>

</div>
</div>

<!-- SISTEMA REPRODUTOR -->
<div class="section">
<div class="card">
<h2>Sistema Reprodutor</h2>

<button class="acordeao">Ovários</button>
<div class="painel">Produzem óvulos e hormônios.</div>

<button class="acordeao">Trompas</button>
<div class="painel">Transportam o óvulo.</div>

<button class="acordeao">Útero</button>
<div class="painel">Desenvolvimento do bebê.</div>

<button class="acordeao">Vagina</button>
<div class="painel">Canal de ligação.</div>

<button class="acordeao">Clitóris</button>
<div class="painel">Prazer sexual.</div>

<button class="acordeao">Hímen</button>
<div class="painel">Membrana variável.</div>

</div>
</div>

<!-- QUIZ -->
<div class="section" id="quiz">
<div class="card" id="quiz-container">
<h2>Quiz</h2>
</div>
</div>

<!-- DUVIDAS -->
<div class="section" id="duvidas">
<div class="card">
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScpEDQnLimCVNfT1gR5rDJN0pbk1Vz32E5c79Oc0Kg8c7SXnA/viewform?embedded=true" width="100%" height="600"></iframe>
</div>
</div>

<!-- MENU -->
<nav>
<button onclick="window.scrollTo(0,0)">Início</button>
<button onclick="document.querySelectorAll('.section')[1].scrollIntoView()">Cuidados</button>
<button onclick="document.querySelectorAll('.section')[2].scrollIntoView()">Dignidade</button>
<button onclick="document.querySelectorAll('.section')[3].scrollIntoView()">Sistema</button>
<button onclick="document.querySelectorAll('.section')[4].scrollIntoView()">Quiz</button>
</nav>

<button id="btnDuvida" class="btn-duvida">?</button>

<script>

// acordeão
document.querySelectorAll(".acordeao").forEach(btn=>{
btn.onclick=function(){
let p=this.nextElementSibling;
p.style.display=p.style.display==="block"?"none":"block";
};
});

// botão dúvida
document.getElementById("btnDuvida").onclick=function(){
document.getElementById("duvidas").scrollIntoView({behavior:"smooth"});
};

// quiz
const perguntas=[
{p:"Função dos ovários?",o:["Hormônios","Digestão","Respiração"],c:0},
{p:"Proteção IST?",o:["DIU","Preservativo","Pílula"],c:1},
{p:"Tecido ideal?",o:["Algodão","Plástico","Lã"],c:0},
{p:"Órgão bebê?",o:["Útero","Ovário","Vagina"],c:0},
{p:"Transporte óvulo?",o:["Trompa","Útero","Ovário"],c:0},
{p:"Método natural?",o:["Tabelinha","DIU","Implante"],c:0},
{p:"Dignidade menstrual?",o:["Absorvente","Roupa","Nada"],c:0},
{p:"Evitar infecção?",o:["Higiene","Nada","Roupas apertadas"],c:0},
{p:"Consulta médica?",o:["Importante","Inútil","Opcional"],c:0},
{p:"Hormônio?",o:["Estrogênio","Insulina","Adrenalina"],c:0}
];

let quiz=document.getElementById("quiz-container");

perguntas.forEach((q,i)=>{
let div=document.createElement("div");
div.innerHTML="<p>"+q.p+"</p>";
q.o.forEach((op,j)=>{
div.innerHTML+=`<label><input type="radio" name="q${i}" value="${j}">${op}</label><br>`;
});
let res=document.createElement("div");
res.className="quiz-result";
div.appendChild(res);
quiz.appendChild(div);
});

let btn=document.createElement("button");
btn.innerText="Ver resultado";

btn.onclick=function(){
let acertos=0;

perguntas.forEach((q,i)=>{
let r=document.querySelector(`input[name=q${i}]:checked`);
let res=document.querySelectorAll(".quiz-result")[i];

if(!r){
res.innerHTML="❌ Não respondeu";
}
else if(parseInt(r.value)===q.c){
res.innerHTML="✅ Correto";
acertos++;
}else{
res.innerHTML="❌ Errado";
}
});

alert("Acertos: "+acertos);
};

quiz.appendChild(btn);

</script>

</body>
</html>
