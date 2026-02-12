# Forem ETL

Small data-ingestion utility that pulls the latest DEV Community articles via the public REST API and stores them locally for downstream processing.

## Quick Start

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python src/fetch_articles.py
```

Results land under `data/raw/<YYYY-MM-DD>/` with a `latest_timestamp.json` file keeping track of the most recent article fetched so incremental runs only pull fresh content.
