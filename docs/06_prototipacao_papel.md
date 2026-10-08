# Entrega 6 — Prototipação em papel

**Data:** 08/10/2026  
**Status:** 🟩 Concluído  
**Responsável:** Luiggi Paschoalini Garcia

## Objetivo

Externalizar ideias de interação por meio de protótipos de baixa fidelidade, permitindo visualizar os principais fluxos da interface e avaliar como o usuário poderá investigar o comportamento de uma aplicação executada em ambiente sandbox.

O processo de prototipação considera o ciclo de construir, simular, observar e revisar, priorizando a organização das informações, a navegação e a compreensão dos resultados.

## 1. Escopo da prototipação

### Persona considerada

**P01 — Rafael Mendes, Analista de Segurança da Informação.**

Persona hipotética utilizada como referência para orientar a organização da interface. Seu objetivo principal é compreender o comportamento de uma aplicação durante a execução controlada, identificando processos, eventos, alterações e evidências relevantes.

### Cenário considerado

**C01 — Investigação do comportamento de uma aplicação potencialmente não confiável.**

O usuário executa uma aplicação em ambiente controlado e precisa analisar as informações coletadas para compreender suas ações no sistema operacional. A interface deve facilitar a identificação de eventos relevantes e permitir a investigação progressiva dos detalhes.

### Tarefas relacionadas

- **T01:** Analisar o comportamento da aplicação após a execução controlada.
- **T02:** Interpretar as evidências coletadas.
- **T03:** Investigar e consolidar os resultados.

### Objetivos da interface

- Apresentar um resumo da execução e de seu estado atual.
- Exibir os processos identificados durante a análise.
- Organizar as atividades observadas, como operações com arquivos, configurações e rede, quando esses dados estiverem disponíveis.
- Permitir a consulta dos detalhes de um processo e dos eventos associados.
- Diferenciar ações observadas de alterações efetivamente registradas.
- Facilitar a navegação entre o resumo e as evidências detalhadas.

A proposta prioriza um dashboard simples de análise, sem reproduzir a interface de ferramentas comerciais existentes ou acrescentar funcionalidades administrativas que não sejam necessárias às tarefas identificadas.

### 1.1 Família de interface escolhida

**Dashboard de análise comportamental**, com telas complementares para consulta de processos e detalhes de eventos.

A escolha é fundamentada na necessidade de organizar uma grande quantidade de informações técnicas e permitir que o usuário passe de uma visão geral para evidências específicas.

## 2. Fluxos escolhidos

| ID | Fluxo | Objetivo | Telas envolvidas |
|---|---|---|---|
| PF01 | Consultar resumo da execução | Compreender o estado da execução e identificar atividades relevantes. | P01 |
| PF02 | Investigar um processo | Consultar informações de um processo e suas atividades relacionadas. | P01 → P02 |
| PF03 | Consultar detalhes de um evento | Compreender uma atividade registrada e sua relação com o processo. | P01 → P02 → P03 |
| PF04 | Retornar à visão geral | Voltar ao resumo após investigar informações específicas. | P03/P02 → P01 |

## 3. Telas e estados

### P01 — Dashboard da execução

**Objetivo:** apresentar a visão geral da execução e permitir identificar rapidamente processos e atividades relevantes.

~~~text
+--------------------------------------------------------------+
| SANDBOX — ANALISE DE EXECUCAO                                |
+--------------------------------------------------------------+
| Aplicacao: exemplo.exe                                       |
| Estado: EM EXECUCAO                 Tempo: 00:02:35            |
+--------------------------------------------------------------+
| RESUMO                                                       |
|                                                              |
| Processos identificados | Eventos registrados | Alertas*      |
|          08             |          42         |      03       |
+--------------------------------------------------------------+
| PROCESSOS                                                    |
|                                                              |
| Nome             PID       Estado       Eventos relacionados |
| exemplo.exe      1520      Em execucao          18           |
| processo_aux.exe 1584      Em execucao          12           |
| servico.exe      1620      Encerrado             05           |
|                                                              |
| [Selecionar processo para consultar detalhes]                |
+--------------------------------------------------------------+
| ATIVIDADES RECENTES                                          |
|                                                              |
| Horario   Tipo          Processo          Resultado registrado|
| 14:02:10  Arquivo       exemplo.exe       Operacao observada  |
| 14:02:14  Processo      exemplo.exe       Processo iniciado   |
| 14:02:21  Rede          processo_aux.exe  Conexao registrada  |
|                                                              |
| [Selecionar evento para consultar detalhes]                  |
+--------------------------------------------------------------+
| *Indicadores dependem dos dados efetivamente coletados.      |
+--------------------------------------------------------------+
~~~

**Elementos de interação:**

- Identificação da aplicação analisada.
- Indicador do estado da execução.
- Resumo quantitativo dos dados coletados.
- Lista de processos identificados.
- Lista de atividades recentes.
- Acesso aos detalhes de processos e eventos.

Os nomes, quantidades, horários e resultados apresentados no desenho são ilustrativos e não representam dados de uma execução real.

### P02 — Detalhes do processo

**Objetivo:** permitir a investigação de um processo específico e a consulta de suas atividades relacionadas.

~~~text
+--------------------------------------------------------------+
| PROCESSO — DETALHES                                          |
+--------------------------------------------------------------+
| [< Voltar ao dashboard]                                      |
|                                                              |
| Nome: exemplo.exe                                            |
| PID: 1520                                                    |
| Processo pai: processo_pai.exe                               |
| Estado: Em execucao                                          |
+--------------------------------------------------------------+
| ATIVIDADES RELACIONADAS                                      |
|                                                              |
| Horario   Tipo          Descricao                            |
| 14:02:10  Arquivo       Operacao em arquivo registrada       |
| 14:02:14  Processo      Processo iniciado                    |
| 14:02:21  Rede          Comunicacao registrada               |
|                                                              |
| [Selecionar evento]                                          |
+--------------------------------------------------------------+
~~~

