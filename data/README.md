# Data Directory

## Official Dataset

Bitbrains GWA-T-12 Virtual Machine Workload Traces:

https://atlarge-research.com/gwa-t-12/

The complete `fastStorage` dataset is downloaded automatically by the Google Colab notebook and stored under:

```text
data/raw/bitbrains_faststorage/
```

The full dataset is intentionally excluded from GitHub because it contains 1,250 VM trace files and is large.

## Directory Use

- `raw/bitbrains_faststorage/` — official downloaded trace files
- `processed/` — cleaned and feature-engineered data
- `sample/` — small clearly labelled demonstration samples only
