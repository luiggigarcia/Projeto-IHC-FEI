# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 08/10/2026  
**Status:** 🟩 Concluído  
**Responsável:** Luiggi Paschoalini Garcia  
**Projeto:** Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.

## Objetivo da atividade

Planejar uma coleta de dados com potenciais usuários da interface proposta, identificando necessidades, dificuldades, expectativas e características de uso relacionadas à investigação do comportamento de aplicações executadas em ambiente sandbox.

A coleta busca produzir evidências que permitam confirmar, refutar ou refinar hipóteses levantadas nas entregas anteriores, especialmente sobre a interpretação de eventos, a organização das informações e a navegação entre resultados resumidos e evidências detalhadas.

A atividade contempla a definição dos participantes, dos dados necessários, dos cuidados éticos, de um instrumento de coleta e dos procedimentos de aplicação e análise.

**Delimitação:** esta entrega documenta o planejamento da pesquisa e o instrumento de coleta. A aplicação do questionário e a análise de respostas reais constituem atividades posteriores.

---

## 1. Hipóteses e lacunas de conhecimento

As entregas anteriores permitiram identificar um problema de interação relacionado à apresentação e à interpretação de informações técnicas produzidas durante a execução controlada de aplicações.

O problema central de IHC é:

**Como apresentar uma grande quantidade de informações técnicas produzidas por uma análise sandbox de maneira que o usuário consiga compreender o comportamento da aplicação e investigar os detalhes relevantes?**

As hipóteses a seguir são derivadas do escopo definido na Entrega 1 e das decisões de design desenvolvidas nas Entregas 3, 4, 5 e 6.

| ID | Hipótese | Lacuna de conhecimento | Decisão que depende da resposta |
|---|---|---|---|
| H01 | Profissionais de Segurança da Informação realizam ou participam de investigações sobre o comportamento de aplicações. | Não foi verificada a frequência nem a forma como esse público realiza a atividade. | Confirmar ou revisar o perfil de usuário prioritário. |
| H02 | O volume e a dispersão dos eventos dificultam a interpretação dos resultados. | Não foram identificadas empiricamente as principais dificuldades encontradas pelos usuários. | Definir prioridades de organização, agrupamento e consulta das informações. |
| H03 | Processos, arquivos, configurações e atividades de rede são informações relevantes para a investigação. | Não foi estabelecida a importância relativa de cada categoria para os usuários. | Priorizar categorias e informações apresentadas no dashboard. |
| H04 | Uma visão resumida, com acesso progressivo aos detalhes, pode facilitar a investigação. | Não foi verificada a preferência dos usuários por essa estrutura de navegação. | Confirmar ou revisar os fluxos e telas da Entrega 6. |
| H05 | Os usuários precisam distinguir operações tentadas, concluídas e não confirmadas. | Não foi investigado como os usuários interpretam o resultado de uma operação. | Definir a apresentação de estados, resultados e limitações das evidências. |

Essas hipóteses não representam conclusões da pesquisa. Elas serão utilizadas para orientar a elaboração do instrumento de coleta e a interpretação dos dados.

### 1.1 Relação com as entregas anteriores

| Entrega | Contribuição para a coleta |
|---|---|
| Entrega 1 — Conhecendo o problema | Identificação inicial do problema, dos usuários potenciais e das dúvidas de pesquisa. |
| Entrega 2 — Análise de concorrência | Identificação de padrões de apresentação de informações e investigação de resultados. |
| Entrega 3 — Personas e contexto de uso | Definição da proto-persona P01 e de suas necessidades hipotéticas. |
| Entrega 4 — Cenários-problema | Descrição do cenário C01 de investigação de uma aplicação potencialmente não confiável. |
| Entrega 5 — Análise de tarefas | Identificação das tarefas T01, T02 e T03. |
| Entrega 6 — Prototipação em papel | Proposta de dashboard com visão geral, detalhes de processos e detalhes de eventos. |

---

# Parte A — Necessidades, requisitos e aspectos éticos

## 2. Necessidades de informação

A pesquisa deverá coletar informações suficientes para compreender o contexto de atuação dos participantes, as atividades que realizam e suas necessidades durante a investigação do comportamento de aplicações.

