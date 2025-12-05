# 🏬 Data Warehouse Supply Chain & Sales Analytics

**Projeto completo de ETL + Modelagem Dimensional + Data Warehouse +
Dashboard BI**

Este projeto implementa uma solução de **Business Intelligence ponta a
ponta**, utilizando dados sintéticos de vendas, produtos, lojas e
estoque.\
O objetivo é demonstrar um fluxo profissional de construção de um **Data
Warehouse Supply Chain & Sales**, incluindo:

-   Processo ETL completo (Bronze → Silver → Gold)
-   Modelagem dimensional (Star Schema)
-   Armazenamento em PostgreSQL (Railway)
-   Criação de métricas logísticas e comerciais
-   Dashboard em Power BI (comercial + supply chain)

------------------------------------------------------------------------

# ⚡ Resumo Técnico

-   **Python**: Pandas, PyArrow, tratamento e limpeza de dados\
-   **ETL**: Pipeline Bronze → Silver → Gold\
-   **Banco de Dados**: PostgreSQL (Railway)\
-   **Modelagem**: Esquema estrela (dimensões + fatos)\
-   **Power BI**: KPIs, DAX, Curva ABC, Ruptura, Giro, Cobertura\
-   **Supply Chain Analytics**: indicadores operacionais completos\
-   **Sales Analytics**: faturamento, categorias, estados, tendências

------------------------------------------------------------------------

# 🎯 Objetivo do Projeto

Criar um Data Warehouse funcional que permita análises estratégicas e
operacionais envolvendo:

### ✔ Área Comercial

-   Faturamento total\
-   Tendência mensal\
-   Top produtos\
-   Desempenho por categoria e estado

### ✔ Área de Supply Chain

-   Giro de estoque\
-   Curva ABC\
-   Ruptura (real ou simulada)\
-   Cobertura de estoque (DOS --- Days of Supply)

Tudo isso integrado ao Power BI, permitindo a tomada de decisão baseada
em dados.

------------------------------------------------------------------------

# 🧱 Arquitetura do Projeto

A solução segue um fluxo organizado em **camadas**, garantindo boa
governança e escalabilidade:

    Arquivos CSV → Bronze
    Bronze → Silver (tratamento com Python)
    Silver → Gold (modelagem dimensional)
    Gold → PostgreSQL (Railway)
    PostgreSQL → Power BI (visualização)

------------------------------------------------------------------------

# ⭐ Modelagem Dimensional (Star Schema)

                    +--------------+
                    |  dim_tempo   |
                    +--------------+
                           |
                           |
    +--------------+   +--------------+   +--------------+
    | dim_produto  |---| fato_vendas |---|  dim_loja     |
    +--------------+   +--------------+   +--------------+
                           |
                           |
                    +--------------+
                    | fato_estoque |
                    +--------------+

------------------------------------------------------------------------

# 🛠️ Processo ETL

### ✔ Bronze → Silver

-   Conversão de tipos\
-   Padronização\
-   Tratamento de nulos\
-   Garantia de integridade\
-   Enriquecimento de dados

### ✔ Silver → Gold

-   Criação das dimensões\
-   Construção das tabelas fato\
-   Cálculo de métricas\
-   Salvamento em Parquet

### ✔ Gold → PostgreSQL

-   Criação das tabelas\
-   Upload via SQLAlchemy\
-   Teste de integridade

------------------------------------------------------------------------

# 📊 Principais Métricas Criadas (DAX & Python)

### Comercial:

-   Faturamento Total\
-   Crescimento Mensal\
-   Crescimento Anual\
-   Ticket Médio

### Supply Chain:

-   Giro de Estoque\
-   Cobertura (Dias)\
-   Ruptura\
-   Classificação ABC

------------------------------------------------------------------------

# 🚀 Como Executar

    git clone https://github.com/USER/dw_supply_chain
    pip install -r requirements.txt
    export POSTGRES_CONN_STRING="sua_string"

Execute:

-   `bronze_to_silver.ipynb`
-   `silver_to_gold.ipynb`
-   `load_to_postgres.ipynb`

Conecte o Power BI ao PostgreSQL.

------------------------------------------------------------------------

# 📌 Licença

MIT License.

------------------------------------------------------------------------

# ✨ Autor

[@joabalm](https://github.com/joabalm)
