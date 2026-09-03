# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 03/09/2026  
**Status:** 🟨 Em desenvolvimento  
**Integrante:** Luiggi Paschoalini Garcia — 22.122.006-4

---

## Objetivo da atividade

Compreender soluções do mesmo domínio e interfaces relacionadas às atividades que poderão ser realizadas pelo público-alvo do projeto.

O objetivo desta análise não é reproduzir a interface de uma solução existente, mas identificar convenções, padrões de interação, formas de apresentação de informações, pontos positivos, limitações e oportunidades que possam contribuir para o desenvolvimento da proposta de IHC.

Para este projeto, foi selecionado o **ANY.RUN** como principal interface representativa do domínio de análise de aplicações potencialmente não confiáveis.

A análise será utilizada como referência para compreender como uma solução existente apresenta informações relacionadas ao comportamento de aplicações, mas **não tem como objetivo criar uma interface semelhante ao ANY.RUN**.

---

# 1. Público-alvo

O público-alvo foi definido inicialmente na Entrega 1 a partir da capacidade técnica do TCC e das possíveis aplicações de seus resultados.

Foram identificados os seguintes grupos:

- Analistas de Segurança da Informação;
- Profissionais de Infraestrutura de TI;
- Pesquisadores da área de Segurança da Informação;
- Pesquisadores da área de Computação;
- Estudantes de Computação;
- Estudantes de Segurança da Informação.

### Usuário principal

Para esta etapa, será considerado como usuário principal o **Analista de Segurança da Informação**, por apresentar forte relação com a atividade de investigar o comportamento de aplicações potencialmente não confiáveis.

Esse usuário precisa compreender o que uma aplicação realizou durante sua execução, identificando alterações e comportamentos relevantes no sistema operacional.

Entre as informações de interesse estão:

- processos criados ou executados;
- arquivos criados, modificados ou removidos;
- alterações no Registro do sistema;
- conexões e atividades de rede;
- utilização de recursos do sistema;
- comportamentos potencialmente suspeitos;
- sequência ou relação entre determinados eventos;
- informações gerais sobre a execução.

Os demais grupos identificados na Entrega 1 serão considerados como possíveis usuários secundários.

### Necessidade central do usuário

A necessidade central identificada é:

> **Compreender, de forma organizada e visualmente acessível, o que uma aplicação realizou no sistema operacional durante sua execução em ambiente controlado.**

O principal problema de IHC identificado não é simplesmente coletar informações.

O desafio é **transformar uma grande quantidade de informações técnicas em uma representação que permita ao usuário compreender rapidamente o comportamento da aplicação e aprofundar a análise quando necessário.**

---

# 2. Revisão das alternativas identificadas na Entrega 1

Na Entrega 1 foram identificadas diferentes soluções e ferramentas relacionadas ao domínio do projeto.

Nesta entrega, o escopo foi concentrado no **ANY.RUN**, pois ele apresenta uma relação direta com a atividade de análise de aplicações em ambiente controlado e possui uma interface rica em informações relacionadas ao comportamento observado durante a execução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| ANY.RUN | Concorrente / análogo | Plataforma de sandbox utilizada para execução e análise de aplicações potencialmente maliciosas, apresentando informações sobre comportamento, processos, rede, indicadores e resultados. | [F] | **Analisar** |
| Windows Sandbox | Análogo | Permite executar aplicações em um ambiente isolado e descartável. | [F] | Não analisar nesta entrega. |
| Process Monitor | Ferramenta profissional análoga | Permite observar eventos relacionados a processos, arquivos, Registro e outras atividades do sistema operacional. | [F] | Não analisar nesta entrega. |
| Cuckoo Sandbox | Concorrente / análogo | Plataforma utilizada para análise automatizada de comportamento de arquivos e aplicações. | [F] | Não analisar nesta entrega. |
| Joe Sandbox | Concorrente / análogo | Plataforma de análise automatizada de ameaças e comportamento de aplicações. | [F] | Não analisar nesta entrega. |

### Justificativa da escolha

O ANY.RUN foi escolhido porque reúne diferentes elementos diretamente relacionados ao problema investigado pelo TCC:

- execução controlada;
- coleta de informações sobre o comportamento da aplicação;
- identificação de eventos relevantes;
- apresentação dos resultados;
- organização de informações técnicas.