| ID | Informação necessária | Finalidade | Hipóteses relacionadas |
|---|---|---|---|
| D01 | Área de atuação e experiência dos participantes. | Caracterizar o público pesquisado. | H01 |
| D02 | Experiência prévia com investigação de aplicações e eventos do sistema operacional. | Verificar a familiaridade com a atividade. | H01 |
| D03 | Frequência de realização de atividades de investigação. | Compreender a recorrência da tarefa. | H01 |
| D04 | Ferramentas e métodos utilizados atualmente. | Identificar práticas existentes. | H01, H02 |
| D05 | Principais dificuldades durante a investigação. | Identificar obstáculos e necessidades de interação. | H02 |
| D06 | Categorias de informações consideradas relevantes. | Priorizar o conteúdo do dashboard. | H03 |
| D07 | Formas utilizadas para relacionar eventos e evidências. | Compreender estratégias de interpretação. | H02, H03 |
| D08 | Necessidade de distinguir tentativas e operações concluídas. | Investigar a interpretação dos resultados registrados. | H05 |
| D09 | Preferências de apresentação e navegação. | Avaliar a proposta de visão geral e detalhamento progressivo. | H04 |
| D10 | Funcionalidades consideradas úteis ou desnecessárias. | Orientar a evolução do protótipo. | H04 |
| D11 | Necessidades não contempladas nas perguntas anteriores. | Identificar requisitos ainda desconhecidos. | H01–H05 |

### 2.1 Necessidades preliminares de interação

Com base nas entregas anteriores, foram identificadas as seguintes necessidades preliminares, ainda sujeitas à validação:

- **N01:** compreender o estado e o contexto de uma execução controlada.
- **N02:** identificar os processos observados durante a execução.
- **N03:** consultar as atividades relacionadas a um processo.
- **N04:** investigar eventos associados a arquivos, configurações, rede e recursos do sistema.
- **N05:** relacionar eventos e compreender sua sequência temporal.
- **N06:** diferenciar ações tentadas de operações efetivamente registradas como concluídas.
- **N07:** reconhecer limitações ou ausência de informações coletadas.
- **N08:** navegar entre uma visão resumida e evidências detalhadas.

Essas necessidades constituem hipóteses de requisitos e não devem ser tratadas como requisitos empiricamente confirmados antes da análise dos dados.

## 3. Público-alvo e participantes

### 3.1 Público prioritário

O público prioritário será composto por profissionais ou estudantes com experiência relacionada à Segurança da Informação, especialmente em atividades como:

- Investigação de eventos de segurança.
- Análise de comportamento de aplicações.
- Monitoramento de processos e atividades do sistema operacional.
- Análise de registros técnicos.
- Investigação de incidentes e evidências.

### 3.2 Público complementar

Poderão participar profissionais de Infraestrutura de TI que tenham experiência com administração de sistemas, monitoramento, análise de processos ou investigação de alterações no ambiente operacional.

A participação desse público permitirá verificar se as necessidades identificadas também se aplicam a contextos próximos à Segurança da Informação.

### 3.3 Critérios de participação

**Critérios de inclusão:**

- Ter 18 anos ou mais.
- Concordar voluntariamente com a participação.
- Atuar ou estudar em uma área relacionada à Tecnologia da Informação.
- Possuir experiência ou interesse técnico em investigação de sistemas, aplicações ou eventos.

**Critérios de exclusão:**

- Não concordar com as condições de participação.
- Não atender à faixa etária estabelecida.
- Não desejar responder ao questionário.

Participantes sem experiência direta na atividade poderão responder às perguntas aplicáveis, sendo essa característica considerada na análise.

### 3.4 Estratégia de recrutamento

Será utilizada uma amostragem não probabilística, por conveniência, com divulgação do questionário entre profissionais e estudantes de Tecnologia da Informação.

Os possíveis canais de divulgação incluem:

- Contatos acadêmicos da área de Computação.
- Profissionais de Segurança da Informação e Infraestrutura de TI.
- Comunidades técnicas e grupos de estudo.
- Contatos profissionais que aceitem participar voluntariamente.

A pesquisa terá caráter exploratório. Seus resultados não serão considerados estatisticamente representativos de todos os profissionais da área.

### 3.5 Quantidade de participantes

A meta inicial proposta é obter entre **5 e 10 respostas válidas**, dependendo da disponibilidade dos participantes.

Essa quantidade é uma meta operacional para uma investigação acadêmica exploratória, não uma garantia de representatividade ou saturação dos dados.

O número efetivo de respostas deverá ser registrado após a aplicação.

## 4. Técnica de coleta escolhida

