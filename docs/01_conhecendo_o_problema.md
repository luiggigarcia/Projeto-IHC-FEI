# Entrega 1 — Conhecendo o projeto, o usuário e o problema

> **Autor:** Luiggi Paschoalini Garcia  
> **Matrícula:** 22.122.006-4  
> **TCC:** Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.  
> **Orientador:** Leonardo Anjoletto  
> **Disciplina:** Interação Humano-Computador  
> **Instituição:** Centro Universitário FEI  
> **Semestre:** 2026/2

---

# 0. Identificação do TCC e da equipe

## 0.1 Membro

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Luiggi Paschoalini Garcia | 22.122.006-4 | @luiggigarcia |

## 0.2 Título atual do TCC

> **Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.**

## 0.3 Orientador

> **Leonardo Anjoletto**

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

- [ ] Sistema/aplicação interativa
- [ ] Algoritmo
- [ ] Modelo de IA/ML/LLM
- [ ] Biblioteca/API/Framework
- [ ] Análise de dataset
- [x] Estudo/benchmark/avaliação experimental
- [x] Infraestrutura/backend
- [ ] Componente embarcado/IoT
- [x] Outro: **Ambiente sandbox para execução controlada e análise comportamental de aplicações**

### Descrição

O TCC prevê a implementação e análise de um ambiente sandbox destinado à execução controlada de aplicações potencialmente não confiáveis.

O ambiente deverá permitir que aplicações sejam executadas de maneira isolada e que seus comportamentos durante a execução sejam observados e analisados.

A proposta envolve investigar quais ações são realizadas pela aplicação no sistema operacional, quais componentes são afetados, quais alterações são produzidas e quais recursos computacionais são utilizados, possibilitando a coleta e organização dessas informações para posterior análise.

---

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [ ] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [x] **Não. O TCC é predominantemente técnico e não previa interface.**

### Explicação

O escopo formal do TCC está concentrado na implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.

O desenvolvimento de uma interface gráfica não constitui, neste momento, um requisito formal do TCC.

Para a disciplina de IHC, será derivado um escopo de interação a partir da contribuição técnica do TCC, buscando investigar como diferentes perfis de usuários poderiam utilizar o ambiente e compreender as informações obtidas durante as análises.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase

> **O TCC implementa e analisa um ambiente controlado capaz de executar aplicações potencialmente não confiáveis e observar de forma estruturada seus comportamentos e efeitos sobre o sistema operacional.**

---

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

**[H] H01 —**

A motivação do TCC está na possibilidade de realizar uma análise mais aprofundada do comportamento de aplicações potencialmente não confiáveis durante sua execução em um sistema operacional.

Uma aplicação pode realizar diversas operações durante sua execução, como criação de processos, alteração de arquivos, modificações de configurações, utilização de recursos e comunicação de rede, que podem não ser facilmente compreendidas apenas pela observação convencional de sua execução.

Dessa forma, o projeto busca investigar a utilização de um ambiente controlado que permita executar essas aplicações e observar de maneira estruturada **o que elas fazem no sistema operacional, quais componentes alteram, como essas alterações ocorrem e quais recursos utilizam**.

A hipótese inicial é que a disponibilização dessas informações de maneira organizada pode contribuir para uma análise mais aprofundada do comportamento das aplicações, especialmente em contextos de Segurança da Informação, Infraestrutura, pesquisa e ensino.

**[?] Lacuna de conhecimento**

Ainda não foi investigado empiricamente quais dessas informações são consideradas mais relevantes pelos diferentes perfis de usuários e quais dificuldades eles enfrentam atualmente durante esse tipo de análise.

---

## 1.3 Qual é a capacidade/contribuição central produzida pelo TCC?

> **Nosso TCC produz a capacidade de executar aplicações potencialmente não confiáveis em um ambiente controlado e analisar, de maneira estruturada, seu comportamento e seus efeitos sobre o sistema operacional.**

Essa capacidade envolve potencialmente:

- observar processos criados e encerrados;
- identificar alterações em arquivos;
- identificar alterações em configurações do sistema;
- observar utilização de recursos computacionais;
- observar atividades de rede;
- registrar eventos ocorridos durante a execução;
- organizar as evidências coletadas;
- permitir uma análise posterior do comportamento observado.

A definição exata das categorias monitoradas ainda será refinada durante o desenvolvimento técnico do TCC.

---

## 1.4 O que se espera que esteja diferente se a contribuição for bem-sucedida?

**[H] H02 —**

Espera-se que seja possível analisar o comportamento de uma aplicação potencialmente não confiável de maneira mais estruturada e aprofundada, reduzindo a dependência de observações manuais ou da consulta isolada a diferentes fontes de informação.

Para profissionais de Segurança da Informação e Infraestrutura, isso pode contribuir para uma compreensão mais detalhada dos efeitos produzidos por determinada aplicação.

Para pesquisadores e estudantes, pode proporcionar um ambiente controlado para experimentação e estudo do comportamento de aplicações e sua interação com o sistema operacional.

---

## 1.5 Mérito técnico/científico × aplicação prática

| Mérito/contribuição técnica do TCC | Possível aplicação/valor em uso |
|---|---|
| Implementação de um ambiente sandbox para execução controlada. | Executar aplicações potencialmente não confiáveis sem depender diretamente do ambiente operacional principal. |
| Isolamento da aplicação durante a execução. | Criar um contexto controlado para experimentação e investigação. |
| Monitoramento do comportamento da aplicação. | Observar como uma aplicação interage com o sistema operacional. |
| Coleta de eventos e evidências. | Apoiar uma análise mais aprofundada do comportamento observado. |
| Análise dos efeitos produzidos pela aplicação. | Identificar alterações realizadas e recursos utilizados. |
| Avaliação do ambiente desenvolvido. | Identificar capacidades, limitações e possibilidades de utilização da solução. |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

> **NÃO SE APLICA AO ESCOPO ORIGINAL.**

O TCC não prevê originalmente uma interface de usuário.

---

## 2.2 Quem poderia usar, configurar, administrar, operar, interpretar ou tomar decisões?

Neste momento, consideramos os seguintes perfis potenciais:

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| **Analista de Segurança da Informação** | Usuário direto potencial | Executaria aplicações potencialmente não confiáveis e investigaria seu comportamento. | [H] |
| **Profissional de Infraestrutura de TI** | Usuário direto potencial | Avaliaria impactos de aplicações sobre o sistema operacional e seus recursos. | [H] |
| **Pesquisador de Computação/Sistemas** | Usuário direto potencial | Utilizaria o ambiente para realizar experimentos controlados. | [H] |
| **Pesquisador de Segurança da Informação** | Usuário direto potencial | Investigaria comportamentos e técnicas utilizadas pelas aplicações. | [H] |
| **Estudante de Computação** | Usuário direto potencial | Utilizaria o ambiente para aprendizado e experimentação. | [H] |
| **Estudante de Segurança da Informação** | Usuário direto potencial | Estudaria na prática o comportamento de aplicações e mecanismos de segurança. | [H] |
| **Administrador do ambiente** | Usuário operacional potencial | Configuraria e manteria o ambiente utilizado para as análises. | [H] |

### Observação metodológica

Os perfis acima representam hipóteses iniciais derivadas do domínio do TCC.

A Entrega 2 e as entregas posteriores deverão fornecer evidências para priorizar os perfis e compreender melhor suas necessidades.

---

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

**[H]**

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Responsável pela Segurança da Informação | Pode utilizar os resultados das análises para apoiar decisões de segurança. | Possivelmente não | [H] |
| Responsável pela Infraestrutura | Pode utilizar informações sobre impactos no sistema operacional. | Possivelmente não | [H] |
| Orientador/pesquisador responsável | Pode avaliar resultados obtidos em experimentos. | Não necessariamente | [H] |
| Organização que utiliza o ambiente | Pode se beneficiar de análises realizadas antes da execução de aplicações em ambientes confiáveis. | Não necessariamente | [H] |

---

## 2.4 Que características desses perfis podem influenciar a interação?

**[H]**

Os perfis considerados possuem diferentes níveis de conhecimento técnico e diferentes objetivos.

Profissionais de Segurança da Informação podem possuir familiaridade com processos, eventos, redes, arquivos, indicadores de comprometimento e análise de comportamento.

Profissionais de Infraestrutura podem possuir maior interesse nos impactos sobre recursos e componentes do sistema operacional.

Pesquisadores e estudantes podem necessitar de maior contextualização e explicação das informações apresentadas.

A interface deverá considerar a possibilidade de diferentes níveis de conhecimento técnico, evitando assumir que todos os usuários interpretarão automaticamente informações de baixo nível produzidas pelo sistema.

**[?] Lacuna de conhecimento**

Ainda não sabemos qual nível de conhecimento deverá ser considerado como padrão para o usuário principal nem quais informações precisam de explicações adicionais.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

**[H]**

O usuário pretende **compreender o comportamento de uma aplicação durante sua execução e identificar quais ações ela realiza sobre o sistema operacional**, utilizando evidências obtidas em um ambiente controlado.

O objetivo não é simplesmente "usar o sandbox".

O objetivo é:

> **Executar → observar → compreender → analisar.**

---

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Selecionar a aplicação que será analisada | Usuário de análise | Média / Alta | [H] |
| A02 | Preparar os parâmetros da análise | Usuário de análise | Média / Alta | [H] |
| A03 | Executar a aplicação no ambiente controlado | Usuário de análise | Alta / Alta | [H] |
| A04 | Acompanhar o comportamento durante a execução | Usuário de análise | Alta / Alta | [H] |
| A05 | Identificar alterações produzidas no sistema | Usuário de análise | Alta / Alta | [H] |
| A06 | Analisar os eventos e evidências coletados | Usuário de análise | Alta / Alta | [H] |
| A07 | Interpretar os resultados da execução | Usuário de análise | Alta / Alta | [H] |
| A08 | Registrar ou consultar os resultados da análise | Usuário de análise | Média / Média | [H] |

---

## 3.3 Qual atividade parece mais frequente? Por quê?

**[H]**

A execução e análise de aplicações tende a ser a atividade central do processo, pois constitui a finalidade principal do ambiente.

Entretanto, ainda não é possível determinar sua frequência real sem investigar o contexto dos diferentes perfis de usuários.

---

## 3.4 Qual parece mais crítica?

**[H]**

A atividade potencialmente mais crítica é a **interpretação dos resultados da execução**, pois o valor da análise não está apenas na coleta de eventos, mas na capacidade de compreender o que esses eventos representam.

Uma interpretação incorreta ou incompleta pode levar o usuário a tirar conclusões inadequadas sobre o comportamento da aplicação.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje?

**[H]**

Existem diferentes abordagens possíveis para investigar o comportamento de aplicações, incluindo execução em máquinas virtuais ou ambientes isolados, ferramentas de monitoramento do sistema operacional, análise de processos, monitoramento de arquivos e registros, captura de tráfego de rede e análise de logs.

Ferramentas como o **Process Monitor**, da Microsoft Sysinternals, permitem observar em tempo real atividades relacionadas ao sistema de arquivos, Registro e processos/threads do Windows.

Soluções específicas de sandbox, como **Cuckoo Sandbox**, permitem submeter arquivos para análise e gerar resultados como logs, relatórios, capturas e informações relacionadas à execução.

O **Windows Sandbox**, por sua vez, fornece um ambiente isolado e descartável para executar aplicações e arquivos não confiáveis.

Portanto, a hipótese inicial é que uma análise aprofundada pode envolver a combinação de diferentes mecanismos e ferramentas, dependendo do objetivo da investigação.

**[?] Lacuna de conhecimento**

Ainda precisamos investigar qual combinação de ferramentas e processos é utilizada pelos perfis que pretendemos priorizar e quais limitações eles encontram nesse processo.

---

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

**[H]**

Uma possível dificuldade está na quantidade de informações produzidas durante uma execução.

Eventos de processos, arquivos, registros, rede e recursos podem gerar grande quantidade de dados, tornando necessário identificar quais eventos são relevantes para a análise.

Outra possível dificuldade é a necessidade de utilizar diferentes ferramentas ou fontes de informação para obter uma visão completa do comportamento da aplicação.

Também pode existir dificuldade de interpretação quando as informações são apresentadas apenas em formato técnico ou como grandes volumes de logs.

**[?] Lacuna de conhecimento**

Essas dificuldades ainda precisam ser validadas com evidências sobre usuários reais e ferramentas existentes.

---

## 4.3 Que informações o profissional precisa interpretar?

**[H]**

Inicialmente, consideramos relevantes:

- processos criados;
- processos encerrados;
- processos filhos;
- árvore de processos;
- arquivos criados;
- arquivos modificados;
- arquivos excluídos;
- alterações em configurações;
- alterações no Registro, quando aplicável;
- conexões de rede;
- endereços e portas utilizados;
- consumo de CPU;
- consumo de memória;
- utilização de disco;
- sequência temporal dos eventos;
- eventos potencialmente suspeitos.

A relevância e prioridade de cada categoria ainda deverá ser investigada.

---

## 4.4 O que acontece quando a atividade falha ou o resultado é interpretado incorretamente?

**[H]**

Uma interpretação incorreta pode levar o usuário a compreender de maneira equivocada o comportamento da aplicação.

Por exemplo, uma alteração realizada no sistema pode ser considerada irrelevante quando possui importância para a análise, ou um comportamento legítimo pode ser interpretado como suspeito.

