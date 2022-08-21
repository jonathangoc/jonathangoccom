---
title: "The Internet of Everything"
date: 2014-08-06T09:06:00+00:00
draft: false
layout: "single"
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
cover:
    image: "/img/iot1.png"
    responsiveImages: true
    hidden: true
tags: ["tech", "novabase", "iot", "internet of things", "ioe", "internet of everything", "cisco", "ibm", "people", "processes", "data", "things", "smart cities", "cidades inteligentes", "aerospace", "transportation", "energy", "utilities", "telecommunications", "media"]
categories: ["Tech", "IoT"]
UseHugoToc: true
showToc: true
TocOpen: true
---

> ***⚠ This article is written in Portuguese. If you would like to get access to the English version please contact me directly.***

## 1.0. Introdução

### 1.1. Motivação
Com o rápido avanço da tecnologia, da medicina e das comunicações, tem- se procurado soluções para combater problemas graves e existentes nas sociedades de hoje em dia. A fome, o acesso a água potável e o aparecimento de novas doenças são ainda factores reais e preocupantes. Como prova, tem-se vindo a verificar que ao longo dos últimos 50 anos a população humana mundial quase triplicou e a poluição industrial, a prática de políticas insustentáveis na agricultura e o mau planeamento cívico levou ao aumento do consumo de água, diminuindo globalmente a quantidade de água potável.

Existem ainda outros factores que ativamente afetam o nosso modo de vida. Diversas fragilidades no sistema financeiro ameaçam constantemente o progresso socioeconómico e o aumento do custo da energia causa instabilidade nos países. A inexistência de um plano ou estratégia bem definida pode causar o aumento de despesas para as empresas e uma política governamental inadequada pode, consequentemente, aumentar a carga fiscal dos consumidores.
Contudo, a Internet é uma tecnologia que tem tremendo potencial para solucionar muitos dos desafios que a sociedade enfrenta. Tem beneficiado pessoas, empresas e países; melhorando a educação através da democratização da informação; tem possibilitando o crescimento econômico através comércio electrónico (e-commerce) e aumentando a inovação empresarial por meio de plataformas de colaboração.

À medida que a Internet evolui, torna-se importante perceber o impacto de como esta pode melhorar a vida dos cidadãos, da indústria e dos países. Através da transmissão adequada da informação à pessoa certa, no momento certo, consegue-se melhorar a qualidade de vida e a tomada de decisões estratégicas.
Finalizando, ter uma compreensão geral sobre as interações entre pessoas, processos, dados e objetos será fundamental para implementar soluções adequadas que satisfaçam as verdadeiras necessidades das pessoas, tornando a sua vida mais simples e mais feliz!

### 1.2. Objetivos
O trabalho que se apresenta neste documento pretende descrever o impacto da Internet of Everything (IoE) no contexto pessoal, empresarial e no futuro dos países.

Ao longo desta investigação iremos apresentar o conceito e o porquê de IoE, com o intuito de familiarizar o leitor com este novo termo. Posteriormente ir-se-á fazer a distinção entre este conceito e um bastante conhecido, designado por Internet of Things (IoT), explicando as diferenças. A área económica também será tema de estudo, no sentido de analisar o valor em jogo dentro deste mercado, tanto para o sector público como para o privado, avaliando as oportunidades e os riscos inerentes a esta transição tecnológica. Adicionando, serão apresentados os desafios e os sectores que podem estar envolvidos na implementação da IoE, assim como será apresentada uma arquitetura de referência proposta pela Cisco para colocar em prática este conceito. Após apresentarmos as principais empresas do mercado (players) e darmos ao leitor uma visão geral sobre o que estas andam a desenvolver atualmente, iremos analisar o que as empresas analistas têm a dizer sobre a IoE e o desenvolvimento das tecnologias de informação e comunicação (TIC). Posto isto, analisaremos as potenciais empresas parceiras e como podemos implementar o conceito de IoE no mercado Africano ao reutilizar soluções já existentes dentro da Novabase. Por fim, serão apresentadas algumas demos e exemplos reais de implementações de soluções de IoE, abordando os exemplos de Barcelona (Espanha), Nice (França) e Nova Iorque (EUA).

Visões para o futuro bem como outras considerações sobre o tema farão parte da conclusão deste estudo.

### 1.3. Organização
O presente documento está organizado pela seguinte ordem:

* **Capítulo 2** introduz uma visão geral sobre o estado da arte, onde se apresenta a definição do IoE e o seu motivo. Faz-se a distinção entre IoE e IoT e é avaliado o valor em jogo deste mercado emergente. De seguida são enumerados os desafios a enfrentar e os sectores nos quais se propiciam melhores condições para se implementar soluções IoE. Para que estas soluções sejam implementadas com sucesso é necessário uma arquitetura end-to-end. Uma das arquiteturas de referência é sugerida pela Cisco e é mencionada neste documento. Para finalizar, serão enumerados vários desafios associados a esta temática.

* **Capítulo 3** descreve-se as principais empresas que estão a desenvolver tecnologia e a implementar soluções IoE. Iremos investigar o que a imprensa e as empresas analistas têm a dizer sobre o IoE e analisar o seu impacto na vida dos cidadãos, no mundo empresarial, nas cidades e países. Posto isto, serão apresentadas empresas que poderão ser um ponto-chave para a Novabase na criação de parcerias por forma a poder implementar soluções IoE nos clientes. Ainda durante este capítulo iremos tentar perceber como podemos implementar abordar o mercado Africano e como podemos reutilizar soluções já existentes na Novabase para espoletar novos negócios. Por fim apesenta-se algumas demos.

* **Capítulo 4** conclui todo o trabalho realizado até ao momento e apresenta considerações futuras assim como uma visão do que poderá ser o IoE nos próximos anos para a Novabase.

## Capítulo 2

### 2.1. Introdução
À medida que a Internet evolui, surge a necessidade de conectar mais objetos a este sistema global de comunicação.
Segundo as previsões da Cisco, a Internet irá conectar cerca de 25 mil milhões de dispositivos em 2015, porém cerca de 1% dos objetos permanecem desligados na Internet. Em 2020, prevê-se que o número de objetos conectados à Internet será de 50 mil milhões (Figura 1).

> **Nota:** É importante salientar que os valores apresentados são baseados nos factos reais de hoje em dia e não têm em consideração os rápidos avanços da Internet ou dos dipositivos tecnológicos. Outra consideração a ter em conta é o facto de o número de dispositivos conectados por pessoa ter um crescimento lento. Isto deve-se ao cálculo ser feito para a população mundial, e como tal, muitas das pessoas ainda não estão conectadas a Internet.

| ![](/img/iot2.png) |
| :--: |
| **Figura 1:** Comparação entre o número de dispositivos e a população mundial. |

Da mesma forma, tem-se verificado uma tendência crescente para os objetos possuírem capacidades que os tornem mais sensíveis ao meio que os rodeia, maior capacidade de processamento e capazes de comunicar através de várias interfaces/tecnologias. Consequentemente, associar estes objetos à recolha de grandes quantidades de dados e utilizando processos adequados para entregar informações úteis às pessoas, faz da IoE a nova era da Internet.

### 2.2. Internet of Everything (IoE)

Antes de entrar em grandes detalhes e discutir as bases que suportam o Internet of Everything, é importante esclarecer o conceito com o objectivo de dar um bom entendimento ao leitor.

A Cisco define Internet of Everything (IoE) como sendo a ideia de ligar pessoas, processos, dados e objetos para tornar a conexões da rede mais importantes e mais valiosas. Ao converter informações em ações cria-se novas oportunidades económicas para pessoas, empresas e países, enriquecendo a experiência.

Para perceber melhor este conceito, vamos analisar a Figura 2 e perceber cada componente constituinte do IoE.

| ![](/img/iot3.png) |
| :--: |
| **Figura 2:** Componentes base do IoE. |

