# HealthStats
Practical data sources + “fetch” tooling you can build around (all have programmatic access):

WHO Global Health Observatory (GHO) OData API (global health indicators)

World Bank Indicators API (health + demographics + economics; long time series)

Government open-data portals via Socrata SODA (many public health + social datasets; e.g., Data.CDC.gov)

Eurostat REST APIs (EU stats; multiple endpoints including STATISTICS/SDMX)

OECD SDMX-based API (cross-country indicators)

Our World in Data (curated datasets; also a DuckDB-backed “data-api” project you can mirror/learn from)

IHME/GHDx “IHME API” page (access patterns for IHME-hosted downloads; many datasets distributed as files/tools rather than a single simple indicator API)

Developer libraries/apps that make “fetch + normalize + serve dashboards” straightforward:

Python: httpx/requests (API calls), pandas or polars (tables), pyarrow (columnar IO), duckdb (local analytics cache), pydantic (schemas), tenacity (retries), sqlalchemy (DB), sodapy (Socrata clients), plus source-specific clients like wbdata (World Bank)

R: packages for WHO GHO access (e.g., GHO OData wrappers)

Dashboards: Streamlit/Dash (Python apps), Grafana (time-series panels), Apache Superset/Metabase (BI over SQL/DuckDB/Postgres).

Pipelines: Prefect/Dagster/Airflow to schedule refresh + caching.