A técnica principal será um **questionário estruturado com perguntas fechadas e abertas**, aplicado preferencialmente por formulário eletrônico.

### Justificativa

O questionário permite:

- Coletar informações de participantes com diferentes experiências.
- Padronizar perguntas e alternativas.
- Identificar frequências e preferências.
- Obter relatos sobre dificuldades e necessidades.
- Comparar respostas sem exigir acesso a ambientes corporativos.
- Registrar os dados de forma organizada para análise posterior.

As perguntas fechadas permitirão organizar os resultados quantitativamente. As perguntas abertas permitirão compreender justificativas, dificuldades e necessidades que não estejam previstas nas alternativas.

### Limitações

O questionário depende do relato dos participantes e não permite observar diretamente como executam suas atividades.

Além disso, uma amostra pequena e por conveniência pode apresentar vieses de seleção.

Por esse motivo, os resultados deverão ser interpretados como evidências exploratórias e poderão orientar avaliações posteriores do protótipo, sem substituir testes de usabilidade.

## 5. Aspectos éticos

### 5.1 Participação voluntária

A participação será voluntária, sem remuneração e sem consequências para quem optar por não participar.

O participante poderá interromper o preenchimento antes do envio, sem necessidade de apresentar justificativa.

Após o envio, a retirada individual de respostas poderá não ser possível caso o formulário seja efetivamente anônimo e não exista um identificador que permita localizar os dados.

### 5.2 Consentimento informado

Antes de responder às perguntas, o participante receberá informações sobre:

- A finalidade acadêmica da pesquisa.
- O tema e os objetivos do estudo.
- O tempo estimado de participação.
- O caráter voluntário da participação.
- Os tipos de dados coletados.
- A forma de utilização e divulgação dos resultados.
- Os riscos e cuidados adotados.

O questionário somente deverá prosseguir após a manifestação de concordância.

### 5.3 Privacidade e minimização de dados

O instrumento não solicitará nome completo, CPF, matrícula, endereço residencial, telefone, empresa ou identificação de clientes.

Também não serão solicitados:

- Senhas ou credenciais.
- Endereços IP internos.
- Logs corporativos confidenciais.
- Arquivos potencialmente maliciosos.
- Amostras de malware.
- Informações restritas sobre incidentes.
- Dados pessoais de terceiros.
- Informações protegidas por acordos de confidencialidade.

Os participantes serão orientados a responder de forma geral, sem divulgar dados sigilosos de organizações.

### 5.4 Armazenamento e tratamento

As respostas serão utilizadas exclusivamente para as atividades acadêmicas relacionadas ao projeto de IHC.

Os dados deverão ser armazenados em local com acesso restrito ao responsável pela pesquisa, evitando a divulgação de respostas individuais identificáveis.

Na apresentação dos resultados, serão priorizados dados agregados e sínteses temáticas.

Caso sejam utilizados trechos de respostas abertas, deverão ser removidos elementos que possam identificar participantes, organizações ou terceiros.

O formulário deverá ser configurado para não solicitar autenticação desnecessária nem coletar automaticamente endereços de e-mail, quando a plataforma permitir.

O prazo de retenção dos dados deverá observar as orientações institucionais aplicáveis. Na ausência de exigência específica, os dados deverão ser eliminados quando não forem mais necessários à finalidade acadêmica.

### 5.5 Riscos e benefícios

**Riscos previstos:**

- Desconforto ao responder perguntas sobre experiência profissional.
- Divulgação involuntária de informações corporativas.
- Possível identificação indireta por respostas excessivamente específicas.

**Medidas de mitigação:**

- Não solicitar dados pessoais identificáveis.
- Evitar perguntas sobre incidentes reais específicos.
- Orientar o participante a não divulgar informações confidenciais.
- Permitir que perguntas não essenciais sejam ignoradas.
- Divulgar resultados de forma agregada.

**Benefícios esperados:**

A pesquisa poderá contribuir para compreender necessidades de profissionais e estudantes que investigam o comportamento de aplicações e orientar o desenvolvimento de uma interface mais adequada a essas atividades.

Não há garantia de benefício direto ao participante.

---

# Parte B — Ferramentas e procedimentos de coleta

## 6. Instrumento de coleta

