# PequiFlux — Documento Mestre do Projeto

## Índice
- [1. Identificação do projeto](#sec-1)
- [2. Finalidade deste documento](#sec-2)
- [3. Visão executiva](#sec-3)
- [4. Problema de pesquisa e de engenharia](#sec-4)
  - [4.1 Formulação conceitual do problema](#sec-4-1)
  - [4.2 Enquadramento do problema](#sec-4-2)
- [5. Proposta de solução](#sec-5)
- [6. Escopo do projeto](#sec-6)
  - [6.1 Escopo incluído](#sec-6-1)
  - [6.2 Escopo excluído no ciclo atual](#sec-6-2)
  - [6.3 Distinção entre ciclo financiado e visão de longo prazo](#sec-6-3)
- [7. Objetivo geral](#sec-7)
- [8. Objetivos específicos](#sec-8)
- [9. Hipóteses do projeto](#sec-9)
  - [9.1 Hipóteses de modelagem e desempenho](#sec-9-1)
  - [9.2 Hipóteses operacionais](#sec-9-2)
  - [9.3 Hipóteses de adoção e valor](#sec-9-3)
  - [9.4 Hipóteses de transição tecnológica](#sec-9-4)
- [10. Fundamentação técnico-científica e método de pesquisa](#sec-10)
  - [10.1 Protocolo experimental mínimo e critérios de aceitação](#sec-10-1)
  - [10.2 Premissas operacionais e limites de validade](#sec-10-2)
- [11. Arquitetura de alto nível](#sec-11)
  - [11.1 Camada de ingestão de dados](#sec-11-1)
  - [11.2 Camada de modelo e decisão](#sec-11-2)
  - [11.3 Camada de aplicação](#sec-11-3)
  - [11.4 Camada de governança](#sec-11-4)
  - [11.5 Atributos de qualidade e controle operacional](#sec-11-5)
- [12. Fontes de dados previstas](#sec-12)
  - [12.1 Dependências externas críticas e critérios de seleção de parceiros](#sec-12-1)
- [13. Artefatos a produzir](#sec-13)
- [14. Roadmap macro do projeto alinhado à DSRM e ao cronograma executivo](#sec-14)
  - [14.1 Macroetapa 1](#sec-14-1)
  - [14.2 Macroetapa 2](#sec-14-2)
  - [14.3 Macroetapa 3](#sec-14-3)
  - [14.4 Macroetapa 4](#sec-14-4)
  - [14.5 Macroetapa 5](#sec-14-5)
  - [14.6 Correspondência entre DSRM e cronograma executivo](#sec-14-6)
  - [14.7 Governança do roadmap e critérios de avanço](#sec-14-7)
- [15. Desafios críticos de execução, validação e transição](#sec-15)
  - [15.1 Desafios de modelagem e solução](#sec-15-1)
  - [15.2 Desafios de dados e evidência experimental](#sec-15-2)
  - [15.3 Desafios organizacionais e de governança](#sec-15-3)
  - [15.4 Desafios de mercado e narrativa de valor](#sec-15-4)
  - [15.5 Desafios de transição para validação futura em campo](#sec-15-5)
  - [15.6 Função metodológica da seção](#sec-15-6)
- [16. Estrutura de governança](#sec-16)
  - [16.1 Papéis centrais](#sec-16-1)
  - [16.2 Ritos de gestão](#sec-16-2)
  - [16.3 Documentos obrigatórios de governança](#sec-16-3)
- [17. Sistema de indicadores e critérios de acompanhamento](#sec-17)
  - [17.1 Indicadores técnicos](#sec-17-1)
  - [17.2 Indicadores de dados](#sec-17-2)
  - [17.3 Indicadores de execução](#sec-17-3)
  - [17.4 Indicadores de negócio e transição](#sec-17-4)
  - [17.5 Regras de uso dos indicadores nos stage-gates](#sec-17-5)
  - [17.6 Modelo de impacto socioambiental estimado e auditabilidade por proxies](#sec-17-6)
- [18. Riscos principais](#sec-18)
  - [18.1 Riscos técnicos](#sec-18-1)
  - [18.2 Riscos operacionais](#sec-18-2)
  - [18.3 Riscos de mercado](#sec-18-3)
  - [18.4 Riscos jurídicos e de compliance](#sec-18-4)
- [19. Estratégia de mitigação](#sec-19)
- [20. Política interna de decisão](#sec-20)
- [21. Estratégia documental do projeto](#sec-21)
  - [21.1 Matriz resumida de rastreabilidade metodológica](#sec-21-1)
  - [21.2 Versão completa como anexo vivo](#sec-21-2)
- [22. Próximas ações imediatas](#sec-22)  
- [23. Regra de manutenção do documento](#sec-23)
- [24. Encerramento](#sec-24)

<a id="sec-1"></a>

## 1. Identificação do projeto
**Nome do projeto:** PequiFlux — Orquestrador Dinâmico de Safra  
**Natureza:** SaaS B2B para orquestração algorítmica de filas e caminhões no agro  
**Contexto de origem:** Projeto estruturado inicialmente no Programa Centelha 3 Goiás  
**Horizonte atual:** Consolidação do artefato tecnológico, da operação de P&D e da preparação para validação externa e entrada comercial

<a id="sec-2"></a>

## 2. Finalidade deste documento
Este documento tem a função de formalizar, para uso interno da equipe, o que é o PequiFlux, qual problema ele resolve, qual solução será construída, quais hipóteses precisam ser validadas, quais entregas serão produzidas, quais riscos existem, como a equipe se organizará e quais decisões deverão orientar a execução daqui em diante. Trata-se do documento central de alinhamento técnico, estratégico e operacional do projeto.

<a id="sec-3"></a>

## 3. Visão executiva
O PequiFlux é uma solução orientada a dados para reduzir filas, espera, variabilidade operacional e ruído decisório no recebimento e expedição de caminhões em cooperativas, cerealistas, armazéns e agroindústrias. A proposta central é substituir a lógica predominantemente manual, baseada em planilhas, rádio, WhatsApp e FIFO rígido, por uma orquestração dinâmica do pátio, auditável, explicável e adaptativa.

No estado atual, o projeto se encontra em fase de formalização e organização pós-submissão da Fase 2 do Centelha. O próximo ciclo exige a transição do material de edital para um sistema interno de gestão do projeto, mais robusto, técnico e contínuo, capaz de orientar P&D, governança, validação, documentação, risco, arquitetura e estratégia de mercado.

<a id="sec-4"></a>

## 4. Problema de pesquisa e de engenharia
Em operações agroindustriais com alto fluxo de caminhões, a coordenação do recebimento e da expedição ocorre em ambiente dinâmico, sujeito à heterogeneidade de recursos físicos, restrições de capacidade, requisitos de qualidade da carga, prioridades contratuais e eventos disruptivos, como chuva, atrasos, indisponibilidade de equipamentos e oscilações no ritmo operacional. Quando tais decisões são conduzidas por regras estáticas ou por decisão humana fragmentada, emergem filas prolongadas, baixa previsibilidade, subutilização de recursos críticos, perda de eficiência sistêmica e aumento da variabilidade operacional.

Do ponto de vista científico, o problema consiste em modelar a orquestração do pátio como um problema dinâmico de escalonamento sob restrições, no qual a sequência de atendimento e a alocação de caminhões a recursos devem ser recalculadas à medida que o estado do sistema evolui.

Do ponto de vista de engenharia, o problema consiste em projetar e avaliar um artefato computacional capaz de representar o estado operacional do pátio, respeitar restrições rígidas, incorporar prioridades operacionais e produzir recomendações auditáveis, explicáveis e em tempo compatível com a operação.

**Pergunta de pesquisa:** Em que medida um motor de decisão baseado em otimização sob restrições e replanejamento orientado a eventos supera heurísticas estáticas, como FIFO e agenda fixa, em métricas de espera, throughput, estabilidade e auditabilidade em ambiente controlado?

**Pergunta de projeto:** Como projetar, implementar e validar um artefato tecnológico capaz de recomendar, em tempo quase real, qual caminhão chamar, para qual recurso direcionar e com qual justificativa operacional?

<a id="sec-4-1"></a>

### 4.1 Formulação conceitual do problema
Sejam **C** o conjunto de caminhões, **R** o conjunto de recursos operacionais do pátio, **T** o conjunto de instantes de decisão e **E** o conjunto de eventos operacionais. Os dados de entrada incluem, entre outros, tempo de chegada, tipo de veículo, tipo e qualidade da carga, prioridades contratuais, status documental, disponibilidade e capacidade dos recursos e eventos exógenos. As variáveis de decisão definem: (i) qual caminhão será chamado, (ii) a qual recurso será alocado e (iii) em qual instante operacional a decisão será executada.

O problema consiste em minimizar uma função-objetivo multicritério que combine makespan, tempo total de espera, espera em cauda, instabilidade de replanejamento e penalizações por violações de prioridades suaves, sujeito a restrições rígidas de compatibilidade carga-recurso, capacidade, janelas operacionais, segurança, qualidade, indisponibilidade de equipamentos e rastreabilidade de decisão.

De forma conceitual, a função-objetivo pode ser expressa como:

**min J = α1 · Makespan + α2 · Espera_total + α3 · Espera_p95 + α4 · Instabilidade + α5 · Penalizações**

sujeita às hard constraints do pátio e às regras operacionais parametrizadas do domínio.

<a id="sec-4-2"></a>

### 4.2 Enquadramento do problema
No contexto do PequiFlux, o problema será tratado como uma variação do **Flexible Job Shop Scheduling Problem (FJSSP)** sob incerteza e orientado a eventos, com necessidade de replanejamento em receding horizon. Esse enquadramento permite representar o pátio como sistema de decisão operacional com múltiplos recursos, heterogeneidade de processamento, restrições rígidas e eventos estocásticos que alteram continuamente a melhor sequência de atendimento.

<a id="sec-5"></a>

## 5. Proposta de solução
A solução proposta consiste em uma plataforma SaaS B2B com motor de decisão para orquestração de pátio em tempo quase real. O sistema consolida dados operacionais, aplica regras do negócio, respeita restrições rígidas, recalcula a fila diante de eventos e recomenda ao operador quem chamar, para onde direcionar e por quê.

A solução será concebida com operador humano no centro, fallback manual, trilha auditável e mecanismos de explicabilidade. A ingestão inicial deverá priorizar CSV e entrada assistida, preservando arquitetura preparada para evolução futura por API, ERP, balança e mensageria.

<a id="sec-6"></a>

## 6. Escopo do projeto
<a id="sec-6-1"></a>

### 6.1 Escopo incluído
- Modelagem formal do problema logístico do pátio
- Definição do motor de decisão e das regras operacionais parametrizáveis
- Arquitetura de dados e ingestão inicial por CSV e inputs assistidos
- Construção de gêmeo digital e ambiente de simulação
- Geração de cenários sintéticos calibrados
- Benchmarking contra baselines como FIFO e agenda fixa
- Replay offline com dados históricos anonimizados, quando disponíveis
- Estruturação de explicabilidade, logs e trilha auditável
- Prototipação de interfaces operacionais e fluxos de mensageria
- Consolidação do MVP beta laboratorial
- Preparação técnica e comercial para futura validação em campo

<a id="sec-6-2"></a>

### 6.2 Escopo excluído no ciclo atual
- Implantação plena em ambiente produtivo real
- Integração profunda com todos os ERPs do mercado já no primeiro ciclo
- Sensoriamento físico avançado e IoT como dependência do produto
- Operação comercial escalada antes da validação técnica mínima
- Customizações extensivas por cliente antes da estabilização do núcleo algorítmico

<a id="sec-6-3"></a>

### 6.3 Distinção entre ciclo financiado e visão de longo prazo
O documento deve separar explicitamente o que pertence ao ciclo formal de execução do projeto financiado e o que pertence à visão ampliada do PequiFlux. No ciclo financiado, a prioridade é a validação laboratorial do núcleo tecnológico, a consolidação do MVP beta em ambiente controlado, a produção de evidências e a preparação de prontidão para campo. Já a visão de longo prazo inclui implantação operacional em clientes, integrações profundas, expansão multiunidade, escala comercial e amadurecimento do produto. Essa separação evita sobrecarga de escopo, promessas implícitas indevidas e conflito entre ambição estratégica e disciplina de execução.

<a id="sec-7"></a>

## 7. Objetivo geral
Projetar, desenvolver e avaliar, em ambiente controlado, um artefato computacional de orquestração dinâmica de pátio capaz de reduzir espera e variabilidade operacional no recebimento e expedição de caminhões no agro, com base em otimização sob restrições, replanejamento orientado a eventos e governança auditável.

<a id="sec-8"></a>

## 8. Objetivos específicos
Os objetivos específicos do PequiFlux devem ser compreendidos como desdobramentos operacionais do objetivo geral e como marcos de construção do artefato no âmbito da Design Science Research Methodology. Em vez de funcionarem apenas como uma enumeração de intenções, eles devem explicitar o que precisa ser produzido, validado e documentado ao longo do ciclo de P&D para que o projeto avance, de modo disciplinado, da formulação do problema à consolidação de um MVP beta laboratorial.

O primeiro objetivo específico é formalizar o problema do pátio como um sistema dinâmico de decisão logística sob restrições, identificando entidades, variáveis, eventos, dependências, restrições rígidas e prioridades operacionais. Esse objetivo corresponde à etapa de explicitação do problema e de definição dos requisitos mínimos do artefato.

O segundo objetivo específico é estruturar a base mínima de dados do projeto, incluindo o dicionário de variáveis, as regras de consistência, o layout inicial de ingestão por CSV e os critérios de qualidade e completude necessários para simulação, replay e evolução futura da arquitetura. Esse objetivo sustenta a transição entre modelagem conceitual e construção experimental.

O terceiro objetivo específico é projetar e implementar o ambiente laboratorial do PequiFlux, composto por gerador de cenários, simulador ou gêmeo digital e infraestrutura técnica reprodutível para execução, monitoramento, versionamento, auditoria e testes do artefato.

O quarto objetivo específico é desenvolver o motor de decisão em versão laboratorial, incorporando regras parametrizáveis, tratamento de restrições, replanejamento orientado a eventos, geração de justificativas operacionais e trilha auditável de decisão.

O quinto objetivo específico é demonstrar o funcionamento do artefato em cenários experimentais representativos, por meio de cenários sintéticos calibrados e, quando disponíveis, replays offline com dados históricos anonimizados, verificando aderência às restrições e comportamento operacional plausível.

O sexto objetivo específico é avaliar sistematicamente o artefato frente a baselines simples, como FIFO e agenda fixa, utilizando métricas de espera, throughput, latência de replanejamento, estabilidade frente a eventos e cobertura de cenários críticos.

O sétimo objetivo específico é consolidar um MVP beta laboratorial demonstrável, com observabilidade, logs auditáveis, fallback manual, documentação técnica mínima e prontidão para futura transição à validação em campo.

O oitavo objetivo específico é documentar os requisitos, critérios de go/no-go, dependências e condições mínimas para validação externa futura, incluindo dados, integrações, segurança, governança e protocolo de deployment assistido.

O nono objetivo específico é converter as evidências técnicas produzidas ao longo do ciclo de P&D em ativos estratégicos de continuidade, como dossiê experimental, estudo de caso, narrativa de ROI, proposta de valor e materiais de preparação comercial.

<a id="sec-9"></a>

## 9. Hipóteses do projeto
As hipóteses do PequiFlux devem ser entendidas como proposições orientadoras da pesquisa e do desenvolvimento do artefato, passíveis de exame progressivo ao longo do ciclo de P&D. Sua função não é apenas registrar crenças iniciais da equipe, mas explicitar aquilo que o projeto pretende verificar por meio de modelagem, demonstração, avaliação experimental e consolidação de evidências. Por essa razão, as hipóteses são organizadas em quatro grupos complementares: hipóteses de modelagem e desempenho, hipóteses operacionais, hipóteses de adoção e hipóteses de transição tecnológica.

<a id="sec-9-1"></a>

### 9.1 Hipóteses de modelagem e desempenho
A primeira hipótese central do projeto é que a dinâmica do pátio agroindustrial pode ser representada adequadamente como um problema de decisão logística sob restrições, suficientemente rico para capturar filas, prioridades, capacidades, eventos e incompatibilidades operacionais sem perder tratabilidade computacional. Essa hipótese decorre diretamente da formulação já assumida pelo projeto, que aproxima o problema de uma variação de escalonamento flexível sob incerteza, com reotimização contínua orientada ao estado do sistema.

A segunda hipótese é que um motor de decisão baseado em otimização sob restrições, simulação e replanejamento orientado a eventos poderá superar heurísticas estáticas simples, como FIFO e agenda fixa, em métricas relevantes de operação, especialmente tempo de espera, throughput, estabilidade frente a eventos e qualidade global do fluxo. Essa hipótese é central para a utilidade do artefato e deverá ser examinada principalmente nas macroetapas de demonstração e avaliação, por benchmarking, Monte Carlo e replay offline.

A terceira hipótese é que a validação laboratorial em ambiente controlado, desde que sustentada por cenários sintéticos calibrados, logs reprodutíveis e comparação contra baselines, pode gerar evidência suficiente para justificar avanço do projeto a estágios superiores de maturidade tecnológica, mesmo sem implantação produtiva no ciclo atual. Essa hipótese está alinhada à estratégia já registrada no projeto de avançar por gêmeo digital, replay histórico e consolidação de evidências auditáveis antes de qualquer integração plena em campo.

<a id="sec-9-2"></a>

### 9.2 Hipóteses operacionais
A quarta hipótese é que a entrada inicial por CSV, combinada com operação assistida e dados mínimos viáveis, reduz o atrito de adoção de forma suficiente para viabilizar demonstração laboratorial robusta e futura transição para pilotos externos. Em termos metodológicos, essa hipótese será considerada sustentada se a base mínima de dados permitir alimentar o simulador, os cenários experimentais e o motor de decisão sem exigir integração profunda precoce.

A quinta hipótese é que a manutenção do operador humano no centro da decisão, associada a fallback manual, justificativas operacionais e trilha auditável, aumenta a aceitabilidade organizacional do sistema e reduz resistência à adoção de recomendações algorítmicas. Essa hipótese é particularmente importante porque o valor do PequiFlux não está apenas em decidir melhor, mas em decidir de forma tecnicamente justificável e socialmente aceitável em ambiente operacional sensível a percepções de favorecimento ou quebra injustificada da fila.

A sexta hipótese é que o uso de mensageria de baixo atrito, como WhatsApp ou solução equivalente, pode reduzir fricção na ponta operacional, principalmente no relacionamento com motoristas, sem exigir a adoção inicial de aplicativo próprio. Essa hipótese não será tratada como tese principal do artefato, mas como hipótese operacional subordinada à estratégia de implantação progressiva e aderência de campo futura.

<a id="sec-9-3"></a>

### 9.3 Hipóteses de adoção e valor
A sétima hipótese é que cooperativas, cerealistas e agroindústrias apresentam disposição de compra para uma solução capaz de reduzir filas, variabilidade e ruído decisório sem demandar, no primeiro momento, CAPEX físico elevado. A oitava hipótese é que uma proposta de valor baseada em implementação inicial e recorrência SaaS é compatível com a lógica de adoção do mercado-alvo, desde que acompanhada de narrativa objetiva de ROI, redução de atritos operacionais e governança auditável. Essas hipóteses serão examinadas sobretudo nas macroetapas finais, em articulação com LOIs, reuniões qualificadas, proposta de valor e estudo de caso.

A nona hipótese é que explicabilidade e auditabilidade não são apenas atributos técnicos desejáveis, mas diferenciais concretos de adoção em contexto agroindustrial, especialmente quando o sistema precisa justificar alterações na ordem aparente de atendimento. Essa hipótese conecta diretamente arquitetura algorítmica, design de interface e narrativa comercial do projeto.

<a id="sec-9-4"></a>

### 9.4 Hipóteses de transição tecnológica
A décima hipótese é que a consolidação de um MVP beta laboratorial com fluxo fim a fim demonstrável, observabilidade mínima, segurança básica, logs auditáveis e protocolo preliminar de deployment constitui base suficiente para planejar validação futura em campo, sem que isso implique implantação real dentro do ciclo financiado. Em outras palavras, o projeto assume que a passagem do laboratório à validação externa depende menos de promessas amplas e mais da acumulação disciplinada de evidências técnicas e documentais.

Metodologicamente, cada hipótese deverá ser tratada como item observável nos stage-gates do projeto. Ao final de cada macroetapa, a equipe deverá classificar as hipóteses relevantes como provisoriamente sustentadas, parcialmente sustentadas, não sustentadas ou ainda não testadas, registrando a evidência utilizada e o impacto dessa conclusão sobre backlog, arquitetura e próximos experimentos. Com isso, a seção 9 deixa de ser apenas declaratória e passa a funcionar como mecanismo de aprendizagem acumulativa do P&D.

<a id="sec-10"></a>

## 10. Fundamentação técnico-científica e método de pesquisa
O PequiFlux situa-se no campo da Pesquisa Operacional aplicada à decisão logística em ambientes dinâmicos e restritos. Seu núcleo técnico parte da modelagem do pátio agroindustrial como um sistema de escalonamento sob restrições, no qual decisões de chamada, sequenciamento e alocação de caminhões a recursos devem ser tomadas em presença de capacidade limitada, heterogeneidade operacional, prioridades concorrentes, qualidade da carga e ocorrência de eventos disruptivos. Nessa perspectiva, o problema pode ser tratado como uma variação de escalonamento flexível sob incerteza, com necessidade de replanejamento contínuo orientado ao estado do sistema. Essa formulação é coerente com a estratégia já assumida pelo projeto de empregar gêmeo digital, cenários sintéticos calibrados, benchmarking contra heurísticas simples e replay offline como base de evidência laboratorial.

Do ponto de vista metodológico, o projeto adota a Design Science Research Methodology como framework principal de condução da pesquisa. A opção por DSRM decorre da natureza do objetivo do PequiFlux: não se pretende apenas descrever um problema operacional do agro, mas projetar, desenvolver, demonstrar, avaliar e consolidar um artefato computacional capaz de apoiar decisões reais de orquestração de pátio. Assim, a pesquisa está centrada na construção de um artefato tecnológico e na produção de evidências sobre sua utilidade, robustez e prontidão de evolução.

A condução do estudo seguirá seis atividades metodológicas articuladas. A primeira consiste na identificação do problema e de sua motivação, compreendendo a explicitação da dor operacional do pátio, a delimitação do escopo do ciclo financiado e a definição das hipóteses técnicas, operacionais e de negócio. A segunda corresponde à definição dos objetivos da solução, estabelecendo quais propriedades o artefato deverá satisfazer para ser considerado relevante, viável e passível de avaliação. A terceira atividade é o design e desenvolvimento do artefato, abrangendo a modelagem formal do domínio, o dicionário de dados, a arquitetura do sistema, o gêmeo digital, o motor de decisão e os mecanismos de rastreabilidade, explicabilidade e governança. A quarta atividade é a demonstração, na qual o artefato é colocado em funcionamento em ambiente controlado, por meio de cenários sintéticos calibrados e, quando possível, replay offline com dados históricos anonimizados. A quinta atividade é a avaliação, realizada de forma sistemática com comparação contra baselines, testes de robustez, Monte Carlo, medição de latência, espera, throughput, estabilidade e integridade dos logs. A sexta atividade é a comunicação, voltada à consolidação das evidências em relatórios técnicos, dossiê experimental, narrativa de valor, estudo de caso e materiais de prontidão para validação futura em campo e amadurecimento comercial.

No contexto do PequiFlux, o artefato central da pesquisa é um sistema de apoio à decisão para orquestração dinâmica do pátio, concebido como plataforma SaaS B2B com motor matemático, regras de negócio parametrizáveis, replanejamento orientado a eventos, logs explicáveis e trilha auditável. Seu desenvolvimento observa, desde o início, a manutenção do operador humano no centro da decisão, a disponibilidade de fallback manual, a ingestão inicial por CSV e o princípio de evolução progressiva da arquitetura, sem tornar integrações profundas uma dependência do ciclo atual.

A demonstração e a avaliação do artefato ocorrerão em ambiente laboratorial controlado, em linha com o escopo do projeto e com o estágio de maturidade tecnológica pretendido. A base experimental será formada por dois eixos principais: cenários sintéticos calibrados e replays offline com dados históricos anonimizados, quando disponíveis. O desempenho do artefato será comparado com estratégias basais de operação, notadamente FIFO e agenda fixa, e examinado em cenários normais e cenários com disrupções, como atraso, chuva, quebra de equipamento, variação de capacidade e mudança de prioridade.

As métricas de avaliação serão estruturadas em quatro grupos. No plano técnico, serão observadas latência p95 de replanejamento, throughput estimado, redução de espera p50 e p95, estabilidade frente a eventos e cobertura de cenários críticos. No plano de dados, serão acompanhadas a qualidade do dicionário de dados, a taxa de completude dos cenários, a reprodutibilidade dos experimentos e a integridade dos logs. No plano de execução, serão monitorados o cumprimento do cronograma, as entregas por etapa, o número de evidências consolidadas e a resolução do backlog crítico. No plano de negócio, serão acompanhadas reuniões qualificadas, propostas emitidas, LOIs, evolução do pipeline e clareza da tese de ROI.

A execução metodológica do projeto será controlada por stage-gates formais ao final de cada macroetapa, com revisão de entregas, indicadores, riscos remanescentes, hipóteses validadas ou rejeitadas e suficiência das evidências acumuladas para progressão. Esse mecanismo conecta método, governança e prestação de contas, e é coerente tanto com a disciplina documental prevista no Documento Mestre quanto com a exigência de monitoramento do plano de trabalho pela FAPEG.

Como ameaças à validade da pesquisa, reconhecem-se a simplificação inevitável do ambiente real, a dependência de dados representativos, a possibilidade de viés na calibração dos cenários sintéticos e a limitação de generalização para operação produtiva antes de validação em campo. Por essa razão, o ciclo atual não é definido como implantação real, mas como construção disciplinada de um artefato validável em laboratório, com produção de evidências auditáveis suficientes para sustentar a transição do TRL 1 ao TRL 4.

<a id="sec-10-1"></a>

### 10.1 Protocolo experimental mínimo e critérios de aceitação
Para que a avaliação do artefato seja experimentalmente defensável, o PequiFlux adota um desenho experimental mínimo explícito, destinado a padronizar a geração de evidências e a reduzir arbitrariedades na comparação entre versões do motor de decisão e entre o artefato e seus baselines. Esse protocolo não substitui o refinamento posterior do plano técnico do artefato, mas estabelece, no próprio Documento Mestre, o nível mínimo de rigor esperado para demonstração, benchmarking, replay offline e consolidação do MVP beta.

O desenho experimental será estruturado em classes de cenários. A primeira classe corresponde a cenários nominais, com operação estável, baixa perturbação e disponibilidade regular de recursos. A segunda classe corresponde a cenários de pico, com aumento de volume, saturação parcial do pátio e maior competição por recursos críticos. A terceira classe corresponde a cenários perturbados, nos quais serão introduzidas disrupções relevantes, como atraso de caminhões, indisponibilidade de equipamentos, chuva, alteração de capacidade operacional, mudança de prioridade e interrupções documentais ou de fluxo. A quarta classe corresponde a cenários extremos ou de estresse, voltados a examinar robustez e limites de comportamento do artefato diante de combinações severas de eventos e gargalos. Sempre que possível, cada classe deverá conter instâncias sintéticas calibradas de baixa, média e alta complexidade operacional.

Os baselines mínimos obrigatórios da avaliação serão FIFO e agenda fixa, por constituírem referências operacionais simples, inteligíveis e compatíveis com a realidade decisória que o projeto busca superar. Quando metodologicamente justificável, poderão ser adicionadas heurísticas intermediárias ou versões simplificadas do próprio motor para fins de comparação incremental, desde que essas comparações adicionais não substituam o benchmark obrigatório contra os baselines centrais.

Cada cenário experimental deverá ser executado múltiplas vezes sob sementes controladas, especialmente quando houver geração sintética estocástica ou eventos amostrados. Como regra inicial de disciplina experimental, recomenda-se que cada família de cenário seja avaliada com um número mínimo previamente fixado de execuções por instância e com registro explícito das sementes utilizadas, de modo a permitir reprodutibilidade, comparação entre versões e auditoria posterior dos resultados. A definição quantitativa final desse número deverá constar do protocolo detalhado mantido como anexo vivo, mas o princípio metodológico é que nenhum resultado comparativo relevante seja aceito sem repetição suficiente para mitigar efeito de acaso.

As comparações entre o artefato e os baselines deverão observar, no mínimo, makespan, throughput, tempo de espera p50 e p95, latência p95 de replanejamento, estabilidade frente a eventos, taxa de factibilidade das soluções e integridade dos logs. Sempre que pertinente, a análise deverá incluir também métricas derivadas de impacto operacional, como estimativas de diesel e CO2 evitados, desde que tais estimativas sejam claramente identificadas como derivadas e não como medições diretas de campo.

O protocolo deverá prever análise de sensibilidade e testes de ablação. A análise de sensibilidade examinará o comportamento do artefato sob variação controlada de parâmetros relevantes, como intensidade de chegada, disponibilidade de recursos, peso relativo de componentes da função-objetivo e severidade das disrupções. Os testes de ablação, por sua vez, deverão investigar a contribuição de componentes específicos do sistema, como mecanismos de replanejamento, regras de prioridade, penalizações suaves, explicabilidade ou módulos auxiliares de suporte à decisão. O objetivo desses procedimentos é distinguir ganho estrutural real de melhoria aparente decorrente de configuração circunstancial.

O logging experimental deverá obedecer a regras mínimas. Cada execução deverá registrar identificador único, versão do artefato, conjunto de parâmetros, semente utilizada, classe do cenário, eventos ocorridos, decisões relevantes tomadas, tempo de execução, métricas resultantes e eventuais violações ou falhas observadas. Esses registros deverão ser preservados em formato reprodutível e vinculados ao dossiê de evidências, de modo que qualquer resultado relevante apresentado em gate, relatório técnico ou material externo possa ser auditado retrospectivamente.

Os critérios mínimos de aceitação deverão ser definidos por macroetapa e interpretados no contexto dos stage-gates. Na Macroetapa 2, o critério mínimo é a existência de um núcleo laboratorial funcional, reproduzível e capaz de executar cenários básicos com logging íntegro. Na Macroetapa 3, o critério mínimo é a demonstração consistente do artefato em cenários calibrados e a produção de comparação metodologicamente válida com os baselines centrais. Na Macroetapa 4, o critério mínimo é a consolidação de evidências suficientemente robustas para sustentar o MVP beta laboratorial, a trilha auditável e a prontidão preliminar para transição. Na Macroetapa 5, o critério mínimo é a organização dessas evidências em forma documental e estratégica adequada à continuidade científica, técnica e comercial do projeto.

A versão completa do protocolo experimental deverá permanecer como anexo vivo próprio, com detalhamento de famílias de cenários, parâmetros, número de execuções por classe, sementes, scripts de geração, formato de logs, procedimentos de análise e template de relatório experimental. Com isso, o Documento Mestre preserva concisão relativa no corpo principal, mas passa a incorporar um padrão explícito de disciplina experimental compatível com a maturidade metodológica pretendida para o PequiFlux.

<a id="sec-10-2"></a>

### 10.2 Premissas operacionais e limites de validade
Para evitar sobre-alegações e assegurar consistência entre modelagem, demonstração, avaliação e futura comunicação dos resultados, o PequiFlux explicita, no próprio Documento Mestre, um conjunto de premissas operacionais e limites de validade. Essas premissas definem sob quais condições o artefato está sendo concebido, qual recorte do domínio está sendo abstraído, quais informações se assume observar com confiabilidade suficiente e em que medida os resultados laboratoriais podem ou não ser extrapolados para contextos reais de operação. Seu papel metodológico é proteger o projeto contra interpretações indevidas de escopo, desempenho ou prontidão tecnológica.

A primeira premissa é que o domínio de referência do PequiFlux, no ciclo atual, corresponde a unidades operacionais agroindustriais com fluxo relevante de caminhões, recursos limitados de atendimento e necessidade de coordenação dinâmica entre chegada, fila, alocação e processamento. O projeto não assume, nesta etapa, cobertura universal de todas as configurações possíveis de cooperativas, cerealistas, terminais ou plantas agroindustriais, mas trabalha com uma abstração suficientemente representativa de ambientes em que há competição por recursos, regras de prioridade, restrições operacionais e eventos perturbadores relevantes.

A segunda premissa é que a granularidade temporal das decisões será compatível com o nível de orquestração tática-operacional do pátio, e não com controle físico instantâneo de chão de operação em resolução subsegundo. Em termos práticos, isso significa que o artefato será concebido para apoiar decisões recorrentes de chamada, sequenciamento, realocação e resposta a eventos em janelas operacionais discretizadas de forma plausível para o contexto de uso, preservando tempo de resposta suficiente para utilidade operacional, mas sem reivindicar controle contínuo em tempo real estrito típico de sistemas embarcados ou de automação industrial profunda.

A terceira premissa é que um conjunto mínimo de variáveis pode ser observado com confiabilidade suficiente para viabilizar simulação, replay offline e decisão assistida. Entre essas variáveis incluem-se, em nível mínimo, identificação do caminhão, tempo ou ordem de chegada, tipo de carga, prioridades operacionais relevantes, disponibilidade declarada dos recursos e registro básico de eventos perturbadores. O projeto não assume, no ciclo atual, observabilidade perfeita, sincronização total entre fontes ou disponibilidade contínua de dados integrados em tempo real. Em vez disso, assume que dados mínimos viáveis, desde que coerentes e suficientemente estruturados, são suficientes para sustentar validação laboratorial metodologicamente aceitável.

A quarta premissa é que o operador humano permanece no centro da decisão. O artefato não substitui integralmente a autoridade operacional local, mas produz recomendações justificadas, passíveis de aceitação, revisão ou rejeição pelo usuário responsável. Essa premissa define o papel exato do sistema no ciclo atual: trata-se de um sistema de apoio à decisão com capacidade de recomendação auditável, e não de um mecanismo de automação autônoma irrestrita. Dessa forma, fallback manual, explicabilidade e trilha auditável não são apenas salvaguardas complementares, mas elementos constitutivos da própria validade operacional do artefato.

A quinta premissa é que a ausência de integração profunda em tempo real é aceitável no estágio atual, desde que não impeça a construção de um ambiente laboratorial reprodutível e a produção de evidências tecnicamente úteis. O projeto assume, portanto, que ingestão por CSV, inputs assistidos e reconstrução experimental do estado operacional são mecanismos metodologicamente suficientes para TRL inicial e intermediário, ainda que não equivalham às condições desejáveis de uma futura operação em campo com integração viva via ERP, balança, portaria ou mensageria automatizada.

A sexta premissa é que os resultados laboratoriais têm validade primária como evidência de comportamento do artefato em ambiente controlado. Eles não devem ser automaticamente generalizados para desempenho produtivo em campo sem consideração das diferenças entre cenários sintéticos, replay offline e operação real. Em particular, não será metodologicamente correto inferir, a partir do ciclo atual, garantias de desempenho absoluto em unidades específicas, economias financeiras realizadas em produção, aceitação organizacional irrestrita ou robustez integral frente a integrações, ruídos e contingências não representados no ambiente experimental.

A sétima premissa é que as ameaças à validade não são um apêndice marginal, mas parte integrante da interpretação dos resultados. Sempre que o projeto reportar melhorias frente a baselines, essas melhorias deverão ser lidas à luz do conjunto de cenários avaliados, da qualidade das entradas, da fidelidade das disrupções modeladas, da granularidade temporal adotada e das simplificações estruturais assumidas. O valor científico e técnico do PequiFlux, nesta fase, reside menos em proclamar generalização ampla e mais em demonstrar, com disciplina metodológica, que o artefato apresenta utilidade plausível, auditável e progressivamente refinável sob condições explicitamente delimitadas.

Em consequência, toda comunicação técnica, relatório, artigo, estudo de caso ou material de apresentação derivado deste ciclo deverá preservar coerência com essas premissas. Sempre que houver extrapolação para contextos de campo, ela deverá ser marcada como hipótese futura, necessidade de validação adicional ou cenário prospectivo, e não como resultado já demonstrado. Essa regra protege a integridade metodológica do projeto e reduz risco de inflar indevidamente o alcance das evidências acumuladas.

A versão expandida dessas premissas deverá permanecer como anexo vivo, articulada ao plano técnico do artefato, ao protocolo experimental e ao registro de riscos, permitindo atualização sempre que uma premissa for refinada, relaxada, contrariada ou substituída ao longo da execução.

<a id="sec-11"></a>

## 11. Arquitetura de alto nível
<a id="sec-11-1"></a>

### 11.1 Camada de ingestão de dados
- Dados macro logísticos
- Dados micrologísticos do pátio
- Eventos operacionais e climáticos
- Registro assistido de exceções humanas

<a id="sec-11-2"></a>

### 11.2 Camada de modelo e decisão
- Estado corrente do pátio
- Regras de negócio parametrizadas
- Restrições rígidas e penalizações operacionais
- Solver e mecanismo de replanejamento por eventos
- Geração de logs e justificativas da decisão

<a id="sec-11-3"></a>

### 11.3 Camada de aplicação
- Interface do operador
- Painéis e fila recalculada
- Mensageria com motoristas
- Trilha auditável e relatórios

<a id="sec-11-4"></a>

### 11.4 Camada de governança
- Controle de acesso
- Versionamento
- Backup
- Observabilidade
- Compliance e LGPD

<a id="sec-11-5"></a>

### 11.5 Atributos de qualidade e controle operacional
Como sistema de apoio à decisão em contexto operacional sensível, o PequiFlux deverá ser avaliado não apenas pela qualidade matemática das recomendações produzidas, mas também pela forma segura, rastreável, governável e operacionalmente prudente com que decide. Por essa razão, os requisitos não funcionais e o protocolo de segurança operacional do artefato são tratados como parte integrante da arquitetura, e não como concernimento periférico de implementação.

A primeira dimensão é a **latência-alvo de decisão e replanejamento**. O sistema deverá operar com tempo de resposta compatível com a granularidade tática-operacional assumida no projeto, de modo que a recomendação chegue em janela útil para decisão humana e reordenação do fluxo. Em termos metodológicos, a latência p95 de replanejamento constitui atributo de qualidade central do artefato, pois uma solução de alta qualidade combinatória, mas entregue fora da janela operacional plausível, perde validade prática no contexto do pátio.

A segunda dimensão é a **rastreabilidade mínima da decisão**. Toda recomendação emitida pelo artefato deverá estar vinculada, no mínimo, ao estado do sistema considerado, ao conjunto de restrições relevantes, aos parâmetros ativos, ao identificador da execução, à versão do motor, à marca temporal da recomendação e à justificativa operacional resumida para a ação sugerida. Essa rastreabilidade é condição necessária para auditoria, depuração, comparação entre versões e legitimação do uso do sistema perante operadores e parceiros futuros.

A terceira dimensão é a **regra de override humano**. O operador responsável deverá poder aceitar, rejeitar ou adiar uma recomendação do sistema, desde que a intervenção fique registrada com identificação do evento, instante, motivo declarado e consequência operacional conhecida, quando cabível. O override humano não será tratado como falha do artefato, mas como componente normal de governança em um sistema de apoio à decisão. O objetivo arquitetural é permitir cooperação controlada entre recomendação algorítmica e autoridade operacional, preservando aprendizado posterior a partir dos desvios registrados.

A quarta dimensão é a **abstenção algorítmica**. O PequiFlux deverá prever condições nas quais o motor, em vez de produzir uma recomendação aparentemente precisa, deverá se abster ou sinalizar confiança insuficiente. Entre essas condições incluem-se entradas incompletas ou incoerentes, violação de pressupostos mínimos de observabilidade, conflito não resolvido entre restrições críticas, degradação relevante da qualidade do estado reconstruído ou ocorrência de situação fora do domínio experimental conhecido. Nesses casos, o comportamento seguro do sistema consiste em explicitar insuficiência decisória, registrar a ocorrência e devolver a decisão ao operador sob modo assistido, em vez de forçar uma recomendação sem base confiável.

A quinta dimensão é a **política de logs e retenção mínima de evidência**. O artefato deverá manter logs suficientes para reconstrução retrospectiva das execuções relevantes, contemplando entradas recebidas, parâmetros, decisões sugeridas, overrides, abstenções, falhas, tempos de execução e resultados observados. A política de logs deverá equilibrar auditabilidade, reprodutibilidade, proteção de dados e custo operacional, assegurando que eventos críticos e execuções utilizadas em benchmarking, replay offline, gates e relatórios permaneçam preservados em formato versionado e recuperável.

A sexta dimensão é a **política de backup e recuperação mínima**. O ambiente laboratorial e os ativos de evidência do projeto deverão dispor de rotinas básicas de backup para configurações, artefatos experimentais, logs, documentos e registros de decisão, com procedimento mínimo de restauração testável. No ciclo atual, não se exige arquitetura de alta disponibilidade de produção, mas exige-se disciplina suficiente para evitar perda de evidência, corrupção de artefatos centrais ou quebra de continuidade metodológica por falha simples de armazenamento.

A sétima dimensão é a **disponibilidade operacional compatível com o estágio do projeto**. Como o ciclo atual é laboratorial, a disponibilidade será tratada como atributo de prontidão experimental e demonstrabilidade, e não como SLA comercial pleno. Ainda assim, o artefato deverá alcançar estabilidade suficiente para suportar demonstrações repetidas, execução de cenários, benchmarking e consolidação do MVP beta sem degradação recorrente que comprometa a coleta de evidências ou a confiança mínima na arquitetura.

A oitava dimensão é a **segurança básica e proteção operacional do sistema**. O PequiFlux deverá adotar, desde o ciclo atual, controles mínimos de acesso, segregação de perfis quando aplicável, proteção dos artefatos versionados, cuidado com credenciais, registro de alterações relevantes e coerência com as exigências de LGPD e uso legítimo de dados. Ainda que o projeto não esteja em fase de operação produtiva ampla, a segurança não pode ser postergada de forma absoluta, pois faz parte da credibilidade do artefato e da sua prontidão para evolução futura.

A nona dimensão é a **observabilidade do comportamento do artefato**. O sistema deverá permitir monitorar estado de execução, falhas, degradação, eventos excepcionais, frequência de override, ocorrências de abstenção e integridade dos fluxos experimentais. A observabilidade não se limita a logs brutos; ela deve permitir leitura operacional da saúde do artefato e apoiar decisões de ajuste, rollback, recalibração e priorização de backlog.

Esses atributos deverão ser tratados como critérios arquiteturais transversais e revisitados nos stage-gates, especialmente nas macroetapas de demonstração, consolidação do MVP beta e prontidão para transição. Sua versão expandida deverá ser mantida como anexo vivo de arquitetura e governança, com parâmetros-alvo, regras de exceção, responsáveis, evidências mínimas e procedimentos de revisão.

<a id="sec-12"></a>

## 12. Fontes de dados previstas
- Check-in de portaria e balança
- Dados de classificação e ERP
- Status de moegas, docas e equipamentos
- Dados climáticos e operacionais externos
- Dados históricos anonimizados de operações parceiras
- Cenários sintéticos calibrados

<a id="sec-12-1"></a>

### 12.1 Dependências externas críticas e critérios de seleção de parceiros
O avanço do PequiFlux depende, em parte, de insumos externos que não estão integralmente sob controle da equipe, especialmente quando se trata de contextualização operacional, obtenção de dados históricos, preparação de replay offline e futura aproximação com parceiros de validação. Por essa razão, o projeto explicita, desde já, suas dependências críticas e os critérios mínimos pelos quais potenciais parceiros deverão ser avaliados, de modo a preservar integridade metodológica, segurança jurídica, coerência documental e autonomia do núcleo técnico do artefato.

A primeira dependência crítica é a disponibilidade de dados históricos e a autorização legítima para seu uso. Sempre que o projeto recorrer a dados de operações parceiras, deverá haver delimitação explícita sobre origem, escopo de uso, finalidade analítica, grau de anonimização, prazo de retenção e restrições de compartilhamento. A inexistência desses dados não inviabiliza o ciclo atual, pois cenários sintéticos calibrados continuam sendo eixo legítimo de validação laboratorial; contudo, limita o alcance de replay offline e reduz a capacidade de contextualizar resultados com maior proximidade do domínio real.

A segunda dependência crítica é a possibilidade de entrevistas operacionais, reuniões técnicas ou sessões de elicitação com atores do domínio. Essas interações são relevantes para identificar regras tácitas, exceções, prioridades locais, restrições informais e critérios de aceitabilidade do fluxo, sobretudo nas macroetapas iniciais de formulação do problema e desenho do artefato. Sempre que realizadas, deverão ser documentadas em formato apropriado, com registro de data, participantes, finalidade e principais insumos incorporados. A ausência desse tipo de interação não impede pesquisa laboratorial, mas reduz fidelidade contextual e aumenta risco de modelagem excessivamente abstrata.

A terceira dependência crítica é a futura seleção de design partners para eventual validação externa. O projeto adota, desde já, critérios mínimos para avaliar a adequação de um parceiro potencial. Entre esses critérios incluem-se existência de dor operacional compatível com o problema tratado, fluxo relevante de caminhões, abertura para entrevistas e esclarecimento de regras operacionais, disponibilidade de dados mínimos ou capacidade de reconstrução razoável do processo, presença de interlocutor institucional apto a autorizar interações e alinhamento explícito de que o ciclo atual não implica implantação produtiva imediata. O design partner desejável é aquele que contribui para aprendizagem disciplinada e futura validação, e não apenas aquele que manifesta interesse comercial genérico.

A quarta dependência crítica diz respeito às fronteiras de propriedade intelectual e de uso de ativos de terceiros. O código-fonte, os modelos, a documentação técnica e os artefatos metodológicos desenvolvidos no âmbito do PequiFlux deverão permanecer segregados dos dados de terceiros e, salvo disposição formal em contrário, constituem ativo do projeto. Dados históricos, planilhas operacionais, registros internos e materiais fornecidos por parceiros externos não deverão ser incorporados ao patrimônio reutilizável do artefato além do que estiver expressamente autorizado. Sempre que houver dúvida sobre derivação, coautoria, reutilização ou publicação, a interpretação padrão deverá favorecer segregação e formalização prévia.

A quinta dependência crítica é a separação entre código, dados e ativos documentais de origem externa. Repositórios, ambientes de armazenamento, logs experimentais e materiais compartilhados deverão preservar segregação suficiente para impedir mistura indevida entre base proprietária do projeto e dados ou documentos de terceiros. Essa separação é importante não apenas por razões de compliance e LGPD, mas também para evitar contaminação metodológica, dificuldades de publicação, conflitos de auditoria e restrições futuras de escalabilidade tecnológica.

A sexta dependência crítica refere-se às condições mínimas para replay offline com dados de terceiros. Para que esse procedimento seja metodologicamente aceitável, deverá haver permissão de uso, ordenação temporal minimamente confiável dos eventos, conjunto mínimo de variáveis observáveis, anonimização compatível com o risco de reidentificação e clareza sobre o que está sendo reconstruído e o que está sendo inferido. Quando essas condições não estiverem presentes, o projeto não deverá apresentar o procedimento como replay offline propriamente dito, mas como aproximação sintética ou reconstrução parcial inspirada em padrões observados.

Essas dependências deverão ser tratadas como objetos permanentes de governança. Sua versão expandida deverá permanecer como anexo vivo próprio, articulada ao documento de dados e LGPD, ao registro de riscos, ao protocolo experimental e ao plano de prontidão para validação futura em campo. Em consequência, qualquer parceria considerada estratégica para o avanço do projeto deverá ser examinada não apenas por interesse comercial, mas por aderência metodológica, segurança documental e compatibilidade com o estágio de maturidade do PequiFlux.

<a id="sec-13"></a>

## 13. Artefatos a produzir
- Documento de requisitos do sistema
- Dicionário de dados e esquema de ingestão
- Modelo conceitual do pátio
- Simulador / gêmeo digital
- Motor de decisão v1, v2 e versões subsequentes
- Biblioteca de cenários sintéticos
- Benchmark técnico contra baselines
- Protótipo de interface do operador
- Protótipo de mensageria
- Dossiê de evidências laboratoriais
- Plano de prontidão para validação em campo
- Estudo de caso e proposta de valor comercial
- Especificação de atributos de qualidade e controle operacional
- Modelo de impacto socioambiental estimado por proxies
- Caderno de dependências externas e critérios de seleção de parceiros

<a id="sec-14"></a>

## 14. Roadmap macro do projeto alinhado à DSRM e ao cronograma executivo
A execução temporal do PequiFlux será organizada de modo que o cronograma físico do projeto represente, de forma operacional, a lógica metodológica da Design Science Research Methodology. Para preservar aderência ao plano de trabalho já assumido no projeto, o roadmap macro será estruturado em cinco macroetapas, correspondentes às etapas do cronograma executivo submetido, sem prejuízo de reconhecer que, no plano conceitual, a DSRM compreende seis atividades. No caso do PequiFlux, algumas dessas atividades metodológicas distribuem-se ao longo da mesma etapa temporal, o que é aceitável e desejável para manter consistência entre método, entregas, orçamento, indicadores e governança.

<a id="sec-14-1"></a>

### 14.1 Macroetapa 1 — Formulação do problema, organização do projeto e especificação do domínio
**Período de referência:** 06/07/2026 a 31/08/2026.

A primeira macroetapa corresponde, predominantemente, às atividades de identificação do problema e definição dos objetivos da solução no âmbito da DSRM. Nessa etapa serão consolidados o kickoff do projeto, o plano de trabalho, a rotina de acompanhamento, a organização do workspace técnico, os repositórios, os mecanismos mínimos de versionamento, backup e reprodutibilidade, bem como o mapeamento das regras, fluxos e restrições do pátio e a definição do dicionário de dados e da estrutura inicial de ingestão por CSV. O objetivo central desta etapa é converter a dor operacional do setor em um problema formal de pesquisa e engenharia, acompanhado de requisitos mínimos, variáveis observáveis e estrutura de dados suficientemente consistente para sustentar o restante do ciclo de P&D. Seus principais produtos esperados são o escopo refinado, o ambiente técnico reprodutível, o modelo conceitual inicial do domínio e a especificação mínima de dados.

<a id="sec-14-2"></a>

### 14.2 Macroetapa 2 — Design inicial do artefato e construção do núcleo laboratorial
**Período de referência:** 01/09/2026 a 31/10/2026.

A segunda macroetapa corresponde ao início da atividade de design e desenvolvimento do artefato. Nela serão construídos o gerador de dados sintéticos em sua primeira versão, o gêmeo digital inicial do pátio, o motor de decisão v1 acoplado ao simulador e a primeira trilha básica de explicabilidade e auditoria. Ao final da etapa, será realizada revisão técnica estruturada para consolidar aprendizados, revisar premissas e explicitar pendências críticas. O objetivo desta macroetapa é materializar o núcleo computacional do PequiFlux em ambiente controlado, produzindo uma primeira versão funcional do artefato e estabelecendo base formal para experimentação subsequente.

<a id="sec-14-3"></a>

### 14.3 Macroetapa 3 — Demonstração experimental e avaliação técnica inicial
**Período de referência:** 01/11/2026 a 31/01/2027.

A terceira macroetapa concentra a transição entre demonstração e avaliação na lógica da DSRM. Nela, o gerador será calibrado para produzir cenários mais representativos, será construída a biblioteca de instâncias experimentais, o motor será comparado com baselines como FIFO e agenda fixa, e serão conduzidos testes de Monte Carlo, testes de estresse e replay offline com dados históricos anonimizados, quando disponíveis, ou com equivalentes sintéticos calibrados. Ao final da etapa, serão estimados os ganhos potenciais do artefato em termos de redução de espera, aumento de throughput, tempo de replanejamento e viabilidade técnico-operacional. O objetivo é demonstrar que o artefato funciona de forma consistente em cenários controlados e gerar a primeira camada robusta de evidências quantitativas sobre sua utilidade.

<a id="sec-14-4"></a>

### 14.4 Macroetapa 4 — Consolidação do MVP beta, governança técnica e prontidão para transição
**Período de referência:** 01/02/2027 a 30/04/2027.

A quarta macroetapa corresponde ao aprofundamento do desenvolvimento, à consolidação do MVP beta laboratorial e à formalização da prontidão para futura validação em campo. Nessa etapa serão estruturados o fluxo fim a fim demonstrável do MVP, a observabilidade, a segurança, os logs auditáveis, os controles mínimos de governança e a arquitetura de integração futura via CSV, API, ERP e balança. Também será produzido o dossiê técnico de evidências e o plano de prontidão comercial e técnica para campo, incluindo critérios de go/no-go, protocolo de deployment, fallback manual, requisitos mínimos de dados e estratégia futura de mensuração de impacto. O objetivo desta fase é encerrar o ciclo laboratorial com um protótipo beta demonstrável, tecnicamente rastreável e documentado de forma suficiente para suportar futura transição para validação externa.

<a id="sec-14-5"></a>

### 14.5 Macroetapa 5 — Comunicação dos resultados, proposta de valor e fechamento do ciclo
**Período de referência:** 01/05/2027 a 05/07/2027.

A quinta macroetapa corresponde predominantemente à atividade de comunicação na DSRM, embora também consolide resultados de avaliação e desdobramentos estratégicos. Nela serão transformados os resultados laboratoriais em estudo de caso, proposta de valor, calculadora simples de ROI, kit comercial, materiais de marketing, abordagem consultiva e ações de relacionamento com potenciais parceiros. Também serão organizadas as entregas finais do projeto, os materiais institucionais e a preparação do fechamento do ciclo, incluindo elementos úteis para prestação de contas e aproximação com validação futura em campo. O objetivo desta etapa é converter o conhecimento produzido ao longo do P&D em ativos documentais, comerciais e institucionais que sustentem a continuidade tecnológica e a evolução do negócio.

<a id="sec-14-6"></a>

### 14.6 Correspondência entre DSRM e cronograma executivo
No PequiFlux, a atividade metodológica de identificação do problema concentra-se majoritariamente na Macroetapa 1. A definição dos objetivos da solução distribui-se entre a Macroetapa 1 e o início da Macroetapa 2. O design e desenvolvimento do artefato ocorrem sobretudo nas Macroetapas 2 e 4. A demonstração está concentrada na Macroetapa 3. A avaliação distribui-se entre as Macroetapas 3 e 4, pois parte das evidências é gerada em benchmarking e replay offline, enquanto outra parte é consolidada no MVP beta e no dossiê técnico. A comunicação, por sua vez, atinge seu ponto máximo na Macroetapa 5, embora a organização parcial de evidências já se inicie no final da Macroetapa 4. Essa distribuição garante fidelidade ao framework DSRM sem romper a coerência com o cronograma físico e com os indicadores oficialmente assumidos no projeto.

<a id="sec-14-7"></a>

### 14.7 Governança do roadmap e critérios de avanço
Cada macroetapa será encerrada com um gate formal de revisão, no qual serão analisados os artefatos produzidos, os indicadores atingidos, os riscos remanescentes, as hipóteses confirmadas ou rejeitadas e a suficiência das evidências para progressão. A governança dessa passagem entre etapas observará os ritos já definidos no projeto, incluindo reuniões semanais de execução, checkpoints quinzenais, revisão mensal de riscos, registro de decisão arquitetural, registro de hipótese validada ou rejeitada e relatório mensal do projeto. Desse modo, o roadmap deixa de ser apenas descritivo e passa a funcionar como instrumento metodológico e gerencial de controle da execução do PequiFlux.

<a id="sec-15"></a>

## 15. Desafios críticos de execução, validação e transição
Os desafios do PequiFlux não devem ser lidos apenas como dificuldades genéricas do projeto, mas como tensões estruturais que condicionam a qualidade da pesquisa, a consistência do artefato e a disciplina da execução. Por isso, esta seção deve funcionar como ponte entre riscos, governança, indicadores e roadmap, explicitando quais obstáculos precisam ser geridos para que o projeto avance de maneira metodologicamente defensável do problema formalizado à consolidação de um MVP beta laboratorial e à preparação de futura validação externa.

<a id="sec-15-1"></a>

### 15.1 Desafios de modelagem e solução
O primeiro grande desafio reside em formalizar corretamente o problema sem reduzi-lo a uma abstração excessivamente simplificada. O pátio real envolve heterogeneidade de veículos, restrições físicas, regras de qualidade, prioridades comerciais, eventos estocásticos e limitações de capacidade que precisam ser traduzidos em variáveis e restrições computáveis sem destruir a viabilidade do modelo. O desafio não é apenas matemático, mas epistemológico: simplificar demais compromete validade; sofisticar cedo demais compromete execução.

Um segundo desafio técnico é equilibrar qualidade da solução, latência de resposta e explicabilidade. Em um ambiente de decisão operacional, uma solução teoricamente superior, mas lenta ou opaca, pode ter menos valor do que uma solução ligeiramente inferior, porém auditável, rápida e confiável. Esse trade-off deverá ser tratado como questão central do design do artefato, e não como ajuste posterior.

Outro desafio relevante é gerar cenários sintéticos e protocolos de avaliação suficientemente realistas para testar robustez sem mascarar fragilidades do modelo. Como o ciclo atual depende fortemente de ambiente laboratorial, a fidelidade dos cenários e a honestidade metodológica dos benchmarks serão decisivas para a credibilidade das evidências produzidas.

<a id="sec-15-2"></a>

### 15.2 Desafios de dados e evidência experimental
No plano de dados, o desafio central é construir uma base mínima viável que seja ao mesmo tempo simples o bastante para execução rápida e suficientemente representativa para sustentar simulação, replay e avaliação. Isso envolve padronizar entradas heterogêneas, lidar com ruído, ausência e incompletude, estruturar anonimização quando houver dados reais e garantir que a arquitetura de ingestão inicial não crie dependências prematuras de integrações profundas.

Há também o desafio de transformar evidência dispersa em dossiê experimental cumulativo. Em projetos de P&D aplicado, o risco recorrente é executar muito e documentar pouco, o que reduz drasticamente a capacidade de demonstrar maturidade técnica, justificar decisões e sustentar transição para validação futura. Por isso, o PequiFlux precisa tratar reprodutibilidade, versionamento, logs, registro de hipóteses e organização das evidências como parte do núcleo metodológico, e não como atividade acessória.

<a id="sec-15-3"></a>

### 15.3 Desafios organizacionais e de governança
No plano organizacional, o desafio mais crítico é manter disciplina de execução em um projeto que combina pesquisa, engenharia de produto, validação experimental e preparação comercial. Existe risco permanente de dispersão entre frentes periféricas, refinamentos prematuros e tarefas que produzem aparência de sofisticação, mas pouca evidência real. A governança do projeto deve, portanto, proteger o núcleo validável e impedir sobrecarga de escopo.

Outro desafio é registrar decisões, lições aprendidas e responsabilidades de forma sistemática. Como o Documento Mestre já define ritos, documentos obrigatórios, política interna de decisão e estratégia documental, o ponto decisivo agora não é inventar novos controles, mas ativar os controles já previstos, conectando-os ao backlog, aos gates e à rotina de trabalho da equipe.

Também deve ser destacado o desafio da prestação de contas técnica e financeira, sobretudo porque a execução do projeto financiado deve ocorrer em conformidade com o plano aprovado e com monitoramento por metas e indicadores. Isso impõe ao grupo a necessidade de alinhar documentação interna, entregas técnicas e cronograma formal, evitando divergência entre o que é executado e o que é institucionalmente reportável.

<a id="sec-15-4"></a>

### 15.4 Desafios de mercado e narrativa de valor
No plano de mercado, o principal desafio é converter validação técnica em narrativa de valor economicamente inteligível. O artefato pode ser metodologicamente elegante e ainda assim fracassar comercialmente se a equipe não conseguir traduzir redução de espera, maior throughput, previsibilidade e auditabilidade em tese clara de ROI para cooperativas, cerealistas e agroindústrias.

Há ainda o desafio de refinar ICP, construir relacionamento com design partners e preparar proposta comercial sem prometer além do validado. Essa contenção é especialmente importante neste estágio, porque o projeto ainda está estruturado como P&D laboratorial; logo, a comunicação de mercado deve ser suficientemente ambiciosa para atrair interesse, mas rigorosa o bastante para não converter hipótese em promessa indevida.

<a id="sec-15-5"></a>

### 15.5 Desafios de transição para validação futura em campo
A transição do laboratório para o campo não depende apenas de ter um algoritmo funcional. Ela exige prontidão técnica, segurança mínima, fallback manual, protocolo de deployment, critérios de go/no-go, requisitos mínimos de dados, estratégia de mensuração de impacto e clareza sobre as condições de operação assistida futura. O desafio aqui é preparar essa transição sem antecipá-la artificialmente. Em termos metodológicos, o sucesso desta etapa não será implantar cedo, mas encerrar o ciclo atual com um plano de prontidão tecnicamente sólido e documentalmente rastreável.

<a id="sec-15-6"></a>

### 15.6 Função metodológica da seção
No novo arranjo do Documento Mestre, os desafios desta seção devem alimentar diretamente três mecanismos de controle. Primeiro, devem orientar o registro de riscos e a estratégia de mitigação. Segundo, devem influenciar a priorização do backlog e a definição de critérios de avanço entre macroetapas. Terceiro, devem ser revisitados nos stage-gates como parte da reflexão metodológica da DSRM, permitindo verificar quais tensões foram resolvidas, quais persistem e quais exigem redirecionamento do projeto. Com isso, a seção 15 deixa de ser apenas um aviso genérico sobre dificuldades futuras e passa a operar como mapa de tensões críticas da execução do PequiFlux.

<a id="sec-16"></a>

## 16. Estrutura de governança
<a id="sec-16-1"></a>

### 16.1 Papéis centrais
**Liderança técnica e modelagem:** Marcus  
**Dados, integrações, segurança e LGPD:** Anna Beatriz  
**Backend, APIs, infraestrutura e observabilidade:** Luiz Felipe  
**Mapeamento operacional e requisitos do pátio:** Rayssa  
**UX, testes e aderência operacional:** Yasmin

<a id="sec-16-2"></a>

### 16.2 Ritos de gestão
- Reunião semanal de execução
- Reunião quinzenal de checkpoint técnico
- Revisão mensal de riscos, backlog e prioridades
- Gate formal ao final de cada macroetapa

<a id="sec-16-3"></a>

### 16.3 Documentos obrigatórios de governança
- Ata de reunião
- Registro de decisão arquitetural
- Registro de risco
- Registro de hipótese validada ou rejeitada
- Relatório mensal do projeto

<a id="sec-17"></a>

## 17. Sistema de indicadores e critérios de acompanhamento
Os indicadores do PequiFlux devem ser entendidos como instrumentos de verificação metodológica do avanço do artefato, e não apenas como métricas soltas de acompanhamento. Sua função é apoiar os stage-gates do projeto, permitindo avaliar, ao final de cada macroetapa, se houve progresso suficiente em termos de construção, demonstração, avaliação e consolidação do artefato. Por essa razão, os indicadores devem ser associados explicitamente às macroetapas do cronograma e às atividades metodológicas da DSRM.

<a id="sec-17-1"></a>

### 17.1 Indicadores técnicos
Os indicadores técnicos medem o desempenho funcional do artefato em ambiente controlado. Serão acompanhados, prioritariamente, a latência p95 de replanejamento, o throughput estimado do sistema, a redução de espera em p50 e p95 frente aos baselines, a estabilidade das recomendações sob ocorrência de eventos críticos e a cobertura de cenários relevantes pelo motor de decisão. Esses indicadores ganham maior centralidade nas macroetapas de demonstração, avaliação e consolidação do MVP beta, quando o artefato deixa de ser apenas uma construção conceitual e passa a ser examinado quanto à sua utilidade prática.

<a id="sec-17-2"></a>

### 17.2 Indicadores de dados
Os indicadores de dados medem a maturidade da base experimental do projeto. Serão acompanhadas a qualidade do dicionário de dados, a taxa de completude dos cenários, a reprodutibilidade dos experimentos e a integridade dos logs e registros gerados. Esses indicadores são especialmente relevantes nas macroetapas iniciais, nas quais a formalização do domínio, a estruturação da ingestão e a criação do ambiente reprodutível condicionam a validade de todas as avaliações posteriores.

<a id="sec-17-3"></a>

### 17.3 Indicadores de execução
Os indicadores de execução medem a disciplina de entrega do projeto e sua aderência ao cronograma pactuado. Serão observadas as entregas concluídas por macroetapa, o cumprimento do cronograma, o número de evidências consolidadas e o volume de backlog crítico resolvido ao final de cada ciclo. Esses indicadores operam como ponte entre a lógica metodológica e a governança prática do projeto, especialmente porque a execução formal deverá ser acompanhada por objetivos, cronograma, metas e indicadores previstos no plano de trabalho.

<a id="sec-17-4"></a>

### 17.4 Indicadores de negócio e transição
Os indicadores de negócio não medem sucesso comercial pleno no ciclo atual, mas o grau de prontidão mercadológica produzido a partir das evidências do P&D. Serão acompanhados o número de reuniões qualificadas, propostas emitidas, LOIs obtidas, evolução do pipeline e clareza da tese de ROI. Esses indicadores assumem maior peso nas macroetapas finais, quando o projeto passa a transformar evidência laboratorial em narrativa comercial disciplinada, sem antecipar promessas de implantação além do validado.

<a id="sec-17-5"></a>

### 17.5 Regras de uso dos indicadores nos stage-gates
Ao final de cada macroetapa, os indicadores deverão ser interpretados de forma integrada. O gate não deverá decidir apenas se uma métrica melhorou, mas se o conjunto de evidências produzidas é suficiente para autorizar o avanço do projeto à etapa seguinte. Assim, na Macroetapa 1, o foco recai sobre qualidade da formulação do problema, organização do workspace, clareza das regras e completude mínima da estrutura de dados. Na Macroetapa 2, o foco recai sobre existência e coerência do núcleo laboratorial. Na Macroetapa 3, o foco recai sobre demonstração e avaliação inicial frente a baselines. Na Macroetapa 4, o foco recai sobre consolidação do MVP beta, logs, governança e prontidão para transição. Na Macroetapa 5, o foco recai sobre organização das evidências, narrativa de valor e ativos de continuidade. Dessa forma, a seção deixa de ser apenas descritiva e passa a funcionar como mecanismo real de controle metodológico do projeto.

<a id="sec-17-6"></a>

### 17.6 Modelo de impacto socioambiental estimado e auditabilidade por proxies
O PequiFlux tratará, no ciclo atual, o impacto socioambiental como objeto de estimativa indireta e auditável, baseado em proxies derivadas do ambiente laboratorial, e não como medição de campo ou comprovação de efeito já realizado em operação produtiva. O objetivo desta subseção é formalizar, de maneira causal e metodologicamente prudente, como externalidades positivas potenciais serão inferidas, comparadas entre cenários e registradas ao longo do ciclo de P&D.

A lógica causal de impacto adotada pelo projeto parte de três encadeamentos principais. O primeiro é que menor tempo de espera e menor ociosidade operacional tendem a reduzir tempo de motor em marcha lenta ou permanência improdutiva em fila, o que implica menor consumo estimado de diesel e, por consequência, menor emissão estimada de CO2e. O segundo é que maior previsibilidade, melhor sequenciamento e menor retrabalho operacional tendem a reduzir movimentações desnecessárias, reencaminhamentos e permanência improdutiva de carga e veículo, o que pode reduzir desperdícios e perdas operacionais. O terceiro é que maior organização do fluxo, menor conflito de prioridades e menor necessidade de intervenção corretiva sob pressão tendem a melhorar segurança processual e reduzir ruído operacional, entendido como desordem decisória, exceções frequentes e instabilidade do sistema.

No estágio atual, tais impactos serão estimados por proxies, e não por mensuração direta em campo. Para o eixo ambiental, os proxies centrais serão minutos de espera evitados frente ao baseline, minutos estimados de marcha lenta ou permanência improdutiva evitados, diesel estimado evitado em fila e CO2e estimado evitado. Em termos conceituais, a estimativa poderá ser estruturada segundo relações do tipo: **Diesel_fila_est = tempo_espera_improdutiva × consumo específico assumido** e **CO2e_est = diesel estimado × fator de emissão adotado**. Os valores de consumo específico e fator de emissão deverão ser explicitados no protocolo detalhado, tratados como parâmetros auditáveis e sempre apresentados como premissas do modelo de estimativa.

Para o eixo de desperdício e eficiência operacional, os proxies incluirão, sempre que tecnicamente justificável, número de reencaminhamentos ou realocações evitadas, redução de tempo de permanência improdutiva, redução de movimentos redundantes e diminuição de ocorrências associadas a retrabalho operacional. O projeto não afirmará, nesta fase, redução medida de perdas físicas de grãos em campo, a menos que tal inferência venha a ser sustentada posteriormente por validação externa apropriada. No ciclo laboratorial, a interpretação correta é a de que o artefato poderá produzir sinais indiretos de redução de desperdício, derivados de melhor organização do fluxo e menor retrabalho.

Para o eixo de segurança e qualidade operacional, os proxies incluirão estabilidade das recomendações, frequência de reordenações abruptas, incidência de conflitos de prioridade, quantidade de overrides críticos, ocorrências de abstenção algorítmica por insuficiência de dados e volume de intervenção corretiva extraordinária exigida do operador. Esses indicadores não equivalem, por si sós, a estatísticas de acidente ou segurança ocupacional em campo, mas funcionam como sinais laboratoriais de qualidade organizacional do fluxo e de robustez procedimental do artefato.

Toda estimativa de impacto socioambiental deverá ser comparativa e contextualizada. Isso significa que, sempre que possível, os valores deverão ser apresentados como diferença entre o desempenho do artefato e o desempenho dos baselines centrais, especialmente FIFO e agenda fixa, sob o mesmo cenário experimental, mesma semente, mesmo conjunto de restrições e mesma estrutura de parâmetros. A finalidade metodológica não é produzir números absolutos descontextualizados, mas examinar se o artefato gera, em ambiente controlado, melhorias relativas que sejam coerentes com externalidades positivas potenciais.

A auditabilidade dessas estimativas exigirá trilha explícita de premissas. Cada resultado relevante deverá estar associado, no mínimo, à versão do artefato, à classe de cenário, à instância executada, à semente utilizada, aos parâmetros do experimento, ao baseline de comparação, à fórmula empregada, aos fatores de emissão ou coeficientes assumidos e ao status da evidência no respectivo gate. Dessa forma, qualquer narrativa futura sobre impacto socioambiental poderá ser retroinspecionada e reavaliada à luz das hipóteses, premissas e simplificações efetivamente adotadas.

Do ponto de vista de validade, os resultados desta subseção deverão ser interpretados como estimativas experimentais de externalidades potenciais sob condições controladas. Não será metodologicamente correto converter essas estimativas, nesta fase, em promessa de redução real de emissões, perdas ou incidentes em unidades produtivas específicas. Toda comunicação derivada do ciclo atual deverá indicar explicitamente que o impacto socioambiental está sendo tratado por proxies laboratoriais e que sua confirmação em campo dependerá de validação externa posterior.

A versão expandida do modelo de impacto socioambiental deverá permanecer como anexo vivo, articulada ao protocolo experimental, ao caderno de premissas operacionais, à matriz de rastreabilidade metodológica e ao dossiê de evidências. Com isso, o projeto passa a incorporar não apenas uma narrativa de benefício potencial, mas um mecanismo explícito de estimação, comparação e auditoria de externalidades positivas compatível com o estágio metodológico do PequiFlux.

<a id="sec-18"></a>

## 18. Riscos principais
<a id="sec-18-1"></a>

### 18.1 Riscos técnicos
- Formulação inadequada do problema
- Overengineering antes da validação mínima
- Falta de dados representativos
- Complexidade computacional excessiva para o estágio

<a id="sec-18-2"></a>

### 18.2 Riscos operacionais
- Desalinhamento da equipe
- Execução sem documentação
- Baixa cadência de entregas
- Dependência excessiva de uma pessoa

<a id="sec-18-3"></a>

### 18.3 Riscos de mercado
- Dor mal quantificada
- ICP mal delimitado
- Narrativa técnica forte, mas narrativa comercial fraca

<a id="sec-18-4"></a>

### 18.4 Riscos jurídicos e de compliance
- Falhas de LGPD
- Falhas de rastreabilidade
- Problemas de PI ou de uso de dados de terceiros

<a id="sec-19"></a>

## 19. Estratégia de mitigação
- Definir stage-gates objetivos
- Registrar decisões arquiteturais
- Priorizar núcleo validável antes de funcionalidades acessórias
- Trabalhar com dados mínimos viáveis e cenários calibrados
- Manter fallback manual e operador no centro
- Instituir revisão mensal de risco
- Formalizar política interna de dados, acesso e versionamento

<a id="sec-20"></a>

## 20. Política interna de decisão
Toda decisão estrutural relevante deverá responder a cinco perguntas:
1. Isso aproxima o projeto de validar o núcleo de valor?  
2. Isso aumenta evidência técnica real ou apenas aparência de sofisticação?  
3. Isso reduz ou amplia dependências externas prematuras?  
4. Isso preserva auditabilidade e governança?  
5. Isso melhora a prontidão para validação futura em campo?

<a id="sec-21"></a>

## 21. Estratégia documental do projeto
O Documento Mestre deve ser o topo da hierarquia documental. Abaixo dele, o grupo deve manter um conjunto enxuto, porém rigoroso, de anexos vivos. Além de organizar a documentação, essa estrutura deve assegurar rastreabilidade entre problema, hipóteses, objetivos, artefatos, métricas, macroetapas, evidências e gates, de modo que a execução possa ser auditada metodologicamente ao longo do ciclo de P&D.

1. Plano técnico do artefato  
2. Documento de arquitetura  
3. Documento de dados e LGPD  
4. Roadmap e cronograma executivo  
5. Registro de riscos  
6. Registro de decisões arquiteturais  
7. Dossiê de evidências e experimentos  
8. Documento comercial e de mercado  
9. Matriz completa de rastreabilidade metodológica  
10. Protocolo experimental detalhado e caderno de execução  
11. Caderno de premissas operacionais e limites de validade  
12. Especificação de atributos de qualidade e controle operacional  
13. Modelo de impacto socioambiental estimado e auditoria por proxies  
14. Caderno de dependências externas e critérios de seleção de parceiros  

<a id="sec-21-1"></a>

### 21.1 Matriz resumida de rastreabilidade metodológica
Para fins de controle metodológico, o Documento Mestre passa a incorporar uma matriz resumida de rastreabilidade, destinada a conectar, no corpo do texto, os principais elementos de pesquisa e execução do projeto. Sua função é permitir que a equipe identifique, de forma rápida, qual pergunta ou subproblema está sendo enfrentado, qual hipótese está em exame, qual objetivo específico orienta a ação, qual artefato deve ser produzido, por qual métrica o avanço será verificado, em qual macroetapa isso ocorrerá, qual evidência será exigida e em qual gate a suficiência dessa evidência será julgada.

| ID | Pergunta ou subproblema | Hipótese associada | Objetivo específico | Artefato principal | Métrica de verificação | Macroetapa prevista | Evidência exigida | Gate correspondente |
|---|---|---|---|---|---|---|---|---|
| R1 | Como formalizar o pátio como sistema dinâmico de decisão sob restrições? | H1 | OE1 | Modelo conceitual do pátio e formulação do problema | Clareza da formulação, consistência das entidades, restrições e eventos | M1 | Modelo conceitual validado internamente, glossário e registro de restrições | Gate da Macroetapa 1 |
| R2 | Qual é a base mínima de dados necessária para simulação, replay e evolução da arquitetura? | H4 | OE2 | Dicionário de dados e esquema inicial de ingestão CSV | Completude mínima dos campos, consistência e reprodutibilidade da ingestão | M1 | Dicionário de dados versionado, layout CSV e regras de consistência | Gate da Macroetapa 1 |
| R3 | Como construir o ambiente laboratorial reprodutível do artefato? | H3, H4 | OE3 | Gerador de cenários, simulador ou gêmeo digital e ambiente técnico reprodutível | Reprodutibilidade experimental e cobertura mínima de cenários | M2 | Ambiente executável, cenários sintéticos iniciais e documentação técnica | Gate da Macroetapa 2 |
| R4 | Como implementar um motor de decisão auditável com replanejamento orientado a eventos? | H2, H5 | OE4 | Motor de decisão v1 com logs e justificativas | Latência de replanejamento, factibilidade das soluções e integridade dos logs | M2 | Protótipo funcional acoplado ao simulador e trilha básica de auditoria | Gate da Macroetapa 2 |
| R5 | O artefato opera de forma plausível em cenários experimentais representativos? | H2, H3 | OE5 | Biblioteca de instâncias e protocolo de demonstração | Estabilidade frente a eventos, aderência às restrições e comportamento plausível | M3 | Execução bem-sucedida em cenários calibrados e replay offline, quando disponível | Gate da Macroetapa 3 |
| R6 | O artefato supera baselines simples como FIFO e agenda fixa? | H2 | OE6 | Benchmark técnico contra baselines | Redução de espera p50/p95, throughput e makespan | M3 | Resultados comparativos, testes de Monte Carlo e análise de sensibilidade | Gate da Macroetapa 3 |
| R7 | O projeto alcançou um MVP beta laboratorial com prontidão mínima para transição? | H10 | OE7, OE8 | MVP beta, dossiê técnico e plano de prontidão para campo | Observabilidade, logs auditáveis, critérios de go/no-go e requisitos mínimos de deployment | M4 | Fluxo fim a fim demonstrável, documentação de prontidão e protocolo preliminar | Gate da Macroetapa 4 |
| R8 | Como converter evidência técnica em continuidade estratégica e narrativa de valor? | H7, H8, H9 | OE9 | Estudo de caso, proposta de valor e narrativa de ROI | Número de evidências consolidadas, clareza da tese de ROI, reuniões qualificadas e LOIs | M5 | Dossiê consolidado, estudo de caso e materiais de preparação comercial | Gate da Macroetapa 5 |

A matriz resumida não substitui a leitura das seções metodológicas do documento, mas funciona como mecanismo de navegação analítica e de controle executivo. Em cada revisão de macroetapa, ela deverá ser utilizada para verificar se os vínculos entre hipótese, objetivo, artefato, métrica e evidência permanecem consistentes com o backlog e com os resultados produzidos.

<a id="sec-21-2"></a>

### 21.2 Versão completa como anexo vivo
A versão completa da matriz de rastreabilidade metodológica deverá ser mantida como anexo vivo próprio, derivado deste Documento Mestre e atualizado ao longo da execução. Essa versão expandida deverá detalhar, para cada linha, identificador único, pergunta ou subproblema, hipótese associada, objetivo específico, macroetapa, artefato, responsável principal, dependências, métrica-alvo, fonte da evidência, status de teste, classificação da hipótese no gate e impacto sobre backlog, arquitetura e riscos. Desse modo, a matriz deixa de ser apenas instrumento de organização textual e passa a operar como dispositivo permanente de governança metodológica do PequiFlux.  

<a id="sec-22"></a>

## 22. Próximas ações imediatas
As próximas ações imediatas do PequiFlux devem ser entendidas como ações de ativação do ciclo de P&D, isto é, como providências necessárias para transformar o Documento Mestre em instrumento operacional efetivo de execução, governança e produção de evidências. Por essa razão, a seção não deve permanecer apenas como um checklist administrativo, mas como uma agenda de curto prazo diretamente subordinada à Macroetapa 1 do roadmap.

A primeira ação imediata é validar formalmente o Documento Mestre com toda a equipe, incorporando as revisões de método, roadmap, objetivos específicos, indicadores e governança, de modo a congelar uma versão de referência institucional coerente com a arquitetura de P&D do projeto.

A segunda ação imediata é abrir e estruturar os anexos vivos previstos na estratégia documental do projeto, com prioridade para o plano técnico do artefato, o documento de arquitetura, o documento de dados e LGPD, o roadmap e cronograma executivo, o registro de riscos, o registro de decisões arquiteturais, o dossiê de evidências e experimentos, a matriz completa de rastreabilidade metodológica, o protocolo experimental detalhado com caderno de execução, o caderno de premissas operacionais e limites de validade, a especificação de atributos de qualidade e controle operacional e o modelo de impacto socioambiental estimado e auditoria por proxies e o caderno de dependências externas e critérios de seleção de parceiros. Sem essa derivação documental, o Documento Mestre permanece conceitualmente correto, mas operacionalmente insuficiente.

A terceira ação imediata é instituir a cadência formal de governança do projeto, incluindo calendário fixo de reunião semanal de execução, checkpoint quinzenal técnico, revisão mensal de riscos e backlog, e definição do rito de gate ao final de cada macroetapa. Essa ação é crítica porque a própria estrutura de governança já está definida no documento, mas ainda precisa ser ativada como prática real.

A quarta ação imediata é criar o backlog mestre do projeto organizado por macroetapa, explicitando, para cada item, sua relação com o objetivo específico correspondente, com o artefato a ser produzido e com o critério de aceitação do gate. Isso impede dispersão e melhora o controle sobre o que é núcleo validável e o que é acessório.

A quinta ação imediata é iniciar a execução da Macroetapa 1 segundo o cronograma executivo já assumido, com foco em kickoff, plano de trabalho, montagem do workspace, mapeamento de regras, fluxos e restrições do pátio, e definição da estrutura mínima de dados e ingestão por CSV. Essas atividades já constam do cronograma submetido e devem aparecer aqui como desdobramento imediato, e não como agenda paralela.

A sexta ação imediata é formalizar os critérios preliminares de go/no-go dos primeiros stage-gates, com especial atenção à suficiência da formulação do problema, à qualidade da estrutura de dados, à existência do ambiente reprodutível e à clareza dos artefatos mínimos exigidos para avançar da fase de estruturação para a fase de design laboratorial.

A sétima ação imediata é iniciar a organização do dossiê de evidências desde o começo do ciclo, evitando que a prova de maturidade técnica seja deixada apenas para o final. Essa ação é estrategicamente importante porque o histórico recente do projeto mostrou que a robustez conceitual precisa vir acompanhada de evidência objetiva, auditável e acumulativa.

<a id="sec-23"></a>

## 23. Regra de manutenção do documento
Este documento deve ser revisado mensalmente ou sempre que ocorrer uma mudança relevante de escopo, arquitetura, dados, parceiros, estratégia comercial ou risco do projeto. Toda nova versão deve registrar data, responsável e justificativa de alteração.

<a id="sec-24"></a>

## 24. Encerramento
O PequiFlux deixa, nesta etapa, de existir apenas como proposta de edital e passa a existir como programa real de construção tecnológica, validação experimental e preparação de mercado. Este documento formaliza essa transição e estabelece o referencial comum do grupo para execução disciplinada, coerência estratégica e acúmulo de evidência ao longo do projeto.

