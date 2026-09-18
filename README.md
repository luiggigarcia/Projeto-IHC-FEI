# Projeto de Interação Humano-Computador (IHC)

> **Projeto acadêmico de IHC derivado do TCC em andamento.**

## Princípio do projeto da disciplina

A disciplina utiliza preferencialmente o tema do TCC em andamento como domínio para exercitar os métodos de Interação Humano-Computador.

Neste projeto, o TCC é predominantemente técnico e não prevê originalmente o desenvolvimento de uma interface. Dessa forma, a disciplina de IHC será utilizada para derivar um possível escopo de interação a partir da contribuição técnica desenvolvida no TCC, investigando quem poderia utilizar ou se beneficiar do resultado, quais atividades precisaria realizar, em qual contexto e quais formas de interação poderiam apoiar essas atividades.

A interface explorada neste projeto de IHC representa uma extensão conceitual do TCC e não constitui, neste momento, uma obrigação de implementação no trabalho de conclusão.

Leia obrigatoriamente o [Guia para definir o escopo de IHC a partir do tema do TCC](GUIA_ESCOPO_IHC.md).

## Identificação

**Título do projeto de IHC:** Interface para análise comportamental de aplicações em ambiente sandbox  
**TCC/projeto de origem:** Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais  
**Orientador(a):** Leonardo Anjoletto  
**Disciplina:** Interação Humano-Computador  
**Instituição:** Centro Universitário FEI  
**Semestre:** 2026/2

### Equipe

| Nome completo | Matrícula | GitHub | Responsabilidade principal |
|---|---:|---|---|
| Luiggi Paschoalini Garcia | 22.122.006-4 | luiggigarcia | Desenvolvimento e documentação do projeto |

## Relação entre TCC e projeto de IHC

| Item | Descrição |
|---|---|
| Tema central do TCC | Implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis em sistemas operacionais. |
| Resultado técnico esperado do TCC | Ambiente sandbox capaz de executar aplicações potencialmente não confiáveis de forma controlada e permitir a observação, coleta e análise de seus comportamentos e efeitos sobre o sistema operacional. |
| O TCC já previa interface? | Não |
| Capacidade técnica que pode gerar valor para pessoas | Permitir a execução controlada de aplicações e a análise aprofundada de seu comportamento no sistema operacional, incluindo processos, arquivos, recursos utilizados, atividades de rede, alterações de configurações e outros eventos relevantes. |
| Usuários principais adotados em IHC | Profissionais de Segurança da Informação, profissionais de Infraestrutura de TI, pesquisadores e estudantes de Computação e Segurança da Informação. |
| Objetivo principal desses usuários | Executar aplicações em um ambiente controlado e compreender, por meio das evidências coletadas, como elas interagem com o sistema operacional. |
| Interface/recorte explorado na disciplina | Interface para seleção e execução de aplicações, acompanhamento do ambiente sandbox, visualização e interpretação dos eventos coletados e geração/consulta de relatórios de análise. |
| Relação com o escopo formal do TCC | Extensão conceitual / protótipo demonstrativo |

> **Importante:** a tabela acima explica a relação entre os dois trabalhos. Ela não altera o compromisso formal do TCC.

## Resumo do projeto pela perspectiva do usuário

Profissionais de Segurança da Informação, profissionais de Infraestrutura de TI, pesquisadores e estudantes precisam compreender como determinadas aplicações se comportam durante sua execução e quais efeitos produzem no sistema operacional. Atualmente, uma análise aprofundada desse comportamento pode exigir a utilização de diferentes ferramentas e a interpretação de diversas informações técnicas. O tema do TCC investiga a implementação e análise de um ambiente sandbox para execução controlada de aplicações potencialmente não confiáveis, permitindo observar e coletar informações sobre suas ações no sistema operacional. Para fins da disciplina de IHC, será explorada uma interface que permita aos usuários executar aplicações em ambiente controlado, acompanhar seu comportamento, consultar as evidências coletadas e obter um relatório estruturado da análise.

