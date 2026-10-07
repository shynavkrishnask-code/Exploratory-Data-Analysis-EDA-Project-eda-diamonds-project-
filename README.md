# Exploratory Data Analysis (EDA) Project
**Internship Task 3 - Data Science Domain**

## Objective
Analyze a dataset to uncover patterns and trends — statistical summaries, visualizations, correlation analysis, and key influencing factors — presented in a structured report.

## Dataset
**Diamonds** (53,940 records, seaborn's built-in dataset) — price and physical/quality attributes of diamonds: carat, cut, color, clarity, cut proportions (depth, table), and physical dimensions (x, y, z).

## Key Findings
- **Carat is the dominant driver of price** (correlation ≈ 0.92), far stronger than any quality grade on its own.
- **Price is right-skewed**; a log transform makes it far more symmetric.
- **Raw average price by cut is misleading** — Fair-cut diamonds average a higher price ($4,359) than Ideal-cut diamonds ($3,458), purely because they tend to be larger (a confounding variable), not because lower cut quality is worth more.
- **Clarity's real effect only appears once carat is controlled for** — price-per-carat trends upward with better clarity grades.
- **x, y, z dimensions are highly correlated with carat and each other**, since they describe the same physical size.

## Files
| File | Description |
|---|---|
| `EDA_Diamonds_Project.ipynb` | Full executed notebook — statistical summaries, univariate/bivariate analysis, correlation study, confound investigation |
| `EDA_Diamonds_Report.html` | Static export of the notebook, viewable in any browser |
| `Final_Report_EDA.docx` | Written report |
| `charts/` | All 9 figures used in the analysis and report |

## How to run
```
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook EDA_Diamonds_Project.ipynb
```
The dataset loads directly via `seaborn.load_dataset('diamonds')`, so no manual download is needed.

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn
