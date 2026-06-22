# Portfólio de Data Analytics & BI
Este repositório centraliza meus projetos práticos de análise de dados, engenharia de
recursos e Business Intelligence. Cada projeto abaixo representa a resolução de um desafio
de negócio real, documentado desde o tratamento da base de dados bruta até a entrega do
relatório executivo.
---
## Projeto 1: BI Aplicado à Logística Internacional
<span class="tag">Power BI</span><span class="tag">Modelagem Star Schema</span><span
class="tag">Análise de Gargalos</span>
* **Contexto de Negócio:** Análise focada na otimização da cadeia de suprimentos e
identificação de atrasos operacionais em fretes internacionais.
* **Desafio Técnico:** Organização de dados temporais dispersos para calcular o tempo
médio de tráfego real entre pontos de controle aduaneiro.
* **Solução Aplicada:** Estruturação de modelo relacional limpo conectando tabelas de
rotas e históricos de movimentação. Desenvolvimento de painel executivo dinâmico que
destaca os principais gargalos e desvios de prazo por transportadora.
* **Entregáveis:** Arquivo original do Power BI (`.pbix`).
---
## Projeto 2: Engenharia de Dados e Analytics Financeiro — Bravos Burger & Co.
<span class="tag tag-tech">Python (Pandas)</span> <span class="tag">Power BI (DAX)</span> <span class="tag">Integridade Relacional</span>
* **Contexto de Negócio:** Consolidação do faturamento real e margens de lucro de uma
operação de fast-food com tabelas fragmentadas.
* **Desafio Técnico:** A base bruta apresentava falhas críticas de escala de faturamento
devido à fragmentação de dados. As tabelas de vendas continham apenas quantidades,
enquanto os preços unitários residiam isolados no cadastro de produtos (Dimensão), gerando
distorções de cálculo por colunas calculadas redundantes que pesavam o modelo.
* **Solução Aplicada:**
1. **Tratamento Prévio (Python):** Limpeza e padronização de strings, tratamento de
casas decimais truncadas e vírgulas flutuantes utilizando a biblioteca Pandas.
2. **Modelagem de Dados:** Construção de arquitetura robusta em **Star Schema**
(Tabela Fato de transações ligada a Tabelas Dimensão de produtos/tempo).
3. **Cálculo Otimizado (DAX):** Para garantir performance e integridade do caixa, foi
desenvolvida uma medida utilizando a função iteradora `SUMX` combinada com a `RELATED`. O
cálculo passou a operar linha por linha diretamente na tabela Fato, multiplicando a
quantidade vendida pelo preço unitário correto da tabela Dimensão.
* **Entregáveis:** Notebook de tratamento em Python e arquivo do Dashboard (`.pbix`).
---
## Filosofia de Trabalho
Meus projetos seguem três diretrizes básicas:
1. **O painel é do negócio, não do analista:** Priorizo a clareza e o entendimento do
usuário final, adaptando o design para apoiar a tomada de decisão sem distrações
estéticas.
2. **Performance em primeiro lugar:** Evito colunas calculadas pesadas, transferindo o
processamento para etapas de ETL (Python/SQL) ou medidas DAX otimizadas.
3. **Integridade de Dados:** Validação rígida de chaves (IDs) entre Fato e Dimensão para
evitar inconsistências ou registros órfãos.
