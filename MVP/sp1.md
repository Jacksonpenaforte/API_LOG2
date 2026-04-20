# MVP 1 - Projeto Logística IBAMA (Cargas Especiais)

## 🎯 Objetivo do MVP

* **Problema que resolve:** A dificuldade de consolidar e limpar dados brutos do IBAMA (RAPP) sobre movimentação de cargas perigosas, garantindo uma base confiável para análise.
* **Hipótese a validar:** O tratamento de dados via Python/Pandas elimina redundâncias e valores nulos, permitindo uma modelagem de dados eficiente para Business Intelligence.
* **Valor entregue:** Base de dados higienizada e primeira carga de dados no Power BI para visualização da movimentação histórica.

## 📝 Descrição da Solução

### Funcionalidades principais incluídas:

* Automação de extração, limpeza e padronização de dados do IBAMA (RAPP) via Python/Pandas no Google Colab.
* Geração de base consolidada em CSV e scripts de carga para o Power BI.
* Dashboards interativos com mapas de fluxo (Origem-Destino), estado e tipo de carga especial.

### Limitações Conhecidas:

* A atualização dos dados depende da extração manual dos relatórios anuais do IBAMA.
* O MVP foca em cargas perigosas e especiais registradas entre **2013 – 2025**.
### Escopo Limitado
* o	Foco em fornecer as primeiras análises de movimentação logística e validar a utilidade da ferramenta para gestores ambientais e analistas de logística.

## 👥 Personas / Usuários-Alvo

* Persona 1 - **Gestor de Logística e Infraestrutura:** Necessita de relatórios precisos para decisões sobre rotas, segurança e investimentos.
* Persona 2 - **Analista de Dados / Ambiental:** Necessita de bases limpas para identificar gargalos e garantir o cumprimento de normas ambientais.

## 🔑 Histórias de Usuário (Sprint 1)

Todas as User stories abaixo possuem **Prioridade Alta** e foram **Concluídas**.

| ID | História do Usuário | Pontos |
|:---|:---|:---:|
| 1 | Como Analista/Gestor, quero tratar valores nulos e duplicados para que a base seja confiável. | 9 |
| 2 | Como Analista/Gestor, quero mapear origens e destinos para negociar melhores rotas. | 4 |
| 3 | Como Analista/Gestor, quero identificar empresas com declaração realizada para garantir o cumprimento das normas. | 4 |
| 4 | Como Analista/Gestor, quero visualizar os modais de transporte para avaliar a eficiência dos acessos. | 3 |
| 5 | Como Analista/Gestor, quero acompanhar a evolução temporal por gráficos históricos. | 3 |

## 💡 Observações

* Ferramentas utilizadas: **Python** para tratamento de dados e **Poqer BI** para visualização e análise, **Jira** para controle das tarefas.
* O foco é fornecer suporte à formulação de **políticas de logistica e segurança ambiental** com dados de movimentação de cargas limpos e confiáveis.
   
## 📅 Sprint(s) Relacionadas

| Sprint | Entregas Principais | Status |
|:---:|:---|:---:|
| 1 | Automação de extração e limpeza de dados (Python + Pandas. | Concluido |
| 2 | Integração com Power BI, matriz Origem-Destino e filtros de modais. | Concluido |
| 3 | Publicação da documentação no GitHub. | Concluido |

## 📊 Critérios de Aceitação e Métricas

* O **MVP** deve permitir que o usuário visualize e filtre os dados consolidados de movimentação de cargas (2013–2025).
* O sistema deve disponibilizar o download da base de dados tratada e consolidada em formato CSV.
* O dashboard deve apresentar obrigatoriamente o Mapa de Fluxo (Matriz Origem-Destino) e a segmentação por modais de transporte.
* Métricas coletadas: tempo de processamento do script de limpeza, precisão na identificação de cargas perigosas e feedback dos gestores sobre a clareza dos indicadores.

## 📈 Métricas de Validação

* Nº de inconsistências (duplicados/nulos) removidas durante o processo de ETL.
* Tempo de processamento para a geração da base consolidada.
* Feedback qualitativo dos analistas sobre a confiabilidade da base inicial.

## 🧠 Próximos Passos: MVP 2 (Sprint 2)

* Ajuste de Precisão nas Métricas: Revisar as medidas DAX (Power BI) para garantir que as toneladas e volumes reflitam exatamente a base tratada, corrigindo casas decimais.
* Análise por Modal: Iniciar o cruzamento de dados para identificar qual modal (Rodoviário, Ferroviário etc.) é predominante para cada categoria de carga perigosa.
* Testes de Usabilidade: Realizar uma demonstração para os "Gestores de Logística" para validar se os filtros de região e estado atendem às necessidades de fiscalização.
* Documentação de ETL: Começar a redigir o manual técnico explicando como o script Python limpa os dados, facilitando a manutenção futura no GitHub.

## 📎 Anexos/Evidencias
- Link google Colabe (https://colab.research.google.com/drive/1LAeYP5MkqIlomHgFZOUsjb7Vgtn842dm?usp=sharing)
- Video Dashboard:
https://github.com/user-attachments/assets/a343540b-de81-4606-b2d5-89f771af1be2




---


