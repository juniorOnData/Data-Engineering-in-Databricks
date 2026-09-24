# Data Ingestion with Lakeflow Connect

Esta seção reúne estudos e práticas de **Data Ingestion no Databricks**, com foco em **Lakeflow Connect** e nos principais recursos utilizados para ingestão de dados em pipelines modernos.

Os notebooks abordam ingestão incremental com **Auto Loader**, processamento de arquivos com **Structured Streaming**, uso de **Unity Catalog Volumes**, leitura de dados semiestruturados em JSON e transformação com funções como `from_json`, `to_json`, `get_json_object` e `parse_json`.

Também são exploradas as diferenças entre **directory listing** e **managed file events**, além dos conceitos de **managed connectors** e **standard connectors** no Lakeflow Connect.

O objetivo é consolidar o entendimento prático desses recursos por meio de exemplos executados diretamente no Databricks, servindo também como material de revisão para estudos de Data Engineering na plataforma.

## Tecnologias

Databricks, PySpark, Spark SQL, Auto Loader, Structured Streaming, Delta Lake, Unity Catalog e Lakeflow Connect.

## Documentação oficial

https://docs.databricks.com/aws/en/ingestion/lakeflow-connect

https://docs.databricks.com/aws/en/ingestion/cloud-object-storage/auto-loader/
