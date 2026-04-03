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
            padding-bottom: 80px; /* espaço para o menu fixo */
        }

        header {
            background: #d81b60;
            color: white;
            text-align: center;
            padding: 20px;
        }

        nav {
            display: flex;
            justify-content: space-around;
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
            max-width: 800px;
            line-height: 1.6;
        }

        h2 {
            color: #d81b60;
        }

        @keyframes fade {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .menu-spacer {
            height: 80px; /* espaço para o menu fixo */
        }

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
            document.querySelectorAll("section").forEach(s => {
                s.classList.remove("ativo");
            });
            document.getElementById(secao).classList.add("ativo");
        }
    </script>
</head>
<body onload="mostrar('inicio')">
    <header>
        <h1>🌸 Saúde da Mulher</h1>
        <p>Projeto Educativo - ODS 4</p>
    </header>

    <div class="menu-spacer"></div>

    <section id="inicio" class="ativo">
        <img class="banner" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRBhQYX5n2q73o_FDwZDA_hXSvAHox4jDzWxZF05kF3RVnXOFWtMLDQ-gaD&s" alt="Mulher">
        <div class="card">
            <h2>Sobre o Projeto</h2>
            <p>Este projeto foi desenvolvido com o objetivo de promover a educação em saúde da mulher, abordando temas importantes como prevenção, cuidados íntimos, métodos contraceptivos e acesso a serviços de saúde.</p>
            <p>As informações são apresentadas de forma clara e acessível, contribuindo para o conhecimento, autonomia e bem-estar.</p>
            <h3>Sobre a autora</h3>
            <p>Meu nome é Beatriz Dias, tenho 21 anos, sou formada como técnica de enfermagem e estudante da área de Tecnologia da Informação. Este projeto foi desenvolvido como atividade acadêmica, com foco em educação e impacto social.</p>
            <p>Este trabalho está alinhado com a ODS 4 (Educação de Qualidade), incentivando o acesso à informação e à conscientização sobre a saúde feminina.</p>
        </div>
    </section>

    <section id="cuidados">
        <img class="banner" src="https://cdn-icons-png.flaticon.com/512/3081/3081559.png" alt="Cuidados">
        <div class="card">
            <h2>Cuidados com a Saúde Íntima</h2>
            <p>A higiene íntima deve ser feita de forma adequada, utilizando produtos suaves e evitando o uso excessivo de sabonetes íntimos, que podem alterar o equilíbrio natural da região.</p>
            <p>O uso de roupas de algodão é recomendado, pois permite melhor ventilação e reduz a umidade, prevenindo infecções.</p>
            <p>É importante evitar roupas muito apertadas, pois elas aumentam o calor e a umidade, favorecendo o crescimento de microrganismos.</p>
            <p>Além disso, manter uma alimentação equilibrada e boa hidratação contribui para o bom funcionamento do organismo.</p>
            <button onclick="mostrar('inicio')">⬅ Voltar</button>
        </div>
    </section>

    <section id="sintomas">
        <img class="banner" src="https://cdn-icons-png.flaticon.com/512/564/564619.png" alt="Sintomas">
        <div class="card">
            <h2>Sintomas de Alerta</h2>
            <p>Alguns sinais indicam possíveis problemas de saúde e não devem ser ignorados.</p>
            <p>Corrimentos com cor amarelada, esverdeada ou com odor forte podem indicar infecções.</p>
            <p>Coceira intensa, ardência ou dor durante a relação também são sinais importantes.</p>
            <p>Ardência ao urinar pode indicar infecção urinária.</p>
            <p>Ao perceber qualquer um desses sintomas, é fundamental procurar um profissional de saúde para avaliação adequada.</p>
            <button onclick="mostrar('inicio')">⬅ Voltar</button>
        </div>
    </section>

    <section id="prevencao">
        <img class="banner" src="https://cdn-icons-png.flaticon.com/512/2913/2913465.png" alt="Prevenção">
        <div class="card">
            <h2>Prevenção</h2>
            <p>A prevenção é a principal forma de manter a saúde.</p>
            <p>O uso de preservativo é essencial para evitar infecções sexualmente transmissíveis.</p>
            <p>Consultas regulares ao ginecologista permitem a detecção precoce de doenças.</p>
            <p>Exames preventivos, como o Papanicolau, são fundamentais para prevenir o câncer do colo do útero.</p>
            <p>Evitar a automedicação também é muito importante, pois pode mascarar sintomas e agravar problemas.</p>
            <button onclick="mostrar('inicio')">⬅ Voltar</button>
        </div>
    </section>

    <section id="sistema">
        <img class="banner" src="https://s1.static.brasilescola.uol.com.br/be/conteudo/images/f5210b9b122d724dc9dac117ace1ff93.jpg" alt="Sistema Reprodutor">
        <div class="card">
            <h2>Sistema Reprodutor Feminino</h2>
            <p>O sistema reprodutor feminino é composto por órgãos responsáveis pela reprodução, produção de hormônios e funcionamento do ciclo menstrual.</p>
            <p>Os principais órgãos são:</p>
            <p>• Ovários: produzem os óvulos e hormônios</p>
            <p>• Trompas de Falópio: transportam o óvulo</p>
            <p>• Útero: local onde o bebê se desenvolve</p>
            <p>• Vagina: canal de saída do fluxo menstrual e parto</p>
            <p>Esses órgãos trabalham juntos para possibilitar a reprodução e manter a saúde do corpo feminino.</p>
            <button onclick="mostrar('inicio')">⬅ Voltar</button>
        </div>
    </section>

    <section id="sus">
        <img class="banner" src="https://cdn-icons-png.flaticon.com/512/2966/2966488.png" alt="Absorventes SUS">
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
            <p>Dica importante: Se você ou alguém que conhece precisa, procure a UBS mais próxima ou o CRAS da sua cidade para receber orientação.</p>
            <button onclick="mostrar('inicio')">⬅ Voltar</button>
        </div>
    </section>

    <section id="contraceptivos">
        <img class="banner" src="https://static.vecteezy.com/ti/vetor-gratis/p1/6922254-contraceptivos-conjunto-controle-de-natalidade-ilustracao-para-impressao-fundos-capas-embalagem-cartoes-cartazes-adesivos-textil-e-design-sazonal-isolado-em-fundo-branco-vetor.jpg" alt="Métodos Contraceptivos">
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

    <nav>
        <button onclick="mostrar('inicio')">
            🏠<span>Início</span>
        </button>
        <button onclick="mostrar('cuidados')">
            🧼<span>Cuidados</span>
        </button>
        <button onclick="mostrar('sintomas')">
            ⚠️<span>Sintomas</span>
        </button>
        <button onclick="mostrar('prevencao')">
            🛡️<span>Prevenção</span>
        </button>
        <button onclick="mostrar('sistema')">
            🧬<span>Sistema</span>
        </button>
        <button onclick="mostrar('sus')">
            🩸<span>SUS</span>
        </button>
        <button onclick="mostrar('contraceptivos')">
            💊<span>Métodos</span>
        </button>
    </nav>
</body>
</html>
