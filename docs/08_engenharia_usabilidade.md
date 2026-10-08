# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 08/10/2026  
**Status:** 🟩 Concluído  
**Responsável:** Luiggi Paschoalini Garcia  
**Projeto:** Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.

## Objetivo da atividade

Definir as características do sistema interativo, os princípios de projeto, as metas de usabilidade e o planejamento de avaliação e evolução da interface proposta para o ambiente sandbox.

A atividade busca estabelecer critérios que permitam verificar se os usuários conseguem compreender o comportamento de aplicações executadas em ambiente controlado, identificar processos e eventos relevantes e consultar evidências de maneira eficaz, eficiente e satisfatória.

As decisões apresentadas consideram as entregas anteriores da disciplina de Interface Humano-Computador e estabelecem uma base para as próximas etapas de projeto e avaliação.

**Delimitação:** esta entrega documenta as decisões de engenharia de usabilidade e os critérios para avaliação futura. As metas quantitativas são objetivos propostos, não resultados de testes já realizados.

---

## 1. Delimitação do sistema interativo

### 1.1 Contexto do projeto

O Trabalho de Conclusão de Curso tem como tema:

**Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.**

A contribuição técnica prevista envolve a implementação e a análise de mecanismos para execução controlada de aplicações, observação de seu comportamento e coleta de informações sobre suas interações com o sistema operacional.

A proposta de interface desenvolvida na disciplina de IHC busca facilitar a consulta e a interpretação dessas informações.

O problema central de interação é:

**Como apresentar uma grande quantidade de informações técnicas produzidas por uma análise sandbox de maneira que o usuário consiga compreender o comportamento da aplicação e investigar os detalhes relevantes?**

### 1.2 Sistema interativo proposto

O sistema interativo consiste em um dashboard de análise comportamental que apresenta informações relacionadas à execução controlada de uma aplicação.

A interface deverá permitir que o usuário:

- Identifique a aplicação analisada.
- Consulte o estado da execução.
- Visualize os processos identificados.
- Consulte eventos registrados durante a execução.
- Identifique operações relacionadas a arquivos, configurações, rede e recursos do sistema, quando essas informações estiverem disponíveis.
- Investigue os eventos associados a um processo.
- Consulte detalhes e evidências de uma atividade.
- Diferencie operações tentadas de operações efetivamente confirmadas.
- Reconheça situações em que os dados coletados são insuficientes ou indisponíveis.

A interface não deverá apresentar uma operação como concluída quando os dados disponíveis indicarem apenas uma tentativa ou não permitirem confirmar seu resultado.

### 1.3 Separação entre o TCC e o projeto de IHC

| Elemento | Escopo |
|---|---|
| Ambiente sandbox | Execução controlada e isolamento de aplicações potencialmente não confiáveis. |
| Monitoramento | Observação e coleta das atividades executadas pela aplicação no sistema operacional. |
| Processamento | Organização dos eventos e das evidências obtidas. |
| Interface de IHC | Apresentação dos resultados e apoio à investigação pelo usuário. |
| Avaliação de usabilidade | Verificação da compreensão, navegação, eficiência e satisfação durante as tarefas. |

A interface poderá ser utilizada como referência para uma futura implementação no TCC, mas sua prototipação na disciplina de IHC não estabelece automaticamente a obrigação de implementá-la integralmente no trabalho técnico.

### 1.4 Plataformas consideradas

Serão mantidas duas alternativas de plataforma:

**Alternativa A — Interface Web**

Dashboard acessado por navegador, com apresentação dos resultados por meio de uma aplicação Web.

**Alternativa B — Interface Desktop**

Aplicação gráfica executada localmente em um sistema operacional, como Windows ou Linux.

A escolha definitiva entre as alternativas dependerá da arquitetura do sandbox, das tecnologias utilizadas, das necessidades de integração e das restrições identificadas durante o desenvolvimento.

Não está prevista, neste momento, a obrigação de implementar ambas as interfaces.

Os requisitos de usabilidade serão definidos de maneira independente da tecnologia, sempre que possível, permitindo que sejam aplicados à alternativa selecionada.

### 1.5 Persona, cenário e tarefas

**Persona prioritária:**

P01 — Rafael Mendes, Analista de Segurança da Informação.

Trata-se de uma proto-persona elaborada nas entregas anteriores, ainda sujeita à validação com usuários.

**Cenário:**

C01 — Investigação do comportamento de uma aplicação potencialmente não confiável.

**Tarefas:**