**Elementos de interação:**

- Retorno ao dashboard.
- Consulta dos atributos disponíveis do processo.
- Lista de eventos relacionados.
- Seleção de um evento para acessar seus detalhes.

As informações exibidas dependem da capacidade de coleta e monitoramento implementada no ambiente sandbox.

### P03 — Detalhes do evento

**Objetivo:** apresentar as informações disponíveis sobre um evento para auxiliar sua interpretação.

~~~text
+--------------------------------------------------------------+
| EVENTO — DETALHES                                             |
+--------------------------------------------------------------+
| [< Voltar ao processo]                                       |
|                                                              |
| Tipo: Operacao com arquivo                                   |
| Data/hora: 14:02:10                                          |
| Processo associado: exemplo.exe                              |
| Recurso: arquivo_exemplo.tmp                                 |
| Operacao observada: Tentativa de escrita                     |
| Resultado registrado: A confirmar pelos dados coletados      |
+--------------------------------------------------------------+
| CONTEXTO E EVIDENCIAS                                         |
|                                                              |
| Informacoes adicionais disponíveis sobre o evento.           |
|                                                              |
| [Consultar processo associado]                               |
+--------------------------------------------------------------+
~~~

**Elementos de interação:**

- Retorno aos detalhes do processo.
- Consulta do tipo e horário do evento.
- Identificação do processo associado.
- Consulta do recurso afetado ou acessado, quando identificado.
- Exibição da operação observada e do resultado registrado.
- Acesso ao processo relacionado.

A interface não deve classificar automaticamente uma atividade como maliciosa apenas por ser incomum. É necessário distinguir uma tentativa de operação de uma alteração ou ação efetivamente confirmada pelos dados coletados.

### Estados considerados

| Estado | Comportamento esperado |
|---|---|
| Execução em andamento | Exibir o estado atual e as informações já coletadas. |
| Execução concluída | Permitir a consulta dos resultados disponíveis. |
| Falha ou indisponibilidade | Informar que os dados não puderam ser obtidos ou consultados. |
| Nenhum evento relacionado | Informar que não foram encontrados eventos relacionados nos dados disponíveis. |
| Dados incompletos | Indicar limitações da coleta, quando conhecidas. |
| Retorno à tela anterior | Preservar o contexto de navegação sempre que possível. |

## 4. Simulação e walkthrough

A simulação tem como objetivo avaliar se uma pessoa que não participou do desenho consegue compreender a organização das informações e realizar as tarefas propostas sem depender de explicações constantes do autor.

### Tarefas propostas para a simulação

| Tarefa | Instrução ao participante | Resultado esperado |
|---|---|---|
| S01 | Identifique o estado da execução e consulte o resumo apresentado. | Localizar o estado da execução e compreender os indicadores disponíveis. |
| S02 | Encontre um processo e consulte suas informações. | Acessar P02 e identificar os dados apresentados. |
| S03 | Selecione um evento e explique o que as informações permitem concluir. | Acessar P03 e distinguir os dados observados das conclusões que não podem ser confirmadas. |
| S04 | Retorne à visão geral da execução. | Voltar a P01 sem se perder na navegação. |

### Registro da simulação

A simulação com um participante externo ao projeto permanece pendente de registro.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| A registrar durante a simulação. | A definir. | A coletar. | Revisar conforme a dificuldade observada. |
| A registrar durante a simulação. | A definir. | A coletar. | Revisar conforme a dificuldade observada. |
| A registrar durante a simulação. | A definir. | A coletar. | Revisar conforme a dificuldade observada. |

Não foram atribuídos resultados fictícios à simulação. As observações e evidências deverão ser preenchidas após a aplicação do walkthrough.

## 5. Alterações após a simulação

As alterações devem ser registradas a partir das dificuldades efetivamente observadas durante a avaliação do protótipo.

| Antes | Problema identificado | Depois | Justificativa |
|---|---|---|---|
| Protótipo inicial. | A avaliar. | A definir após a simulação. | A alteração deverá responder a uma dificuldade observada. |
| Protótipo inicial. | A avaliar. | A definir após a simulação. | A alteração deverá responder a uma dificuldade observada. |

### Síntese da proposta

A prototipação estabelece uma interface centrada na análise comportamental de aplicações executadas em ambiente sandbox. O dashboard concentra o resumo da execução, os processos identificados e as atividades recentes. As telas complementares permitem investigar processos e consultar detalhes de eventos.

A navegação segue uma progressão do geral para o específico, com retorno à visão geral. A proposta prioriza a compreensão das evidências, sem confundir operações tentadas com alterações confirmadas e sem afirmar comportamentos que não tenham sido registrados.

A estrutura documentada fornece uma base de baixa fidelidade para avaliação e evolução da interface. Os resultados da simulação e as alterações decorrentes deverão ser registrados quando essa atividade for realizada.

## Checklist de entrega

- [x] Escopo relacionado à persona, ao cenário e às tarefas da Entrega 5.
- [x] Família de interface definida e justificada.
- [x] Fluxos principais identificados.
- [x] Telas numeradas e organizadas em sequência navegável.
- [x] Controles e transições de navegação descritos.
- [x] Estados alternativos considerados.
- [x] Protótipo mantido em baixa fidelidade.
- [x] Ausência de funcionalidades administrativas desnecessárias.
- [x] Simulação planejada com tarefas objetivas.
- [x] Estrutura para registrar observações e evidências definida.
- [x] Estrutura para documentar alterações após a simulação definida.
~~~