A plataforma permite enviar arquivos ou URLs, executar a análise em ambiente controlado e visualizar informações relacionadas ao comportamento observado.

Entretanto, o projeto de IHC **não pretende reproduzir a experiência completa do ANY.RUN**.

A proposta deste projeto será mais específica:

> **O sandbox realizará a execução e coleta das informações, enquanto a interface de IHC terá como objetivo apresentar os resultados dessa análise por meio de um dashboard organizado, permitindo que o usuário compreenda o que a aplicação realizou no sistema operacional.**

---

# 3. Concorrente / interface representativa

## C01 — ANY.RUN

**Autor:** Luiggi Paschoalini Garcia — 22.122.006-4  
**Tipo:** Concorrente / interface representativa do domínio  
**Link oficial:** https://any.run/  
**Data de acesso:** 03/09/2026

### Contexto e proposta

O **ANY.RUN** é uma plataforma de sandbox interativa voltada principalmente à análise de malware e ameaças.

A plataforma permite enviar arquivos ou URLs, configurar o ambiente de análise e acompanhar o comportamento da amostra durante sua execução.

Também disponibiliza informações relacionadas a:

- processos;
- rede;
- indicadores;
- técnicas;
- eventos;
- comportamento;
- relatórios.

A solução possui relação direta com o domínio deste TCC porque utiliza um ambiente controlado para permitir a observação do comportamento de uma aplicação.

Entretanto, existem diferenças importantes entre a proposta do ANY.RUN e o recorte definido para este projeto.

O ANY.RUN possui como foco principal a investigação interativa de ameaças e permite que o usuário interaja diretamente com a máquina virtual durante a análise.

No projeto de IHC, **essa interação direta com a máquina virtual não será adotada**.

A interface proposta será construída com foco na etapa posterior à execução.

### Fluxo conceitual

Aplicação / arquivo  
↓  
Sandbox  
↓  
Execução controlada  
↓  
Monitoramento do sistema operacional  
↓  
Coleta dos eventos  
↓  
Processamento das informações  
↓  
Dashboard  
↓  
Análise e interpretação pelo usuário

Dessa maneira, o ANY.RUN será utilizado principalmente como referência para estudar:

- organização das informações;
- visualização de resultados;
- hierarquia de informações;
- apresentação de dados técnicos;
- indicadores;
- relatórios;
- detalhamento progressivo.

---

# 4. Funcionalidades relevantes do ANY.RUN

| Funcionalidade | Como é realizada | Evidência / print | Observação de IHC |
|---|---|---|---|
| Envio de arquivo | O usuário fornece um arquivo para iniciar a análise. | `../assets/02_concorrencia/anyrun_upload.png` | O início da atividade principal deve ser simples e compreensível. |
| Análise de URL | A plataforma permite fornecer uma URL para análise. | `../assets/02_concorrencia/anyrun_url.png` | Demonstra a utilização de diferentes tipos de entrada. |
| Execução em ambiente controlado | A amostra é executada em uma máquina virtual. | `../assets/02_concorrencia/anyrun_analysis.png` | O usuário precisa compreender que a aplicação está sendo executada em ambiente controlado. |
| Visualização de processos | Os processos envolvidos na análise podem ser apresentados em estrutura organizada. | `../assets/02_concorrencia/anyrun_processes.png` | A organização hierárquica pode facilitar a compreensão das relações entre processos. |
| Detalhamento de processos | O usuário pode consultar informações específicas de determinado processo. | `../assets/02_concorrencia/anyrun_process_details.png` | Demonstra o princípio de apresentação progressiva das informações. |
| Informações de rede | A plataforma apresenta informações relacionadas às comunicações realizadas durante a análise. | `../assets/02_concorrencia/anyrun_network.png` | Agrupar informações por categoria facilita a investigação. |
| Indicadores | Indicadores relacionados à atividade analisada são apresentados. | `../assets/02_concorrencia/anyrun_iocs.png` | Informações técnicas podem ser destacadas para facilitar a identificação de eventos relevantes. |
| Técnicas e comportamentos | A plataforma relaciona comportamentos observados a técnicas conhecidas. | `../assets/02_concorrencia/anyrun_ttps.png` | Uma camada interpretativa pode facilitar a compreensão dos dados técnicos. |
| Relatório | Os resultados podem ser organizados em formato de relatório. | `../assets/02_concorrencia/anyrun_report.png` | Facilita a consulta e comunicação dos resultados. |
| Visão geral | Informações gerais da análise podem ser visualizadas de forma consolidada. | `../assets/02_concorrencia/anyrun_dashboard.png` | Uma visão inicial ajuda o usuário a compreender rapidamente o contexto da análise. |