- **T01:** Analisar o comportamento da aplicação após a execução controlada.
- **T02:** Interpretar as evidências coletadas.
- **T03:** Investigar e consolidar os resultados.

### 1.6 Fluxos principais

Os fluxos definidos anteriormente serão preservados:

| ID | Fluxo | Objetivo |
|---|---|---|
| PF01 | Consultar o dashboard | Identificar o estado da execução e compreender o resumo das atividades. |
| PF02 | Investigar um processo | Consultar informações e eventos associados a um processo. |
| PF03 | Investigar um evento | Identificar o tipo de operação, o recurso envolvido e o resultado registrado. |
| PF04 | Retornar à visão geral | Recuperar o contexto após consultar informações detalhadas. |

As telas correspondentes são:

- **P01 — Dashboard da execução.**
- **P02 — Detalhes do processo.**
- **P03 — Detalhes do evento.**

---

## 2. Características da plataforma

### 2.1 Características gerais

| Dimensão | Característica proposta | Implicação para a interface |
|---|---|---|
| Software | Aplicação Web ou Desktop. | Preservar os mesmos fluxos e conceitos de interação nas alternativas. |
| Sistema operacional | Windows ou Linux, conforme a implementação. | Considerar as diferenças de integração e apresentação de informações do sistema. |
| Hardware | Computador ou notebook. | Priorizar visualização de tabelas, processos e informações técnicas em telas maiores. |
| Entrada | Mouse e teclado. | Disponibilizar controles identificáveis e navegação acessível. |
| Saída | Interface gráfica com tabelas, indicadores e painéis. | Organizar informações por categorias e níveis de detalhamento. |
| Processamento | Dados provenientes do monitoramento e da análise. | Apresentar estados de carregamento e disponibilidade das informações. |
| Conectividade | Dependente da arquitetura escolhida. | Não pressupor conexão com a internet para consultar resultados locais. |
| Segurança | Separação entre ambiente de execução, monitoramento e apresentação. | Evitar exposição desnecessária de dados e ações privilegiadas pela interface. |
| Volume de informações | Possibilidade de grande quantidade de eventos. | Considerar organização, agrupamento, pesquisa e filtros. |
| Disponibilidade | Informações podem estar incompletas ou indisponíveis. | Apresentar mensagens claras sobre limitações dos dados. |

### 2.2 Alternativa A — Interface Web

A interface Web poderá utilizar tecnologias de desenvolvimento de aplicações para navegador.

**Possíveis vantagens:**

- Flexibilidade na construção de dashboards.
- Facilidade de organização de tabelas e painéis.
- Possibilidade de acesso por diferentes sistemas operacionais.
- Separação entre apresentação e processamento.

**Possíveis restrições:**

- Necessidade de comunicação com os componentes responsáveis pela coleta e pelo processamento dos dados.
- Dependência de um serviço local ou remoto, conforme a arquitetura.
- Necessidade de controlar o acesso aos dados disponibilizados.
- Possíveis diferenças de comportamento entre navegadores.

A utilização de uma interface Web não implica que o ambiente sandbox precise executar aplicações remotamente ou disponibilizar dados pela internet.

### 2.3 Alternativa B — Interface Desktop

A interface Desktop poderá ser desenvolvida utilizando tecnologias de aplicações gráficas nativas ou multiplataforma.

**Possíveis vantagens:**

- Integração com componentes e serviços locais.
- Execução em uma janela própria do sistema operacional.
- Possibilidade de funcionamento sem navegador.
- Utilização de recursos de interface adequados à apresentação de informações técnicas.

**Possíveis restrições:**

- Necessidade de distribuição e configuração da aplicação.
- Diferenças entre Windows e Linux.
- Dependência das bibliotecas gráficas selecionadas.
- Necessidade de controlar permissões e comunicação com os componentes de monitoramento.

Python com PySide6 constitui uma alternativa tecnológica inicial para o desenvolvimento de uma interface Desktop, sem representar uma decisão definitiva.

### 2.4 Decisão atual sobre a plataforma

**Decisão:** manter Web e Desktop como alternativas viáveis, sem escolher uma plataforma definitiva nesta entrega.

**Justificativa:** o objetivo atual é definir os requisitos de interação e usabilidade antes de estabelecer a implementação tecnológica.

As duas alternativas deverão permitir a realização das tarefas principais de investigação.

A escolha posterior deverá considerar:

1. Compatibilidade com o sistema operacional utilizado pelo sandbox.
2. Integração com os mecanismos de monitoramento.
3. Complexidade de desenvolvimento e manutenção.
4. Requisitos de segurança.
5. Facilidade de utilização pelo público-alvo.
6. Capacidade de apresentar eventos e processos de maneira organizada.

### 2.5 Restrições e premissas

- O monitoramento poderá produzir diferentes categorias de eventos conforme a tecnologia implementada.
- Nem todas as informações previstas na interface estarão necessariamente disponíveis.
- O protótipo poderá utilizar dados simulados, identificados como demonstrativos.
- Os dados simulados não comprovam o funcionamento do sandbox.
- O desempenho da interface dependerá do volume de dados e da arquitetura escolhida.
- A interface deverá informar limitações conhecidas da coleta.
- Não serão adicionadas funcionalidades administrativas sem necessidade identificada.
- A avaliação de usabilidade deverá considerar a plataforma efetivamente utilizada no protótipo avaliado.

---

## 3. Princípios gerais de projeto

### 3.1 Referenciais de usabilidade

A engenharia de usabilidade será orientada pelos conceitos de eficácia, eficiência e satisfação apresentados na ISO 9241-11:2018.

Para este projeto:

- **Eficácia:** capacidade do usuário de realizar corretamente as tarefas de investigação.
- **Eficiência:** recursos, tempo e esforço necessários para realizar essas tarefas.
- **Satisfação:** percepção do usuário sobre a clareza, facilidade e adequação da interface.

Também serão considerados princípios de design centrado no usuário, consistência, visibilidade do estado do sistema, prevenção de erros e acessibilidade.

As recomendações das WCAG 2.2 poderão orientar aspectos de acessibilidade aplicáveis à interface, especialmente contraste, identificação de controles, navegação por teclado e apresentação não exclusivamente visual das informações.

### 3.2 Princípios aplicados ao projeto

| ID | Princípio | Aplicação proposta |
|---|---|---|
| PR01 | Visibilidade do estado do sistema | Exibir claramente se a execução está em andamento, concluída ou apresenta falha. |
| PR02 | Consistência | Manter terminologia, categorias e padrões de navegação entre as telas. |
| PR03 | Hierarquia da informação | Apresentar primeiro o resumo e permitir acesso progressivo aos detalhes. |
| PR04 | Reconhecimento em vez de memorização | Disponibilizar identificação clara dos processos, eventos e controles. |
| PR05 | Prevenção de erros de interpretação | Distinguir tentativas, operações confirmadas e resultados desconhecidos. |
| PR06 | Controle e liberdade do usuário | Permitir retornar às telas anteriores e recuperar o contexto de investigação. |
| PR07 | Clareza e simplicidade | Evitar elementos e funcionalidades sem relação com as tarefas prioritárias. |
| PR08 | Feedback | Informar carregamento, ausência de dados, falhas e indisponibilidade de informações. |
| PR09 | Acessibilidade | Considerar contraste, foco visível, teclado e identificação textual de estados. |
| PR10 | Rastreabilidade | Relacionar informações apresentadas aos eventos e às evidências disponíveis. |

### 3.3 Aplicação nas telas

**P01 — Dashboard da execução**

Deverá priorizar:

- Identificação da aplicação.
- Estado da execução.
- Resumo dos processos e eventos.
- Lista de processos.
- Atividades recentes.
- Acesso às informações detalhadas.

**P02 — Detalhes do processo**

Deverá priorizar:

- Identificação do processo.
- PID e demais atributos disponíveis.
- Estado do processo.
- Relação com outros processos, quando disponível.
- Eventos associados.
- Retorno ao dashboard.

**P03 — Detalhes do evento**

Deverá priorizar:

- Tipo de evento.
- Data e horário.
- Processo associado.
- Recurso envolvido.
- Operação observada.
- Resultado registrado.
- Evidências disponíveis.
- Retorno ao processo ou à visão geral.

### 3.4 Tratamento de estados excepcionais

| Situação | Comportamento esperado |
|---|---|
| Execução em andamento | Apresentar indicador de execução e dados disponíveis até o momento. |
| Execução concluída | Informar a conclusão e permitir consultar os resultados. |
| Falha na execução | Exibir mensagem de falha sem apresentar resultados incompletos como definitivos. |
| Nenhum evento encontrado | Informar que não foram encontrados eventos nos dados consultados. |
| Resultado desconhecido | Indicar que não foi possível confirmar o resultado da operação. |
| Dados indisponíveis | Informar a indisponibilidade e evitar exibir valores enganosos. |
| Grande volume de eventos | Disponibilizar mecanismos de organização e consulta conforme a necessidade validada. |

