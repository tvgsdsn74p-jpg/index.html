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
    padding-bottom: 80px;
}
.menu-app {
    position: fixed;
    bottom: 0;
    width: 100%;
    background: #fff;
    display: flex;
    justify-content: space-around;
    border-top: 2px solid #eee;
    padding: 10px 0;
}

.menu-app button {
    background: none;
    border: none;
    font-size: 12px;
    color: #d81b60;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.card {
    padding: 15px;
    margin: 10px;
    background: #fff;
    border-radius: 10px;
}
.banner {
    width: 100%;
    max-height: 200px;
    object-fit: cover;
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
<p>Meu nome é Beatriz Dias e sou estudante da área de Tecnologia da Informação. Este projeto foi criado como atividade acadêmica com foco na educação e impacto social.</p>
<p>O projeto está alinhado com a ODS 4 (Educação de Qualidade), promovendo o acesso à informação e conscientização sobre a saúde feminina.</p>
</div>
</section>

<!-- CUIDADOS -->
<section id="cuidados">
<img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg">
<div class="card">
<h2>Cuidados com a saúde íntima</h2>
<p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região.</p>
<p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções.</p>
<p>É importante evitar roupas muito apertadas, pois elas aumentam o calor e a umidade, favorecendo o crescimento de microrganismos.</p>
<p>Além disso, manter uma alimentação equilibrada e boa hidratação contribui para o bom funcionamento do organismo.</p>
</div>
</section>

<!-- SINTOMAS -->
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

<!-- PREVENÇÃO -->
<section id="prevencao">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/2913/2913465.png">
<div class="card">
<h2>Prevenção</h2>
<p>A prevenção é a principal forma de manter a saúde.</p>
<p>O uso de preservativo é essencial para evitar infecções sexualmente transmissíveis.</p>
<p>Consultas regulares ao ginecologista permitem a detecção precoce de doenças.</p>
<p>Exames preventivos, como o Papanicolau, são fundamentais para prevenir o câncer do colo do útero.</p>
<p>Evitar a automedicação também é muito importante.</p>
</div>
</section>

<!-- SISTEMA REPRODUTOR -->
<section id="sistema">
<img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg">
<div class="card">
<h2>Sistema Reprodutor Feminino</h2>
<p>O sistema reprodutor feminino é responsável pela reprodução e produção de hormônios importantes para o corpo.</p>
<p>Ele é composto por:</p>
<p>• Ovários: produzem os óvulos e hormônios</p>
<p>• Trompas de Falópio: transportam o óvulo</p>
<p>• Útero: onde o bebê se desenvolve</p>
<p>• Vagina: canal de saída e relação</p>
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<!-- SUS -->
<section id="sus">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5FAPNcvSzS8-WXlbQcIKfN9ACxaG1GGaymuUit2SXuw&s" style="width: 220px; display: block; margin: 10px auto;">
<h2>Absorventes Gratuitos pelo SUS</h2>
<div class="card">
<p>O acesso a absorventes é um direito ligado à saúde, higiene e dignidade. No Brasil, o governo criou o Programa de Proteção e Promoção da Dignidade Menstrual, garantindo a distribuição gratuita de absorventes para pessoas em situação de vulnerabilidade.</p>
<!-- resto do conteúdo do SUS -->
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<!-- MÉTODOS CONTRACEPTIVOS -->
<section id="contraceptivos">
<img src="https://static.vecteezy.com/ti/vetor-gratis/p1/6922254-contraceptivos-conjunto-controle-de-natalidade-ilustracao-para-impressao-fundos-capas-embalagem-cartoes-cartazes-adesivos-textil-e-design-sazonal-isolado-em-fundo-branco-vetor.jpg" style="width: 260px; display: block; margin: 10px auto; border-radius: 10px;">
<h2>Métodos Contraceptivos</h2>
<div class="card">
<!-- conteúdo dos métodos -->
<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<!-- PROJETO DE EXTENSÃO -->
<section id="projeto">
<div class="card">
<h2>Projeto de Extensão</h2>

<h3>Objetivo</h3>
<p>Promover a educação em saúde da mulher por meio de um site informativo, facilitando o acesso ao conhecimento sobre prevenção, autocuidado e direitos relacionados à saúde.</p>

<h3>Justificativa</h3>
<p>A falta de informação sobre saúde feminina ainda é um problema que afeta muitas mulheres, especialmente em contextos de vulnerabilidade.</p>

<h3>Público-alvo</h3>
<p>Mulheres jovens e adultas, estudantes e pessoas que buscam informações sobre saúde íntima, métodos contraceptivos e serviços de saúde.</p>

<h3>Relação com a ODS 4</h3>
<p>O projeto está alinhado com a ODS 4 – Educação de Qualidade.</p>

<h3>Impacto Social</h3>
<p>Contribui para a conscientização, prevenção de doenças e melhoria da qualidade de vida.</p>

<h3>Conclusão</h3>
<p>O uso da tecnologia como ferramenta educativa permite ampliar o alcance da informação e promover mudanças positivas na sociedade.</p>

<h3>Referências</h3>
<p>Ministério da Saúde</p>
<p>Organização Mundial da Saúde (OMS)</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>

<!-- QUIZ -->
<section id="quiz">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/3135/3135755.png">
<div class="card">
<h2>Quiz Educativo</h2>
<p>Teste seus conhecimentos:</p>
<!-- perguntas do quiz -->
<button onclick="resultado()">Ver resultado</button>
<p id="res"></p>
</div>
</section>

</body>
</html>