---

# 5. Experiência do usuário e opiniões

A análise de avaliações públicas permite identificar algumas percepções sobre a experiência de utilização do ANY.RUN.

Avaliações disponíveis em plataformas como G2 apresentam comentários positivos relacionados à facilidade de utilização, à realização das análises e à visualização das informações produzidas durante a execução.

Também existem relatos destacando a possibilidade de observar e interagir com a aplicação durante a análise como uma característica importante da ferramenta.

Essas informações devem ser consideradas como **opiniões de usuários específicos**, e não como evidências universais sobre a qualidade da interface.

Também foram identificadas limitações relacionadas à quantidade de informações apresentada em análises extensas.

Interfaces voltadas à investigação podem apresentar grande volume de dados, o que pode dificultar a localização de uma informação específica.

### Síntese das opiniões

| Aspecto | Evidência | Interpretação de IHC |
|---|---|---|
| Facilidade de utilização | Avaliações públicas destacam a facilidade de uso | Uma interface de análise deve reduzir a barreira inicial para o usuário. |
| Visualização dos resultados | Usuários destacam a utilidade das informações apresentadas | A organização dos dados é importante para a compreensão da análise. |
| Interatividade | Usuários destacam a possibilidade de interação com o ambiente | Demonstra uma estratégia possível, mas que não será adotada no nosso escopo. |
| Grande quantidade de informações | Existem relatos sobre interfaces mais carregadas em análises extensas | A densidade de informações deve ser controlada para evitar sobrecarga cognitiva. |
| Relatórios | A plataforma oferece diferentes formas de apresentação dos resultados | Resultados consolidados podem facilitar a comunicação da análise. |

---

# 6. Preço e modelo de negócio

O ANY.RUN utiliza um modelo de planos que inclui uma modalidade gratuita e planos pagos.

A modalidade Community possui limitações de funcionalidades, tempo de execução e tamanho máximo de arquivo.

A página oficial informa, por exemplo, limite de 60 segundos de execução da VM e tamanho máximo de 16 MB para arquivos no plano gratuito.

Planos superiores aumentam esses limites e disponibilizam recursos adicionais.

### Relação com IHC

As limitações impostas pelo modelo de negócio podem influenciar a experiência do usuário.

Em uma análise que exige maior tempo de execução, limites temporais podem criar pressão sobre o usuário e dificultar investigações mais detalhadas.

Para o nosso projeto, essa observação reforça a importância de comunicar claramente:

- estado da análise;
- andamento;
- conclusão;
- eventuais limitações;
- falhas;
- disponibilidade dos resultados.

---

# 7. Padrões e tendências percebidos

## 7.1 Visão geral antes do detalhe

A plataforma apresenta informações consolidadas que permitem compreender o contexto geral da análise antes do aprofundamento em eventos específicos.

### Aplicação ao projeto

O dashboard deverá apresentar inicialmente um **resumo da análise**, permitindo que o usuário compreenda rapidamente o comportamento geral da aplicação.

---

## 7.2 Organização das informações por categorias

As informações da análise são organizadas em diferentes categorias, como processos, rede, indicadores e técnicas.

### Aplicação ao projeto

Os resultados do sandbox poderão ser organizados em categorias relacionadas diretamente ao sistema operacional:

- Processos;
- Arquivos;
- Registro;
- Rede;
- Recursos do sistema;
- Comportamentos identificados.

---

## 7.3 Detalhamento progressivo

O usuário pode iniciar pela visão geral e posteriormente acessar informações mais específicas.

### Aplicação ao projeto

O dashboard deverá priorizar informações essenciais inicialmente e permitir que o usuário consulte detalhes quando necessário.

---

## 7.4 Representação visual de informações técnicas

