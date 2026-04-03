<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Saúde da Mulher - ODS 4</title>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding-bottom: 120px;
    background: #fff0f5;
}

header {
    text-align: center;
    padding: 20px 10px;
    background-color: #f8d7f0;
}

header h1 { margin: 0; color: #d81b60; }
header p { margin: 5px 0 0; font-size: 16px; color: #880e4f; }

nav {
    position: fixed;
    bottom: 0;
    width: 100%;
    background: #fff;
    display: flex;
    justify-content: space-around;
    border-top: 2px solid #eee;
    padding: 10px 0;
    z-index: 1000;
}

nav button {
    background: none;
    border: none;
    font-size: 12px;
    color: #d81b60;
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
}

nav button:hover { color: #880e4f; }

section { display: none; padding: 20px; }

section img.banner {
    width: 100%;
    max-height: 250px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 15px;
}

.card {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.card button {
    margin: 5px 5px 10px 0;
    padding: 8px 12px;
    border-radius: 5px;
    border: 1px solid #d81b60;
    background: #fff0f5;
    cursor: pointer;
}

.card button:hover { background: #d81b60; color: #fff; }

h2, h3, h4 { color: #d81b60; }
p { line-height: 1.6; }
</style>

<script>
function mostrar(secao){
    document.querySelectorAll("section").forEach(s => s.style.display="none");
    document.getElementById(secao).style.display="block";
}

let pontos = 0;
function responder(correta){ if(correta) pontos++; }
function resultado(){
    let msg = "";
    if(pontos <= 4) msg = "Você precisa estudar mais 😢";
    else if(pontos <= 7) msg = "Você está no caminho certo 👍";
    else msg = "Excelente conhecimento! 👏💖";
    document.getElementById("res").innerHTML = "Pontuação: " + pontos + "/10 <br>" + msg;
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
<button onclick="mostrar('projeto')">📚 Projeto</button>
<button onclick="mostrar('cuidados')">🧼 Cuidados</button>
<button onclick="mostrar('sintomas')">⚠️ Sintomas</button>
<button onclick="mostrar('prevencao')">🛡️ Prevenção</button>
<button onclick="mostrar('sistema')">🧬 Sistema</button>
<button onclick="mostrar('sus')">🩸 SUS</button>
<button onclick="mostrar('contraceptivos')">💊 Métodos</button>
<button onclick="mostrar('quiz')">🧠 Quiz</button>
</nav>

<!-- INÍCIO -->
<section id="inicio">
<img class="banner" src="https://img.freepik.com/vetores-gratis/conceito-de-sistema-reprodutivo-feminino_52683-45450.jpg">
<div class="card">
<h2>Educação em Saúde da Mulher</h2>
<p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher, abordando temas importantes como prevenção, cuidados íntimos, métodos contraceptivos e acesso a serviços de saúde.</p>
<p>O conteúdo busca informar de forma simples e acessível, contribuindo para o conhecimento, autonomia e bem-estar.</p>
<h3>Sobre a autora</h3>
<p>Meu nome é Beatriz Dias, tenho 21 anos e sou **técnica de enfermagem formada** e estudante da área de Tecnologia da Informação. Este projeto foi criado como atividade acadêmica com foco na educação e impacto social, garantindo credibilidade e domínio do conteúdo.</p>
<p>O projeto está alinhado com a ODS 4 (Educação de Qualidade), promovendo o acesso à informação e conscientização sobre a saúde feminina.</p>
</div>
</section>

<!-- PROJETO -->
<section id="projeto">
<div class="card">
<h2>Projeto de Extensão</h2>
<h3>Objetivo</h3>
<p>Promover a educação em saúde da mulher por meio de um site informativo, facilitando o acesso ao conhecimento sobre prevenção, autocuidado e direitos relacionados à saúde. O projeto inclui conteúdos didáticos, quizzes, dicas de prevenção e informações detalhadas sobre o SUS e métodos contraceptivos.</p>
<h3>Justificativa</h3>
<p>A falta de informação sobre saúde feminina ainda é um problema que afeta muitas mulheres, especialmente em contextos de vulnerabilidade. Este projeto busca contribuir para disseminar conhecimento de forma acessível, confiável e digital, promovendo empoderamento, autonomia e saúde integral.</p>
<h3>Público-alvo</h3>
<p>Mulheres jovens e adultas, estudantes e pessoas que buscam informações sobre saúde íntima, métodos contraceptivos, prevenção de doenças e acesso a serviços de saúde. O conteúdo também é útil para educadores e familiares.</p>
<h3>ODS 4 – Educação de Qualidade</h3>
<p>O projeto promove educação inclusiva e equitativa, incentivando leitura, compreensão e tomada de decisões conscientes sobre a saúde.</p>
<h3>Impacto Social</h3>
<p>Ao oferecer informação confiável e acessível, o projeto contribui para redução de doenças, melhora da qualidade de vida e empoderamento feminino. Promove também conscientização sobre igualdade de gênero, autocuidado e saúde sexual.</p>
<h3>Conclusão</h3>
<p>O uso da tecnologia como ferramenta educativa permite ampliar o alcance da informação e gerar mudanças positivas na sociedade, estimulando curiosidade, aprendizado contínuo e hábitos saudáveis.</p>
<h3>Referências</h3>
<p>• Ministério da Saúde</p>
<p>• Organização Mundial da Saúde (OMS)</p>
<p>• Conteúdos educativos sobre saúde da mulher</p>
</div>
</section>

<!-- Cuidados -->
<section id="cuidados">
<img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg">
<div class="card">
<h2>Cuidados com a saúde íntima</h2>
<p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região genital.</p>
<p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções. Evite roupas muito apertadas e sintéticas.</p>
<p>Manter uma alimentação equilibrada, boa hidratação e hábitos saudáveis contribuem para o bom funcionamento do organismo.</p>
<p>Trocar absorventes ou roupas íntimas com regularidade e consultar profissional de saúde em caso de alterações é essencial.</p>
</div>
</section>

<!-- Sintomas -->
<section id="sintomas">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/564/564619.png">
<div class="card">
<h2>Sintomas de alerta</h2>
<p>Alguns sinais indicam possíveis problemas de saúde e não devem ser ignorados:</p>
<p>• Corrimentos com cor amarelada, esverdeada ou com odor forte podem indicar infecções.</p>
<p>• Coceira intensa, ardência ou dor durante a relação sexual.</p>
<p>• Ardência ao urinar ou sangue fora do período menstrual.</p>
<p>Ao perceber qualquer um desses sinais, é fundamental procurar um profissional de saúde para avaliação adequada.</p>
</div>
</section>

<!-- Prevenção -->
<section id="prevencao">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/2913/2913465.png">
<div class="card">
<h2>Prevenção</h2>
<p>O uso de preservativos é essencial para evitar infecções sexualmente transmissíveis (ISTs) e prevenir gravidez indesejada.</p>
<p>Consultas regulares ao ginecologista permitem a detecção precoce de doenças.</p>
<p>Exames preventivos como o Papanicolau são fundamentais para prevenção do câncer do colo do útero.</p>
<p>Evitar a automedicação é importante, pois pode mascarar sintomas e agravar problemas de saúde.</p>
</div>
</section>
