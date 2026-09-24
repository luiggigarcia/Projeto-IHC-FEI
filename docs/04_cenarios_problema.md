# Entrega 4 — Cenários de análise/problema

**Data:** 24/09/2026  
**Status:** 🟩 Concluído  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo

Descrever situações atuais em que o usuário busca atingir um objetivo e encontra dificuldades, tornando visíveis o contexto, os atores, as ações realizadas e as possíveis rupturas durante a atividade.

Como o TCC não possui uma interface definida, o cenário descreve a atividade humana relacionada à análise do comportamento de aplicações potencialmente não confiáveis, sem propor uma solução de interface neste momento.

---

# C01 — Investigação do comportamento de uma aplicação potencialmente não confiável

**Autor:** Luiggi Paschoalini Garcia — 22.122.006-4  
**Persona:** P01 — Rafael Mendes, Analista de Segurança da Informação  
**Necessidade:** R01 — Compreender o comportamento de uma aplicação potencialmente não confiável durante sua execução, utilizando as evidências coletadas em um ambiente controlado para identificar suas ações e efeitos no sistema operacional.

## 1. Cenário inicial

Rafael Mendes, Analista de Segurança da Informação, recebe um arquivo executável cuja procedência ou comportamento não é conhecido. Antes de permitir que a aplicação seja executada diretamente em um ambiente de produção, ele precisa compreender o que ela pode realizar no sistema operacional.

Para isso, Rafael utiliza um ambiente controlado para executar a aplicação e observar seu comportamento durante a execução. Nesse processo, são observados diferentes tipos de eventos e informações, como processos criados ou encerrados, alterações em arquivos e configurações do sistema, utilização de recursos e comunicações de rede.

Após a execução, Rafael precisa analisar os eventos registrados para identificar quais comportamentos são relevantes para a investigação. A quantidade e a variedade das informações coletadas podem dificultar a localização dos acontecimentos mais importantes. Além disso, determinados comportamentos podem depender da relação entre eventos de diferentes categorias ou ocorridos em momentos distintos.

Dessa forma, a atividade não envolve apenas coletar eventos, mas também compreender o que ocorreu durante a execução, relacionar as evidências disponíveis e registrar as conclusões obtidas a partir da investigação.

### Hipóteses relacionadas

- **H01:** A análise de uma aplicação potencialmente não confiável pode envolver diferentes tipos de comportamento no sistema operacional, como criação de processos, alterações em arquivos e configurações, utilização de recursos e comunicação de rede.
- **H02:** A quantidade e a variedade de informações produzidas durante a execução podem dificultar a interpretação dos resultados, exigindo uma organização que permita relacionar diferentes evidências.

---

# 2. Questões de refinamento

As questões abaixo buscam aprofundar o cenário e identificar informações ainda não confirmadas sobre a atividade, considerando perguntas relacionadas a **por quê**, **como**, **o que é** e relações entre elementos da atividade.

| # | Questão | Por que investigar? | Fonte / forma de obtenção |
|---|---|---|---|
| Q1 | Por que a aplicação é executada em um ambiente controlado? | Identificar quais riscos ou necessidades justificam o isolamento durante a investigação. | Literatura sobre sandboxing e entrevistas com profissionais. |
| Q2 | O que Rafael precisa descobrir para considerar que compreendeu o comportamento da aplicação? | Identificar quais informações são realmente relevantes para o objetivo da análise. | Entrevistas e observação da atividade. |
| Q3 | Como Rafael determina quais eventos são relevantes para a investigação? | Compreender os critérios utilizados para diferenciar informações relevantes de eventos secundários. | Entrevistas, observação e literatura de análise comportamental. |
| Q4 | Os eventos de processos, arquivos, configurações, rede e recursos fazem parte da mesma investigação? | Verificar como diferentes categorias de evidências são relacionadas durante a análise. | Entrevistas e análise de práticas existentes. |
| Q5 | Como Rafael relaciona eventos que acontecem em momentos diferentes durante a execução? | Investigar a importância da sequência temporal para compreender o comportamento da aplicação. | Entrevistas e observação da atividade. |
| Q6 | A quantidade de eventos registrados pode dificultar a investigação? | Verificar se o volume de informações constitui uma dificuldade real para o usuário. | Entrevistas, observação e literatura. |
| Q7 | Por que um único evento registrado pode não ser suficiente para compreender determinado comportamento? | Identificar situações em que é necessário relacionar diferentes evidências para interpretar uma ação. | Entrevistas e análise de casos. |
| Q8 | Um mesmo evento pode possuir interpretações diferentes dependendo dos outros eventos observados? | Investigar a importância do contexto para a interpretação dos resultados. | Entrevistas e análise de casos. |
| Q9 | Como o profissional registra e comunica as conclusões obtidas durante a investigação? | Compreender como os resultados são documentados e compartilhados atualmente. | Entrevistas e observação. |
| Q10 | O que acontece quando uma informação relevante não é registrada durante a execução? | Identificar possíveis consequências de uma coleta incompleta de evidências. | Entrevistas e literatura. |

---

# 3. Cenário refinado