Além disso, caso o ambiente não consiga registrar determinada atividade, o resultado da análise pode ficar incompleto.

**[H]**

Em um contexto de Segurança da Informação, uma conclusão inadequada pode influenciar decisões posteriores sobre permitir, bloquear, investigar ou encaminhar determinada aplicação.

---

## 4.5 Conte uma situação concreta

**[H]**

Um profissional recebe um arquivo executável cuja procedência ou comportamento ainda não é conhecido.

Antes de executá-lo diretamente em uma máquina utilizada para atividades importantes, ele deseja compreender o que a aplicação realiza durante sua execução.

O profissional precisa executar o arquivo em um ambiente controlado e observar suas ações.

Durante a execução, podem ocorrer criação de processos, alterações em arquivos, modificações de configurações, utilização de recursos e comunicações de rede.

O profissional precisa então analisar essas ocorrências e compreender quais delas são relevantes para determinar o comportamento da aplicação.

Caso as informações estejam dispersas ou sejam difíceis de interpretar, o profissional poderá ter dificuldade para construir uma visão completa do que ocorreu durante a execução.

---

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Microsoft Learn — Windows Sandbox | Existência de ambiente isolado para execução de aplicações e arquivos não confiáveis. | Não representa necessariamente o processo completo de análise comportamental. |
| Microsoft Learn — Process Monitor | Monitoramento de arquivos, Registro e processos/threads em tempo real. | É uma ferramenta técnica de monitoramento, não necessariamente uma solução completa de sandbox/análise. |
| Documentação do Cuckoo Sandbox | Execução e monitoramento de arquivos em ambiente isolado e geração de resultados. | É uma solução específica e não representa todos os possíveis contextos de uso. |
| ANY.RUN — Interactive Sandbox | Demonstra que análise interativa de aplicações/malware pode envolver execução em VM, acompanhamento em tempo real e relatórios. | Produto comercial específico e voltado principalmente à análise de ameaças. |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

**[H]**

A interação poderia ocorrer em um laboratório de Segurança da Informação, ambiente acadêmico de pesquisa, laboratório de ensino, equipe de Segurança da Informação ou ambiente de Infraestrutura de TI.

O contexto dependeria do perfil que for priorizado nas próximas etapas.

---

## 5.2 Em quais dispositivos/equipamentos?

**[H]**

A interação provavelmente ocorreria em um computador desktop ou notebook, utilizando teclado, mouse e monitor para configurar a análise, acompanhar a execução e consultar os resultados.

---

## 5.3 Existem condições físicas relevantes?

**[H]**

Por se tratar de uma atividade predominantemente técnica, a análise provavelmente ocorrerá em ambiente de trabalho ou estudo, com necessidade de concentração e visualização de informações técnicas.

Dependendo do contexto, privacidade das amostras, interrupções e pressão de tempo podem ser fatores relevantes.

**[?] Lacuna de conhecimento**

Ainda não temos evidências suficientes para afirmar quais condições físicas são predominantes para os usuários reais.

---

## 5.4 Existem fatores sociais ou organizacionais?

**[H]**

Em ambientes profissionais, a análise pode estar inserida em uma estrutura organizacional na qual diferentes pessoas possuem responsabilidades distintas.

Um profissional pode realizar a análise, enquanto outro pode ser responsável pela infraestrutura ou tomar decisões com base nos resultados.

Questões como controle de acesso às amostras, responsabilidade sobre análises, compartilhamento de resultados e auditoria podem ser relevantes em determinados contextos.

---

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

**[H]**

Existe potencial necessidade de histórico e rastreabilidade, principalmente porque uma análise pode precisar ser consultada posteriormente, comparada com outra execução ou utilizada como evidência de uma investigação.

Entretanto, a necessidade e o nível de detalhamento do histórico deverão ser investigados antes de serem transformados em requisitos da interface.

---

## 5.6 Um erro pode produzir consequência relevante?

**[H]**

Sim.

Uma interpretação incorreta dos resultados pode levar a uma compreensão equivocada do comportamento da aplicação.

Em um contexto de Segurança da Informação, isso pode influenciar decisões relacionadas à investigação ou utilização de determinada aplicação.

Também existe a possibilidade de falhas técnicas no próprio ambiente de análise produzirem resultados incompletos ou incorretos.

---

# 6. Entendendo mercado e alternativas existentes