**Identificador:** I01  
**Nome:** Questionário sobre investigação do comportamento de aplicações em sistemas operacionais.  
**Técnica:** Questionário eletrônico.  
**Público:** Profissionais e estudantes de Segurança da Informação, Infraestrutura de TI e áreas relacionadas.  
**Tempo estimado:** 5 a 8 minutos.  
**Aplicação:** Individual e voluntária.  
**Estado:** Instrumento elaborado e documentado.

### 6.1 Texto de apresentação ao participante

**Pesquisa acadêmica — Investigação do comportamento de aplicações em sistemas operacionais**

Este questionário faz parte de uma atividade acadêmica da disciplina de Interface Humano-Computador do curso de Ciência da Computação da FEI.

O objetivo é compreender como profissionais e estudantes de Tecnologia da Informação investigam o comportamento de aplicações em sistemas operacionais, quais informações consideram relevantes e quais dificuldades encontram durante essa atividade.

As respostas serão utilizadas para orientar a proposta de uma interface de consulta e interpretação de resultados produzidos por um ambiente sandbox.

A participação é voluntária e o preenchimento leva aproximadamente 5 a 8 minutos.

Não serão solicitados dados pessoais de identificação. Evite mencionar nomes de empresas, clientes, endereços internos, incidentes confidenciais ou quaisquer informações restritas.

Os resultados serão analisados para fins acadêmicos e apresentados preferencialmente de forma agregada.

Você poderá interromper o preenchimento antes de enviar suas respostas.

### 6.2 Consentimento

**Q00 — Você confirma que possui 18 anos ou mais, compreendeu as informações apresentadas e concorda voluntariamente em participar desta pesquisa?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Sim, concordo em participar.
- ( ) Não concordo em participar.

**Regra:** caso a resposta seja "Não concordo em participar", o questionário deverá ser encerrado sem coletar as demais respostas.

## 7. Questionário completo

### Bloco 1 — Perfil e experiência

**Q01 — Qual é sua principal área de atuação profissional ou acadêmica?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Segurança da Informação.
- ( ) Infraestrutura de TI.
- ( ) Suporte Técnico.
- ( ) Desenvolvimento de Software.
- ( ) Administração de Sistemas.
- ( ) Estudante de Tecnologia da Informação.
- ( ) Outra área relacionada à TI.
- ( ) Prefiro não informar.

**Objetivo:** caracterizar o perfil dos participantes.  
**Hipótese relacionada:** H01.

---

**Q02 — Você já participou de alguma atividade de investigação do comportamento de aplicações, processos ou eventos em um sistema operacional?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Sim, frequentemente.
- ( ) Sim, algumas vezes.
- ( ) Sim, apenas em atividades acadêmicas ou de estudo.
- ( ) Não, mas conheço o assunto.
- ( ) Não tenho experiência com esse tipo de atividade.

**Objetivo:** identificar a experiência prévia dos participantes.  
**Hipótese relacionada:** H01.

---

**Q03 — Com que frequência você realiza atividades relacionadas à análise de processos, eventos ou comportamento de aplicações?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Diariamente.
- ( ) Semanalmente.
- ( ) Mensalmente.
- ( ) Raramente.
- ( ) Nunca.

**Objetivo:** compreender a recorrência da atividade.  
**Hipótese relacionada:** H01.

### Bloco 2 — Processo atual de investigação

**Q04 — Quais ferramentas ou métodos você utiliza ou já utilizou para investigar atividades de aplicações ou sistemas operacionais?**

**Tipo:** Seleção múltipla.  
**Obrigatória:** Não.

- [ ] Gerenciador de Tarefas ou ferramentas equivalentes.
- [ ] Visualizador de Eventos ou análise de logs.
- [ ] Process Monitor ou ferramentas semelhantes.
- [ ] Ferramentas de monitoramento de rede.
- [ ] Ambientes sandbox.
- [ ] Ferramentas de monitoramento de segurança.
- [ ] Scripts ou comandos do sistema operacional.
- [ ] Outras ferramentas.
- [ ] Não utilizei ferramentas desse tipo.

**Objetivo:** identificar práticas e ferramentas conhecidas.  
**Hipóteses relacionadas:** H01 e H02.

---

**Q05 — Quais são as principais dificuldades que você encontra ou acredita que encontraria ao investigar o comportamento de uma aplicação?**

**Tipo:** Seleção múltipla.  
**Obrigatória:** Sim.

