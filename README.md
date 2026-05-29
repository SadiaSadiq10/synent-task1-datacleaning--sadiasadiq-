# Task 2: Data Visualization — Iris Dataset

## Problem Statement
Numbers in a table tell you very little until you see them. This project uses six visualization techniques to reveal patterns in the classic Iris dataset (150 flowers, 4 features, 3 species).

## Dataset
- **Source:** [Kaggle — Iris Species (UCI)](https://www.kaggle.com/datasets/uciml/iris)
- **File:** `iris.csv` (150 rows × 5 columns: sepal_length, sepal_width, petal_length, petal_width, species)

## Approach
The notebook builds six visualizations, each answering a different question:

| # | Visualization | Question it answers |
|---|---|---|
| 1 | Bar chart | Are the classes balanced? |
| 2 | Histograms | What's the distribution of each feature? |
| 3 | Scatter plots | Do features separate the species? |
| 4 | Box plots | How do features compare across species? |
| 5 | Correlation heatmap | Which features move together? |
| 6 | Pair plot | All feature pairs at a glance |

## Key Insights
1. The dataset is perfectly balanced — 50 samples per species
2. Petal measurements separate species far better than sepal measurements
3. Setosa is easy to distinguish; Versicolor and Virginica overlap on sepals but separate on petals
4. Petal length and petal width are highly correlated (~0.96) — redundant information
5. Sepal width is the weakest discriminator

## Files
- `iris_visualization.ipynb` — main notebook with all visualizations and insights
- `iris.csv` — Iris dataset

## How to Run
1. Clone this repo
2. Install dependencies: `pip install pandas numpy matplotlib seaborn jupyter`
3. Open `iris_visualization.ipynb` in Jupyter and run all cells

## Tools
- Python 3
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook
