<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Saúde da Mulher - Projeto ODS 4</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #fff0f5;
            padding-bottom: 90px; /* espaço para menu fixo */
        }
        header {
            background: #d81b60;
            color: white;
            text-align: center;
            padding: 20px;
        }
        nav {
            display: flex;
            overflow-x: auto;
            background: #fff;
            border-top: 2px solid #eee;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
            z-index: 10;
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
            min-width: 80px;
            margin: 0 5px;
        }
        nav button span {
            margin-top: 2px;
        }
        section {
            display: none;
            padding: 20px;
            animation: fade 0.3s;
        }
        section.ativo {
            display: block;
        }
        .banner {
            width: 100%;
            max-height: 220px;
            object-fit: contain;
            background: white;
        }
        .card {
            background: white;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            max-width: 900px;
            line-height: 1.6;
        }
        h2 {
            color: #d81b60;
        }
        @keyframes fade { from {opacity:0;} to {opacity:1;} }
        .menu-spacer { height: 90px; }
        button {
            margin-top: 10px;
            padding: 10px;
            border-radius: 10px;
            border: none;
            background: #d81b60;
            color: white;
            cursor: pointer;
        }
    </style>
    <script>
        function mostrar(secao) {
            document.querySelectorAll("section").forEach(s => s.classList.remove("ativo"));
            document.getElementById(secao).classList.add("ativo");
            window.scrollTo(0,0);
        }
    </script>
</head>
<body onload="mostrar('inicio')">

<header>
    <h1>🌸 Saúde da Mulher</h1>
    <p>Projeto Educativo - ODS 4</p>
</header>

<div class="menu-spacer"></div>

<!-- INÍCIO -->
<section id="inicio" class="ativo">
    <img class="banner" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRBhQYX5n2q73o_FDwZDA_hXSvAHox4jDzWxZF05kF3RVnXOFWtMLDQ-gaD&s" alt="Mulher">
    <div class="card">
        <h2>Sobre o Projeto</h2>
        <p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher, abordando temas importantes como prevenção, cuidados íntimos, métodos contraceptivos e acesso a serviços de saúde.</p>
        <p>As informações são apresentadas de forma clara e acessível, contribuindo para o conhecimento, autonomia e bem-estar.</p>
        <h3>Sobre a autora</h3>
        <p>Meu nome é Beatriz Dias, tenho 21 anos, sou formada como técnica de enfermagem e atualmente estudante da área de Tecnologia da Informação. Minha formação em enfermagem me proporciona conhecimento sólido sobre saúde feminina, garantindo que o conteúdo apresentado seja confiável, relevante e fundamentado em práticas de cuidado real.</p>
        <p>Este trabalho foi desenvolvido como atividade acadêmica, com foco em educação e impacto social, e está alinhado com a ODS 4 (Educação de Qualidade), incentivando o acesso à informação e à conscientização sobre a saúde feminina.</p>
    </div>
</section>

<!-- CUIDADOS ÍNTIMOS -->
<section id="cuidados">
    <img class="banner" src="https://thumbs.dreamstime.com/b/%C3%ADcones-de-higiene-%C3%ADntima-feminina-menstrua%C3%A7%C3%A3o-menstrual-bem-estar-sa%C3%BAde-prote%C3%A7%C3%A3o-conforto-pureza-mulher-cuidados-%C3%ADntimos-398322790.jpg" alt="Cuidados Íntimos">
    <div class="card">
        <h2>Cuidados com a Saúde Íntima</h2>
        <p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região.</p>
        <p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções.</p>
        <p>Evitar roupas muito apertadas é importante para não aumentar o calor e a umidade, reduzindo risco de infecções.</p>
        <p>Manter alimentação equilibrada e boa hidratação contribui para o bom funcionamento do organismo.</p>
        <p>Higiene adequada também inclui troca regular de absorventes, secagem correta após o banho e cuidado ao utilizar produtos íntimos.</p>
        <button onclick="mostrar('inicio')">⬅ Voltar</button>
    </div>
</section>

<!-- SISTEMA REPRODUTOR -->
<section id="sistema">
    <img class="banner" src="https://png.pngtree.com/png-clipart/20201208/original/pngtree-female-reproductive-system-health-hand-drawn-png-image_5518539.jpg" alt="Sistema Reprodutor">
    <div class="card">
        <h2>Sistema Reprodutor Feminino</h2>
        <p>O sistema reprodutor feminino é composto por órgãos responsáveis pela reprodução, produção de hormônios e funcionamento do ciclo menstrual.</p>
        <p>Principais órgãos:</p>
        <p>• Ovários: produzem os óvulos e hormônios</p>
        <p>• Trompas de Falópio: transportam o óvulo</p>
        <p>• Útero: local onde o bebê se desenvolve</p>
        <p>• Vagina: canal de saída do fluxo menstrual e parto</p>
        <p>Esses órgãos trabalham juntos para possibilitar a reprodução e manter a saúde do corpo feminino.</p>
        <button onclick="mostrar('inicio')">⬅ Voltar</button>
    </div>
