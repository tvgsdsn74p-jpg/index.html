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
    color: #d81b60;   /* 👈 ESSENCIAL */
    font-weight: bold;
}

section {
    display: none;
}

.banner {
    width: 100%;
    max-height: 220px;
    object-fit: contain; /* 👈 ESSENCIAL */
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
<button onclick="mostrar('sistema')">🧬 Sistema</button>
<button onclick="mostrar('sus')">🩸 SUS</button>
<button onclick="mostrar('contraceptivos')">💊 Métodos</button>
<button onclick="mostrar('quiz')">🧠 Quiz</button>
</nav>

<section id="inicio">
<img class="banner" src="https://img.freepik.com/vetores-gratis/conceito-de-sistema-reprodutivo-feminino_52683-45450.jpg">
<div class="card">
<h2>Educação em Saúde da Mulher</h2>

<p>Este projeto tem como objetivo promover a educação em saúde da mulher, alinhado à ODS 4, que busca garantir educação de qualidade para todos.</p>

<p>A saúde feminina envolve cuidados físicos, emocionais e preventivos. Ter acesso à informação permite que a mulher reconheça sinais do próprio corpo e busque ajuda quando necessário.</p>

<p>A educação em saúde é essencial para reduzir doenças, melhorar a qualidade de vida e incentivar o autocuidado.</p>

</div>
</section>

<section id="cuidados">
<img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg">
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
<section id="sistema">
<img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg">

<div class="card">
<h2>Sistema Reprodutor Feminino</h2>

<p>O sistema reprodutor feminino é responsável pela reprodução e pela produção de hormônios importantes para o corpo.</p>

<p>Ele é composto por órgãos que trabalham juntos:</p>

<p>• Ovários: produzem os óvulos e hormônios</p>
<p>• Trompas de Falópio: transportam o óvulo</p>
<p>• Útero: onde o bebê se desenvolve</p>
<p>• Vagina: canal de saída e relação</p>

<p>Conhecer o próprio corpo é essencial para identificar alterações e cuidar da saúde.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>
<section id="sus">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/2966/2966488.png">

<div class="card">
<h2>Absorventes Gratuitos pelo SUS</h2>

<p>O acesso a absorventes é um direito ligado à saúde, higiene e dignidade. No Brasil, o governo criou o Programa de Proteção e Promoção da Dignidade Menstrual, garantindo a distribuição gratuita de absorventes para pessoas em situação de vulnerabilidade.</p>

<h3>O que é dignidade menstrual?</h3>

<p>Dignidade menstrual significa ter acesso a produtos de higiene, informação e condições adequadas durante o período menstrual.</p>

<p>A falta de absorventes pode levar ao uso de materiais inadequados, aumentando o risco de infecções e problemas de saúde.</p>

<h3>Quem tem direito?</h3>

<p>• Estudantes da rede pública de baixa renda</p>
<p>• Pessoas em situação de rua</p>
<p>• Pessoas inscritas no Cadastro Único (CadÚnico)</p>
<p>• Mulheres em unidades prisionais</p>
<p>• Pessoas em situação de extrema vulnerabilidade social</p>

<h3>Como conseguir?</h3>

<p>Os absorventes podem ser retirados gratuitamente em locais autorizados:</p>

<p>• Unidades Básicas de Saúde (UBS)</p>
<p>• Farmácias credenciadas pelo programa</p>
<p>• Escolas públicas participantes</p>
<p>• Centros de Referência de Assistência Social (CRAS)</p>

<p>Em alguns casos, é necessário apresentar documento com foto e estar inscrito no CadÚnico.</p>

<h3>Impactos na saúde e educação</h3>

<p>A falta de acesso a absorventes pode causar:</p>

<p>• Infecções íntimas</p>
<p>• Baixa autoestima</p>
<p>• Faltas na escola</p>
<p>• Dificuldade no trabalho</p>

<p>Com o acesso gratuito, há melhora na qualidade de vida, na saúde e na permanência escolar.</p>

<h3>Importância social</h3>

<p>Esse programa combate a pobreza menstrual, promovendo igualdade de gênero, saúde pública e inclusão social.</p>

<p>Também contribui diretamente para a educação, pois muitas meninas deixam de frequentar a escola durante o período menstrual por falta de recursos.</p>

<h3>Dica importante</h3>

<p>Se você ou alguém que conhece precisa, procure a UBS mais próxima ou o CRAS da sua cidade para receber orientação.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>
<section id="contraceptivos">
<img class="banner" src="https://cdn-icons-png.flaticon.com/512/3209/3209265.png">

<div class="card">
<h2>Métodos Contraceptivos</h2>

<p>Os métodos contraceptivos são formas de evitar a gravidez e, em alguns casos, também ajudam na prevenção de infecções sexualmente transmissíveis (ISTs).</p>

<h3>Tipos de métodos</h3>

<h4>🛡️ Métodos de barreira</h4>
<p>• Preservativo masculino</p>
<p>• Preservativo feminino</p>
<p>Esses métodos impedem o contato entre espermatozoide e óvulo e também protegem contra ISTs.</p>

<h4>💊 Métodos hormonais</h4>
<p>• Pílula anticoncepcional</p>
<p>• Injeção anticoncepcional</p>
<p>• Adesivo hormonal</p>
<p>• Anel vaginal</p>
<p>Atuam impedindo a ovulação.</p>

<h4>🧬 Dispositivos intrauterinos (DIU)</h4>
<p>• DIU de cobre</p>
<p>• DIU hormonal</p>
<p>São colocados dentro do útero e impedem a gravidez por vários anos.</p>

<h4>📅 Métodos naturais</h4>
<p>• Tabelinha</p>
<p>• Observação do ciclo menstrual</p>
<p>Possuem maior risco de falha.</p>

<h3>Métodos oferecidos pelo SUS</h3>

<p>O Sistema Único de Saúde (SUS) oferece gratuitamente diversos métodos contraceptivos:</p>

<p>• Preservativo masculino e feminino</p>
<p>• Pílula anticoncepcional</p>
<p>• Injeção anticoncepcional</p>
<p>• DIU de cobre</p>

<p>Esses métodos podem ser obtidos em Unidades Básicas de Saúde (UBS), com orientação de profissionais de saúde.</p>

<h3>Métodos disponíveis na rede particular</h3>

<p>Alguns métodos geralmente são encontrados em clínicas e farmácias particulares:</p>

<p>• DIU hormonal</p>
<p>• Implante hormonal</p>
<p>• Adesivo anticoncepcional</p>
<p>• Anel vaginal</p>

<p>Esses métodos podem ter custo mais elevado, mas oferecem alta eficácia.</p>

<h3>Qual método escolher?</h3>

<p>A escolha deve ser feita com orientação de um profissional de saúde, considerando idade, histórico de saúde e estilo de vida.</p>

<p>O uso de preservativos é sempre recomendado, pois além de evitar gravidez, protege contra infecções.</p>

<h3>Importância da prevenção</h3>

<p>O acesso à informação e aos métodos contraceptivos contribui para a saúde da mulher, autonomia e planejamento familiar.</p>

<button onclick="mostrar('inicio')">⬅ Voltar</button>
</div>
</section>
</body>
</html>
