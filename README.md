#   Aprendizado por Projeto Integrado (API) 
##  Grupo G2 Logística - 2 Semestre - LogTeam


# Índice
* [Objetivo do Projeto](#objetivo-do-projeto)
* [Equipe](#equipe)
* [Backlog do produto](#Backlog-Logteam)
* [Competências desenvolvidas](#competências-desenvolvidas)
* [Registro das Sprints](#registro-das-sprints)


# Projeto (API) 
  A Aprendizagem  por Projetos Integradores estabelece um modelo educacional dinâmico, espelhando princípios das metodologias ágeis. O propósito fundamental deste método reside em capacitar os estudantes, permitindo que eles adquiram saberes e competências por meio da participação ativa em empreendimentos práticos. A estrutura de trabalho organiza-se em fases sequenciais de idealização, concretização e avaliação reflexiva. Esta abordagem enfatiza a aplicação colaborativa de saberes oriundos de distintas disciplinas para enfrentar problemas factuais, o que fomenta uma constante capacidade de ajuste e a entrega progressiva de entregáveis funcionais.

  Integrative Project-Based Learning establishes a dynamic educational model that reflects the principles of agile methodologies. The fundamental objective of this method is to empower students by enabling them to acquire knowledge and skills through active participation in practical projects. The work structure is organized into sequential phases of ideation, implementation, and reflective evaluation. This approach emphasizes the collaborative application of knowledge from different disciplines to address concrete problems, which fosters a constant capacity for adaptation and the progressive delivery of functional results.

  

# Equipe
| Função         | Nome     | GitHub | |
|----------------|----------|----------|--------|
| Product Owner  | Alisson Paulo de Andrade  | [GitHub](https://github.com/alisson051013) | |
| Scrum Master   | Bianca Ayumi Nakamura | [GitHub](https://github.com/BiancaAyumiNakamura) | |
| Team Member    | Jackson David Rodrigues Penaforte | [GitHub](https://github.com/Jacksonpenaforte) |  |
| Team Member    | Marcelo R. Osako  | [GitHub](https://github.com/marceloosako-mo) |  |
| Team Member    | Raquel Araújo Lima | [GitHub](https://github.com/RaquelAraujoL) |  |
| Team Member    | Vinícius Alessandro Moreira | [GitHub](https://github.com/Viniimoreira)|  |


# Objetivo do Projeto
O objetivo principal deste projeto é o desenvolvimento de uma solução de Business Intelligence (BI) focada na análise do fluxo de cargas especiais e perigosas,como foco em combustíveis,  utilizando como base os dados registrados no Relatório Anual de Atividades Potencialmente Poluidoras (RAPP) do IBAMA.

A plataforma visa transformar dados brutos em indicadores estratégicos, permitindo:


* Monitoramento de Movimentação: Analisar métricas nacionais e estaduais sobre os tipos de cargas movimentadas e sua evolução temporal entre os anos de 2013 e 2025.

* Análise Logística: Identificar os principais modais de transporte utilizados e a matriz de Origem e Destino (OD) das cargas.

* Mapeamento de Atores: Identificar as principais empresas movimentadoras de cargas perigosas com declarações ativas no sistema.

* Suporte à Decisão: Fornecer uma interface visual limpa e intuitiva que auxilie na formulação de políticas públicas e no desenvolvimento de estudos acadêmicos sobre a segurança e logística de produtos perigosos no Brasil.

Para alcançar esses objetivos, o projeto utiliza um pipeline de dados que envolve a extração e limpeza via Python (Pandas) no ambiente Google Colab, com a visualização final e painéis de indicadores construídos em Power BI.


## Ferramentas Utilizadas

* Jira Software
* Power BI
* Whatsapp
* Python (Colab)



# Backlog - LogTeam

|   RANK | PRIORIDADE   | USER STORY                                                                                                                                                                                                                                                 |   ESTIMATIVA |   SPRINT | STATUS    |
|-------:|:-------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------:|---------:|:----------|
|      1 | Alta         | Como Analista/Gestor, eu quero realizar a extração e o tratamento de valores nulos e duplicados dos dados do IBAMA com registro no RAPP, para que a base de dados do dashboard seja confiável e livre de redundâncias que possam distorcer os indicadores. |            9 |        1 | Andamento |
|      2 | Alta         | Como Analista/Gestor, quero mapear as principais origens e destinos das mercadorias para negociar melhores rotas com armadores e transportadoras.                                                                                                          |            4 |        1 | Andamento |
|      3 | Alta         | Como Analista/Gestor, quero identificar as empresas que movimentam cargas perigosas com declaração realizada para garantir o cumprimento das normas ambientais.                                                                                            |            4 |        1 | Andamento |
|      4 | Alta         | Como Analista/Gestor, quero visualizar os modais de transporte utilizados para avaliar a eficiência dos acessos terrestres e planejar expansões.                                                                                                           |            3 |        1 | Andamento |
|      5 | Alta         | Como Analista/Gestor, quero acompanhar a evolução da movimentação ao longo do tempo através de gráficos históricos para embasar decisões estratégicas.                                                                                                     |            3 |        1 | Andamento |
|      6 | Média        | Como Analista/Gestor eu quero que os nomes das cargas perigosas sejam padronizados, para que eu consiga filtrar e agrupar os tipos de produtos de forma precisa, sem variações ortográficas que separem o mesmo item.                                      |            3 |        2 | Pendente  |
|      7 | Média        | Como Analista/Gestor, eu quero visualizar a Matriz Origem-Destino em um mapa interativo, para que eu possa identificar as rotas de cargas perigosas com maior fluxo e otimizar o planejamento de fiscalização regional.                                    |            5 |        2 | Pendente  |
|      8 | Média        | Como Analista/Gestor, eu quero filtrar os dados por região, estado e tipo de carga, para que eu possa realizar análises granulares e entender o comportamento logístico de nichos específicos.                                                             |            3 |        2 | Pendente  |
|      9 | Média        | Como Analista/Gestor, eu quero visualizar a evolução da movimentação através de gráficos de linhas ao longo dos anos, para que eu possa prever tendências de crescimento ou identificar quedas atípicas na movimentação de produtos perigosos.             |            4 |        2 | Pendente  |
|     10 | Média        | Como Analista/Gestor, eu quero identificar os modais mais utilizados (Rodoviário, Ferroviário, etc.) para cada categoria de carga perigosa, para que eu possa validar a adequação da infraestrutura utilizada e os riscos associados a cada modal.         |            5 |        2 | Pendente  |
|     11 | Baixa        | Como Analista/Gestor, eu quero extrair relatórios baseados na análise de impacto dos dados, para que eu possa embasar decisões governamentais sobre segurança ambiental e investimentos em rodovias ou ferrovias.                                          |            6 |        3 | Pendente  |
|     12 | Baixa        | Como Analista/Gestor, eu quero localizar os gargalos logísticos nos estados (áreas de alta retenção ou saturação), para que eu possa sugerir melhorias em pontos críticos da malha de transporte.                                                          |            4 |        3 | Pendente  |
---



# Registro das Sprints

| Sprint            | Previsão   | Status   | Histórico |
|-------------------|------------|----------|-----------|
| 01                | 23/04/2026 | Andamento |   |
| 02                | 30/10/2025 | A fazer |  |
| 03                | 13/11/2025 | A fazer |   |
| Feira de Soluções | 04/12/2025 | A fazer|  |