</section>

<!-- ABSORVENTES SUS -->
<section id="sus">
    <img class="banner" src="https://img.freepik.com/vetores-gratis/conceito-de-sistema-reprodutivo-feminino_52683-45450.jpg?semt=ais_hybrid&w=740&q=80" alt="Absorventes SUS">
    <div class="card">
        <h2>Absorventes Gratuitos pelo SUS</h2>
        <p>O acesso a absorventes é um direito ligado à saúde, higiene e dignidade. No Brasil, o governo garante distribuição gratuita para pessoas em situação de vulnerabilidade.</p>
        <h3>O que é dignidade menstrual?</h3>
        <p>Dignidade menstrual significa ter acesso a produtos de higiene, informação e condições adequadas durante o período menstrual.</p>
        <h3>Quem tem direito?</h3>
        <p>• Estudantes da rede pública de baixa renda</p>
        <p>• Pessoas em situação de rua</p>
        <p>• Pessoas inscritas no CadÚnico</p>
        <p>• Mulheres em unidades prisionais</p>
        <p>• Pessoas em situação de extrema vulnerabilidade social</p>
        <h3>Como conseguir?</h3>
        <p>Os absorventes podem ser retirados gratuitamente em locais autorizados:</p>
        <p>• Unidades Básicas de Saúde (UBS)</p>
        <p>• Farmácias credenciadas pelo programa</p>
        <p>• Escolas públicas participantes</p>
        <p>Em alguns casos, é necessário apresentar documento com foto e estar inscrito no CadÚnico.</p>
        <h3>Impactos na saúde e educação</h3>
        <p>A falta de acesso a absorventes pode causar infecções, baixa autoestima e faltas escolares. O acesso gratuito melhora a qualidade de vida e promove inclusão social.</p>
        <button onclick="mostrar('inicio')">⬅ Voltar</button>
    </div>
</section>

<!-- MÉTODOS CONTRACEPTIVOS -->
<section id="contraceptivos">
    <img class="banner" src="https://static.vecteezy.com/ti/vetor-gratis/p1/6922254-contraceptivos-conjunto-controle-de-natalidade-ilustracao-para-impressao-fundos-capas-embalagem-cartoes-cartazes-adesivos-textil-e-design-sazonal-isolado-em-fundo-branco-vetor.jpg" alt="Métodos Contraceptivos">
    <div class="card">
        <h2>Métodos Contraceptivos</h2>
        <p>Os métodos contraceptivos são formas de evitar a gravidez e, em alguns casos, também ajudam na prevenção de infecções sexualmente transmissíveis (ISTs).</p>
        <h3>Tipos de métodos</h3>
        <p>🛡️ Métodos de barreira: preservativo masculino e feminino.</p>
        <p>💊 Métodos hormonais: pílula, injeção, adesivo, anel vaginal.</p>
        <p>🧬 Dispositivos intrauterinos (DIU): cobre ou hormonal.</p>
        <p>📅 Métodos naturais: tabelinha, observação do ciclo menstrual.</p>
        <h3>Métodos oferecidos pelo SUS</h3>
        <p>• Preservativo masculino e feminino</p>
        <p>• Pílula anticoncepcional</p>
        <p>• Injeção anticoncepcional</p>
        <p>• DIU de cobre</p>
        <h3>Métodos disponíveis na rede particular</h3>
        <p>• DIU hormonal</p>
        <p>• Implante hormonal</p>
        <p>• Adesivo anticoncepcional</p>
        <p>• Anel vaginal</p>
        <h3>Importância da escolha correta</h3>
        <p>A escolha do método deve ser feita com orientação de um profissional de saúde, considerando idade, histórico de saúde e estilo de vida.</p>
        <button onclick="mostrar('inicio')">⬅ Voltar</button>
    </div>
</section>

<nav>
    <button onclick="mostrar('inicio')">🏠<span>Início</span></button>
    <button onclick="mostrar('cuidados')">🧼<span>Cuidados</span></button>
    <button onclick="mostrar('sistema')">🧬<span>Sistema</span></button>
    <button onclick="mostrar('sus')">🩸<span>SUS</span></button>
    <button onclick="mostrar('contraceptivos')">💊<span>Métodos</span></button>
</nav>

</body>
</html>