> **Observação:** esta seção representa apenas um levantamento inicial. A análise aprofundada será realizada na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Windows Sandbox | Usuários técnicos e não técnicos | Executar aplicações/arquivos em ambiente isolado. | [F] |
| Process Monitor | Profissionais técnicos | Monitorar arquivos, Registro e processos/threads. | [F] |
| Cuckoo Sandbox | Pesquisadores/analistas de segurança | Executar e analisar arquivos em ambiente isolado. | [F] |
| ANY.RUN | Analistas/SOC/pesquisadores | Análise interativa de malware e ameaças. | [F] |
| Joe Sandbox | Analistas/pesquisadores | Análise automatizada e detalhada de arquivos/URLs suspeitos. | [F] |

---

## 6.2 Existem produtos que atuam na mesma área?

**[F]**

Sim.

Existem soluções especificamente destinadas à execução e análise de aplicações ou arquivos potencialmente maliciosos, como ANY.RUN, Joe Sandbox e Cuckoo Sandbox.

Também existem ferramentas de isolamento e monitoramento que podem ser utilizadas em atividades relacionadas, como Windows Sandbox e Process Monitor.

---

## 6.3 Quais interfaces profissionais esse público já conhece?

**[H]**

Dependendo do perfil, os usuários podem estar familiarizados com:

- ferramentas de monitoramento;
- gerenciadores de processos;
- terminais e consoles;
- ferramentas de análise de logs;
- dashboards de segurança;
- ferramentas de análise de rede;
- ambientes virtualizados;
- interfaces de sandbox;
- sistemas de geração de relatórios.

A Entrega 2 deverá investigar essas interfaces de maneira mais aprofundada.

---

## 6.4 O que essas soluções parecem fazer bem?

**[F/H]**

As soluções analisadas inicialmente demonstram diferentes formas de facilitar a observação do comportamento das aplicações.

O Windows Sandbox prioriza a criação de um ambiente isolado e descartável, com uma experiência relativamente simples para execução de aplicações.

O Process Monitor oferece grande quantidade de informações técnicas e recursos de filtragem para investigar eventos específicos.

O ANY.RUN utiliza interação em tempo real com o ambiente e apresenta relatórios voltados à análise de ameaças.

O Joe Sandbox combina configuração da análise, execução, interação e geração de relatórios detalhados.

O Cuckoo organiza diferentes resultados da análise, incluindo logs, relatórios e arquivos produzidos durante a execução.

---

## 6.5 O que parecem fazer mal, dificultar ou não atender?

**[?]**

Ainda não podemos afirmar quais problemas de usabilidade são efetivamente encontrados pelos usuários dessas soluções sem realizar uma análise sistemática das interfaces e de avaliações/experiências de usuários.

**[H]**

Uma questão que merece investigação é o equilíbrio entre a grande quantidade de informações técnicas disponíveis e a capacidade do usuário de identificar rapidamente os eventos mais relevantes para sua tarefa.

Essa questão será investigada especialmente na **Entrega 2**.

---

## 6.6 Que padrões de interface ou vocabulário parecem familiares?

**[H]**

Alguns termos parecem recorrentes no domínio, como:

- análise;
- execução;
- processo;
- arquivo;
- evento;
- rede;
- log;
- relatório;
- amostra;
- sandbox;
- ambiente;
- comportamento;
- alerta;
- resultado.

Também parecem recorrentes padrões como seleção/upload de arquivo, configuração de parâmetros, execução de análise, acompanhamento de eventos e consulta de resultados.

A familiaridade desses termos deverá ser investigada com maior profundidade na análise de concorrência.

---

# 7. Derivando o escopo de IHC

## 7.1 Escolha do caminho

### Caminho A — TCC já possui interface

> **Não se aplica**, pois o TCC não prevê originalmente uma interface de usuário.

### Caminho B — TCC não possui interface prevista

#### 1. Quem poderia contratar/adotar a solução?

**[H]**

- empresas com equipes de Segurança da Informação;
- equipes de Infraestrutura de TI;
- laboratórios de pesquisa;
- instituições de ensino;
- laboratórios acadêmicos;
- pesquisadores independentes.

#### 2. Quem seria o usuário direto?

**[H]**

> Profissionais de Segurança da Informação, profissionais de Infraestrutura de TI, pesquisadores e estudantes.

#### 3. Quem administraria/configuraria?

**[H]**

> Profissionais responsáveis pela infraestrutura ou pela administração do ambiente de análise.

#### 4. Quem interpretaria resultados?

**[H]**

> Profissionais de Segurança da Informação, Infraestrutura, pesquisadores ou estudantes, dependendo do contexto.

#### 5. Quem tomaria decisões?

**[H]**

> O próprio profissional que realiza a análise ou, em um ambiente organizacional, um responsável pela Segurança da Informação ou Infraestrutura que utilize os resultados para apoiar uma decisão.

#### 6. Quais dados/entradas seriam necessários?

**[H]**

- aplicação/arquivo a ser analisado;
- parâmetros da execução;
- duração da análise;
- configurações do ambiente;
- eventualmente parâmetros específicos da aplicação.

#### 7. Quais resultados deveriam ser compreendidos?

**[H]**

- processos;
- alterações em arquivos;
- alterações em configurações;
- utilização de recursos;
- atividades de rede;
- eventos registrados;
- sequência temporal de ações;
- possíveis comportamentos suspeitos;
- resumo da execução;
- evidências detalhadas.

#### 8. Que erros/rupturas seriam possíveis?

**[H]**

- falha na execução;
- aplicação incompatível;
- monitoramento incompleto;
- excesso de eventos;
- dificuldade de interpretação;
- perda de evidências;
- configuração inadequada do ambiente;
- falha na coleta de informações.

---

# 7.2 Qual perfil será priorizado?

Neste momento, propõe-se:

> **Analista de Segurança da Informação**

### Por que esse perfil foi escolhido?

**[H]**

O perfil foi escolhido inicialmente por apresentar forte relação entre suas atividades potenciais e a capacidade central do TCC: executar aplicações potencialmente não confiáveis, observar seu comportamento e interpretar evidências produzidas durante a execução.

Entretanto, essa escolha ainda deverá ser validada pela investigação das próximas entregas.

Profissionais de Infraestrutura, pesquisadores e estudantes também permanecerão como perfis relevantes para o projeto.

---

# 7.3 Qual objetivo será priorizado?

> **Compreender o comportamento de uma aplicação potencialmente não confiável durante sua execução, utilizando as evidências coletadas no ambiente controlado para identificar suas ações e seus efeitos sobre o sistema operacional.**

---

# 7.4 Que interface será explorada?

> **Para fins da disciplina de IHC, será projetada uma interface que permita ao analista de Segurança da Informação utilizar a capacidade de execução controlada e monitoramento do sandbox para analisar aplicações potencialmente não confiáveis, acompanhar seu comportamento e interpretar os resultados obtidos durante a execução, no contexto de uma investigação técnica em ambiente controlado.**

---

# 7.5 Qual é a relação dessa interface com o TCC?

- [ ] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [x] **É uma extensão conceitual criada para a disciplina.**
- [x] **É um protótipo demonstrativo de aplicação potencial.**
- [ ] Outra.

> A interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | **Sim** | Apresentar resumo do comportamento e estado da análise. | [H] |
| Configuração/parametrização | **Sim** | Definir parâmetros antes da execução. | [H] |
| Entrada/upload/seleção | **Sim** | Selecionar a aplicação a ser analisada. | [H] |
| Acompanhamento de processamento | **Sim** | Acompanhar a execução e eventos em tempo real. | [H] / soluções existentes |
| Relatório/resultados | **Sim** | Consolidar e interpretar evidências. | [H] / soluções existentes |
| Histórico com busca/filtros | **Talvez** | Consultar análises anteriores. | [H] |
| Comparação de resultados | **Talvez** | Comparar execuções ou aplicações. | [H] |
| Explicabilidade/detalhamento | **Sim** | Permitir investigar eventos específicos. | [H] |
| Administração/configurações globais | **Talvez** | Administrar o ambiente. | [H] |
| Usuários/perfis/permissões | **Talvez** | Controlar acesso em contexto organizacional. | [?] |
| CRUD de entidade do domínio | **Não inicialmente** | Nenhuma necessidade identificada. | [H] |
| Auditoria/logs | **Sim** | Registrar e consultar eventos da análise. | [H] |
| Alertas/ocorrências | **Sim** | Destacar eventos potencialmente relevantes. | [H] |
| Ajuda/documentação | **Talvez** | Explicar informações técnicas para diferentes perfis. | [H] |

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Compreensão mais aprofundada do comportamento da aplicação | Dificuldade de observar todas as ações realizadas durante a execução | Analista de Segurança | [H] |
| Organização das evidências | Grande quantidade de informações técnicas | Analista/Pesquisador | [H] |
| Acompanhamento da execução | Necessidade de observar eventos durante o processamento | Analista | [H] |
| Consulta estruturada dos resultados | Necessidade de compreender o que ocorreu | Todos os perfis | [H] |
| Apoio à investigação | Necessidade de analisar aplicações desconhecidas | Segurança/Infraestrutura | [H] |
| Ambiente para experimentação | Necessidade de executar aplicações em contexto controlado | Pesquisadores/Estudantes | [H] |

---

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Selecionar uma aplicação | Iniciar uma análise | Alta |
| F02 | Configurar parâmetros da execução | Definir o contexto da análise | Alta |
| F03 | Iniciar uma execução | Observar o comportamento da aplicação | Alta |
| F04 | Acompanhar a execução | Identificar eventos relevantes | Alta |
| F05 | Consultar processos | Compreender atividades realizadas | Alta |
| F06 | Consultar alterações em arquivos/configurações | Identificar efeitos sobre o SO | Alta |
| F07 | Consultar atividades de rede | Compreender comunicações realizadas | Média/Alta |
| F08 | Consultar utilização de recursos | Avaliar comportamento e impacto | Média |
| F09 | Consultar eventos detalhados | Investigar comportamentos específicos | Alta |
| F10 | Visualizar resumo da análise | Compreender rapidamente o resultado | Alta |
| F11 | Gerar/consultar relatório | Documentar os resultados | Alta |
| F12 | Consultar histórico | Recuperar análises anteriores | Média |

---

# 9.3 Tecnologias/restrições já definidas no TCC

Como o exercício determina que a tecnologia apareça **depois do entendimento do uso**, neste momento podemos registrar apenas as restrições que já estão relacionadas ao domínio.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Ambiente sandbox | Necessário para executar aplicações de forma controlada. | O usuário poderá precisar selecionar/configurar o ambiente de execução. |
| Sistema operacional hospedeiro | O comportamento da aplicação será observado em relação ao SO. | Informações apresentadas deverão fazer sentido dentro do contexto do SO analisado. |
| Isolamento | Reduzir o impacto direto da aplicação sobre o ambiente principal. | O estado e as limitações do ambiente deverão ser compreensíveis ao usuário. |
| Monitoramento | Necessário para coletar informações sobre a execução. | A interface poderá apresentar grande quantidade de eventos. |
| Coleta de eventos | Necessária para posterior análise. | Será necessário organizar e priorizar informações para evitar sobrecarga cognitiva. |

---

# 10. Hipóteses e dúvidas prioritárias

Estas são as hipóteses consideradas mais importantes para as próximas entregas:

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| **H01** | Usuários podem se beneficiar de uma análise aprofundada do comportamento de aplicações em ambiente controlado. | É a justificativa central da aplicação prática. | Entregas 2, 3 e 7 |
| **H02** | Processos, arquivos, configurações, rede e recursos estão entre as informações relevantes para compreender o comportamento de uma aplicação. | Define quais dados deverão receber destaque. | Entregas 2, 3 e 7 |
| **H03** | A quantidade de informações produzidas durante uma análise pode dificultar sua interpretação. | Influencia diretamente a organização da interface. | Entregas 2, 3 e 7 |
| **H04** | Diferentes perfis — Segurança, Infraestrutura, pesquisa e ensino — possuem necessidades distintas ao analisar aplicações. | Pode exigir diferentes formas de apresentação das informações. | Entregas 2 e 3 |
| **H05** | Um relatório estruturado pode facilitar a compreensão e documentação dos resultados. | Pode justificar uma funcionalidade central da interface. | Entregas 2, 3 e 7 |
| **H06** | O histórico de análises pode ser útil para consulta e comparação posterior. | Define se histórico/comparação devem fazer parte do escopo. | Entregas 2, 3 e 7 |
| **H07** | Uma interface que organiza eventos técnicos em informações contextualizadas pode facilitar a interpretação em comparação com logs brutos. | É uma hipótese central de IHC sobre apresentação da informação. | Entregas 2, 3 e 7 |
| **H08** | Analistas de Segurança constituem o perfil mais adequado para ser o usuário prioritário. | Define persona, tarefas e protótipo posteriores. | Entregas 2 e 3 |
| **H09** | Pesquisadores e estudantes possuem necessidades suficientemente relevantes para serem considerados usuários do sistema. | Define amplitude do público-alvo. | Entregas 2 e 3 |
| **H10** | A interface deve apresentar tanto uma visão resumida quanto informações técnicas detalhadas. | Pode definir arquitetura de informação e níveis de detalhe. | Entregas 2, 3 e 7 |