**Pessoas:** Em IoE, as pessoas terão a capacidade de se conectar à Internet das mais diversas formas. Hoje em dia, a maioria das pessoas que se liga à Internet usa dispositivos para aceder às redes sociais (Facebook, Twitter, LinkedIn, Pinterest). À medida que a Internet evolui no sentido de conectar tudo e todos, iremos criar ligações cada vez mais relevantes e de elevado valor. Como exemplo, num futuro próximo, as pessoas terão acesso a comprimidos que incorporam sensores e que irão reportar o estado de saúde do seu sistema digestivo ao doutor através de uma ligação segura à Internet. Sensores serão colocados na roupa para recolher informações sobre os sinais vitais das pessoas, onde elas próprias se tornarão os nós da Internet, gerando e transmitindo constantemente informações sobre as atividades do ser humano.

**Dados:** A crescente tendência para os objetos se ligarem à Internet leva-os a recolher dados e a transmiti-los através da Internet para as bases de dados, onde posteriormente são analisados e processados. Mais importante do que apenas transmitir dados, é combinar de forma inteligente as informações que levarão a tomar decisões mais acertadas. Em IoE, transformar dados em informações úteis é importante porque irá permitir tomar decisões inteligentes com maior rapidez, assim como controlar eficientemente o contexto de uma determinada situação, ou ambiente.

**Objetos:** São considerados os itens físicos, como sensores, dispositivos e ativos das empresas que estão conectados à Internet e a outras redes. No âmbito de IoE, estes objetos irão recolher mais dados, tornando-se sensíveis ao meio que os rodeia e ao fornecer mais informações irão ajudar as pessoas e as máquinas a tomar decisões. Alguns exemplos de objetos com estas características são: sensores inteligentes embutidos em pontes, sensores no parque de estacionamento e sensores colocados nas embalagens dos alimentos.

**Processos:** Esta componente tem um papel fundamental em como os três grupos acima referidos (Pessoas, Dados e Objetos) se interligam para entregar valor num mundo completamente conectado. Com os processos adequados, as ligações à Internet tornam-se mais valiosas porque a informação é entregue de maneira apropriada à pessoa certa no momento indicado.

A IoE será construída sobre mil milhões de conexões, implementando redes de redes e onde iremos criar oportunidades sem precedentes. Contudo, novos riscos irão aparecer e no qual é necessário um trabalho cuidado para os mitigar de forma a fazer da IoE uma realidade irrevogável.

O verdadeiro valor do sucesso ao usufruir da IoE traduz-se nos benefícios obtidos pela humanidade. As pessoas têm a percepção do mundo através dos sentidos e neste contexto a IoE torna-se um elemento intermédio para sentir, perceber e gerir o mundo. Nos negócios, o sucesso define-se pela capacidade de gerar lucro, e através das potencialidades da IoE será possível atingir os objetivos traçados, criando novas oportunidades.

Na conjuntura de uma nação, existem diversas formas de governação, todavia a transparência é um factor crítico para os países prestarem serviços aos seus cidadãos. Quando corretamente aplicada à privacidade, segurança e proteção, a IoE irá ajudar a aumentar os níveis de transparência em qualquer área do governo beneficiando todas as pessoas. Apesar disto, a IoE enfrentará muitos obstáculos à medida que se concretiza a sua implementação. Alguns desses desafios abrangem temas como segurança, privacidade e fiabilidade, enquanto outros problemas requerem discussões sociais e politicas.

O conceito de IoE invoca um outro conceito que está na moda mas que não é novo, designando-se por Internet of Things (IoT) e descreve sistemas em que os objetos do mundo físico e sensores estão conectados à Internet via ligações com fios e/ou sem fios. Esses sensores podem usar tecnologias locais como RFID, NFC, Wi-Fi, Bluetooth e Zigbee e ainda usar tecnologias globais de comunicação como é o caso do GSM, GPRS, 3G e LTE para recolha e transmissão de dados. Contudo a IoT refere-se à simples conexão de objetos físicos a uma rede, sendo uma transição tecnológica singular, ao invés da IoE que abrange várias transições tecnológicas, incluindo pessoas, processos e a própria IoT. A IoE continuará a criar oportunidades sem precedentes para o cidadão, para as organizações, para comunidades e países criando valor através das ligações em rede entre as pessoas, processos, dados e objetos.

### 2.3. O Valor em Jogo

**Valor da Oportunidade Global**

Existe uma oportunidade enorme em ligar objetos que ainda não estão conectados à Internet. A Cisco prevê que em 2020, 50 mil milhões de objetos estarão ligados a Internet e por isso estima que o valor mundial desta oportunidade será de 19 biliões de dólares. Este é o melhor valor, ou seja, o valor para o qual o rendimento é máximo e o custo mínimo. A investigação da Cisco indica que destes 19 biliões de dólares, 14.4 biliões estão associados ao sector privado e 4.6 biliões ao sector público (Figura 3).

| ![](/img/iot4.png) |
| :--: |
| **Figura 3:** Valor da Oportunidade. |

Para perceber o impacto da IoE nos valores acima referidos, são apresentados os cinco impulsionadores desta oportunidade, tanto para o sector privado como para o sector público. Nos próximos 10 anos, os cinco factores que irão impulsionar o sector privado, para perfazer 14.4 biliões de dólares, serão:

* A utilização de ativos ($2.5 biliões): ao implementar soluções IoE, as empresas irão reduzir os custos nas áreas administrativas, vendas e outras mais gerais e ainda reduzir custo de produção e de posse dos materiais, ao melhorar a execução de processos e a aumentar a eficiência do capital.

* Produtividade dos trabalhadores ($2.5 biliões): IoE aumentará a eficiência dos trabalhadores ou irá diminuir o número de horas dos mesmos (ex.: diminuir horas das deslocações ou até mesmo elimina- las).

* Cadeia de entrega e logística ($2.7 biliões): Melhorar a gestão do stock e a eficiência nos processos.

* Experiência do consumidor ($3.7 biliões): Ao adicionar mais consumidores, a IoE irá aumentar a cota do mercado.

* Inovação, incluindo redução do time to market ($3.0 biliões): IoE irá aumentar o retorno do investimento em Investigação e Desenvolvimento (I&D), reduzir o time to market e aumentar os canais de receitas através de novos modelos de negócio e oportunidades.

Dentro do sector público os cinco pontos que irão valorizar a oportunidade em 4.6 biliões de dólares, nos próximos 10 anos são:

* Produtividade dos trabalhadores ($1.8 biliões): Ao instalar soluções IoE iremos aumentar eficácia laboral, através de soluções de colaboração.

* Conectar as defesas militarizadas ($1.5 biliões): Ao conectar os veículos militarizados com o centro de comando, o exército poderá aumentar a capacidade de gestão e de reconhecimento de determinas situações.

* Redução de Custos ($740 mil milhões): IoE irá reduzir os custos de operação, melhorar a eficiência laboral e diminuir a despesas.

* Experiência do Cidadãos ($412 mil milhões): IoE irá diminuir os tempos de pesquisa, melhorando o ambiente que nos rodeia, produzindo melhores resultados para a saúde.

* Aumento das receitas ($125 mil milhões): As soluções da IoE irão permitir ajustar o fornecimento de produtos de acordo com a necessidade, melhorando, ao mesmo tempo, a monitorização.

Avaliando estes factores observa-se como a IoE tem potencial para mudar os processos do sector privado e público. Contudo, a capacidade para capitalizar as soluções dentro destes factores impulsionadores depende de vários aspetos chave. Para usufruir desta oportunidade, as organizações devem combinar tecnologia que permita segurança (tanto lógica como física) com politicas e processos criados para proteger a informação privada da empresa, consumidor e/ou cidadão. O crescimento deste conceito (IoE), principalmente no sector privado, depende, na sua maioria, do sucesso deste esforço.

**Valor da Oportunidade para o Sector Privado (Empresas e Indústria)**

Como foi mencionado anteriormente, o melhor valor do IoE para o sector privado a nível mundial (empresas e indústria) é de 14.4 biliões de dólares nos próximos 10 anos. As empresas e indústrias que melhor souberem aproveitar as potencialidades do IoE irão beneficiar de duas formas:
1. Ao criar valor através da inovação tecnológica.
2. Ao ganhar avanço competitivo e ao aumentar a cota do mercado em
relação aos concorrentes.

A maior parte do valor em jogo para o sector privado (66%) advém da transformação baseada em casos específicos da indústria, como por exemplo, Smart Grids e Smart Buildings. Os outros 34% resultam de benefícios de novas metodologias de trabalho e de plataformas de colaboração que irá diminuir ou até mesmo evitar viagens (ver Figura 4).

