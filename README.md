# Performance Comercial e Rentabilidade no Varejo: Do Entendimento dos Dados à Análise Exploratória

**Artigo completo:**
[![Medium](https://img.shields.io/badge/Artigo%20completo-Medium-black?logo=medium)](https://medium.com/@luizamarchenib/performance-comercial-e-rentabilidade-no-varejo-do-entendimento-dos-dados-%C3%A0-an%C3%A1lise-explorat%C3%B3ria-34f097d1632e?postPublishedType=repub)

**SQL — Mapeamento e Tratamento dos Dados:**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qap_76RqmwwjBKzxEw3-zRcovI0KDJlx?usp=sharing)

**Python — Análise Exploratória (EDA):**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HA91Evskn_pTTIWq4J0F1mhqa9dmVjT?usp=sharing)

## Contexto

Uma empresa global de varejo solicitou uma análise de dados históricos de pedidos, vendas, produtos e entregas para compreender sua performance comercial e rentabilidade, identificando oportunidades de melhoria e possíveis pontos de atenção.

Os dados estão armazenados em um banco PostgreSQL e são organizados em quatro tabelas relacionais: `market_fact`, `orders_dim`, `prod_dim` e `shipping_dim`.

A primeira etapa do projeto foi dedicada ao **mapeamento, profiling, avaliação da qualidade e preparação dos dados**, antes da análise de performance.

## Objetivo

Compreender a performance comercial e de rentabilidade da empresa e identificar quais produtos, categorias e modalidades de envio apresentam os melhores e piores resultados.

A análise busca responder:

> **Como estão as vendas e a rentabilidade da empresa e quais produtos, categorias e modalidades de envio apresentam os melhores e piores resultados?**

## Análise

O projeto foi estruturado em duas partes complementares. Esta primeira etapa concentrou-se no entendimento e preparação dos dados.

Foram realizadas:

* Mapeamento das tabelas, colunas, chaves e relacionamentos;
* Data profiling e análise da qualidade dos dados;
* Validação da granularidade da tabela fato;
* Identificação e tratamento de outliers;
* Análise univariada e bivariada;
* Análise da variabilidade entre grupos por meio do **coeficiente de determinação**;
* Definição das principais KPIs de vendas e rentabilidade;
* Preparação das bases para análises posteriores no Power BI e Python.

Entre as principais métricas analisadas estão **venda líquida, lucro, margem de lucro, custo de frete sobre vendas e custo implícito sobre vendas**.

## Tecnologias

* PostgreSQL 15.17
* SQL
* Python
* Pandas
* NumPy
* Matplotlib
* Google Colab
* Power BI
* GitHub

## Estrutura do projeto

```text
analise_performance_varejista/
│
├── EDA_Python.ipynb                  # Análise exploratória em Python
├── base_python.csv                   # Base utilizada na análise em Python
├── market_fact_BI.csv               # Base tratada para o Power BI
├── market_fact_Base_Bruta.csv       # Base bruta da tabela market_fact
├── orders_dim_BI.csv                # Base tratada para o Power BI
├── orders_dim_Base_Bruta.csv        # Base bruta da tabela orders_dim
├── prod_dim_BI.csv                  # Base tratada para o Power BI
├── prod_dim_Base_Bruta.csv          # Base bruta da tabela prod_dim
├── shipping_dim_BI.csv              # Base tratada para o Power BI
├── shipping_dim_Base_Bruta.csv      # Base bruta da tabela shipping_dim
```

## Como reproduzir a análise

### Python — Análise Exploratória

A maneira mais simples é acessar o notebook diretamente no Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HA91Evskn_pTTIWq4J0F1mhqa9dmVjT?usp=sharing)

O notebook contém a análise exploratória realizada em Python e utiliza a base disponibilizada no repositório.

### SQL — Mapeamento e Tratamento dos Dados

O código SQL pode ser acessado diretamente no Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qap_76RqmwwjBKzxEw3-zRcovI0KDJlx?usp=sharing)

Para reproduzir a análise, é necessário utilizar um ambiente **PostgreSQL** e executar o código do notebook sobre as **bases brutas disponibilizadas no repositório** (`market_fact_Base_Bruta.csv`, `orders_dim_Base_Bruta.csv`, `prod_dim_Base_Bruta.csv` e `shipping_dim_Base_Bruta.csv`).

O notebook contém os comandos SQL utilizados para o **mapeamento, profiling, validação, tratamento dos dados e preparação das bases**.

## Artigo completo

A descrição detalhada da metodologia, dos resultados e das conclusões está disponível no Medium:

[Performance Comercial e Rentabilidade no Varejo: Do Entendimento dos Dados à Análise Exploratória](https://medium.com/@luizamarchenib/performance-comercial-e-rentabilidade-no-varejo-do-entendimento-dos-dados-%C3%A0-an%C3%A1lise-explorat%C3%B3ria-34f097d1632e?postPublishedType=repub)
