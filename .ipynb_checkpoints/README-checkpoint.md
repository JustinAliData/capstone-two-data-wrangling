# Capstone Two: Data Wrangling (U.S. Lower 48 Electricity)

## Project Overview
This project prepares an hourly time-series dataset of electricity demand and net generation by source for the U.S. Lower 48. The goal of this phase is to produce a clean, merged, analysis-ready dataset to support exploratory analysis and demand forecasting in later capstone stages.

## Data
Input CSVs are stored in:
- `data/raw/`

The cleaned, merged output is saved to:
- `data/processed/us_lower48_hourly_clean.csv`

## Notebook
Primary notebook:
- `notebooks/CapstoneTwo_DataWrangling.ipynb`

## Wrangling Summary
- Standardized timestamps to timezone-aware UTC datetimes
- Standardized column naming (`datetime`, `<source>_mw`)
- Filled missing generation values with zero
- Clipped negative solar values to zero
- Merged demand and generation datasets on `datetime`
- Exported final cleaned dataset for downstream modeling

## Next Steps
- Exploratory analysis of demand patterns and generation mix
- Feature engineering (time-based features, lag features)
- Forecasting models for demand prediction