| ![](/img/iot5.png) |
| :--: |
| **Figura 4:** Análise do valor em jogo para o sector privado. |

O valor total não inclui potenciais valores gerados pelos consumidores, pelo sector publico ou por benefícios sociais.

**Valor da Oportunidade de acordo com a geografia**

Outra análise realizada pela Cisco baseia-se no valor da oportunidade de acordo com a geografia. Analisando a Figura 5, denota-se uma distribuição dos 19 biliões de dólares pelas maiores regiões. Também se pode verificar o grau do impacto por cada região que é determinado pela divisão do valor em jogo pelo tamanho da indústria. Os factores que estimulam estes valores baseiam-se no crescimento relativo da economia de cada região e pelo tamanho relativo de cada indústria em cada região. Como exemplo, nos EUA e na EU as oportunidades são mais predominantes no sector de serviços.

| ![](/img/iot6.png) |
| :--: |
| **Figura 5:** Distribuição do Valor em Jogo pelas regiões geográficas [Fonte: Cisco IBSG, 2013]. |

No próximo subcapítulo iremos abordar a IoE nas Smart Cities e descrever algumas aplicações nos diferentes sectores. Na visão da Novabase são consideradas sete (7) áreas importantes para os cidadãos, negócios e para a cidade em si. Estas sete áreas são compostas por cinco (5) verticais e duas (2) transversais.

### 2.4. IoE nas Cidades

Desenvolver cidades inteligentes e colocar em prática soluções IoE não são tarefas fácies e os desafios são amplamente divergentes. Para que uma cidade se torne inteligente é necessário que os serviços implementados sejam pensados com base no cidadão. E claramente que as soluções variam de cidade para cidade. Porém, cada cidade pode considerar o desenvolvimento de um plano para a criação de uma rede convergente e unificada.

Posto isto, algumas questões são colocadas:
* Como é que as cidades irão adoptar a inovação e as novas ideias?
* Como é que se consegue investimento adicional para escalar as
ideias e torna-las reais?
* Que tipo de serviços se deve considerar em primeiro lugar?

As cidades têm que estar dispostas a experimentar, a investir em novas ideias com riscos calculados e colaborar com diferentes intervenientes e entidades públicas e privadas.

As cidades podem pensar de forma criativa para financias iniciativas de Smart Cities. As cidades têm uma forte tendência para o negócio com base num orçamento e os programas de longa duração são financiados sem qualquer tipo de acompanhamento, revisão e alinhamento com as estratégias de Smart Cities. Frequentemente as entidades governamentais têm que lutar por orçamentos sem qualquer tipo de colaboração e interconexão. Mecanismos tradicionais de financiamento, como subsídios por parte do governo, fazem com que as cidades fiquem limitadas a certo tipo de projetos. Isto não permite que as próprias cidades financiem os projetos que vão de acordo com a sua visão e que melhor se adequa aos seus cidadãos.

Adicionando ao processo de orçamentação e financiamento, que em muitos casos é descoordenado, as entidades governamentais das cidades tem que lidar com a duplicação de ativos. Os líderes têm que desenvolver e promover um plano digital que impacte toda a cidade para atrair investimento para as diferentes estruturas públicas. O primeiro serviço a ser considerado é a criação desse plano digital, que deverá ser continuo e progressivo com plano de investimento superior a 10 anos. Uma análise dos principais desafios deverá ser feita e deverá ser estudada os serviços necessários para resolver esses desafios.

| ![](/img/iot7.png) |
| :--: |
| **Figura 6:** Soluções segmentadas de acordo com os sectores económicos. |

Os serviços podem ser segmentados de acordo com sectores económicos. Na Figura 6: Soluções segmentadas de acordo com os sectores económicos é possível verificar a distribuição de alguns dos serviços possíveis pelas diferentes áreas endereçadas pela Novabase.

**Aerospace and Transportation** – área que integra todos os transportes privados terrestres, náuticos e aéreos. Tem-se como exemplo de serviços Smart Vehicles no qual veículos comunicam entre si e entre si e a infraestrutura permitindo que os carros criem uma rede móvel de comunicação designada por VANET (Vehicular Ad-hoc Network) que possibilita o acesso à Internet. Os condutores e passageiro irão usufruir de maior comunidade, menos tempo despendido no trafego através do cálculo de melhores rotas e de uma experiencia de entretenimento através do acesso a conteúdos multimédia atualizados. A forma como as diferentes empresas irão alavancar negócio através da distribuição e comercialização de serviços e aplicações em redes veiculares apresentará por si só um tremendo desafio. Os modelos de negócios devem ser rentáveis para as operadoras de telecomunicações e os serviços devem prezar por preços acessíveis e atraentes. Para tal, deve haver sistemas de pagamentos e mecanismos de contabilidade especiais baseados na rapidez e flexibilidade. Nos aviões poderão existir mecanismos de interação entre os smartphones e os sistemas de entretenimento.

**Government and Healthcare** – os governos podem tirar proveito das soluções IoE ao implementarem sistemas inovadores de Smart Parking, Smart Traffic Management, Waste Management, entre outro. Estas soluções permitirão obter receitas mais facilmente através de processos de pagamento inovadores e facilitar a vida dos cidadãos. Melhorar o ambiente urbano e ter um maior controlo sobre as atividades públicas no que se refere à gestão da cidade são mais dois benefícios deste tipo de soluções. Médicos e enfermeiros irão falar com os seus pacientes através de plataformas de colaboração evitando que o paciente se desloque ao centro de saúde e uma análise do estado do paciente possa ser feita através de sensores que irão monitorizar o seu estado de saúde.

**Energy and Utilities** – o sucesso da indústria petrolífera e da exploração de gás e minerais dependerá de estratégias inovadoras que ajudem a encontrar os recursos minerais e hidrocarbonetos, independentemente destes se encontrarem em locais muito remotos e profundos. Soluções IoE de mobilidade, colaboração, vídeo e sensores podem ter um papel diferenciador na transformação desta indústria ao introduzir melhorias e otimizações nos processos de extração, monitorização analise e transporte dos recursos. Hoje em dia, as empresas de fornecimento de eletricidade utilizam uma infraestrutura com base no melhor esforço, ou seja, geram energia e transportam-na pela rede sem tirar total partido das suas capacidades. Isso faz com que a rede seja vulnerável a falhas e que o fluxo de fornecimento de energia seja feito apenas numa direção: do fornecedor para o cliente. As soluções de IoE irão melhorar a performance da rede elétrica através da detecção de problemas e resolução autónoma dos mesmos, controlar os fluxos elétricos com base na necessidade em tempo real e utilizar mais as energias renováveis como fonte principal de geração de energia.

**Manufacturing and Services** – ao nível industrial o IoE poderá ajudar as empresas a diminuir os custos operacionais através de soluções de gestão das frotas com forme a necessidade do cliente e consequentemente optimizar as rotas dos veículos de transporte. Por outro lado poderá aumentar a produtividade dos colaboradores e melhorar a eficiência dos processos de eliminação dos resíduos provocados pelo fabrico dos produtos. Por outro lado, ao monitorizar as vendas, as indústrias poderão a adaptar dinamicamente o nível de produção, diminuindo os custo de stock elevado e da própria produção.

**Telecommunications and Media** – as operadoras de telecomunicações e as empresas de media irão ter um papel fundamental na criação de soluções IoE e elas próprias irão beneficiar com a sua implementação. Estas empresas irão fornecer serviços móveis e serviços de dados, assim como dar acesso a conteúdos media sempre atualizados. Por outro lado poderão criar mecanismos de Smart Payment que facilitará a vida dos cidadãos.

**Security** – o mundo do IoE irá permitir aos cidadãos, empresas e cidades utilizar uma arquitetura de rede integrada, sensores inteligentes, grande capacidade de computação e analítica. Porém, com o crescimento das redes e número de dispositivos e com o aparecimento de novas tecnologias de comunicação a privacidade e a segurança da informação poderá estar comprometida. O ecossistema IoE e as soluções que nele residem devem ser robustos e seguros, tanto ao nível físico como ao nível lógico. As políticas e processos devem ser desenhados para proteger a privacidade dos cidadãos, empresas (públicas e privadas) e governo. A cibersegurança tem ser considerada a quando da implementação das soluções. A Novabase acredita que este será um factor diferenciador entre soluções.