---

## 4. Metas de usabilidade

### 4.1 Objetivo das metas

As metas de usabilidade estabelecem critérios verificáveis para avaliar a qualidade da interação.

Serão consideradas três dimensões principais:

1. Eficácia.
2. Eficiência.
3. Satisfação.

Também será avaliada a compreensão correta das informações, devido à importância da interpretação das evidências no contexto de Segurança da Informação.

### 4.2 Metas qualitativas

| ID | Meta qualitativa | Resultado esperado |
|---|---|---|
| MQ01 | Compreensão da execução | O usuário compreende o estado da execução e o significado dos indicadores apresentados. |
| MQ02 | Clareza das informações | O usuário diferencia processos, eventos e resultados de operações. |
| MQ03 | Facilidade de navegação | O usuário compreende como acessar detalhes e retornar à visão geral. |
| MQ04 | Confiança na interpretação | O usuário reconhece quando os dados não permitem confirmar uma conclusão. |
| MQ05 | Organização das informações | O usuário consegue localizar categorias e evidências sem depender de explicações constantes. |

### 4.3 Metas quantitativas

Os limites definidos são metas iniciais de projeto. Sua adequação poderá ser revisada após avaliações com usuários.

| ID | Dimensão | Tarefa avaliada | Métrica | Meta |
|---|---|---|---|---|
| MU01 | Eficácia | Identificar o estado e o resumo da execução. | Taxa de conclusão sem ajuda. | ≥ 80% |
| MU02 | Eficácia | Localizar um processo e seus eventos relacionados. | Taxa de conclusão sem ajuda. | ≥ 80% |
| MU03 | Eficiência | Localizar os detalhes de um evento específico. | Mediana do tempo de conclusão. | ≤ 90 segundos |
| MU04 | Compreensão | Diferenciar tentativa de operação e alteração confirmada. | Percentual de respostas corretas. | ≥ 80% |
| MU05 | Satisfação | Avaliar a facilidade de realização das tarefas. | Média das avaliações em escala de 1 a 5. | ≥ 4,0 |
| MU06 | Navegação | Retornar dos detalhes ao dashboard. | Taxa de conclusão sem ajuda. | ≥ 90% |

### 4.4 Priorização das metas

| Meta | Peso | Justificativa |
|---|---|---|
| MU01 | 20% | Compreender o estado da execução é necessário para iniciar a investigação. |
| MU02 | 20% | A investigação dos processos constitui uma atividade central da interface. |
| MU03 | 15% | O acesso eficiente aos detalhes reduz o esforço de investigação. |
| MU04 | 20% | A interpretação incorreta de uma operação pode comprometer as conclusões do usuário. |
| MU05 | 15% | A satisfação contribui para avaliar a percepção de facilidade e adequação da interface. |
| MU06 | 10% | A navegação de retorno é importante para manter o contexto da investigação. |
| **Total** | **100%** | |

A priorização atribui maior importância à eficácia e à compreensão das informações, considerando a finalidade técnica do sistema.

### 4.5 Operacionalização das métricas

**MU01 — Identificação do estado da execução**

O participante receberá a tarefa de identificar o estado atual de uma execução e explicar os principais indicadores do dashboard.

A tarefa será considerada concluída quando o participante identificar corretamente o estado e as informações solicitadas sem ajuda do avaliador.

**MU02 — Localização de um processo**

O participante deverá localizar um processo previamente definido no cenário de teste e acessar os eventos associados.

A tarefa será considerada concluída quando o processo correto e seus eventos forem encontrados sem ajuda.

**MU03 — Consulta dos detalhes de um evento**

O participante deverá localizar um evento específico e consultar suas informações.

O tempo será medido desde a apresentação da tarefa até a identificação correta do evento e de seus detalhes.

A mediana será calculada a partir dos tempos dos participantes que concluírem a tarefa. Falhas e desistências serão registradas separadamente, evitando que uma mediana favorável oculte dificuldades de conclusão.

**MU04 — Interpretação do resultado de uma operação**

O participante deverá analisar uma situação apresentada na interface e identificar se:

- A operação foi apenas tentada.
- A operação foi confirmada como concluída.
- O resultado não pode ser determinado com os dados disponíveis.

A resposta será comparada ao resultado previamente definido no cenário de avaliação.

**MU05 — Satisfação**

Após as tarefas, o participante avaliará a facilidade de uso em uma escala de cinco pontos:

1. Muito insatisfeito.
2. Insatisfeito.
3. Neutro.
4. Satisfeito.
5. Muito satisfeito.

Será calculada a média das avaliações válidas.

**MU06 — Retorno ao dashboard**

O participante deverá retornar à visão geral após consultar os detalhes de um processo ou evento.

A conclusão será registrada quando conseguir retornar sem orientação do avaliador.

### 4.6 Condições de avaliação

Para permitir a comparação dos resultados, as avaliações deverão utilizar:

- Cenários de teste padronizados.
- Tarefas descritas previamente.
- Dados demonstrativos equivalentes para os participantes.
- Critérios claros de sucesso e falha.
- Registro do tempo quando aplicável.
- Identificação da plataforma utilizada.
- Registro de intervenções do avaliador.
- Coleta de comentários e dificuldades observadas.

As tarefas deverão ser aplicadas preferencialmente a participantes com experiência ou familiaridade com Segurança da Informação, Infraestrutura ou análise de sistemas.

Os resultados deverão apresentar números absolutos e percentuais, considerando as limitações de amostras pequenas.

### 4.7 Critérios de verificação

| Meta | Critério de atendimento |
|---|---|
| MU01 | Pelo menos 80% dos participantes identificam corretamente o estado e o resumo sem ajuda. |
| MU02 | Pelo menos 80% dos participantes encontram o processo e seus eventos sem ajuda. |
| MU03 | A mediana do tempo de conclusão da tarefa é de até 90 segundos, com falhas reportadas separadamente. |
| MU04 | Pelo menos 80% dos participantes interpretam corretamente o resultado da operação. |
| MU05 | A média de satisfação é igual ou superior a 4,0. |
| MU06 | Pelo menos 90% dos participantes retornam ao dashboard sem ajuda. |

Esses critérios serão utilizados nas avaliações posteriores previstas para as Entregas 12 a 14, conforme o planejamento da disciplina.

---

## 5. Ciclo de vida e planejamento da iteração

### 5.1 Abordagem escolhida

Será adotada uma abordagem iterativa e centrada no usuário.

O desenvolvimento da interface deverá considerar continuamente:

1. Compreensão do contexto de uso.
2. Identificação de necessidades.
3. Definição de requisitos e metas.
4. Elaboração de soluções de interface.
5. Avaliação com usuários.
6. Revisão das decisões de projeto.

O processo não será tratado como uma sequência rígida e definitiva. Resultados de avaliações poderão exigir revisões em etapas anteriores.

### 5.2 Relação com as entregas da disciplina

| Etapa | Atividades | Entregas relacionadas |
|---|---|---|
| Compreensão do problema | Identificação do domínio, usuários e dificuldades. | 1 e 2 |
| Compreensão do contexto | Construção de persona e cenário de uso. | 3 e 4 |
| Análise das atividades | Identificação e modelagem das tarefas. | 5 |
| Proposição da solução | Prototipação inicial da interface. | 6 |
| Planejamento da pesquisa | Hipóteses, coleta de dados e aspectos éticos. | 7 |
| Engenharia de usabilidade | Características da plataforma, princípios e metas. | 8 |
| Avaliação e refinamento | Verificação da interação e revisão das soluções. | Entregas posteriores |

### 5.3 Planejamento das iterações

| Iteração | Objetivo | Atividades previstas | Produto esperado |
|---|---|---|---|
| I01 | Estruturar a solução inicial. | Organizar dashboard, processos, eventos e navegação. | Protótipo inicial de baixa fidelidade. |
| I02 | Refinar a organização das informações. | Revisar hierarquia, terminologia, estados e controles. | Protótipo revisado. |
| I03 | Verificar as metas de usabilidade. | Aplicar tarefas e registrar eficácia, eficiência e satisfação. | Resultados de avaliação. |
| I04 | Corrigir problemas identificados. | Priorizar dificuldades e revisar a interface. | Versão aprimorada do protótipo. |

As iterações I02, I03 e I04 representam planejamento e não atividades declaradas como já executadas.

### 5.4 Critérios para priorização de problemas

Os problemas encontrados nas avaliações poderão ser classificados considerando:

- Impacto na realização da tarefa.
- Frequência observada.
- Gravidade da interpretação incorreta.
- Dificuldade de recuperação.
- Relação com as metas de usabilidade.
- Esforço estimado para correção.

Problemas que levem o usuário a interpretar incorretamente uma operação deverão receber prioridade elevada, especialmente quando envolverem a distinção entre uma tentativa e uma alteração confirmada.

### 5.5 Registro das alterações

