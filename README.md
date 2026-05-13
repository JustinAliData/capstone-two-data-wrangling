# U.S. Lower 48 Energy Usage — EDA

> End-to-end data wrangling and exploratory analysis of energy consumption across the 48 contiguous U.S. states. Produces a clean, pipeline-ready dataset plus a set of regional consumption findings.

**Stack:** Python · Pandas · NumPy · Matplotlib · Seaborn
**Status:** Completed (foundation for the Texas Electricity Demand forecasting capstone)
**Author:** Justin Ali · [LinkedIn](https://www.linkedin.com/in/justin-ali-data/)

---

## The problem

Energy datasets are notoriously messy: inconsistent state codes, mixed units, gaps, duplicate rows, schemas that change year to year. Before you can do *anything* useful with state-level consumption data — forecasting, peer-state comparison, demand-driver analysis — you need a single clean table you can trust. This project does that wrangling end to end and uses the cleaned data to surface regional consumption patterns.

## The data

Raw U.S. state-level energy consumption data covering the contiguous 48 states. The source records contained the usual real-world headaches: missing values, inconsistent formatting, and duplicate records.

## Approach

1. **Inventory** — Profile the raw data: columns, types, missingness per column, suspected duplicates.
2. **Cleaning** — Standardize state codes, unify units, deduplicate, and impute or drop missing values with a documented rule per case.
3. **Restructuring** — Reshape into a tidy long-format table suitable for grouping by state, region, and year.
4. **EDA** — Per-state and per-region trend lines, summary statistics, and visual comparisons surfacing where consumption is climbing, flat, or declining.
5. **Deliverable** — A clean dataset ready to drop into a downstream forecasting pipeline, plus an EDA notebook for stakeholders.

## Results

A pipeline-ready energy-usage table and a set of regional findings: which census regions are growing fastest in total demand, which states are outliers relative to their region, and where the data quality issues cluster (a helpful map for the next analyst).

## What I would do next

- Layer in weather data: heating- and cooling-degree-days explain most year-over-year residential variance.
- Add sector breakouts (residential, commercial, industrial, transport). Aggregate state totals hide the drivers.
- Use this cleaned dataset as the upstream feed for a state-level demand-forecasting model.

## Repo contents

```
.
├── notebooks/
├── data/
└── README.md
```

## How to run

```bash
git clone https://github.com/JustinAliData/us-energy-usage-eda.git
cd us-energy-usage-eda
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

## Acknowledgments

Built as part of the **Springboard Data Science Career Track**. Companion project to the Texas Electricity Demand Forecasting capstone.
