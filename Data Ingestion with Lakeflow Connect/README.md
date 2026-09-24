## Data Ingestion with Lakeflow Connect

Nesta etapa dos estudos, o foco principal é **Data Ingestion with Lakeflow Connect**, incluindo conceitos e práticas relacionados a:

* Lakeflow Connect;
* Auto Loader;
* ingestão incremental de arquivos;
* Structured Streaming;
* Unity Catalog Volumes;
* dados semiestruturados e JSON;
* `from_json`, `to_json`, `get_json_object` e `parse_json`;
* diferença entre acesso a JSON com `:` e acesso a campos de `STRUCT` com `.`;
* directory listing;
* file notifications e managed file events;
* managed connectors e standard connectors;
* pipelines de ingestão no Databricks;
* arquitetura Bronze e Silver.

## Objetivo

O objetivo deste repositório é reunir notebooks, exemplos de código e pequenos laboratórios práticos para consolidar os conceitos de Engenharia de Dados utilizando Databricks.

Os exercícios utilizam principalmente **PySpark, Spark SQL, Auto Loader, Delta Lake, Unity Catalog e Lakeflow**.

## Estrutura do repositório

Exemplo de organização:

```text
data-engineering-databricks/
│
├── notebooks/
│   └── data-ingestion-lakeflow-connect.ipynb
│
├── datasets/
│
├── exercises/
│
└── README.md
```

A estrutura poderá evoluir conforme novos tópicos e laboratórios forem adicionados.

## Principais tópicos praticados

### Dados semiestruturados

Prática de leitura e transformação de JSON utilizando recursos como:

```sql
coluna:campo
```

```sql
struct_col.campo
```

```sql
from_json(...)
```

```sql
to_json(...)
```

```sql
get_json_object(...)
```

```sql
parse_json(...)
```

### Auto Loader

Uso do Auto Loader para ingestão incremental de arquivos:

```python
spark.readStream \
    .format("cloudFiles") \
    .option("cloudFiles.format", "json") \
    .load(source)
```

Também são explorados conceitos como:

* `schemaLocation`;
* checkpoints;
* detecção de novos arquivos;
* directory listing;
* managed file events.

### Lakeflow Connect

Estudo das diferentes formas de conectar fontes de dados ao Databricks, incluindo:

* managed connectors;
* standard connectors;
* fontes de arquivos;
* bancos de dados;
* aplicações SaaS;
* ingestão incremental.

## Tecnologias

* Databricks
* Apache Spark
* PySpark
* Spark SQL
* Delta Lake
* Unity Catalog
* Auto Loader
* Structured Streaming
* Lakeflow Connect
* Lakeflow Declarative Pipelines

## Documentação oficial

A principal referência utilizada nos estudos é a documentação oficial do Databricks:

https://docs.databricks.com/

Documentação do Lakeflow Connect:

https://docs.databricks.com/aws/en/ingestion/lakeflow-connect

Documentação do Auto Loader:

https://docs.databricks.com/aws/en/ingestion/cloud-object-storage/auto-loader/

## Sobre o repositório

Este é um repositório de estudo e prática. Os notebooks podem sofrer alterações conforme novos conceitos forem estudados e os laboratórios forem aprimorados.
