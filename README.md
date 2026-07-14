# AI-Driven Predictive Resource Optimization for On-Premises Virtualized Enterprise Data Centers

This repository supports the **QM640 Data Analytics Capstone synopsis**:

> **AI-Driven Predictive Resource Optimization for On-Premises Virtualized Enterprise Data Centers Using Machine Learning**

The study investigates whether machine-learning and time-series forecasting models can predict short-term CPU and memory utilization, identify likely infrastructure bottlenecks earlier than static threshold monitoring, and support proactive resource-allocation decisions in enterprise-oriented on-premises virtualized data centers.

## Synopsis-Stage Status

This repository is prepared for the synopsis stage. A fully trained production model is not required at this stage. The repository demonstrates that:

- the public dataset has been identified;
- the project structure has been created;
- the Google Colab workflow is reproducible;
- dataset validation and exploratory-analysis steps are documented;
- figures and reports can be generated from the notebook;
- the full implementation plan is clearly defined.

## Primary Notebook

Open the following notebook in Google Colab:

```text
notebooks/01_Capstone_Project_Workflow.ipynb
```

The notebook performs the following tasks:

1. Mounts Google Drive for persistent storage.
2. Creates the project workspace.
3. Downloads the official Bitbrains GWA-T-12 `fastStorage` dataset.
4. Extracts and validates 1,250 VM trace files.
5. Loads and checks the dataset schema.
6. Produces the required dataset evidence:
   - `df.head()`
   - `df.shape`
   - `df.info()`
   - `df.describe()`
   - missing-values summary
7. Generates CPU, memory, time-series, and correlation visualizations.
8. Saves figures and dataset summaries for the synopsis.

## Dataset

The project uses the public **Bitbrains GWA-T-12 Virtual Machine Workload Traces**.

Official source:

https://atlarge-research.com/gwa-t-12/

The primary analysis uses the `fastStorage` trace, which contains anonymized, timestamped telemetry for 1,250 virtual machines.

### Data Availability

The complete dataset is not stored in GitHub because of its size. The notebook downloads the official dataset directly from the provider and stores it in Google Drive.

The expected local layout is:

```text
data/raw/bitbrains_faststorage/
```

A small schema sample may be kept under `data/sample/` for demonstration purposes. It must be clearly labelled and must not be represented as original Bitbrains data.

## Research Questions

1. How accurately can machine-learning-based time-series forecasting models predict CPU and memory utilization over 5-minute, 15-minute, and 30-minute horizons?
2. Which infrastructure metrics most significantly influence forecast accuracy?
3. Can predictive analytics identify bottlenecks earlier than traditional threshold-based monitoring?
4. Does predictive optimization improve resource-allocation efficiency?
5. What measurable utilization, estimated cost, and ROI improvements can be achieved?

## Planned Models

- Persistence baseline
- Regularized linear regression
- ARIMA
- Random forest
- XGBoost
- Long short-term memory network

## Planned Evaluation Metrics

- Mean Absolute Error
- Root Mean Squared Error
- Mean Absolute Percentage Error
- Coefficient of Determination
- Precision, recall, and F1 score
- Warning lead time
- Over-provisioning and under-provisioning ratios
- Return on investment and payback period

## Repository Structure

```text
AI-Predictive-Resource-Optimization/
├── notebooks/
│   └── 01_Capstone_Project_Workflow.ipynb
├── data/
│   ├── raw/
│   │   └── bitbrains_faststorage/
│   ├── processed/
│   ├── sample/
│   └── README.md
├── images/
├── reports/
├── docs/
│   ├── DATA_DICTIONARY.md
│   ├── REPRODUCIBILITY.md
│   └── SYNOPSIS_CHECKLIST.md
├── src/
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## How to Reproduce

1. Open the notebook in Google Colab.
2. Run the notebook from the first cell to the last cell.
3. Approve Google Drive access when prompted.
4. Confirm that the official dataset downloads successfully.
5. Review the generated outputs and figures.
6. Save the notebook back to GitHub after execution.

## Author

**Yashwanth Sairam Dudi**  
QM640: Data Analytics Capstone  
Walsh College

## License

The original code in this repository is released under the MIT License. The Bitbrains dataset remains subject to the terms and acknowledgments of its original provider and is not redistributed through this repository.