**Citizen Experience** – para a Novabase, as soluções tem que estar orientadas para o cidadão e a experiência vivida por estes a quando da utilização de soluções IoE deve ser simples e feliz. Muitas das soluções IoE irão melhorar a qualidade de vida, melhorar o meio ambiente e produzir mais benefícios para a saúde. As características de design e experiência de utilização deverão estar presentes nas soluções que compõem o ecossistema da Figura 6: Soluções segmentadas de acordo com os sectores económicos.

### 2.5. Arquitetura IoE para as Cidades

As arquiteturas IoE para as cidades requerem uma integração perfeita de sensores num ambiente de comunicação semelhante. Tradicionalmente, uma determinada rede é implementada de acordo com uma dada aplicação, como por exemplo: gestão da iluminação pública, vídeo vigilância ou monitorização do ambiente urbano. Porém, atualmente as redes fornecem um ambiente de separação entre elas, o que as torna menos eficientes em termos de custos e segurança. Acrescentando, as interações entre os sensores e outros dispositivos requerem integrações específicas em cada rede.

Algumas cidades estão a explorar o desenvolvimento de infraestruturas horizontais de múltiplos serviços, que irão albergar todos os sistemas da cidade. Estas abordagens são desenhadas para facilitar a integração de novas aplicações que normalmente requerem instalação nos dispositivos terminais. Garantir que os custos de implementação de futuros serviços são mínimos e que haja disrupção da atual arquitetura de rede são os objetivos que se pretende atingir com a proposta de uma arquitetura de referência. A eficácia desta arquitetura de referência será determinada por diversos factores, dos quais salientamos a conexão das pessoas com as máquinas e sensores nas cidades; a recolha segura em tempo real de dados e posteriormente o seu armazenamento e por fim, analisar os dados e identificar padrões, de modo a prever tendências de mercado. Deste modo, a arquitetura de referência deve ser capaz de gerir milhões de dispositivos e sensores, milhares de servidores, transmissão multidimensional, processamento e streaming de grandes quantidades de dados. Apesar disto, a infraestrutura necessita de processar os dados, detetar a tendência e tomar decisões na extremidade da rede. Numa primeira análise, uma solução para os superar poderia passar por aumentar o poder de processamento a atual arquitetura de rede. Contudo, para atingir os objetivos acima mencionados, uma nova arquitetura é necessária. A cidade de Nice, através do serviço piloto de Smart Parking, propôs uma arquitetura. Ver Figura 7.

| ![](/img/iot8.png) |
| :--: |
| **Figura 7:** Arquitetura de referência para Smart Cities. |

Esta arquitetura é constituída por quatro camadas:

* **Layer 1** – Sensores e dispositivos de rede ligados através de redes com topologia mesh: permite uma integração eficiente destes dispositivos, melhorando a resiliência da cidade.

* **Layer 2**  – Recolha de dados, processamento, armazenamento e análise distribuídos pela cidade: Desta forma reduz-se a complexidade da arquitetura e assegura a extensibilidade da rede. Além disso, uma arquitetura distribuída aumenta a escalabilidade e aumenta a capacidade de resposta em tempo real.

* **Layer 3** – Combinação de Interfaces de Programação de Aplicações (APIs), com a recolha de dados, processamento, armazenamento e análise.

* **Layer 4** – Aplicações e serviços inovadores tanto para as entidades gestoras da cidade como para os seus residentes.

Esta arquitetura de referência engloba várias características únicas que a torna mais extensível, resiliente e robusta comparativamente com outros sistemas usados nos últimos cinco anos pelas cidades.

Esta arquitetura apresenta as seguintes vantagens:

1. **Simplicidade e disponibilidade:** A combinação entre comunicações IP end-to-end, largura de banda, optimização de frequência com topologias de rede mesh e resiliência garante alta qualidade de serviço e pouca manutenção.
2. **Segurança:** Mecanismos de segurança IP garantem um sistema mais robusto e resiliente. Mais ainda, modelos peer-to-peer separam diferentes componentes e previnem falhas, eliminando o risco de colocar em perigo todo o sistema
3. **Interoperabilidade:** Soluções baseadas em standards tornam mais fácil para a cidade e parceiros adicionar serviços.
4. **Multisserviço:** As soluções implementadas também dão enfâse aos dados, voz, vídeo e sensores. Em adição, a arquitetura é agnóstica no sentido em que as diferentes aplicações podem coexistir no mesmo ambiente, independentemente da origem e do tipo de dados.
5. **Escalabilidade tecnológica:** Ao utilizar tecnologia IPv6 e ao distribuir o processamento dos dados pela rede, a arquitetura está apta para lidar com o crescente número de objetos conectados à rede.
6. **Escalabilidade do negócio:** Esta arquitetura oferece a possibilidade de pagar conforme as necessidades do utilizador.
7. **Gestão:** O facto de a arquitetura ter uma natureza end-to-end, torna- a de fácil manutenção pois permitir uma visibilidade global da infraestrutura, desde a camada de aplicação até a camada física.
8. **Extensibilidade:** os requisitos para que as novas aplicações se integrem com a infraestrutura existentes são os terminais e APIs.
9. **Flexibilidade:** A arquitetura permite às entidades gestoras da cidade e também aos cidadãos, utilizar os mesmos serviços e informações para necessidades específicas.

Concluindo, esta arquitetura de referência pode servir como exemplo para implementação do conceito IoE noutras cidades, envolvendo governo, negócios e cidadãos num ambiente único de partilhas de informação e colaboração.

### 2.6. Demos e Exemplos Pilotos

Já existem na atualidade cidades que estão a implementar projetos e plataformas relacionadas com o IoE, beneficiando das vantagens acima mencionadas na secção 2.3. Neste sentido, a experiência retirada de exemplos piloto pode dar às outras cidades estratégias de progressão e de desenvolvimento das suas próprias iniciativas. Nesta secção iremos apresentar alguns exemplos de soluções IoE implementadas em algumas cidades.

**Barcelona, Espanha**

A cidade está, neste momento, a utilizar o conceito IoE ao difundir Internet através de Hotspots Wi-fi consegue fornecer novos serviços, enriquecer a experiência dos utilizadores e aumentar as oportunidades económicas.
Um dos serviços implementados neste projeto de Smart City foi a gestão de lugares de estacionamento, através da instalação de sensores em cada lugar e através de uma plataforma que comunica com dispositivos no interior do carro, que permite encontrar lugares livres (Figura 8).

| ![](/img/iot9.png) |
| :--: |
| **Figura 8:** Sensores implementados nos lugares de estacionamento. |

Este tipo de serviço tem a vantagem de, por um lado, reduzir o tempo de procura de lugares livres, e por outro, diminuir o trafego rodoviário e reduzir o consumo de combustível. Neste âmbito, outros serviços foram implementados, tais como o Smart Bus Stops and Buses, Lighting Management e Environmental Management, que pretendem melhorar a vida dos cidadãos e das entidades responsáveis pela gestão da cidade. Como exemplo, nas paragens de autocarros os cidadãos podem obter informação sobre os horários e sobre as rotas, assim como, obter informações sobre pontos de interesse (negócios, comércio, espetáculos, etc.) nos arredores. Podem também aceder à Internet através dos dispositivos pessoais.

Quanto à iluminação, Barcelona instalou luzes extremamente eficientes que automaticamente fazem a gestão da energia necessária (Figura 9).

| ![](/img/iot10.png) |
| :--: |
| **Figura 9:** Gestão a Iluminação Pública. |

Através da instalação de sensores que se encontram distribuídos pela cidade, oferece às entidades de gestão da cidade informações relevantes para que possam tomar decisões mais acertadas e que se baseiam em dados em tempo real. Desta forma, consegue-se fazer uma melhor gestão das operações, reduzir custos e também melhorar a sustentabilidade económica, social e ambiental.

**Nice, França**

Em Nice, a Cisco e outras empresas parceiras focaram-se em desenvolver um projeto Smart City cujos objetivos são testar e validar uma arquitetura de tecnologia IP, um modelo económico e determinar os benefícios do conceito IoE.
Este projeto baseia-se numa plataforma partilhada para tornar mais simples as conexões que são críticas para a cidade se tornar uma Smart City. O projeto servirá como catalisador, combinando descobertas fulcrais desta e doutras iniciativas Smart City.

Este projeto inclui quatro serviços que demonstram realmente os benefícios e o verdadeiro valor de soluções IoE:

* Controlo inteligente do tráfego

* Iluminação inteligente

* Gestão inteligente do lixo urbano

* Monitorização inteligente do ambiente

A Cisco e a cidade de Nice estão a avaliar como utilizar a informação que é obtida a partir da análise dos dados recolhidos dos diferentes serviços. As implicações do cruzamento de dados e da colaboração de diferentes entidades vai para além da viabilidade da tecnologia porque também tem um tremendo impacto nas tomadas de decisões por parte dos gestores da cidade, dos departamentos governamentais e das operações.

**Nova Iorque, EUA**

Para revitalizar as maiores cidades mundiais, a empresa City24/7 com o objectivo de tornar as comunicações públicas acessíveis a todos e em qualquer lugar, em colaboração com a Cisco e a cidade de Nova Iorque, desenvolveu uma plataforma interativa que integra informações de programas governamentais, de negócios locais e de cidadãos para partilhar o conhecimento independentemente do local, momento ou dispositivo.

O produto desenvolvido por esta empresa tem o nome de City24/7 Smart Screens e incorpora interfaces de ecrã táctil, voz e áudio para permitir o acesso a uma vasta gama de informações, como por exemplo: serviços e promoções em tempo real. Este produto pode ser encontrado em paragens de autocarros e/ou comboios, centros comerciais, centros desportivos e principais locais turísticos.

| ![](/img/iot11.png) |
| :--: |
| **Figura 10:** City24/7 Smart Screens. |

As principais vantagens deste produto são:

* Dar a conhecer informações relevantes sobre os locais, produtos e promoções na proximidade.

* Proteger melhor a cidade ao dar informações aos polícias e bombeiros de ocorrências. Posteriormente estas entidades podem providenciar apenas os recursos necessários.

* Revitalizar a cidade ao aumentar o comércio, investimento e turismo.

Para desenvolver soluções que funcionem com o sector público e privado, assim como para os cidadãos, City24/7 precisou de concretizar um método de pagamento dos serviços. Esta barreira tem impedido o sucesso de parcerias público-privadas com objetivos semelhantes. Contudo, a City24/7 trabalhou com muitas organizações durante as fases de desenvolvimento e teste incluindo o Departamento de Telecomunicações e Tecnologias de Informação de Nova Iorque, Amtrack, Hospitais e Metro de Nova Iorque entre outros.

Ao implementar mais Smart Screens, a rede vai crescer e consequentemente os dados recolhidos e as previsões também. Desta forma a empresa irá entregar mais valor às cidades, negócios e cidadãos. À medida que os cidadãos começam a utilizar cada vez mais esta plataforma, a rede ganha mais valor e os negócios poderão fornecer melhores serviços, aumentando o envolvimento com as pessoas. Concluindo, cria-se um ciclo vicioso e vantajoso para todas as partes envolvidas.

### 2.7. Desafios

À medida que soluções baseadas no conceito IoE são implementadas nas cidades, desafios terão de ser ultrapassados nos próximos 10 anos. Alguns desses desafios são familiares, como por exemplo: segurança, privacidade e mobilidade; enquanto outros requerem debates abertos que foquem temas sociais e políticos.

Para além dos desafios enumerados acima ainda existem obstáculos tecnológicos que precisam de ser ultrapassados. IPv6 deve tornar-se uma realidade para acompanhar a tendência crescente do número de conexões, assim como, encontrar fontes de energia para suportar o grande número de dispositivos (sensores, dispositivos, objetos que começam a estar ligados a Internet).

Salientando o tema da segurança e privacidade, a questão mais importante que se coloca é como vamos tratar estas duas vertentes num mundo ainda mais conectado. Computadores e sistemas são alvos diários de ataques de hackers e nenhuma organização está imune. Visto que é fácil roubar e fazer uso indevido das informações é natural haver uma certa preocupação sobre este problema à medida que se liga cada vez mais pessoas, processos, dados e dispositivos a uma única rede de comunicação. De seguida são apresentadas algumas ideias que podem desempenhar um papel importante na abordagem dos problemas de segurança e privacidade:

* Informações pessoais tornam-se legalmente reconhecidas como pertencentes ao utilizador. Enquanto entidades governamentais estão a tentar implementar políticas de privacidade do consumidor, existe paralelamente uma grande mudança em curso que vai mudar radicalmente a segurança e privacidade. No futuro, o utilizador poderá ter os direitos dos seus próprios dados ou daqueles que criou online, em vez de pertencerem às empresas como Amazon, Facebook, Google ou Twitter. Quando o utilizador tem direitos legais sobre as suas próprias informações, é possível ter mais controlo sobre a forma como é recolhida e utilizada por terceiros. Está visão está a ganhar força no Reino Unido, no World Economic Forum e na União Europeia.

* As informações pessoais tornam-se dinheiro. Inteligência será adicionada aos dados recolhidos e os blocos de dados serão aumentados para incluir informações sobre onde os dados foram criados, quem os criou e para onde são enviados. Deste ponto de vista, os dados tornam-se como dinheiro na conta bancaria online, onde se pode fazer o acompanhamento e transferir dados entre contas. É importante referir que esta transformação irá permitir auditar a informação pessoal para se fazer cumprir com as leis e politicas quando os problemas surgirem. Para concluir, os direitos associados aos dados pessoais terão um tratamento jurídico e judicial semelhante aos direitos de propriedade intelectual existentes hoje em dia.

* Empresas de armazenamento de dados pessoais protegem a informação. Para além de permitir saber e controlar a própria informação, o facto de possuir o poder sobre os dados irá permitir ao utilizador proteger a informação. As empresas de armazenamento de dados irão ajudar o utilizador a beneficiar com as suas próprias informações. Ao partilhar informações com outras empresas, os utilizadores podem ganhar uma pequena taxa ou uma compensação pelo facto de terem partilhado informações úteis que irão ajudar empresas (comercio, retalho e lojistas) a fornecer melhores serviços e produtos.

Em adição a estas ideias, a própria rede tem um papel essencial em melhorar a segurança. Para isso a inteligência e os processos de decisão devem estar distribuídos pelos nós da rede, isto é, nos nós onde são mais necessários. Com este esquema, as ameaças à segurança poderiam ser antecipadas, identificadas, localizadas e posteriormente eliminadas.

## Capítulo 3

### 3.1. Players IoE
Nesta secção iremos avaliar os principais Players do mercado que estão a investir em tecnologia e soluções IoE e também na temática Smart Cities. Iremos apresentar a sua visão e o tipo de produtos/serviços que disponibilizam no momento.

**Cisco**

Cisco afirma que é possível conectar a saúde (organização) ao sofá (utilizador) através de soluções de pequenas células (Cisco Small Cell Solutions). Os operadores de telecomunicações têm mostrado bastante interesse neste tipo de soluções pois ajuda a optimizar os serviços de telecomunicações móveis 3G, 4G e Wi-Fi. A solução Cisco Small Cell apresenta inovação na arquitetura da rede móvel, transformando pequenas células numa plataforma de serviço inovadora.

A gestão de tráfego rodoviário pode conectar-se com o carro através da solução Cisco Connected Roadways que conecta com segurança os sistemas de transportes inteligentes com o objetivo de melhorar o fluxo de tráfego, reduzir os acidentes de estrada e proporcionar uma visão centralizada das estradas. As entidades responsáveis pela gestão do tráfego rodoviário irão beneficiar desta solução pois irão melhorar as tomadas de decisões e diminuir os custos de operação e manutenção. Esta solução pode englobar sistemas de colaboração como por exemplo IPICS, switches Cisco IE 2000/3000, pontos de acesso Cisco Aironet 3500, routers com serviços integrados Cisco 819 e câmaras de vídeo vigilância Cisco Video Surveillance 6000 Series IP Cameras.

A Cisco apresenta a solução Connected Mobile Experiences (CMX), para detectar, conectar e envolver os utilizadores num determinado local. Estando o utilizador ligado sempre à rede de um centro comercial, hospital, escola ou de um local de prestação de serviços públicos, pode ter o privilégio de ter acesso à Internet em troca da informação da sua localização. Assim o CMX permite explorar o estilo de vida conectado e oferecer aos utilizadores conteúdos móveis relevantes sobre produtos, serviços e promoções e dar aos lojistas informações sobre perfis dos consumidos e respetivas análises dessas informações.

**IBM**

A IBM é outro grande player dentro desta temática, chamando-lhe Smarter Cities. A IBM define a cidade como um sistema de sistemas conectados entre eles, onde as cidades do futuro serão mais inteligentes e irão impulsionar o crescimento económico sustentável. Os líderes terão as ferramentas necessárias para analisar os dados para tomarem melhores decisões, antecipar problemas e coordenar os recursos, operando de uma forma mais eficaz.

Segundo a IBM, à medida que a exigência aumenta e os orçamentos são cada vez mais reduzidos, as soluções também têm que ser mais inteligentes, abordando a cidade como um todo. Através da recolha de grande quantidade de dados e posteriormente fazendo a sua análise, a ferramenta IBM Intelligent Operations Center organiza e partilha os dados e dá uma visão única, criando uma imagem global para os gestores das cidades. A IBM Intelligent Operations Center permite aceder a uma plataforma executiva para ajudar os gestores da cidade a ter uma visão sobre os diferentes aspetos da mesma. Esta plataforma permite fazer uma sondagem e receber informações de agências que se encontram sobre a alçada de uma de hierarquia superior, tais como segurança pública, serviços sociais, transportes públicos, hospitais, entre outras. Esta solução permite fazer a gestão de ambientes citadinos complexos, comunicar eficazmente com os cidadãos, entender o estado da cidade e colaborar com os diferentes departamentos e entidades. Em suma, a solução Intelligent Operations Center reduz os custos aumentando assim as receitas.

Por outro lado, o conceito de Smarter Cities da IBM assenta em três pilares fundamentais: Planeamento e gestão, Infraestrutura e Seres Humanos (Figura 11).

* **Planeamento e Gestão:** Fazer previsões a longo prazo que se baseiem na análise de dados, e fazer uma gestão diária irá ajudar a cidade a ficar revigorada e mais segura para os cidadãos e empresas. Do ponto de vista de resolução de problemas a IBM apresenta soluções nas áreas de Segurança Pública, Edifícios Inteligentes, Planeamento Urbano e Administração Pública. Algumas das soluções da IBM são:

    * Integrated Intelligence Analysis o Video Correlation and Analysis o Energy Optimization

    * Facilities Management

    * Performance Management for Government

    * Cloud Computing for Regional and Local Governments

* **Infraestrutura:** A entrega de serviços, como por exemplo transportes públicos, faz de uma cidade mais desejada pelos cidadãos. Porém, manter a cidade pronta para a mudança constante, torna-se uma característica essencial. A IBM tem uma oferta de diversas soluções para as áreas de Energia, Ambiente e Transportes. Abaixo estão mencionadas algumas delas:

    * IBM Intelligent Utility Network Solution
    * Smart Metering and Beyond
    * IBM Enterprise Asset Management for Energy and Utilities o Airport Operations Management Systems
    * Intelligent Transportation
    * IBM Intelligent Water

* **Seres Humanos:** as Smart Cities irão usar sistemas de sistemas para ganharem vantagem, satisfazendo as necessidades dos cidadãos através de programas sociais, de saúde e educação. As soluções apresentadas são:

    * IBM Cúram Social Program Management
    * Fraud and abuse management for payers o Healthcare asset management
    * Patient Care and Insights
    * Framework for smarter education
    * Campus solutions for higher education

| ![](/img/iot12.png) |
| :--: |
| **Figura 11:** Pilares das Smarter Cities da IBM. Fonte: [IBM Smarter Cities](http://www.ibm.com/smarterplanet/us/en/smarter_cities/overview/index.html). |

Desta forma, a IBM apresenta-se como uma das empresas a apostar no mercado e Internet of Everything.

** Qualcomm** 

Qualcomm é vista como outra empresa que terá um papel fundamental na implementação de soluções IoE visto que tem apostado durantes vários anos em chips e tecnologias de rádio. Para esta empresa, IoE é uma transformação onde objetos inteligentes estão conectados, criando uma nova era de oportunidades para os consumidores, empresas, governos e cidades. Esta empresa prevê que a IoE irá mudar o nosso mundo e que o seu efeito será profundo na vida quotidiana dos cidadãos. A caminhar no sentido de um mundo em que os cidadãos estarão rodeados de ligações que inteligentemente irão dar respostas a questões como o que precisamos e o que queremos.

Através de sensores, a Qualcomm acredita na criação de um novo conceito: Sexto Sentido Digital. Esta experiência será muito dinâmica e intuitiva fazendo com que pareça uma extensão das nossas próprias habilidades. No futuro, os cidadãos terão a capacidade de descobrir, concretizar e usufruir mais e melhor das informações recolhidas pelos sensores e pelas tomadas de decisões de processos e da inteligência da rede. Por outro lado, os smartphones e as redes sem fios serão elementos essenciais para tornar real o conceito de IoE. A implementação de uma camada de conectividade sem fios, que irá ser facilitada por esta empresa, e o uso de poderosos dispositivos móveis irá permitir que todos tenham acesso a soluções IoE.

Sendo um dos principais players, a Qualcomm possui um portfólio de soluções de comunicação e conectividade para suportar a IoE. De seguida apresenta-se algumas destas soluções.

* **AllJoyn Software Connectivity & Services Framework:** É um software universal e aberto a toda a comunidade que permite conectividade e comunicação entre objetos inteligentes independentemente da marca e do sistema operativo. Foi inicialmente desenvolvido pelo Qualcamm Innovation Center, Inc mas é agora um projeto do AllSeen Alliance (Consortium sem fins lucrativos dedicado à IoE).

* **Industrial Automation and Enterprise:** A Qualcomm desenvolve chips para comunicações móveis, conectividade e computação. Exemplos de implementação desta tecnologia podem encontrar-se em ATMs, máquinas de vendas e sistemas de pontos de vendas que utilizem modens Gobi 3G/4G. A conectividade destes dispositivos é complementada com soluções Wi-Fi e HomePlug Green PHY.

* **Development Platform:** Qualcomm fornece uma plataforma para desenvolvimento de hardware e software para construir dispositivos IoE e M2M (Machine-to-machine), com interfaces de ligação à rede móvel. Esta plataforma suporta Oracle Java Embedded ME SDK e inclui tudo o que é necessário para ligar à rede e começar a programar. No ponto de vista de prototipagem, contem uma plataforma com sensores, indicadores e relés para rápido desenvolvimento do protótipo inicial.

Existem ainda outras soluções como Smart Energy and Security e ainda soluções para conectar os veículos através de tecnologias sem fios.

**Outros Players**

Existem ainda uma série de players importantes neste ecossistema. Empresas como a General Electric, Ford, Apple and AT&T, Inter, Google, Microsoft Corp. e International Business Machines Corp fazem parte desse grupo de players no mercado IoE.

### 3.2. Visão de Consultoras

Nesta secção iremos apresentar a visão de duas empresas consultoras de tecnologias da informação, aproveitando para mostrar a visão de cada uma, bem como os resultados dos estudos efetuados pela Gartner sobre a temática Internet of Everything e posteriormente os da IDC (International Data Corporation).

**Gartner**

De acordo com a Gartner, a digitalização mudará por completo o mercado da tecnologia através do Internet of Things (things, people, places and systems). Na Europa, Médio Oriente e África o investimento em tecnologias de informação irá provocar um crescimento medio anual de 2.2% até 2017, a IoT irá criar novos mercados e uma nova economia.

Os investigadores da Gartner estão a avaliar o futuro do mundo digital e, pelos seus estudos, concluíram que em 2009 havia 2.5 mil milhões de dispositivos conectados à Internet e que na sua maioria eram telemóveis, PCs e tablets. Concluíram também que em 2020 haverá 30 mil milhões de dispositivos de diversas variedades conectados à Internet (Figura 12).
Esta consultora prevê que o valor económico máximo que o IoT irá adicionar ao mercado é de 1.9 biliões de dólares em 2020, distribuídos por inúmeras indústrias. Os sectores que estão a adoptar estas soluções são: Manufatura (15%), Saúde (15%) e Seguros (11%).

| ![](/img/iot13.png) |
| :--: |
| **Figura 12:** Número de dispositivos conectados, em unidades de mil milhões. Fonte: Gartner (Novembro 2013). |

Por exemplo, o sector de Manufatura irá beneficiar deste tipo de soluções através do uso de milhares de dispositivos que permitem fazer um controlo mais eficiente dos materiais e outros componentes e que se traduzem numa melhor relação custo-beneficio. No sector da saúde, chinelos inteligentes com sensores e outros dispositivos portáteis para idosos que contêm sensores podem ajudar a detetar quedas, assim como, as condições de saúde dos pacientes. Neste caso, se algo estiver errado o dispositivo irá alertar o médico via correio electrónico e possivelmente irá prevenir a queda do idoso e uma deslocação ao local por parte do médico. Outro exemplo bastante real no futuro passa por colocar sensores nos carros e proporcionar seguros de acordo com o perfil do condutor.

Quando se trata do assunto dos negócios, a IoE irá reinventar as indústrias em três níveis distintos: processo de negocioção, modelo de negócio e o momento do negócio.

* Processo de negociação: A tecnologia digital está a melhorar os produtos, serviços e processos, experiencia dos clientes e a maneira como as pessoas trabalham nas empresas e com os parceiros.

* Modelo de negócio: À medida que as empresas digitalizam produtos e processos, novas formas de fazer negócios surgem. Os analistas da Gartner esperam mais transformações ao nível do modelo de negócio à medida que a digitalização reinventa as indústrias. Empresas como a Nike e Google estão a reinventar-se, apresentando produtos como roupas que monitorizam os sinais vitais e veículos autónomos, respetivamente.

* Momento do negócio: Terceiro nível da reinvenção digital e é criado pela necessidade de competir pelo facto de haver uma maior agilidade e velocidade na concretização de negócios hoje em dia.

As empresas precisam de um plano de liderança digital que reconheça as inúmeras oportunidades de novos modelos de negócio, podendo criar liberdade e agilidade para concretizar momentos de negócio e estender-se a ela própria para ultrapassar barreiras que levem a transformar o ecossistema.

**IDC**

A IDC publicou uma análise sobre o mercado da IoT que prevê que as tecnologias e serviços inerentes a este conceito vão gerar 8,9 biliões de dólares em 2020.

As soluções IoT irão incluir tecnologias de informação e comunicação, vendedores de hardware, SP (Service Providers) e integradores de sistemas tanto para o sector privado como público. Os países desenvolvidos serão os primeiros a beneficiar de muitas das tecnologias utilizadas por soluções IoT, mas os países em desenvolvimento irão rapidamente contribuir para as receitas.

Segundo a IDC, o crescimento deste mercado será impulsionado pelo desenvolvimento de produtos inteligentes usados pelos consumidores todos os dias, assim como o desenvolvimento da infraestrutura. Ao criar uma cultura mais ligada, irá ser melhorado a conectividade entre diferentes componentes, ligando Smart Cities, casas, automóveis e outros produtos.

A IDC espera que em 2020 cerca de 212 mi milhões de objetos estejam ligados entre si, incluindo 30.1 mil milhões de objetos autónomos. Por esta data veremos instalados sistemas inteligentes que recolhem dados e usando aplicações de para o mercado de massas e empresarial.

Embora a tecnologia proporcione muitas oportunidades nos próximos anos, alguns problemas podem impedir o crescimento deste mercado. Estes obstáculos terão de ser ultrapassados pelas empresas e pelos próprios fornecedores, sendo que alguns dos desafios aparecerão do lado da oferta, segundo a IDC. Estes desafios devem-se a falta de standards, escalabilidade global e um ecossistema de desenvolvimento de aplicações pouco definido. É importante perceber que as industria têm pouca experiencia nesta área e é inevitável a instalação de um ambiente de comunicação sem fios. De notar que a tecnologia sem fios é essencial para usar os recursos do planeta de uma forma mais eficiente, num mundo em que a população está a crescer exponencialmente.

### 3.3. Potenciais Parceiros

Para potenciar soluções IoE e alavancar o negócio da Novabase, é importante perceber de que forma se vai enfrentar o mercado e que soluções se vão implementar tendo em consideração a satisfação da necessidade do cliente e do retorno de investimento.

Para tal é necessário constituir uma rede de parceiros que esteja estrategicamente posicionada dentro do mercado IoE. Do ponto de vista de avaliação e seleção dos parceiros, definimos parâmetros (pontos-chave) que os parceiros devem conter: experiência no desenvolvimento e entrega da solução tecnológica, referências em projetos com alguma dimensão e estabilidade financeira.

Depois de uma avaliação apresentamos de seguida alguns parceiros que podem ser fundamentais para esta área:

* **Cisco:** É uma empresa parceira da Novabase, pelo que faz todo a sentido desenvolver projetos IoE com a mesma. Cisco é um grande e importante player no mercado de redes e comunicações destacando- se a oferta de routers e switches. Apresenta também plataformas de colaboração de vídeo e VoIP. No contexto IoE, esta empresa apresenta um estudo intensivo sobre tecnologias, economia e sectores, tendo já implementado, com ajuda de parceiros, diversos pilotos que foram bem sucedidos. Entre outros, alguns exemplos passam por implementação de soluções IoE para Smart Cities em Barcelona, Nova Iorque e Nice. A Cisco é uma empresa parceira fundamental para a Novabase na implementação e/ou atualização da infraestrutura de rede, desde o Acesso até o Data Center, passando pela Core e pela Edge, de operadores, empresas do sector da energia, e outras que tenham uma infraestrutura de rede. Em adição, a Cisco tem uma plataforma designada por CMX (Connected Mobile Experiences) que permite explorar o estilo de vida conectado aos dispositivos e oferece conteúdos móveis relevantes através da análise de informações. Através do uso da rede sem fios Cisco e do uso da inteligência de localização fornecida pelo Mobility Services Engine (MSE), CMX ajuda a criar experiencias personalizadas para os utilizadores finais e aumentar a eficiência operacional.

* **ISA (Intelligent Sensing Anywhere):** É uma empresa portuguesa de base tecnológica com experiencia de mais de 20 anos em soluções de machine-to-machine para Smart Cities, abrangendo desenvolvimento de hardware e software. ISA é especializada nas áreas de Energy e Oil & Gas. A empresa está presente em França, Espanha, Brasil, EUA e Egito e já desenvolveu sistemas electrónicos de aquisição de dados para clientes a nível mundial, nomeadamente para a Agencia Espacial Europeia e para laboratórios multinacionais industriais. Alguns dos seu principais clientes são: BP, Shell, Galp Energia, Primagaz e Repsol YPF que usam soluções de telemetria com o objectivo de reduzir os custos e melhorar o serviço de cliente.

* **Urbiotica:** É uma empresa baseada em Barcelona cuja soluções desenvolvidas são projetadas especificamente para integrar o meio existente. Os sensores e dispositivos de comunicação desenvolvidos por esta empresa são robustos e de baixo consumo energético e de baixo impacto visual. Para além disso tem uma plataforma de gestão de dados, do tipo cloud, que é completamente modular e adaptável a cada cliente. 

    Algumas das soluções que a Urbiotica tem a disposição são:

    * **Sensores**: Smart Parking sensor, Waste Container Fill Level sensor, Smart traffic sensor, Acoustic and Air Quality sensors, entre outros.
    * **Transmissão de dados:** Urban Multisensor Network Router, Urban Multisensor Network Gateway e Solar Power Supply.
    * **Plataformas:** Internet of Things software platform e Device management cloud-based application.

    Esta empresa desenvolveu um projeto em Nice (França) que tinha como objetivo a simplificação da mobilidade na cidade. Colocaram mais de 10 mil sensores em lugares de estacionamento, reduziram o custo de operação em 30% e conseguiram reduzir a poluição e congestão em 10%.

    Em suma, em Barcelona instalaram sensores de monitorização dos caixotes de lixo e em Espanha colocaram sensores de trafego rodoviário no qual instalaram mais de 60 pontos de medição de trafego, conseguiram detetar mais de 30 mil veículos por dia e, com base nas informações recolhidas pelos sensores, fizeram alterações no planeamento do trafego.

* **Philips:** é uma empresa com atividade diversificada, mas centrada em melhorar a qualidade de vida das pessoas através da inovação nas áreas de Saúde, Consumo e Iluminação. Philips pode tornar-se uma parceira interessante para a Novabase para implementação de soluções de iluminação pública e melhorar a gestão deste serviço diminuindo a consumo energético. Esta empresa esteve envolvida no projeto de Smart Cities de Barcelona, onde se desenvolveu um piloto de iluminação pública.

* **JCDecaux:** é líder mundial em comunicações do exterior, estando presente em 5 continentes e em mais de 50 países. Esta envolvida no projeto Smart Cities de Barcelona e para esta empresa a inovação é um ponto de alavancagem de negócio. Nesse sentido, a empresa torna-se uma parceira interessante para a NB no sentido em que se pode implementar soluções IoE associadas à publicidade. JCDecaux tem como produtos: Mobiliário Urbano, Grande Formato e Aeroportos.

Outas potenciais parcerias estão neste momento a ser avaliadas.

### 3.4. Mercado Africano
Dentro desta secção iremos discutir a importância ou não, do mercado Africado para implementar soluções IoE.
À data do documento, não se encontrou informação concreta e relevante sobre o potencial mercado IoE na África emergente. Porém, segundo a análise do estudo feito e conjugando as informações da Cisco e da IDC, consegue-se concluir que será difícil implementar soluções deste tipo nos países emergentes de África. O rápido crescimento desta ideia vai passar pelos EUA, Europa e China.

Contudo, uma solução de bilhética desenvolvida pela Novabase e que já está implementada em alguns países será interessante e poderá ser um ponto de partida nos países como Moçambique, Gana e Angola.

## Capítulo 4

### 4.1. Visões

A Novabase, numa primeira fase, pretende criar um grupo de trabalho, para estudar as diferentes soluções IoE emergentes, estudar o seu potencial de negócio e criar Forums de debates, artigos, e apresentações com o objectivo de influenciar as pessoas. Numa fase posterior, expandir o grupo de trabalho e abraçar os parceiros e clientes interessados para a criação de demos, pilotos com o intuído de fazer um PoC (Proof of concept).

Do ponto de vista macroeconómico, a Novabase poderá usufruir desta nova transformação tecnológica ao posicionar-se junto dos grandes players e ao desenvolver projetos em parceria com empresas estratégicas do ponto de vista tecnológico. A alavancagem do negócio poderá passar por usar soluções já existentes dentro ou fora da empresa e adapta-las para esta realidade. Como factor diferenciador, e do ponto de vista administrativo e operacional, deverá criar a sua própria estratégia. Do ponto de vista tecnológico deverá criar a sua própria analítica ganhando vantagem competitiva em relação aos concorrentes.

### 4.2. Conclusões

Num mundo onde a mudança é cada vez mais rápida é extremamente importante estar preparado e atendo para o futuro. Por causa da tremenda transformação e disrupção que a Internet of Everything irá criar, não é cedo para planear soluções e modelos de negócios num mundo onde as pessoas, informações, processos e objetos estarão mais ligados que nunca.
Em conclusão, coloca-se algumas questões que são de facto críticas para desenvolver soluções e fazer negócios IoE:

* Como definir prioridades para usufruir das oportunidades que IoE irá criar?
* Dado o impacto que a Internet tem tido nos negócios, o que irá acontecer quando novas categorias de objetos se conectarem a uma taxa exponencial?
* Quais são os benefícios e potenciais riscos do IoE para os negócios e para as organizações governamentais?
* Como é que as organizações se devem posicionar em torno da informação e dos processos?

Encontrar respostas a estas e outras questões é fundamental com o intuito de preparar o ecossistema existente para a nova transição tecnológica.

## Bibliografia

[1] D. Evans, “The Internet of Things - How the Next Evolution of the Internet is Changing Everything,” Cisco, 2011.

[2] D. Evans, "The Internet of Everything - How More Relevant and Valuable Connections Will Change the World," Cisco IBSG, 2012.

[3] D. Evans, “Answering the Two Most-Asked Questions About the Internet of Everything,” Cisco, [Online]. Disponível em: http://blogs.cisco.com/ioe/answering-the-two-most-asked-questions-about-the-internet-of-everything/. [Acedido em 15 Abril 2014].

[4] J. Barbier, P. K. Bhatia e D. Kapoor, “Internet of Everything in ASEAN,” Cisco, 2014.

[5] Cisco, “The Internet of Everything - Global Public Sector Economic Analysis,” Cisco, 2013.

[6] J. Bradley, J. Barbier e D. Handler, “Embracing the Internet of Everything To Capture Your Share of $14.4 Trillion,” Cisco, 2013.

[7] Cisco, “The Internet of Everything for Cities - Point of View,” Cisco, 2013.

[8] J. Bradley, J. Loucks, J. Macaulay e A. Noronha, “Internet of Everything (IoE) Value Index,” Cisco, 2013.

[9] Cisco, “Cisco Connected Roadways,” Cisco, [Online]. Disponível em: http://www.cisco.com/web/strategy/transportation/roadways.html. [Acedido em 17 Abril 2014].

[10] Cisco, “Connected Mobile Experiences,” Cisco, [Online]. Disponível em: http://www.cisco.com/c/en/us/solutions/enterprise-networks/connected-mobile-experiences/index.html. [Acedido em 2014 Abril 18 ].

[11] IBM, “Smarter Cities,” IBM, [Online]. Disponível em: http://www.ibm.com/smarterplanet/us/en/smarter_cities/overview/. [Acedido em 18 Abril 2014].

[12] Qualcomm, “Internet of Everything,” Qualcomm, [Online]. Disponível em: http://www.qualcomm.com/solutions/ioe. [Acedido em 19 Abril 2014].

[13] Gartner, “Gartner Says Personal Worlds and the Internet of Everything Are Colliding to Create New Markets,” Gartner, [Online]. Disponível em: http://www.gartner.com/newsroom/id/2621015. [Acedido em 28 April 2014].

[14] F. Griffin, “IDC Forecasts $8.9 Trillion Internet of Things Market by 2020,” [Online]. Disponível em: http://machine-to-machine-solutions.tmcnet.com/topics/machine-to-machine-solutions/articles/355763-idc-forecasts-89-trillion-internet-things-market-2020.htm. [Acedido em 28 April 2014].

[15] Cisco, “Cisco,” [Online]. Disponível em: http://www.cisco.com/. [Acedido em 28 April 2014].

[16] ISA, “ISA - Intelligent Sensing Anywhere,” [Online]. Disponível em: http://www.isasensing.com/pt/. [Acedido em 28 April 2014].

[17] Urbiotica, “Urbiotica,” [Online]. Disponível em: http://www.urbiotica.com/. [Acedido em 28 April 2014].

[18] Philips, “Philips,” [Online]. Disponível em: http://www.philips.pt/. [Acedido em 28 April 2014].

[19] JCDecoux, “JCDecoux,” [Online]. Disponível em: http://www.jcdecaux.pt/home. [Acedido em 28 April 2014].

[20] “Soluções de Bilhética da Novabase em foco na Expotrans Angola 2012,” [Online]. Disponível em: http://www.novabase.pt/pt/Liga/press-zone/Nas-Noticias/Pages/Solu%C3%A7%C3%B5es-de-Bilh%C3%A9tica-da-Novabase-em-foco-na-Expotrans-Angola-2012-.aspx. [Acedido em 29 April 2014].

[21] CloudTimes, “Gartner: Internet of Things will Grow Exponentially to 26 Billion Devices by 2020,” CloudTimes, [Online]. Disponível em: http://cloudtimes.org/2013/12/20/gartner-the-internet-of-things-will-grow-30-times-to-26-billion-by-2020/. [Acedido em 20 Abril 2014].