- [ ] Grande quantidade de eventos registrados.
- [ ] Informações distribuídas entre diferentes ferramentas.
- [ ] Dificuldade para identificar eventos relevantes.
- [ ] Dificuldade para relacionar processos e eventos.
- [ ] Dificuldade para compreender a sequência temporal das ações.
- [ ] Informações técnicas difíceis de interpretar.
- [ ] Dificuldade para confirmar se uma operação foi concluída.
- [ ] Falta de informações ou evidências.
- [ ] Não identifico dificuldades relevantes.
- [ ] Outra dificuldade.

**Objetivo:** identificar obstáculos à investigação.  
**Hipótese relacionada:** H02.

---

**Q06 — Descreva, se possível, uma dificuldade que você já encontrou ao interpretar processos, registros ou eventos de um sistema operacional.**

**Tipo:** Resposta aberta.  
**Obrigatória:** Não.

**Orientação:** não inclua informações confidenciais, nomes de organizações ou dados de incidentes reais que possam identificar pessoas ou sistemas.

**Objetivo:** aprofundar a compreensão das dificuldades relatadas.  
**Hipótese relacionada:** H02.

### Bloco 3 — Informações e evidências

**Q07 — Quais categorias de informações você considera mais importantes para compreender o comportamento de uma aplicação?**

**Tipo:** Seleção múltipla.  
**Obrigatória:** Sim.

- [ ] Processos iniciados ou encerrados.
- [ ] Relações entre processos.
- [ ] Arquivos acessados, criados ou modificados.
- [ ] Alterações em configurações do sistema.
- [ ] Conexões e atividades de rede.
- [ ] Consumo de CPU, memória e outros recursos.
- [ ] Sequência temporal dos eventos.
- [ ] Resultado das operações realizadas ou tentadas.
- [ ] Outras informações.
- [ ] Não sei avaliar.

**Objetivo:** identificar categorias de informações relevantes.  
**Hipótese relacionada:** H03.

---

**Q08 — Quando precisa compreender o comportamento de uma aplicação, como você prefere investigar os eventos registrados?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Começando por um resumo geral e acessando detalhes conforme necessário.
- ( ) Consultando diretamente uma lista completa de eventos.
- ( ) Analisando uma linha do tempo das atividades.
- ( ) Investigando primeiro os processos e suas relações.
- ( ) Utilizando outra abordagem.
- ( ) Não sei avaliar.

**Objetivo:** investigar estratégias de consulta e navegação.  
**Hipóteses relacionadas:** H02 e H04.

---

**Q09 — Qual é a importância de identificar se uma operação foi apenas tentada, concluída com sucesso ou não pôde ter seu resultado confirmado?**

**Tipo:** Escala de 1 a 5.  
**Obrigatória:** Sim.

- ( ) 1 — Nada importante.
- ( ) 2 — Pouco importante.
- ( ) 3 — Moderadamente importante.
- ( ) 4 — Muito importante.
- ( ) 5 — Extremamente importante.
- ( ) Não sei avaliar.

**Objetivo:** investigar a relevância da distinção entre os resultados das operações.  
**Hipótese relacionada:** H05.

### Bloco 4 — Necessidades de interface

**Q10 — Qual forma de apresentação você considera mais útil para consultar os resultados de uma análise de comportamento?**

**Tipo:** Escolha única.  
**Obrigatória:** Sim.

- ( ) Dashboard com resumo e indicadores.
- ( ) Tabela detalhada de eventos.
- ( ) Linha do tempo.
- ( ) Visualização das relações entre processos.
- ( ) Relatório textual estruturado.
- ( ) Outra forma.
- ( ) Não sei avaliar.

**Objetivo:** identificar preferências de apresentação.  
**Hipótese relacionada:** H04.

---

**Q11 — Quais recursos seriam mais úteis em uma interface destinada à investigação do comportamento de aplicações?**

**Tipo:** Seleção múltipla.  
**Obrigatória:** Sim.

- [ ] Visão geral da execução.
- [ ] Lista de processos identificados.
- [ ] Consulta dos eventos associados a cada processo.
- [ ] Filtros por categoria de evento.
- [ ] Pesquisa por processo ou recurso.
- [ ] Linha do tempo das atividades.
- [ ] Detalhamento de evidências.
- [ ] Indicação do resultado de cada operação.
- [ ] Identificação de informações indisponíveis ou incompletas.
- [ ] Exportação de relatório.
- [ ] Outros recursos.
- [ ] Não sei avaliar.

**Objetivo:** identificar funcionalidades consideradas úteis.  
**Hipóteses relacionadas:** H03, H04 e H05.

