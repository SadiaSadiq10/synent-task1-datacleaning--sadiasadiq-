# Task 1: Data Cleaning & Preprocessing — Titanic Dataset

## Problem Statement
Real-world datasets are rarely clean. The raw Titanic dataset contains missing values, mixed data types, and column names that aren't analysis-friendly. This project cleans and preprocesses the dataset so it's ready for downstream EDA and modeling.

## Dataset
- **Source:** [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **File used:** `train.csv` (891 rows × 12 columns)

## Approach
1. **Inspect** the raw data — shape, dtypes, missing values, duplicates
2. **Handle missing values**:
   - `Age` (177 missing) → impute with **median** (robust to outliers)
   - `Embarked` (2 missing) → impute with **mode**
   - `Cabin` (687 missing, ~77%) → extract first letter as new `Deck` column, then drop original
3. **Remove duplicates** — none found, but check is run defensively
4. **Convert data types** — categorical columns to `category`, `Age` to `int`
5. **Rename columns** — convert to clear `snake_case`
6. **Save** cleaned dataset as `titanic_cleaned.csv`

## Results
| | Before | After |
|---|---|---|
| Rows | 891 | 891 |
| Columns | 12 | 12 (Cabin replaced with Deck) |
| Missing values | 866 | 0 |
| Duplicates | 0 | 0 |

## Files
- `titanic_data_cleaning.ipynb` — main notebook with all cleaning steps
- `train.csv` — raw Titanic dataset
- `titanic_cleaned.csv` — output cleaned dataset

## How to Run
1. Clone this repo
2. Install dependencies: `pip install pandas numpy jupyter`
3. Open `titanic_data_cleaning.ipynb` in Jupyter and run all cells

## Tools
- Python 3
- pandas, numpy
- Jupyter Notebook
