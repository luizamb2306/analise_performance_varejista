# Performance Comercial e Rentabilidade no Varejo: Da Exploração dos Dados à Geração de Insights

**Artigo parte 1:**
[![Medium](https://img.shields.io/badge/Artigo%20completo-Medium-black?logo=medium)](https://medium.com/@luizamarchenib/performance-comercial-e-rentabilidade-no-varejo-do-entendimento-dos-dados-%C3%A0-an%C3%A1lise-explorat%C3%B3ria-34f097d1632e?postPublishedType=repub)

**Artigo parte 2:**
[![Medium](https://img.shields.io/badge/Artigo%20completo-Medium-black?logo=medium)](https://medium.com/@luizamarchenib/performance-comercial-e-rentabilidade-no-varejo-an%C3%A1lise-de-performance-e-insights-266a1ed1cb02)

**SQL — Mapeamento e Tratamento dos Dados:**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qap_76RqmwwjBKzxEw3-zRcovI0KDJlx?usp=sharing)

**Python — Análise Exploratória (EDA):**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HA91Evskn_pTTIWq4J0F1mhqa9dmVjT?usp=sharing)

---

## Contexto

Uma empresa global de varejo solicitou uma análise de dados históricos de pedidos, vendas, produtos e entregas para compreender sua **performance comercial e rentabilidade**, identificando oportunidades de melhoria e possíveis pontos de atenção.

Os dados estão armazenados em um banco PostgreSQL e são organizados em quatro tabelas relacionais:

* `market_fact`
* `orders_dim`
* `prod_dim`
* `shipping_dim`

O projeto foi desenvolvido de forma estruturada, seguindo uma abordagem de análise de dados baseada nas etapas de **entendimento, preparação, exploração e análise dos dados**, utilizando SQL, Python e Power BI.

---

## Objetivo

A análise busca responder:

> **Como estão as vendas e a rentabilidade da empresa e quais produtos, categorias, períodos e modalidades de envio apresentam os melhores e piores resultados?**

Além da visão consolidada da empresa, o projeto busca identificar **diferenças relevantes de performance entre segmentos e combinações de dimensões**, transformando os resultados em oportunidades e pontos de atenção para o negócio.

---

# Estrutura do projeto

O projeto foi dividido em **duas etapas complementares**.

### Parte 1 — Entendimento, preparação e análise exploratória dos dados

Foco na compreensão da estrutura dos dados, qualidade, tratamento e exploração estatística.

### Parte 2 — Análise de performance comercial e rentabilidade

Foco na avaliação dos resultados de negócio, identificação dos melhores e piores desempenhos e geração de insights para tomada de decisão.

---

# Parte 1 — Entendimento e Exploração dos Dados

A primeira etapa foi dedicada ao **mapeamento, profiling, avaliação da qualidade e preparação dos dados**, antes da análise de performance.

Foram realizadas:

* Mapeamento das tabelas, colunas, chaves e relacionamentos;
* Validação da estrutura e granularidade da tabela fato;
* Data profiling e análise da qualidade dos dados;
* Identificação de valores ausentes e inconsistências;
* Análise da distribuição das variáveis;
* Identificação e tratamento de outliers;
* Análise univariada e bivariada;
* Avaliação da variabilidade entre grupos por meio do **coeficiente de determinação (R²)**;
* Definição das principais KPIs de vendas e rentabilidade;
* Preparação das bases para as análises posteriores.

### Tecnologias utilizadas

* PostgreSQL
* SQL
* Python
* Pandas
* NumPy
* Matplotlib
* Google Colab

---

# Parte 2 — Análise de Performance Comercial e Rentabilidade

Com os dados tratados e as principais características da base compreendidas, a segunda etapa concentrou-se na **análise da performance comercial e rentabilidade**.

O objetivo foi transformar os dados explorados na primeira etapa em uma visão analítica capaz de apoiar decisões de negócio.

---

## Análise agregada

Inicialmente, foi construída uma visão consolidada da performance da empresa, permitindo avaliar:

* Volume total de vendas;
* Lucro gerado;
* Margem de lucro;
* Evolução dos indicadores ao longo do tempo;
* Variação da performance entre períodos;
* Relação entre crescimento de vendas e rentabilidade.

---

## Classificação de desempenho

Para identificar os melhores e piores desempenhos de forma mais consistente, foram utilizados critérios de **performance relativa entre os grupos analisados**.

A classificação considera principalmente:

* Volume de vendas;
* Margem de lucro;
* Rentabilidade;
* Posição relativa dentro da distribuição;
* Combinação entre volume e margem.

A utilização de medidas de posição, como **mediana e percentis**, permite evitar que a classificação dependa apenas de valores extremos.

---

## Dashboard

Os resultados da segunda etapa foram consolidados em um **dashboard interativo no Power BI**, permitindo explorar a performance por diferentes dimensões.

---

# Tecnologias

* **Power BI**
* **DAX**
* **GitHub**

---

# Estrutura do projeto

```text
analise_performance_varejista/
│
├── EDA_Python.ipynb                  # Análise exploratória em Python
├── Performance.pbix                  # Dashboard de performance no Power BI
├── README.md
│
├── SQL_Mapeamento_e_Tratamento...    # Mapeamento e tratamento dos dados
│
├── base_python.csv                   # Base utilizada na análise em Python
│
├── market_fact_BI.csv                # Base tratada para o Power BI
├── market_fact_Base_Bruta.csv        # Base bruta da tabela market_fact
│
├── orders_dim_BI.csv                 # Base tratada para o Power BI
├── orders_dim_Base_Bruta.csv         # Base bruta da tabela orders_dim
│
├── prod_dim_BI.csv                   # Base tratada para o Power BI
├── prod_dim_Base_Bruta.csv           # Base bruta da tabela prod_dim
│
├── shipping_dim_BI.csv               # Base tratada para o Power BI
└── shipping_dim_Base_Bruta.csv       # Base bruta da tabela shipping_dim
```

---

# Como reproduzir a análise

## SQL — Mapeamento e Tratamento dos Dados

O código SQL pode ser acessado diretamente no Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qap_76RqmwwjBKzxEw3-zRcovI0KDJlx?usp=sharing)

Para reproduzir essa etapa, é necessário utilizar um ambiente **PostgreSQL** e executar o código do notebook sobre as **bases brutas disponibilizadas no repositório**:

* `market_fact_Base_Bruta.csv`
* `orders_dim_Base_Bruta.csv`
* `prod_dim_Base_Bruta.csv`
* `shipping_dim_Base_Bruta.csv`
---

## Python — Análise Exploratória

A análise exploratória pode ser reproduzida diretamente no Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HA91Evskn_pTTIWq4J0F1mhqa9dmVjT?usp=sharing)

O notebook utiliza a base preparada na etapa de tratamento e realiza as análises estatísticas e exploratórias em Python.

---

## Power BI — Análise de Performance

A etapa de análise de performance foi desenvolvida no **Power BI**, utilizando as bases tratadas e as métricas definidas ao longo das etapas anteriores.

As métricas e análises foram estruturadas em **DAX**, permitindo análises agregadas, comparações temporais e avaliação relativa dos desempenhos.
entendimento-dos-dados-%C3%A0-an%C3%A1lise-explorat%C3%B3ria-34f097d1632e?postPublishedType=repub)
