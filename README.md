# Online Foods Data Cleaning

End-to-end data cleaning of an online food ordering survey dataset using **Python** and **Pandas**, turning a raw CSV into an analysis-ready file.

| | Rows | Columns |
|---|---|---|
| Raw data | 388 | 13 |
| Cleaned data | 244 | 10 |

## Problem

The raw survey data contained duplicate records (37% of rows), irrelevant columns and fields that were not ready for analysis. Analysing it as-is would give inflated counts and misleading patterns.

## Cleaning steps

1. **Inspect** shape, data types, and missing values
2. **Drop irrelevant columns**: `latitude`, `longitude`, `Pin code`, `Unnamed: 12`
3. **Rename** `Monthly Income` to `Monthly Salary`
4. **Remove 144 duplicate rows**
5. **Validate** that there are no null values
6. **Feature engineering**
   - `Age (Months)` = `Age` x 12
   - `Gender`: Female / Male to `F` / `M`
   - `Family size`: above 3 is `Large`, otherwise `Small`
   - `Output`: Yes / No to `1.0` / `0.0`
7. **Export** to Excel and CSV

## Project structure

```
online-foods-data-cleaning/
├── data/
│   ├── raw/onlinefoods.csv
│   └── cleaned/Cleaned_Data.xlsx
├── notebooks/
│   └── data_cleaning.ipynb
├── clean_data.py
├── requirements.txt
└── README.md
```

## How to run

```bash
git clone https://github.com/<your-username>/online-foods-data-cleaning.git
cd online-foods-data-cleaning
pip install -r requirements.txt
python clean_data.py
```

Cleaned files are written to `data/cleaned/`.

## Tech stack

Python, Pandas, OpenPyXL, Jupyter Notebook

## Possible next steps

- Exploratory analysis of order behaviour by income, occupation and education
- Interactive dashboard in Power BI
- Predictive model for the `Output` column

## Author

**Gowtham G** - [LinkedIn](https://www.linkedin.com/in/gowtham-gnanasekar/) | [GitHub](https://github.com/gowtham-g-2002)
