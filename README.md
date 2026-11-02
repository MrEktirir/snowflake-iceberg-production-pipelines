# Snowflake Iceberg Production Pipelines

### End-to-End Data Engineering | AWS Glue, Apache Iceberg, Snowflake & Streamlit

An end-to-end lakehouse implementation demonstrating how to ingest event data into Apache Iceberg, expose externally managed tables through Snowflake Catalog-Linked Databases, transform data using Dynamic Iceberg Tables, and visualize analytics with Streamlit in Snowflake.

Built using the official [Snowflake Labs Lakehouse Production Pipelines](https://github.com/Snowflake-Labs/sfguide-lakehouse-iceberg-production-pipelines) project, with hands-on implementation, troubleshooting, and validation.

## Architecture

```mermaid
flowchart TD
    A["Python Event Generator"] --> B["AWS Glue + Apache Iceberg"]
    B --> C["Amazon S3 - Bronze"]
    D["AWS Lake Formation"] --> E["Snowflake Catalog Integration"]
    B --> E
    E --> F["Catalog-Linked Database"]
    F --> G["Snowflake Dynamic Iceberg Tables"]
    G --> H["Amazon S3 - Silver"]
    G --> I["Streamlit in Snowflake Dashboard"]