> Essas hipóteses deverão ser registradas também na `RASTREABILIDADE.md`.

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Implementar e analisar um ambiente sandbox capaz de executar aplicações potencialmente não confiáveis de forma controlada e observar seus comportamentos e efeitos sobre o sistema operacional. |
| O TCC já previa interface? | Não. |
| Quem é o usuário prioritário de IHC? | Inicialmente, o Analista de Segurança da Informação. A escolha ainda é uma hipótese. |
| O que ele precisa alcançar? | Compreender o comportamento de uma aplicação durante sua execução e analisar seus efeitos sobre o sistema operacional. |
| Qual problema/atividade será estudado? | A execução controlada e análise aprofundada do comportamento de aplicações potencialmente não confiáveis. |
| Como isso acontece hoje? | Por meio de diferentes ferramentas e abordagens de isolamento, monitoramento e análise. A combinação utilizada pelo público-alvo ainda precisa ser investigada. |
| Qual é o contexto de uso? | Ambientes de Segurança da Informação, Infraestrutura, pesquisa e ensino. |
| Que interface/recorte será explorado? | Interface para seleção, execução, acompanhamento, visualização, interpretação e documentação dos resultados de análises realizadas no sandbox. |
| Como a interface se relaciona ao TCC? | É uma extensão conceitual/protótipo demonstrativo criado para a disciplina de IHC. |
| Quais pontos ainda são hipóteses? | H01–H10, principalmente necessidades dos usuários, relevância das informações, público prioritário e benefícios da interface. |

---

# 12. Delimitação

## Dentro do escopo de IHC

Investigação das pessoas que poderiam utilizar o sandbox, suas atividades, objetivos, necessidades e dificuldades, além do projeto de uma possível interface para selecionar aplicações, iniciar e acompanhar análises, visualizar eventos, interpretar resultados e gerar/consultar relatórios.

## Fora do escopo de IHC

A implementação dos mecanismos internos de isolamento, monitoramento, execução e coleta de eventos do sandbox, exceto quando esses aspectos forem necessários para compreender as possibilidades e limitações da interação.

## Dentro do escopo formal do TCC

Implementação e análise do ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis e investigação dos comportamentos e efeitos produzidos por essas aplicações no sistema operacional.

## A interface da disciplina será implementada no TCC?

> **Não definido.**

Inicialmente, a interface será considerada um artefato de aprendizagem e protótipo demonstrativo da disciplina de IHC.

Sua eventual implementação ou incorporação ao TCC dependerá de decisão posterior da equipe e do orientador.

---

# 13. Como esta entrega alimenta as próximas

- **Entrega 2:** investigar concorrentes, ferramentas análogas e interfaces profissionais.
- **Entrega 3:** aprofundar os perfis de Segurança, Infraestrutura, pesquisa e ensino e definir personas/contextos.
- **Entrega 4:** transformar as dificuldades encontradas em cenários concretos.
- **Entrega 5:** decompor as atividades principais em tarefas.
- **Entrega 6:** experimentar diferentes alternativas de interação.
- **Entrega 7:** investigar as hipóteses com dados.
- **Entrega 8:** estabelecer metas e critérios de usabilidade.
- **Entregas 9–11:** transformar o conhecimento acumulado em modelo de interação, MoLIC e protótipo.
- **Entregas 12–14:** avaliar e melhorar a interface.

A Entrega 1 estabelece a base conceitual para as etapas seguintes. As hipóteses levantadas poderão ser confirmadas, modificadas ou descartadas conforme novas evidências sejam obtidas.

---

# 14. Relação com INOVA e comunicação do projeto

> **Problema/atividade humana:** Pessoas que trabalham ou estudam com sistemas operacionais podem precisar compreender de forma aprofundada o que uma aplicação realiza durante sua execução, especialmente quando seu comportamento ainda é desconhecido.
>
> **Contribuição técnica do TCC:** O projeto implementa e analisa um ambiente sandbox capaz de executar aplicações potencialmente não confiáveis de forma controlada e observar seus comportamentos e efeitos sobre o sistema operacional.
>
> **Como uma pessoa poderia utilizar essa contribuição:** Um usuário poderia executar uma aplicação no ambiente controlado, acompanhar os eventos produzidos, analisar as alterações realizadas e consultar um relatório estruturado sobre seu comportamento.

---

# 15. Referências iniciais

- MICROSOFT. **Windows Sandbox**. Microsoft Learn.
- MICROSOFT. **Process Monitor**. Microsoft Sysinternals.
- CUCKOO SANDBOX. **Cuckoo Sandbox Documentation**.
- ANY.RUN. **Interactive Online Malware Sandbox**.
- JOE SANDBOX. **Automated Malware Analysis**.

> As referências serão aprofundadas e formalizadas ao longo das próximas entregas, especialmente durante a análise de concorrência da Entrega 2.