O ANY.RUN utiliza diferentes formas de representação para tornar informações técnicas mais compreensíveis.

### Aplicação ao projeto

O projeto poderá utilizar:

- gráficos;
- indicadores;
- tabelas;
- cartões informativos;
- agrupamentos;
- elementos visuais de destaque.

Entretanto, esses elementos somente deverão ser utilizados quando contribuírem para a compreensão da análise.

---

## 7.5 Relatório consolidado

A plataforma oferece formas estruturadas de apresentar os resultados da análise.

### Aplicação ao projeto

O resultado da análise poderá ser apresentado como um relatório visual dentro do dashboard, facilitando a interpretação e eventual documentação da atividade.

---

# 8. Padrões de interface relevantes ao escopo de IHC

Foram mantidos somente os padrões considerados relevantes para o recorte atual do projeto.

| Padrão observado | Produto | Para qual tarefa serve | Vantagem percebida | Risco / limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| Dashboard / visão geral | ANY.RUN | Compreender rapidamente o resultado geral de uma análise. | Permite identificar informações importantes sem consultar cada evento individualmente. | Pode concentrar muitas informações em uma única tela. | **Sim** |
| Relatório | ANY.RUN | Consultar e comunicar os resultados da análise. | Organiza as informações e facilita a interpretação posterior. | Um relatório excessivamente detalhado pode dificultar a leitura. | **Sim** |
| Organização por categorias | ANY.RUN | Separar diferentes tipos de informações observadas durante a análise. | Facilita a localização e compreensão dos dados. | Categorias mal definidas podem dificultar a navegação. | **Sim** |
| Detalhamento progressivo | ANY.RUN | Passar de informações resumidas para informações técnicas específicas. | Evita apresentar todos os dados simultaneamente. | O usuário precisa identificar onde aprofundar a investigação. | **Sim** |
| Indicadores visuais | ANY.RUN | Destacar informações ou comportamentos relevantes. | Permite identificar rapidamente pontos de atenção. | Uso excessivo pode gerar ruído visual. | **Sim** |
| Feedback / estado da análise | ANY.RUN | Informar o andamento ou resultado da análise. | Mantém o usuário informado sobre o estado do sistema. | Informações insuficientes podem gerar incerteza. | **Sim** |

### Padrões avaliados e descartados

Alguns padrões presentes ou relacionados ao domínio foram avaliados, mas não fazem parte do escopo atual.

| Padrão | Decisão | Justificativa |
|---|---|---|
| Histórico + filtros | **Não** | Não faz parte do objetivo principal da interface definida para o projeto. |
| Interação direta com VM | **Não** | A proposta é que a interface apresente os resultados de uma análise já executada pelo sandbox. |
| Comparação de resultados | **Provavelmente não** | Não existe, neste momento, uma necessidade identificada que justifique comparação entre diferentes análises. |
| Administração / CRUD | **Não** | Não existe necessidade identificada de administração de entidades como parte da tarefa principal do usuário. |

> O fato de uma funcionalidade existir no ANY.RUN não significa que ela será incorporada ao projeto. A adoção de cada padrão dependerá de sua relação com as tarefas e necessidades identificadas ao longo das próximas etapas de IHC.

---

# 9. Direcionamento da interface do projeto

A análise do ANY.RUN permitiu definir um direcionamento próprio para a interface.

O objetivo não será criar uma versão simplificada do ANY.RUN.

O projeto terá como foco a **apresentação dos resultados produzidos pelo sandbox**.

## Conceito

> **Sandbox técnico por trás + Dashboard de análise para o usuário.**

O usuário não terá como objetivo principal controlar a máquina virtual.

Em vez disso, o usuário receberá os resultados produzidos pelo sandbox e utilizará a interface para compreender o comportamento da aplicação.

### Fluxo principal

Aplicação / Arquivo  
↓  
Sandbox  
↓  
Execução controlada  
↓  
Monitoramento do SO  
↓  
Coleta de eventos  
↓  
Processamento / análise  
↓  
Dashboard  
↓  
Interpretação do usuário

---

# 10. Conceito inicial do dashboard

O dashboard deverá apresentar inicialmente uma visão consolidada da análise.

### Exemplo conceitual

**ANÁLISE DA APLICAÇÃO**

**Aplicação:** exemplo.exe  
**Status:** Análise concluída

| Processos | Arquivos | Registro | Rede |
|---:|---:|---:|---:|
| 7 | 23 | 8 | 4 |

### Resumo do comportamento

> A aplicação criou 7 processos, modificou 23 arquivos e realizou 4 conexões de rede durante a execução.

**Comportamentos que merecem atenção:** 2

### Detalhamento

- Processos
- Arquivos
- Registro
- Rede
- Recursos

O exemplo acima representa apenas o **conceito inicial** da interface.

Ele não constitui ainda um protótipo ou definição visual final.

A estrutura deverá ser refinada nas próximas entregas conforme forem definidos:

- personas;
- necessidades;
- cenários;
- tarefas;
- modelo conceitual;
- arquitetura da informação;
- protótipo;
- avaliação.

---

# 11. Síntese comparativa

Como esta equipe possui apenas um integrante e foi selecionada uma única solução representativa, a síntese compara o ANY.RUN com as necessidades identificadas para o projeto.

| Critério | ANY.RUN | Oportunidade para o projeto |
|---|---|---|
| Navegação | A plataforma organiza diferentes informações relacionadas à análise e permite passar da visão geral para informações específicas. | Criar uma navegação simples e coerente, organizada de acordo com as principais categorias de comportamento do sistema operacional. |
| Feedback / estado | A análise fornece informações durante sua execução e apresenta resultados após o processamento. | Apresentar claramente o estado da análise e permitir que o usuário compreenda quando os resultados estão disponíveis. |
| Prevenção / recuperação de erro | A plataforma controla a execução da amostra em ambiente isolado, mas existem condições e limitações que podem afetar a análise. | Comunicar claramente falhas ou limitações e informar quando uma análise não produziu dados suficientes. |
| Terminologia | Utiliza termos técnicos relacionados à segurança, processos, indicadores e análise de ameaças. | Utilizar terminologia técnica adequada ao público, mas apresentar explicações quando um conceito puder gerar dúvida. |
| Acessibilidade | A interface apresenta grande quantidade de informações técnicas, exigindo atenção à organização e legibilidade. | Priorizar hierarquia visual, tamanho adequado dos elementos, contraste e organização das informações. |
| Eficiência | A plataforma disponibiliza uma visão consolidada e diferentes formas de investigação dos resultados. | Permitir que o usuário compreenda rapidamente o comportamento geral da aplicação sem precisar analisar todos os eventos individualmente. |

---

# 12. Recomendações derivadas

As recomendações abaixo foram derivadas da análise do ANY.RUN e das necessidades identificadas para o projeto.

## RC01 — Utilizar uma visão geral da análise

A interface deverá apresentar inicialmente um resumo do comportamento observado.

**Derivada de:** C01 — ANY.RUN.

**Justificativa:** uma visão consolidada permite que o usuário compreenda rapidamente o contexto antes de acessar informações detalhadas.

---

## RC02 — Organizar os resultados por categorias

As informações coletadas deverão ser agrupadas em categorias relacionadas ao comportamento da aplicação no sistema operacional.

**Derivada de:** C01 — ANY.RUN.

### Possíveis categorias iniciais

- Processos;
- Arquivos;
- Registro;
- Rede;
- Recursos;
- Comportamentos.

---

## RC03 — Utilizar detalhamento progressivo

A interface deverá apresentar inicialmente informações essenciais e permitir que o usuário aprofunde a análise quando necessário.

**Derivada de:** C01 — ANY.RUN.

**Justificativa:** reduz a quantidade de informações apresentada simultaneamente e pode diminuir a sobrecarga cognitiva.

---

## RC04 — Destacar comportamentos relevantes

Informações que mereçam atenção deverão possuir destaque visual adequado.

**Derivada de:** C01 — ANY.RUN.

**Justificativa:** indicadores e informações destacadas podem auxiliar na identificação rápida de eventos relevantes.

---

## RC05 — Apresentar o estado da análise de maneira clara

O sistema deverá informar claramente se a análise está:

- aguardando execução;
- em execução;
- processando resultados;
- concluída;
- concluída com limitações;
- ou com erro.

**Derivada de:** C01 — ANY.RUN.

