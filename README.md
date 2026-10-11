# Supermarket Sales - Exploratory Data Analysis

**Devixo Solutions - Data Science Internship | Task 01**

## Project Description
An end-to-end exploratory data analysis (EDA) of supermarket transactions. The project cleans the data, analyses the features, studies correlations, builds 16 visualizations, and turns the findings into 16 business insights and 7 recommendations.

## Dataset Information
- **Name:** Supermarket Sales (Kaggle)
- **Records:** 1,000 transactions, 17 columns
- **Period:** 1 Jan 2019 - 30 Mar 2019 (89 trading days)
- **Branches:** A (Yangon), B (Mandalay), C (Naypyitaw)
- **Columns:** Invoice ID, Branch, City, Customer type, Gender, Product line, Unit price, Quantity, Tax 5%, Total, Date, Time, Payment, cogs, gross margin percentage, gross income, Rating
- **File:** `data/supermarket_sales.csv`
- **Source:** Kaggle "Supermarket sales" dataset (copy used here: https://raw.githubusercontent.com/selva86/datasets/master/supermarket_sales.csv)

## Technologies Used
Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy (statistical tests), Jupyter Notebook

## Analysis Performed
1. Data import and understanding (shape, types, statistics)
2. Data cleaning (missing values, duplicates, types, inconsistent values, formula checks)
3. Feature analysis (min / max / mean / median, categories, IQR outliers)
4. Correlation analysis and heatmap
5. 16 visualizations (histogram, bar, count, pie, scatter, line, box, violin, heatmap, pair plot, distribution, area)
6. 16 business insights, checked with significance tests (ANOVA, Mann-Whitney, chi-square)
7. 7 business recommendations

## Key Findings
- Total revenue is about $322,967. Branch C leads (34.2%), but differences between branches are small and not statistically significant.
- Basket value (`Total`) depends on quantity (r = 0.71) and unit price (r = 0.63), and those two are unrelated to each other.
- Customer rating is not related to any measured variable (|r| < 0.04).
- 19:00 is the peak hour and Saturday the best day; Monday is the weakest.
- Members do not spend more than normal customers (p = 0.59).
- `gross income` equals the tax column and the gross margin is a constant, so true profitability cannot be analysed from this dataset.
- Category differences by gender and by branch look large but were **not** statistically significant (p of about 0.32 and 0.33), so they are treated as ideas to test.

## Business Recommendations (summary)
1. Redesign the membership programme with spend-based tiers.
2. Align staffing and promotions with the hourly and weekday curve.
3. Pilot a Health and beauty improvement (Branch B's approach in Branch A).
4. Test a Home and lifestyle layout change in Branch C.
5. Use bundles / multi-buy offers to raise items per basket.
6. Investigate Branch B satisfaction with a short feedback survey.
7. Record real product cost so profit can be analysed.

## Repository Structure
```
.
├── EDA_Supermarket_Sales.ipynb     # full analysis notebook (with outputs)
├── data/supermarket_sales.csv      # dataset
├── graphs/                         # all 16 saved graph images
├── screenshots/                    # code and output screenshots
├── report/EDA_Report.pdf           # final PDF report
├── requirements.txt
└── README.md
```

## How to Run
1. Clone the repository:
   ```
   git clone <your-repository-link>
   cd <repository-folder>
   ```
2. Install the requirements:
   ```
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```
   jupyter notebook EDA_Supermarket_Sales.ipynb
   ```
4. Choose **Kernel > Restart & Run All**. The graphs are saved to the `graphs/` folder automatically.

**Google Colab:** upload the notebook and the `data/` folder, then run all cells.
