# 📊 Dashboard de Vendas — Power BI

Projeto final do curso [SQL para Análise de Dados](https://www.udemy.com/course/sql-para-analise-de-dados/) (Udemy). O objetivo original do curso era construir o dashboard no Excel; optei por refazer a solução completa no **Power BI**, desde a modelagem dos dados até a construção visual.

![Preview do dashboard](./screenshot/dashboard-vendas.jpg)

🔗 O arquivo `.pbix` está disponível neste repositório — abra no Power BI Desktop (gratuito) para explorar o dashboard.

> **Nota:** os gráficos não possuem correlação entre si (cross-filtering), pois cada um foi construído a partir de queries SQL independentes, que já retornavam os dados agregados prontos para cada visual — seguindo a estrutura proposta no curso.

## Objetivo do projeto

Acompanhar a evolução de vendas ao longo do tempo, identificar os produtos/vendedores/regiões com melhor desempenho e apoiar decisões comerciais.

## Fonte dos dados

Verificar a relação entre a data, receitas e os leads, além de verifiar os estados que mais vende e os top 5 de marcas que vendem, lojas também, e as visitas pelos dias da semana

## O que foi feito

1. **Extração e tratamento dos dados via SQL**
   As queries utilizadas para extrair e tratar os dados estão em [`/sql/queries.sql`](./sql/queries.sql).

2. **Modelagem no Power BI**
   Diferente de um modelo relacional tradicional, os dados foram preparados previamente via queries SQL individuais, cada uma já retornando o resultado agregado necessário para um gráfico específico (ex: cruzamento do ano com a receita, os leads, qual estado que vende mais, além dos Top 5 marcas vendidas no mês, as lojas e visitas nos dias das semana). Os resultados dessas queries foram exportados para uma planilha Excel, com uma aba/tabela por consulta, e importados diretamente no Power BI.
   Como cada tabela já representa uma visão consolidada e independente, não há relacionamentos entre elas dentro do modelo — cada uma alimenta seu respectivo visual de forma isolada. Essa abordagem concentra o tratamento e a agregação dos dados na camada SQL, deixando o Power BI responsável apenas pela visualização.


3. **Construção dos visuais**
   Foi feito um dashboard baseado com gráfico de gênero, status profissional, faixa etária, faixa salarial, classicação dos veículos, idade do veículo e modelos mais visitados.

## Principais insights

- Insight 1 — Começo de 2021 e final de 2020 foram aonde teve o pico de ticket médio porem a reiceta maior foi so no começo do 
               segundo   semestre de 2021.
- Insight 2 — O estado de São Paulo foi o que mais teve venda.
- Insight 3 — Houve um aumento mensal gradativo de leads e conversão.
- Insight 4 — A Fiat é a marca mais vendida no mês.
- Insight 5 — E o dia com mais visita no site é segunda e a menor domingo.

## Diferencial em relação ao projeto original do curso

O curso ensinava a montagem da análise em Excel. Refiz o projeto do zero em Power BI, com modelagem relacional, medidas DAX e recursos de interatividade não presentes na versão original.

## Estrutura da pasta

```
dashboard-vendas/
├── README.md
├── analise-leads.pbix
├── /sql
│   └── queries.sql
└── /screenshots
    ├── perfil-leads.jpg
```

## Tecnologias

- SQL
- Power BI 