---

## RC06 — Priorizar compreensão em vez de volume de dados

A interface não deverá simplesmente apresentar todos os eventos coletados pelo sandbox.

O objetivo será transformar os dados técnicos em informações organizadas que auxiliem o usuário na compreensão do comportamento da aplicação.

**Derivada de:** C01 — ANY.RUN + problema de IHC identificado na Entrega 1.

---

## RC07 — Permitir acesso às evidências técnicas

Embora o dashboard priorize informações resumidas, o usuário deverá conseguir consultar os detalhes que sustentam determinada informação quando necessário.

**Derivada de:** C01 — ANY.RUN.

**Justificativa:** o usuário precisa poder passar da interpretação para a evidência técnica.

---

## RC08 — Não reproduzir a interface do ANY.RUN

A interface do projeto não terá como objetivo copiar o fluxo ou a experiência do ANY.RUN.

O ANY.RUN será utilizado como **referência de domínio e de padrões de apresentação de informações**, enquanto a solução desenvolvida terá como foco específico a visualização dos resultados obtidos pelo sandbox.

**Derivada de:** decisão de escopo da equipe.

---

## RC09 — Não incluir funcionalidades sem tarefa associada

Funcionalidades como:

- histórico avançado;
- filtros complexos;
- comparação de análises;
- administração / CRUD;
- interação direta com a VM;

não deverão ser incluídas apenas por existirem em ferramentas do mesmo domínio.

Sua inclusão dependerá da identificação de uma necessidade real do usuário nas próximas etapas de IHC.

**Derivada de:** princípio metodológico da disciplina + decisão de escopo da equipe.

---

# 13. Relação com o TCC

A interface proposta nesta disciplina está relacionada à capacidade técnica desenvolvida no TCC, mas não constitui automaticamente parte do TCC.

### TCC

O TCC possui como tema:

> **Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais.**

Seu foco principal está na implementação e análise do ambiente capaz de executar aplicações potencialmente não confiáveis de maneira controlada e observar seus comportamentos e efeitos sobre o sistema operacional.

### IHC

A disciplina de IHC utiliza essa capacidade técnica como domínio para investigar:

> **Como apresentar ao usuário os resultados produzidos durante a análise de uma aplicação de maneira organizada, compreensível e adequada às suas atividades?**

Assim, a interface de IHC será inicialmente tratada como uma **extensão conceitual do TCC**, podendo futuramente ser incorporada ao projeto principal caso isso seja definido junto ao orientador.

---

# 14. Hipóteses atualizadas

A análise do ANY.RUN permite atualizar algumas hipóteses levantadas na Entrega 1.

### H01 — Dashboard pode facilitar a compreensão inicial

**Hipótese:** uma visão geral dos resultados pode permitir que o usuário compreenda rapidamente o comportamento geral da aplicação antes de investigar eventos específicos.

---

### H02 — Organização por categorias pode reduzir a complexidade

**Hipótese:** organizar os resultados em categorias como processos, arquivos, Registro, rede e recursos pode facilitar a interpretação de informações técnicas.

---

### H03 — Excesso de informações pode gerar sobrecarga cognitiva

**Hipótese:** apresentar todos os eventos coletados simultaneamente pode dificultar a localização e interpretação das informações relevantes.

---

### H04 — Informações resumidas e detalhadas devem coexistir

**Hipótese:** usuários podem precisar de um resumo inicial, mas também de acesso às evidências técnicas que sustentam esse resumo.

---

### H05 — O Analista de Segurança é um usuário prioritário

**Hipótese:** o Analista de Segurança da Informação representa inicialmente o perfil mais adequado para orientar o desenvolvimento da interface.

Essa hipótese deverá ser validada ou modificada nas próximas entregas.

---

### H06 — A interface não precisa reproduzir a experiência de uma sandbox interativa

**Hipótese:** para o objetivo definido neste projeto, uma interface focada na visualização e interpretação dos resultados pode ser mais adequada do que uma interface voltada ao controle direto da máquina virtual.

---

### H07 — A interface pode ser orientada à análise pós-execução

**Hipótese:** o usuário poderá realizar suas principais atividades de investigação a partir dos dados coletados após a execução da aplicação.

---