Rafael Mendes, Analista de Segurança da Informação, recebe um arquivo executável cuja procedência ou comportamento não é conhecido. Antes de permitir sua execução direta em um ambiente de produção, ele precisa compreender o comportamento da aplicação e identificar possíveis ações realizadas no sistema operacional.

**[NOVO: Para reduzir a exposição do ambiente utilizado na investigação, Rafael executa a aplicação em um ambiente controlado, no qual seu comportamento pode ser observado durante a execução.]**

Durante a execução, **[NOVO: Rafael acompanha diferentes categorias de eventos, incluindo processos, arquivos, configurações do sistema, utilização de recursos e comunicações de rede.]** Esses eventos podem representar diferentes aspectos do comportamento da aplicação e precisam ser considerados dentro do contexto da investigação.

Após a execução, Rafael analisa as informações coletadas para identificar os acontecimentos relevantes. **[NOVO: A relevância de um evento pode depender de outros acontecimentos registrados durante a mesma execução, especialmente quando diferentes eventos estão relacionados ou ocorrem em momentos distintos.]**

**[NOVO: O volume e a variedade das informações podem tornar mais difícil localizar os acontecimentos importantes e compreender a relação entre eles.]** Por esse motivo, Rafael precisa interpretar as evidências disponíveis e construir uma compreensão do comportamento observado, em vez de apenas consultar eventos isolados.

**[NOVO: Ao final da investigação, Rafael registra ou comunica as conclusões obtidas a partir das evidências analisadas.]** Quando informações relevantes não são registradas ou quando os eventos não podem ser relacionados adequadamente, **[NOVO: a compreensão sobre o comportamento da aplicação pode permanecer incompleta.]**

O cenário, portanto, envolve uma atividade de investigação na qual o profissional precisa compreender o comportamento de uma aplicação a partir de diferentes evidências produzidas durante sua execução controlada.

---

# 4. Elementos extraídos do cenário

| Elemento | Descrição |
|---|---|
| **Atores** | Analista de Segurança da Informação; aplicação potencialmente não confiável; ambiente controlado; sistema operacional. |
| **Objetivo** | Compreender o comportamento da aplicação e identificar suas ações e efeitos no sistema operacional. |
| **Contexto** | Investigação de uma aplicação cuja procedência ou comportamento é desconhecido, utilizando um ambiente controlado. |
| **Recursos / informações** | Eventos de processos, arquivos, configurações do sistema, utilização de recursos, comunicações de rede e informações relacionadas à execução. |
| **Ações** | Receber a aplicação; preparar a execução; executar em ambiente controlado; observar eventos; identificar acontecimentos relevantes; relacionar evidências; interpretar resultados; registrar ou comunicar conclusões. |
| **Problemas / rupturas** | Grande quantidade de eventos; variedade de informações; dificuldade para identificar acontecimentos relevantes; necessidade de relacionar eventos; dificuldade de interpretar eventos isolados; possibilidade de informações relevantes não serem registradas. |
| **Consequências** | Compreensão incompleta do comportamento da aplicação; dificuldade para interpretar as evidências; necessidade de realizar análises adicionais; possíveis conclusões baseadas em informações incompletas. |

---

# 5. Implicações para as próximas entregas

A partir do cenário refinado, as próximas etapas devem investigar principalmente:

- Como o profissional interpreta os resultados produzidos durante a análise.
- Quais informações são consideradas relevantes para compreender o comportamento da aplicação.
- Como diferentes eventos e evidências são relacionados durante a investigação.
- Qual importância a sequência temporal dos eventos possui para a compreensão do comportamento.
- Quais dificuldades surgem diante de grandes volumes de informações.
- Como o profissional identifica e trata eventos que, isoladamente, possuem pouco significado.
- Como as conclusões da investigação são registradas e comunicadas.
- Quais informações são consultadas em conjunto durante a atividade.
- Em quais situações uma coleta incompleta de informações prejudica a investigação.
- Quais dessas dificuldades são efetivamente observadas por profissionais e não apenas hipóteses do projeto.

Neste momento, não são definidas telas, componentes, funcionalidades ou soluções de interface. Essas decisões deverão ser derivadas posteriormente a partir da compreensão mais aprofundada das atividades e necessidades identificadas.

---

# Checklist

- [x] O cenário possui rastreabilidade com a Entrega 1.
- [x] O cenário está relacionado à persona P01.
- [x] A necessidade R01 está representada.
- [x] A situação concreta da Entrega 1 foi utilizada como base.
- [x] O cenário descreve uma atividade humana/problema atual.
- [x] O cenário apresenta atores, objetivo, contexto, ações e dificuldades.
- [x] Foram incluídas questões para refinamento do cenário.
- [x] As questões buscam identificar informações ainda não confirmadas.
- [x] O cenário foi refinado a partir das questões.
- [x] As informações adicionadas ao refinamento estão identificadas.
- [x] Foram extraídos os principais elementos do cenário.
- [x] Foram identificadas implicações para as próximas entregas.
- [x] Não foram propostas soluções de interface nesta etapa.
- [x] O cenário permanece alinhado ao domínio do TCC.
- [ ] As hipóteses ainda precisam ser validadas empiricamente com usuários/profissionais.
