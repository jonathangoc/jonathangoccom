---
title: "Network Functions Virtualization (NFV) - Arquitetura"
date: 2015-08-18T16:45:00+00:00
draft: false
layout: "single"
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
cover:
    image: "/img/nfv5.png"
    responsiveImages: true
    hidden: true
tags: ["tech", "novabase", "etsi", "virtualisation", "Network Functions Virtualization", "nfv"]
categories: ["Tech", "NFV"]
---

# Índice
1. [Âmbito](#1.0)
2. [Sumário Executivo](#2.0)
    1. [Estrutura do Documento](#2.1)
    2. [Objetivos da virtualização de funções de rede (NFV)](#2.2)
    3. [Descrição da abordagem do ETSI](#2.3)
3. [Framework NFV](#3.0)
    1. [Introdução](#3.1)
    2. [Descrição de alto nível da framework NFV](#3.2)
4. [Serviços de Rede No Contexto NFV](#4.0)
    1. [Virtualização dos Blocos Funcionais]((#4.1))
    2. [Implicações no NFV](#4.2)
5. [Arquitetura Detalhada Da Framework NFV](#5.0)
    1. [Introdução](#5.1)
    2. [Visão Geral dos Blocos Funcionais da Arquitetura NFV](#5.2)
    3. [Virtualised Network Function (VNF)](#5.3)
    4. [Element Managament (EM)](#5.4)
    5. [NFV Infrastructure](#5.4)
    6. [Virtualised Infrastructure Manager(s)](#5.6)
    7. [NFV Orchestrator](#5.7)
    8. [VNF Manager(s)](#5.8)
    9. [Service, VNF and Infrastructure Description](#5.9)
    10. [Operations and Business Support Systems (OSS/BSS)](#5.10)
    11. [Interfaces de Referência](#5.11)
6. [Conclusão e Trabalho Futuro](#6.0)
    1. [Conclusão](#6.1)
    2. [Trabalho Futuro](#6.2)
7. [Bibliografia](#7.0)


## 1. Âmbito <a id="1.0"></a>

O presente documento introduz a arquitetura conceptual de alto nível da virtualização de funções de rede (NFV) definida pelo European Telecommunications Standards Institute (ETSI) no Group Specification NFV 002 v1.2.1. Adicionalmente, descreve a infraestrutura, blocos funcionais e interfaces, assim como a ligação e suporte desta arquitetura.

Através deste documento, pretende-se mostrar ao leitor os fundamentos do NFV. 

Pela sua própria essência este estudo é orientado para a rede dos operadores de telecomunicações.

## 2. Sumário Executivo <a id="2.0"></a>

### 2.1. Estrutura do Documento <a id="2.1"></a>

O presente documento está estruturado da seguinte forma:

- O **Capítulo 2** apresenta o âmbito e objetivos da virtualização de rede. Adicionalmente descreve a abordagem do ETSI no contexto do NFV.
- O **Capítulo 3** introduz os conceitos mais importantes no processo de virtualização e descreve genericamente a arquitetura NFV e blocos funcionais propostos pelo ETSI.
- O **Capítulo 4** aborda o tema dos serviços de rede num ambiente NFV e as suas implicações.
- O **Capítulo 5** apresenta detalhadamente a framework do NFV e descreve os blocos constituintes assim como as interfaces de interação entre estes.
- Por fim, o **Capítulo 6** conclui o presente documento e especifica o trabalho que a se pretende realizar no futuro.


### 2.2. Objetivos da virtualização de funções de rede (NFV) <a id="2.2"></a>

De uma forma geral, o NFV tem como principais objetivos:

- Redução de custos quando comparado com implementações em que o hardware é dedicado, ou seja, através do uso de equipamento disponível no mercado hoje em dia (ex. servidores e equipamentos de armazenamento) e aplicando técnicas específicas de virtualização é possível desenvolver funções de rede com base em software. Estas funções de rede são designadas por funções de rede virtualizadas (VNFs – Virtualised Network Functions). Consequentemente, a partilha de hardware e a redução do número de arquiteturas leva a uma redução de custos.
- Aumento de flexibilidade ao implementar VNFs e que se traduz em maior escalabilidade. Isto permite que as funcionalidades da rede sejam desagregadas do local onde se encontram e que sejam implementadas no local da rede mais apropriado (nas premissas do cliente, no data center, no central office, etc). Este tipo de flexibilidade permite o reuso das funções de rede, maior suporte durante a fase de testes, melhoria da resiliência através da virtualização e maior partilha dos recursos.
- Rápida inovação de serviços através da implementação dos mesmos a partir de software.
- Maior eficiência operacional resultante de processos de automação e operação.
- Redução dos custos energéticos através do balanceamento de cargas e adaptação da energia com base no uso efetuado pelo hardware.

### 2.3. Descrição da abordagem do ETSI <a id="2.3"></a>

Segundo o ETSI, as redes de telecomunicações são constituídas por diferentes funções de rede. Estas funções de rede estão ligadas entre si de forma a criar uma determinada funcionalidade ou serviço e para o qual a rede foi desenhada. Na sua maioria, os serviços de redes de telecomunicações são definidos com base em funções de rede estáticas e que podem ser representados por diagramas designados por Network Function Forwarding Graph (NF Forwarding Graph). 

> **Note:** NF Forwarding Graph designa o diagrama lógico das ligações entre nós NF com o intuito de representar o fluxo de tráfego entre funções de rede.

O maior avanço tecnológico é o facto da virtualização, no contexto do NFV, disponibilizar métodos dinâmicos para criar e gerir as funções de rede e os fluxos de tráfego entre eles. Com isto, o conceito de NFV foca-se em explorar a criação e gestão dinâmica do conjunto de funções de rede e da sua interação com o plano de dados, controlo e de gestão. A título de exemplo, o NF Forwarding Graph foca-se nas relações entre funções de redes no que diz respeito à sua conectividade e aos aspectos introduzidos pela sua virtualização.

Para além disso, os serviços de rede do futuro serão diferentes dos atuais. Para se ter uma ideia, esses serviços irão incluir uma diversidade de funções de rede não-virtuais e virtuais, sendo esta última suportada por uma infraestrutura de rede e capacidade de computação virtualizada. Ao conjugar estes dois domínios (o virtual e o não-virtual) haverá a necessidade de interoperabilidade entre ambos.

Os atributos dos serviços, em particular fiabilidade, disponibilidade, segurança e desempenho, dependerão das capacidades individuais das funções de rede virtualizadas e da forma como essas funções estão ligadas. Esses atributos estão dependentes uns dos outros pelo que é importante a concepção de uma arquitetura que suporte a grande diversidade de funções de rede que potencialmente podem ser virtualizadas.

O ETSI tem-se dedicado ao estudo e desenvolvimento de uma arquitetura e dos elementos constituintes que permita implementar o conceito de NFV de uma forma normalizada e que possibilite interoperabilidade. Através desta abordagem, diferentes funções de rede virtualizadas podem ser implementadas sobre um ambiente de virtualização com o objetivo de suportar serviços end-to-end (E2E). E que adicionalmente, possa ser aplicado aos diferentes cenários de rede de um operador de telecomunicações, diminuindo o esforço de configuração e integração

Para o grupo de trabalho, dedicado ao NFV dentro do ETSI, a virtualização significa que parte da infraestrutura de rede e as funções integrantes são implementadas em software, e como tal, a criação de uma arquitetura NFV é um aspeto importante para a construção de uma framework de trabalho.

## 3.0. Framework NFV <a name="3.0"></a>

### 3.1. Introdução <a name="3.1"></a>

Geralmente em redes não-virtualizadas, as funções de rede são implementadas com base numa combinação de software/hardware de um fabricante específico e que muitas vezes são designados por nós rede ou elementos de rede.

O NFV representa uma inovação para os apaixonados pelas redes de telecomunicações, introduzindo várias diferenças comparativamente à forma como os serviços são provisionados. Algumas dessas diferenças são:

- Separar software do hardware: permite que o software tenha uma linha de evolução diferente e separada da do hardware. Assim, a evolução de ambos é independente.
- Implementação flexível das funções de rede: a desagregação do software do hardware ajuda a reatribuir e a partilhar os recursos da infraestrutura física e assim cada uma das componentes pode desempenhar funções diferentes. Assumindo que o conjunto de recursos físicos se encontra instalado num determinado Network Functions Virtualization Infrastructure Point-of-Presence (NFVI-POP), o processo de instanciação de funções de rede pode tornar-se mais mecânico. Isto permite aos operadores de redes implementar, sobre a mesma plataforma física, novos serviços de rede.
- Operação dinâmica: ao separar as funcionalidades das funções de rede em componentes capazes de serem instanciadas permitirá maior escalabilidade, dinamismo e ainda maior desempenho das VNFs. Por exemplo, permite ajustar dinamicamente o desempenho da VNF de acordo com o padrão de tráfego.

De acordo com o que foi descrito anteriormente, de seguida apresenta-se a framework NFV que se baseia nos seguintes pressupostos:

- Suportar um grande número de serviços de rede com diferentes níveis de fiabilidade e disponibilidade, alavancando novas técnicas de virtualização.
- Assegurar que a virtualização não provoca novas ameaças de segurança.
- Minimizar o impacto da interoperabilidade entre as funções de rede virtualizadas e não-virtualizadas.
- Alavancar tecnologia existente no Data Center.

As funções de redes incorporam diferentes aspetos que muitas vezes estão associados à componente física ou virtual e que não são abordados neste documento.

### 3.2. Descrição de alto nível da framework NFV <a name="3.2"></a>

O NFV prevê a implementação de funções de rede como entidades baseadas em software e que operam sobre a infraestrutura de NFV designada por NFV Infrastructure (NFVI). A figura seguinte ilustra a framework aqui apresentada.

| ![](/img/nfv1.png) |
| :--: |
| **Figura 1:** Blocos constituintes da Framework NFV.  |

A framework NFV apresenta três grandes domínios:

- **Virtualised Network Functions (VNFs)** que corresponde à implementação de funções de rede em software e que tem a capacidade de operar sobre o domínio NFVI.
- **NFV Infastructure (NFVI)** é composta pela grande diversidade de recursos físicos existentes, assim como, a sua virtualização através da camada intermédia. Este domínio suporta as VNFs.
- **NFV Management and Orchestration** corresponde a todos os processos e tarefas específicos da gestão da virtualização. Este domínio abrange ainda o processo de orquestração e de gestão do ciclo de vida do hardware e software que suportam a infraestrutura de virtualização.

Esta framework permite a gestão dinâmica das VNFs e a criação de relações entre elas e o plano de dados, bem como, controlo e gestão das suas dependências.

Com base em diferentes perspetivas e de acordo com determinados contextos, esta framework pode permitir:

- Implementar e integrar máquinas virtuais sobre um ambiente de virtualização;
- Utilizar um conjunto de programas/aplicações de um determinado fabricante que pode incluir várias máquinas virtuais interligadas e templates de implementação que definem os atributos;
- Ou ainda, operar e gerir VNFs, que do ponto de vista do operador, podem ser adquiridas através de um programa/aplicação.

De acordo com as utilizações acima mencionadas, existe a seguinte relação entre VNFs:
- VNF Forwarding Graph (VNF-FG) representa as ligações entre VNF que estão especificadas, como por exemplo: VNFs ligadas em cascata formando um caminho até à camada de web server (firewall, NAT, load balancer).
- VNF Set representa as ligações entre VNFs que não estão especificadas (ex. conjunto de web server).

De seguida apresenta-se os blocos funcionais dos serviços de rede e a sua associação com os gráficos VNF-FG. Pretende-se assim clarificar o leitor para o facto de que os serviços de rede end-to-end (ex. Internet, VPN, dados móveis e voz) podem ser descritos por um gráfico do tipo NF Forwarding Graph.

## 4.0. Serviços de Rede No Contexto NFV <a name="4.0"></a>

### 4.1. Virtualização dos Blocos Funcionais <a name="4.1"></a>

Do ponto de vista do desenho da arquitetura, os serviços de rede podem ser vistos como um gráfico de encaminhamento constituído por funções de rede (NFs) interligados através de uma infraestrutura física. Estas funções de rede podem ser implementadas na rede de um operador de telecomunicações ou em redes de operadores distintos. A forma como as funções de rede operam influência o desempenho dos serviços de alto nível e por conseguinte, o desempenho dos serviços de rede tornam-se numa combinação de procedimentos dos seus blocos funcionais, que podem incluir NFs individuais, um conjunto de NFs, gráficos de encaminhamento NFs e/ou a própria infraestrutura de rede.

Os end points e as funções de rede de um determinado serviço são representados como nós de rede e que podem corresponder a dispositivos, aplicações e/ou servidores físicos. Num gráfico de encaminhamento de serviços as ligações lógicas podem ser unidirecionais, bidirecionais, ligações em multicast e/ou broadcast.

A Figura 2 apresenta um serviço de rede end-to-end que inclui no centro uma representação de um NF Forwarding Graph formado pelas NF 1, NF 2 e NF 3, ligadas logicamente. Os end points estão ligados aos NFs através de uma infraestrutura física (wireless ou wired), resultando assim numa ligação lógica entre os dois. Essas ligações lógicas estão representadas por uma linha tracejada.

| ![](/img/nfv2.png) |
| :--: |
| **Figura 2:** Representação gráfica de um serviço de rede ponto-a-ponto.  |

A Figura 3 ilustra o detalhe de um serviço de rede end-to-end e as diferentes camadas que estão envolvidas no processo de virtualização. Neste exemplo, a arquitetura que suporta o serviço de rede é formado por VNFs e dois end points. A camada de virtualização é responsável por desagregar o software do hardware, originando uma camada de abstração entre o sofware e os recursos físicos.

Os NFVI-PoPs representam os recursos físicos instalados pelo operador (computation, storage e networking).

Como se pode observar na Figura 3, as funções de rede virtualizadas (VNFs) operam sobre a camada de virtualização, que é uma componente integrante do NFV Infrastructure. O gráfico VNF Forwarding apresentado na Figura 2 também está incluído na ilustração abaixo apresentada. Neste caso específico verifica-se que existe um aglomerado de VNFs designado por VNF-FG-2 e que é composto por VNF-2A, VNF-2B e VNF-2C. Pretende-se assim demonstrar que as interfaces entre funções de rede físicas ou virtuais e a própria infraestrutura de rede num ambiente multi-vendor devem ser baseados em standards.

| ![](/img/nfv3.png) |
| :--: |
| **Figura 3:** Exemplo de um serviço ponto-a-ponto com VNFs e um aglomerado de VNF-FG.  |

### 4.2. Implicações no NFV <a name="4.2"></a>

A criação de modelos de serviços de rede end-to-end através de técnicas de virtualização pressupõe a introdução de funcionalidades adicionais. O ETSI identifica modelos de serviços aplicáveis no contexto NFV e os requisitos de implementação e operação desses modelos. Porém, este tema está fora do âmbito do presente documento.

## 5.0 Arquitetura Detalhada Da Framework NFV <a name="5.0"></a>

### 5.1. Introdução <a name="5.1"></a>

A arquitetura da framework NFV baseia-se nas mudanças que poderão ter que acontecer numa rede de operador devido aos processos de virtualização das funções de rede. É por isso que o ETSI continua a focar os seus esforços em desenvolver uma framework que se baseia em novos blocos funcionais e pilares de referência. De seguida apresenta-se os blocos da arquitetura NFV.

### 5.2. Visão Geral dos Blocos Funcionais da Arquitetura NFV <a name="5.2"></a>

A framework NFV identifica de forma clara os blocos funcionais e principais interfaces de referência entre os blocos. Posto isto, apresenta-se os blocos funcionais:

- Virtualised Network Function (VNF);
- Element Management (EM);
- NFV Infrastructure, que inclui:
    - Recursos Físicos (Hardware),
    - Virtualisation Layer e Recursos virtualizados,

- Virtualised Infrastructure Manager(s);
- NFV Orchestrator;
- VNF Manager(s);
- Service, VNF and Infrastructure Description;
- Operations and Business Support Systems (OSS/BSS).


A Figura 4 ilustra a arquitetura de referência do NFV, os seus blocos funcionais e as interfaces de interação entre eles. Nesta figura, considera-se que as linhas sólidas que ligam alguns dos blocos funcionais correspondem as interfaces de referência mais importantes e que estão no âmbito do estudo feito pelo ETSI no contexto do NFV.
Esta arquitetura foca-se nas funcionalidades necessárias para a virtualização e consequentemente para a operação da rede do operador de telecomunicações. Segundo o ETSI, esta framework não especifica quais as funções de rede que devem ser virtualizadas, cabendo assim esta tarefa ao operador de telecomunicações, em conjunto com os seus parceiros (integradores e fabricantes), de analisar e decidir quais as funções de rede podem ou devem ser virtualizadas com base em requisitos tecnológicos e/ou de negócio.

| ![](/img/nfv4.png) |
| :--: |
| **Figura 4:** Arquitetura de referência do NFV.  |

Os subcapítulos seguintes descrevem sucintamente cada um dos blocos funcionais.

### 5.3. Virtualised Network Function (VNF) <a name="5.3"></a>

A virtualização de funções de rede é, como o próprio nome indica, abstrair funções de rede implementadas num equipamento físico, que estão profundamente interligadas, e virtualiza-las na própria rede. A título de exemplo, funções de rede como Mobility Management Entity (MME), Serving Gateway (SGW) e Packet Data Network Gateway (PGW) podem ser virtualizadas. Outros exemplos são: servidores de Dynamic Host Configuration Protocol (DHCP), firewalls e Residential Gateways (RGWs).

O ETSI alega que os modos de funcionamento das funções de rede não estão dependentes da forma como são implementados, isto é, se são implementadas fisicamente ou virtualmente. É espectável que o modo de funcionamento e o desempenho das interfaces externas das funções de rede física e das funções de rede virtuais venham a ser iguais.

Uma VNF pode ser constituída por várias componentes. Por exemplo, uma VNF pode ser implementada em diferentes máquinas virtuais onde cada uma destas máquinas virtuais acomoda uma das componentes da VNF. No entanto, a mesma VNF pode ser instanciada na mesma máquina virtual.

### 5.4. Element Managament (EM) <a name="5.4"></a>

O Element Management é responsável pela gestão de uma ou variais VNFs.

### 5.5. NFV Infrastructure <a name="5.4"></a>

**Definição de NFV Infrastructure**

A Infraestrutura NFV ou NVF Infrastructure corresponde a todas as componentes de hardware e software que permitem criar o ambiente necessário para implementar, gerir e manter VNFs. Esta infraestrutura pode estar espalhada pelas diferentes NFVI-PoPs.

Do ponto de vista das VNFs, a camada de virtualização e os recursos físicos apresentam-se como uma entidade única fornecendo os recursos virtuais necessário ao funcionamento da VNF.

**Recursos Físicos (Hardware)**

No âmbito do NFV, os recursos físicos incluindo computação, armazenamento e recursos de rede, fornecem às VNFs computação, armazenamento e conectividade através da camada de virtualização. Assume-se que a capacidade de processamento seja fornecida por hardware genérico e não hardware dedicado e desenvolvido com o propósito de suportar uma determinada função de rede.

**Virtualisation Layer e Recursos virtualizados**

A camada de virtualização abstrai os recursos físicos e permite desagregar o software da infraestrutura física. Desta forma é possível garantir que o tempo de vida do hardware é distinto do software.

Em suma, a camada de virtualização é responsável por:

- Abstrair os recursos físicos;
- Permitir que as VNFs utilizem a infraestrutura virtualizada;
- Fornecer recursos virtuais às VNFs.

Como mencionado anteriormente, a Arquitetura de referência do NFV é apresentada na Figura 4. A camada de virtualização garante que as VNFs são dissociadas dos recursos de hardware e, portanto, o software pode ser implantado nos diferentes recursos físicos. Normalmente, este tipo de flexibilidade é fornecido por recursos de computação e armazenamento sob a forma de hypervisors e VMs.

Esta arquitetura permite o uso de qualquer solução de virtualização, pelo que, é expectável no contexto NFV seja utilizado camadas de virtualização com características e interfaces standard. Em alguns casos, as VMs podem ter acesso direto a recursos de hardware (por exemplo, interface de rede) para um melhor desempenho. No entanto, em NFV, VMs devem permitir abstrair os recursos físicos da rede.

### 5.6. Virtualised Infrastructure Manager(s) <a name="5.6"></a>

A gestão da infraestrutura virtualizada possui funcionalidades que são usadas para controlar e gerir a interação das VNFs com os recursos físicos da rede (computação, armazenamento e comunicação). Analisando a Figura 4 e tendo em consideração os recursos físicos especificados nesta arquitetura, o Virtualised Infrastructure Manager é responsável por:

- Fazer a gestão dos hypervisors, capacidade de processamento, comunicação e armazenamento dedicados à infraestrutura NFV;
- Alocar máquinas virtuais sobre os ambientes de virtualização disponíveis, capacidade de processamento, conectividade de rede e armazenamento para o efeito;
- Gerir os recursos da infraestrutura, ou seja, alocar mais capacidade de processamento às VMs (se necessário) e diminuir o consumo energético (quando possível).
- Dar visibilidade sobre os recursos disponíveis nesta infraestrutura NFV;
- Recolha de informação relevante para permitir um planeamento mais detalhado da infraestrutura, assim como, monitorizar e optimizar;
- Reportar falhas da infraestrutura.

Em suma, num ambiente NFV, vários Virtualised Infrastructure Manager podem ser implementados.

### 5.7. NFV Orchestrator <a name="5.7"></a>

O orquestrador NFV é responsável por orquestrar e fazer a gestão da infraestrutura NFV, das aplicações e dos serviços de rede.

### 5.8. VNF Manager(s) <a name="5.8"></a>

O Gestor de VNF tem como função gerir o tempo de vida das funções de rede virtualizadas, ou seja, instalar, atualizar, manter e desinstalar.

Vários Gestores de VNF podem ser instanciados para gerir várias VNFs ou apenas um Gestor de VNF pode ser instalado para gerir o conjunto de VNFs.

### 5.9. Service, VNF and Infrastructure Description <a name="5.9"></a>

Este conjunto de dados fornece informações sobre o modelo/template de implementação de VNF, informações relacionadas com o serviço e VNF Forwarding Graph. Estes modelos/templates são utilizados internamente na gestão e orquestração em NFV. Os blocos funcionais da Gestão NFV e Orquestração lidam diretamente com as informações contidas nos modelos/templates e têm a capacidade para disponibilizar essa informação se necessário.

### 5.10. Operations and Business Support Systems (OSS/BSS) <a name="5.10"></a>

As ferramentas de OSS e BSS estão ilustradas na arquitetura da Figura 4 e correspondem às ferramentas existentes na rede do operador de telecomunicações.

### 5.11. Interfaces de Referência <a name="5.11"></a>

As interfaces de referência entre os blocos funcionais da arquitetura NFV correspondem aos pontos de interação entre estes. O presente documento não detalha e/ou especifica as interfaces pelo que é importante ficar com a ideia de que as interfaces entre os blocos funcionais definem o modo como estes comunicam uns com os outros.

## 6.0. Conclusão e Trabalho Futuro <a name="6.0"></a>

### Conclusão <a name="6.1"></a>

O NFV apresenta-se como uma mudança de paradigma nas redes de telecomunicações, na sua operação e na sua gestão. O presente documento focou-se em demonstrar e explicar a arquitetura NFV proposta pelo ETSI, assim como, os seus blocos constituintes, interfaces de referência e da camada de virtualização.

A implementação bem-sucedida da arquitetura NFV ilustrada neste documento depende do desenvolvimento dos blocos funcionais e das interfaces de comunicação. À data do presente documento, existem tecnologias e soluções capazes de desempenhar as funções de cada bloco funcional descrito anteriormente. O poder de decisão, pelas escolhas de soluções que se enquadram na framework NFV, pertence ao Operador de Telecomunicações e que pode ter em consideração os requisitos técnicos e de negócio.

### Trabalho Futuro <a name="6.2"></a>

Como trabalho futuro, pretende-se explorar em detalhe da tecnologia NFV e estudar soluções existentes no mercado que refletem um ou vários blocos funcionais da arquitetura NFV.

## Bibliografia <a name="7.0"></a>

As referências apresentadas neste capítulo formam a base da criação do presente documento:

[1] ETSI GS NFV 001: "Network Functions Virtualisation (NFV); Use Cases".

[2] ETSI GS NFV 002: “Network Functions Virtualisation (NFV); Architectural Framework”.

[3] ETSI GS NFV 003: "Network Functions Virtualisation (NFV); Terminology for Main Concepts in NFV".

[4] ETSI GS NFV 004: "Network Functions Virtualisation (NFV); Virtualisation Requirements".