Cada revisão deverá ser documentada com:

| Campo | Descrição |
|---|---|
| Identificador | Código da alteração. |
| Problema observado | Dificuldade ou falha identificada. |
| Evidência | Registro que fundamenta a necessidade de mudança. |
| Tela afetada | Local da interface relacionado ao problema. |
| Alteração proposta | Modificação prevista. |
| Justificativa | Relação entre o problema e a solução. |
| Meta relacionada | Meta de usabilidade afetada. |
| Resultado da reavaliação | Verificação posterior da alteração, quando realizada. |

Nenhuma alteração deverá ser apresentada como validada empiricamente sem evidências de avaliação.

---

## 6. Rastreabilidade

### 6.1 Relação entre tarefas e metas

| Tarefa | Metas relacionadas |
|---|---|
| T01 — Analisar o comportamento da aplicação após a execução controlada. | MU01, MU02, MU05 |
| T02 — Interpretar as evidências coletadas. | MU03, MU04, MU05 |
| T03 — Investigar e consolidar os resultados. | MU02, MU03, MU04, MU06 |

### 6.2 Relação entre telas e metas

| Tela | Metas relacionadas |
|---|---|
| P01 — Dashboard da execução | MU01, MU02, MU05, MU06 |
| P02 — Detalhes do processo | MU02, MU03, MU05, MU06 |
| P03 — Detalhes do evento | MU03, MU04, MU05, MU06 |

### 6.3 Relação entre princípios e metas

| Princípio | Metas relacionadas |
|---|---|
| PR01 — Visibilidade do estado | MU01 |
| PR02 — Consistência | MU02, MU03, MU06 |
| PR03 — Hierarquia da informação | MU01, MU02, MU03 |
| PR04 — Reconhecimento em vez de memorização | MU02, MU03 |
| PR05 — Prevenção de erros de interpretação | MU04 |
| PR06 — Controle e liberdade do usuário | MU06 |
| PR07 — Clareza e simplicidade | MU01, MU05 |
| PR08 — Feedback | MU01, MU04 |
| PR09 — Acessibilidade | MU02, MU03, MU06 |
| PR10 — Rastreabilidade | MU03, MU04 |

---

## 7. Síntese da entrega

A Entrega 8 estabelece as bases de engenharia de usabilidade para a interface de análise comportamental do ambiente sandbox.

O sistema interativo foi delimitado como um dashboard destinado à consulta de processos, eventos e evidências relacionadas à execução controlada de aplicações.

Foram mantidas duas possibilidades de implementação: **interface Web e interface Desktop**, sem obrigatoriedade de desenvolver ambas. A escolha definitiva será realizada conforme as necessidades técnicas e as restrições identificadas no desenvolvimento do TCC.

Foram estabelecidos dez princípios gerais de projeto, cinco metas qualitativas e seis metas quantitativas de usabilidade, com critérios de medição e prioridades definidas.

Também foi documentado um ciclo de desenvolvimento iterativo, relacionando as entregas anteriores às futuras atividades de avaliação e refinamento.

As metas propostas poderão ser verificadas posteriormente por meio de tarefas padronizadas e avaliações com usuários, permitindo identificar dificuldades e fundamentar melhorias.

**Conclusão:** a documentação de engenharia de usabilidade está concluída. A escolha definitiva da plataforma, a execução dos testes e a verificação das metas permanecem como atividades futuras.

## 8. Checklist de entrega

- [x] Sistema interativo delimitado.
- [x] Relação entre o TCC e o escopo de IHC esclarecida.
- [x] Persona, cenário e tarefas relacionados à proposta.
- [x] Características da plataforma identificadas.
- [x] Alternativas Web e Desktop consideradas.
- [x] Restrições técnicas e premissas documentadas.
- [x] Princípios gerais de projeto definidos.
- [x] Referenciais de usabilidade e acessibilidade considerados.
- [x] Metas qualitativas estabelecidas.
- [x] Metas quantitativas estabelecidas.
- [x] Métricas e critérios de verificação definidos.
- [x] Metas de usabilidade priorizadas.
- [x] Condições de avaliação documentadas.
- [x] Ciclo de vida iterativo definido.
- [x] Planejamento das iterações elaborado.
- [x] Critérios para priorização de problemas definidos.
- [x] Rastreabilidade entre tarefas, telas, princípios e metas documentada.
- [x] Metas preparadas para verificação nas avaliações posteriores.
- [x] Documentação da Entrega 8 concluída.

**Status final da documentação:** 🟩 Concluído.