---

**Q12 — Existe alguma informação, funcionalidade ou dificuldade relacionada à investigação do comportamento de aplicações que não foi abordada neste questionário?**

**Tipo:** Resposta aberta.  
**Obrigatória:** Não.

**Objetivo:** identificar necessidades adicionais e aspectos não previstos nas hipóteses iniciais.  
**Hipóteses relacionadas:** H01–H05.

## 8. Procedimento de aplicação

### 8.1 Preparação

1. Criar um formulário eletrônico com as perguntas descritas no instrumento I01.
2. Incluir o texto de apresentação e a pergunta de consentimento.
3. Configurar o encerramento do formulário quando não houver consentimento.
4. Desabilitar a coleta automática de identificação pessoal, quando possível.
5. Verificar se perguntas opcionais podem ser deixadas sem resposta.
6. Revisar a clareza das perguntas e alternativas.
7. Testar o funcionamento do formulário antes da divulgação.

### 8.2 Recrutamento

1. Identificar potenciais participantes pertencentes ao público definido.
2. Encaminhar um convite breve explicando a finalidade acadêmica.
3. Informar o tempo estimado de preenchimento.
4. Esclarecer que a participação é voluntária.
5. Disponibilizar o acesso ao formulário.

### 8.3 Aplicação

1. O participante acessará o formulário.
2. Lerá a apresentação e as informações sobre a pesquisa.
3. Manifestará ou não seu consentimento.
4. Caso concorde, responderá às perguntas.
5. Poderá deixar questões opcionais sem resposta.
6. Ao final, enviará suas respostas.

Não será exigida a utilização de ferramentas específicas nem a execução de aplicações durante o preenchimento.

### 8.4 Encerramento

Após o período de coleta:

1. Encerrar o recebimento de novas respostas.
2. Registrar a quantidade de respostas recebidas.
3. Verificar a existência de respostas incompletas.
4. Excluir eventuais registros sem consentimento, caso existam.
5. Preparar os dados para análise.
6. Remover informações identificáveis eventualmente inseridas em respostas abertas.

## 9. Plano de análise dos dados

A análise será realizada de maneira descritiva e exploratória.

### 9.1 Perguntas fechadas

Para perguntas de escolha única, serão calculadas:

- Frequência absoluta de cada alternativa.
- Frequência relativa, quando aplicável.
- Distribuição das respostas entre os perfis participantes.

Para perguntas de seleção múltipla, será contabilizada a quantidade de participantes que selecionou cada alternativa.

As porcentagens, quando apresentadas, deverão utilizar como denominador o número de participantes que respondeu à respectiva pergunta.

### 9.2 Perguntas abertas

As respostas abertas serão analisadas por agrupamento temático.

O procedimento previsto é:

1. Ler integralmente as respostas.
2. Identificar dificuldades, necessidades e sugestões mencionadas.
3. Agrupar conteúdos semelhantes em categorias.
4. Registrar a frequência de temas recorrentes, quando pertinente.
5. Identificar respostas divergentes.
6. Relacionar os temas às hipóteses e decisões de interface.

Possíveis categorias iniciais incluem:

- Volume de informações.
- Organização dos eventos.
- Relação entre processos.
- Interpretação de resultados.
- Navegação e consulta.
- Evidências incompletas.
- Necessidades adicionais.

Essas categorias poderão ser alteradas conforme o conteúdo efetivamente coletado.

### 9.3 Interpretação das hipóteses

| Hipótese | Evidência a observar | Possível consequência |
|---|---|---|
| H01 | Experiência, frequência e área de atuação dos participantes. | Confirmar ou revisar o público prioritário. |
| H02 | Dificuldades selecionadas e relatos abertos. | Priorizar mecanismos de organização e investigação. |
| H03 | Categorias de informações selecionadas. | Revisar a hierarquia das informações do dashboard. |
| H04 | Preferências de consulta e funcionalidades escolhidas. | Manter ou revisar os fluxos da prototipação. |
| H05 | Importância atribuída ao resultado das operações. | Definir como apresentar tentativas, sucessos, falhas e informações não confirmadas. |

Uma hipótese poderá receber evidências favoráveis, contrárias ou inconclusivas.

As conclusões deverão considerar o tamanho da amostra, a experiência dos participantes e as limitações do instrumento.

## 10. Rastreabilidade entre perguntas e hipóteses