> Afirmações sobre necessidades específicas dos usuários, processos atualmente utilizados e preferências de interação serão tratadas como hipóteses até que sejam investigadas nas próximas entregas.

## Por que pensar em interface mesmo em TCCs técnicos?

Embora o TCC tenha como foco principal a implementação e análise do ambiente sandbox, sua aplicação potencial envolve pessoas que precisam interagir com os resultados produzidos pelo sistema.

Um ambiente desse tipo pode ser utilizado por diferentes perfis, incluindo profissionais de Segurança da Informação, profissionais de Infraestrutura de TI, pesquisadores e estudantes. Esses usuários podem precisar:

- selecionar aplicações para análise;
- iniciar e acompanhar uma execução;
- observar processos e atividades realizadas;
- verificar alterações em arquivos e configurações;
- analisar utilização de recursos computacionais;
- observar atividades de rede;
- consultar eventos registrados durante a execução;
- interpretar os resultados obtidos;
- consultar análises anteriores;
- gerar relatórios;
- comparar resultados de diferentes execuções;
- investigar comportamentos específicos.

Essas atividades fornecem um campo para exercitar os métodos de IHC e investigar como as informações produzidas pelo ambiente sandbox podem ser apresentadas de forma compreensível e útil.

A interface será definida progressivamente ao longo das entregas da disciplina. Não serão assumidos elementos de interface apenas por serem comuns em sistemas computacionais; cada funcionalidade deverá estar relacionada a uma atividade ou objetivo identificado para os usuários.

## Relação com apresentação e potencial de aplicação

A reflexão sobre usuários ajuda a apresentar o projeto para públicos externos, inclusive em eventos acadêmicos e de inovação, como a INOVA.

Em vez de apresentar somente os mecanismos técnicos utilizados para implementar o sandbox, o projeto pode ser comunicado a partir da relação:

**problema humano → contribuição computacional → forma de uso → impacto potencial**

O sandbox pode possuir aplicações potenciais nas áreas de Segurança da Informação e Infraestrutura de TI, além de ambientes de pesquisa e ensino.

Para profissionais de Segurança da Informação, o ambiente pode apoiar a investigação do comportamento de aplicações potencialmente não confiáveis.

Para profissionais de Infraestrutura, pode possibilitar a observação dos impactos de determinadas aplicações sobre o sistema operacional e seus recursos.

Para pesquisadores e estudantes, pode fornecer um ambiente controlado para experimentação, investigação e aprendizado sobre o funcionamento de aplicações e sua interação com o sistema operacional.

O protótipo de IHC poderá funcionar como uma demonstração desse potencial de aplicação, sem necessariamente integrar a implementação final do TCC.

## Como usar este repositório

1. Leia o [Guia de uso e apresentação](GUIA_DE_USO.md).
2. Leia o [Guia de definição de escopo de IHC](GUIA_ESCOPO_IHC.md), especialmente porque o TCC não prevê originalmente uma interface.
3. Preencha as entregas na ordem em que forem trabalhadas na disciplina.
4. Em toda entrega individual, identifique o autor.
5. Salve imagens, diagramas e evidências em [`assets/`](assets/README.md).
6. Mantenha a [Matriz de rastreabilidade](RASTREABILIDADE.md) atualizada.
7. Na Entrega 1, diferencie **[F] fatos**, **[H] hipóteses** e **[?] lacunas de conhecimento**.
8. Antes de cada entrega, revise o checklist do arquivo e o [Checklist final](CHECKLIST_FINAL.md).
9. Sempre que uma evidência posterior contrariar uma hipótese inicial, revise o projeto. IHC é um processo iterativo.

## Entregas

| # | Entrega | Quantidade mínima / responsabilidade | Status |
|---:|---|---|---|
| 1 | [Conhecendo o projeto, o usuário e o problema](docs/01_conhecendo_o_problema.md) | 1 solução consolidada por equipe | 🟩 |
| 2 | [Público-alvo e análise de concorrência](docs/02_analise_concorrencia.md) | no mínimo 1 concorrente/interface representativa por integrante + síntese | 🟩 |
| 3 | [Personas, empatia, contexto e jornada](docs/03_personas_contexto_jornada.md) | 1 persona por integrante; demais artefatos consolidados | 🟩 |
| 4 | [Cenários de análise/problema](docs/04_cenarios_problema.md) | 1 solução completa por integrante | ⬜ |
| 5 | [Análise de tarefas: HTA, GOMS e CTT](docs/05_analise_tarefas.md) | cada integrante: pelo menos 1 HTA + 1 GOMS + 1 CTT | ⬜ |
| 6 | [Prototipação em papel](docs/06_prototipacao_papel.md) | 1 protótipo integrado por equipe | ⬜ |
| 7 | [Coleta de dados e aspectos éticos](docs/07_coleta_dados.md) | soluções individuais + técnicas distintas; questionário entre as técnicas | ⬜ |
| 8 | [Ciclo de vida e engenharia de usabilidade](docs/08_engenharia_usabilidade.md) | 1 solução consolidada por equipe | ⬜ |
| 9 | [Modelo conceitual e design centrado na comunicação](docs/09_modelo_conceitual.md) | soluções individuais + consolidação de objetivos/signos | ⬜ |
| 10 | [MoLIC](docs/10_molic.md) | 1 diagrama completo por integrante | ⬜ |
| 11 | [Protótipo no Figma](docs/11_figma.md) | 1 protótipo integrado por equipe, cobrindo fluxos modelados | ⬜ |
| 12 | [Planejamento da avaliação — DECIDE](docs/12_planejamento_avaliacao.md) | 1 plano consolidado por equipe | ⬜ |
| 13 | [Avaliação heurística](docs/13_avaliacao_heuristica.md) | 1 avaliação completa por integrante, todas as telas/estados e 10 heurísticas | ⬜ |
| 14 | [Avaliação por observação de usuários](docs/14_observacao_usuario.md) | avaliação consolidada; nº de participantes finais = nº de integrantes | ⬜ |

> Se o docente definir quantidade diferente para a turma/semestre, a orientação da disciplina prevalece.

## Visão de continuidade

O projeto deve formar uma cadeia de evidências:

**tema/contribuição do TCC → possível aplicação → usuários/stakeholders → objetivos → problema/contexto → alternativas → necessidades → personas → cenários → tarefas → modelo conceitual → MoLIC → protótipo → planejamento → inspeção → teste com usuários → melhorias**

Para este projeto, a cadeia parte da capacidade técnica do sandbox e investiga progressivamente como essa capacidade poderia ser utilizada por diferentes perfis.

O foco inicial será compreender a necessidade de executar aplicações em ambiente controlado e analisar de maneira aprofundada seus efeitos sobre o sistema operacional.

As entregas seguintes deverão investigar e validar:

- quais perfis possuem maior interesse na solução;
- quais atividades realizariam;
- quais informações consideram mais relevantes;
- como ferramentas existentes apresentam essas informações;
- quais dificuldades existem nas alternativas atuais;
- como os resultados poderiam ser organizados;
- quais interações são realmente necessárias;
- como uma interface poderia apoiar a análise;
- como avaliar a qualidade dessa interação.

Uma entrega não deve reiniciar o projeto. As decisões tomadas nas etapas iniciais deverão ser utilizadas como base para personas, cenários, tarefas, modelo conceitual, MoLIC, protótipo e avaliações posteriores, salvo quando novas evidências justificarem a revisão do projeto.

## Documentos de apoio

- [Guia de uso e apresentação](GUIA_DE_USO.md)
- [Guia para definir o escopo de IHC a partir do TCC](GUIA_ESCOPO_IHC.md)
- [Matriz de rastreabilidade](RASTREABILIDADE.md)
- [Checklist final](CHECKLIST_FINAL.md)
- [Bibliografia de IHC](BIBLIOGRAFIA.md)
- [Orientações de contribuição no GitHub](CONTRIBUTING.md)
- [Instrumentos reutilizáveis](instrumentos/README.md)