# 15. Síntese da Entrega 2

A análise do ANY.RUN permitiu compreender como uma solução existente organiza e apresenta informações relacionadas à execução e análise de aplicações em ambiente controlado.

Entretanto, a análise também permitiu identificar que o projeto de IHC não precisa reproduzir a mesma abordagem.

A direção definida para o projeto é:

> **Executar e monitorar tecnicamente no sandbox; apresentar e interpretar os resultados por meio de um dashboard.**

O foco da interface será a **compreensão do comportamento da aplicação no sistema operacional**, e não o controle direto da máquina virtual.

O dashboard deverá apresentar uma visão geral da análise e permitir o acesso progressivo às informações detalhadas.

As principais categorias inicialmente consideradas são:

- Processos;
- Arquivos;
- Registro;
- Rede;
- Recursos;
- Comportamentos.

Essa estrutura ainda é preliminar e deverá ser validada a partir das próximas atividades de IHC.

---

# 16. Como esta entrega alimenta as próximas etapas

A Entrega 2 produz informações que serão utilizadas nas próximas etapas do projeto.

### Público-alvo

Usuário prioritário inicial:

> **Analista de Segurança da Informação.**

Outros públicos permanecem como possibilidades:

- Infraestrutura;
- pesquisadores;
- estudantes.

### Problema de IHC

> **Como apresentar uma grande quantidade de informações técnicas produzidas por uma análise sandbox de maneira que o usuário consiga compreender o comportamento da aplicação e investigar os detalhes relevantes?**

### Direção inicial

> **Dashboard para visualização e interpretação dos resultados da análise.**

### Próximos elementos a investigar

- Persona;
- objetivos do usuário;
- cenários de uso;
- tarefas;
- informações necessárias;
- hierarquia de informações;
- modelo conceitual;
- organização do dashboard;
- prototipação;
- avaliação.

---

# Referências

- ANY.RUN. **Interactive Malware Analysis Sandbox for SOC Teams**. Disponível em: https://any.run/features/
- ANY.RUN. **Interactive Online Malware Sandbox**. Disponível em: https://any.run/
- ANY.RUN. **Plans and Pricing for Malware Sandbox**. Disponível em: https://any.run/plans/
- ANY.RUN. **Malware Analysis in a Sandbox**. Disponível em: https://any.run/cybersecurity-blog/malware-analysis-in-a-sandbox/
- G2. **ANY.RUN Sandbox Reviews**. Avaliações públicas de usuários da plataforma. Disponível em: https://www.g2.com/products/any-run-sandbox/reviews
- Gartner Peer Insights. **ANY.RUN — Likes & Dislikes**. Avaliações e percepções de usuários. Disponível em: https://www.gartner.com/reviews/market/intrusion-prevention-systems/vendor/any-run
- GitHub. **Projeto-IHC-FEI — Entrega 2: Público-alvo e análise de concorrência**. Modelo acadêmico utilizado na disciplina.

---

# Checklist

- [x] O mapa inicial de alternativas da Entrega 1 foi revisitado.
- [x] Foi selecionada uma interface representativa para análise.
- [x] Há pelo menos uma análise completa para o integrante da equipe.
- [ ] Prints legíveis da interface foram adicionados ao diretório `assets/02_concorrencia/`.
- [ ] Os prints mostram telas/estados relevantes da interface.
- [x] O ANY.RUN foi analisado sob a perspectiva de IHC.
- [x] Padrões de interface foram relacionados às tarefas do público-alvo.
- [x] O ANY.RUN foi utilizado como referência e não como modelo a ser copiado.
- [x] Histórico + filtros foi descartado do escopo atual.
- [x] Interação direta com a VM foi descartada do escopo atual.
- [x] Comparação de resultados foi considerada provavelmente não aplicável ao escopo atual.
- [x] Administração / CRUD foi descartada do escopo atual.
- [x] Foi definido o dashboard como direção inicial para a interface.
- [x] Foram identificadas possíveis categorias de informações para o dashboard.
- [x] Foram levantadas recomendações de IHC.
- [x] Foram atualizadas as hipóteses do projeto.
- [x] Foi estabelecida a relação entre a Entrega 2 e as próximas etapas.
- [x] A relação entre TCC e IHC foi explicitada.
