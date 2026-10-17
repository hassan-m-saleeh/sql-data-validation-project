# SQL Data Validation Project

A reproducible SQLite demo for finding duplicate identifiers, blank fields, and simple format anomalies in synthetic customer data.

## Run
Use SQLite or DB Browser for SQLite and execute `sql/schema_and_sample_data.sql`, then run the queries in `sql/analysis_queries.sql`. If the SQLite CLI is installed:
```bash
sqlite3 data_quality_demo.db < sql/schema_and_sample_data.sql
sqlite3 data_quality_demo.db < sql/analysis_queries.sql
```

## Included checks
Duplicate nonblank IDs, missing emails, missing names/countries, approximate email-format screening, and record counts by country.

## Limitations
Queries identify records for review; they do not establish the correct repair. The email check is a heuristic only.
