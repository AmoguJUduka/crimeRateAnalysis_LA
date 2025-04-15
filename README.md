# Los Angeles Crime Data Analytics Platform

## Project Overview
A distributed big data analytics framework for processing, analyzing, and modeling crime data from the Los Angeles Police Department (LAPD). This system employs advanced ETL pipelines, spatial-temporal analysis algorithms, and machine learning models to extract actionable intelligence from multi-terabyte crime datasets spanning over 15 years.

## Technical Architecture

### Data Pipeline
- **Ingestion Layer**: Apache Kafka/NiFi for real-time data acquisition from LAPD APIs
- **Storage Layer**: HDFS/S3 data lake with Parquet format and Delta Lake for ACID transactions
- **Processing**: Spark 3.4+ for distributed batch and stream processing
- **Query Engine**: Presto/Trino for SQL analytics across heterogeneous data sources

### Analysis Components
- **Spatiotemporal Analysis**: GeoPandas + PostGIS integration for complex geospatial queries
- **Time Series Decomposition**: Prophet + statsmodels for seasonal trend detection
- **Anomaly Detection**: Isolation Forest and DBSCAN algorithms for outlier identification
- **Clustering**: K-means and HDBSCAN for crime pattern classification

### Visualization & Insights
- **Interactive Dashboard**: Dash/Plotly backend with React frontend
- **Mapping Service**: Deck.gl for rendering high-performance geospatial visualizations
- **Report Generation**: Automated PDF generation with statistical significance testing

## Performance Metrics
- Processing capability: ~500M crime records/hour
- Model refresh: Daily incremental training
- Query latency: Sub-second for pre-aggregated metrics, <5s for ad-hoc spatial queries

## Development Environment
- Docker-compose for local development
- CI/CD via GitHub Actions
- Unit tests with pytest and integration tests with Great Expectations

## Data Sources
- LAPD Crime Data (2010-Present)
- LA County Census Tracts
- Socioeconomic indicators from American Community Survey