| Pergunta | Informação investigada | Hipóteses |
|---|---|---|
| Q01 | Área de atuação. | H01 |
| Q02 | Experiência com investigação. | H01 |
| Q03 | Frequência da atividade. | H01 |
| Q04 | Ferramentas e métodos utilizados. | H01, H02 |
| Q05 | Dificuldades de investigação. | H02 |
| Q06 | Relatos de dificuldades. | H02 |
| Q07 | Categorias de informações relevantes. | H03 |
| Q08 | Estratégias de investigação. | H02, H04 |
| Q09 | Importância do resultado das operações. | H05 |
| Q10 | Preferências de apresentação. | H04 |
| Q11 | Funcionalidades consideradas úteis. | H03, H04, H05 |
| Q12 | Necessidades adicionais. | H01–H05 |

## 11. Utilização dos resultados no projeto

Os resultados da coleta serão utilizados para revisar as decisões de interação estabelecidas anteriormente.

### 11.1 Persona

As respostas poderão indicar se a proto-persona P01 representa adequadamente o público prioritário ou se será necessário ajustar suas características, objetivos e dificuldades.

### 11.2 Cenário de uso

As dificuldades e práticas relatadas poderão contribuir para refinar o cenário C01, tornando mais precisas as condições e necessidades da investigação.

### 11.3 Análise de tarefas

As informações sobre estratégias de investigação poderão contribuir para revisar as tarefas T01, T02 e T03, especialmente a sequência de consulta e interpretação das evidências.

### 11.4 Prototipação

Os resultados poderão orientar alterações nas telas propostas na Entrega 6:

**P01 — Dashboard da execução**

- Organização dos indicadores.
- Priorização das categorias de eventos.
- Apresentação dos processos.
- Exibição das atividades recentes.

**P02 — Detalhes do processo**

- Informações prioritárias do processo.
- Relações entre processos.
- Organização dos eventos associados.

**P03 — Detalhes do evento**

- Informações necessárias para interpretar a operação.
- Identificação do recurso envolvido.
- Diferenciação entre tentativa, conclusão e resultado desconhecido.
- Apresentação de evidências e limitações.

Nenhuma alteração será considerada empiricamente justificada antes da obtenção e interpretação das respostas.

---

## 12. Síntese da entrega

A Entrega 7 estabelece um plano de coleta de dados para investigar as necessidades de usuários relacionados à análise do comportamento de aplicações em sistemas operacionais.

A pesquisa foi estruturada a partir das hipóteses e lacunas identificadas nas entregas anteriores, considerando como público prioritário profissionais de Segurança da Informação e, complementarmente, profissionais de Infraestrutura de TI e estudantes com experiência relacionada.

Foi elaborado o instrumento I01, composto por uma pergunta de consentimento e 12 perguntas sobre perfil, experiência, dificuldades, informações relevantes e preferências de interação.

Também foram definidos os procedimentos de recrutamento, aplicação, cuidados éticos, tratamento dos dados e análise dos resultados.

A coleta buscará produzir evidências para revisar a persona, o cenário, as tarefas e a prototipação do dashboard.

**Conclusão:** o planejamento metodológico, a definição dos participantes, os aspectos éticos, o instrumento de coleta e o plano de análise foram documentados. A execução da pesquisa com participantes e a análise dos dados permanecem como atividades futuras.

## 13. Checklist de entrega

- [x] Hipóteses e lacunas de conhecimento identificadas.
- [x] Relação com as entregas anteriores documentada.
- [x] Necessidades de informação definidas.
- [x] Público-alvo e critérios de participação estabelecidos.
- [x] Técnica de coleta escolhida e justificada.
- [x] Cuidados éticos e de privacidade documentados.
- [x] Texto de apresentação e consentimento elaborados.
- [x] Questionário completo desenvolvido.
- [x] Perguntas relacionadas às hipóteses de pesquisa.
- [x] Procedimento de aplicação definido.
- [x] Plano de análise dos dados elaborado.
- [x] Relação entre resultados esperados e decisões de design documentada.
- [x] Planejamento da coleta de dados concluído.
- [x] Instrumento de pesquisa preparado para aplicação.
- [x] Limitações da pesquisa identificadas e documentadas.

### Atividades posteriores à entrega

A aplicação do questionário, a coleta de respostas e a revisão das hipóteses com base nos resultados serão realizadas posteriormente, caso previstas no cronograma acadêmico.

**Status final da documentação:** 🟩 Concluído.
