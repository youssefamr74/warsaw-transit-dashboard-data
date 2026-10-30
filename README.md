# Warsaw Transit Pulse: dashboard data

Aggregated data published nightly by the
[warsaw-transit-pipeline](https://github.com/youssefamr74/warsaw-transit-pipeline) project,
read by its public dashboard. This repo is overwritten on every export.

| File | One row = |
|---|---|
| `line_hourly.parquet` | one line, one hour: speed sums and weather |
| `speed_grid.parquet` | one map square (~275 m), line, day and time window: speed sums |
| `collection_hourly.parquet` | one hour of data collection |
| `dq_results.parquet` | one data quality check run (last 7 days) |
| `manifest.json` | export time, date range and row counts |

Speeds are stored as sums (`total_distance_m`, `total_seconds`), so any filter or roll-up
is computed correctly as total distance / total time.

**Sources:** Źródłem pochodzenia danych jest Miasto Stołeczne Warszawa (dane.um.warszawa.pl).
Weather data by Open-Meteo.com (CC BY 4.0).
