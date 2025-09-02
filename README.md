# Happiness-Index

## Structure
````
happiness-index-eda/
│── data/
│   └── world-happiness-report-2021.csv   # dataset (from Kaggle)
│── notebooks/
│   └── Happiness_Index.ipynb             # original notebook
````

---

## requirements

numpy
pandas
matplotlib
seaborn

---

## Project Structure
```

happiness-index-eda/
│── data/                 # Dataset (download and place here)
│── notebooks/            # Jupyter/Colab notebook with full analysis
````

---

## Dataset Description
The dataset provides scores and rankings of happiness based on survey responses and socioeconomic indicators.

| Feature         | Description |
|-----------------|-------------|
| Country         | Country name |
| Region          | Geographical region |
| Happiness       | Happiness (Ladder) score |
| GDP             | Logged GDP per capita |
| Social support  | Perceived social support |
| Life_Expectancy | Healthy life expectancy |
| Freedom         | Freedom to make life choices |
| Generosity      | Generosity level |
| Corruption      | Perceptions of corruption |

---

## EDA Workflow

1. **Data Cleaning**
   - Removed unnecessary columns (e.g., Dystopia scores, whiskers, residuals)
   - Renamed columns for clarity (`Country`, `Region`, `GDP`, `Happiness`, etc.)
   - Checked and removed duplicates
   - Verified no missing data

2. **Univariate Analysis**
   - Histograms and boxplots for `Happiness`, `GDP`, `Life_Expectancy`, etc.
   - Detected skewness and outliers

3. **Outlier Handling**
   - Used **IQR method** to remove extreme values in `Happiness`, `Social support`, `Corruption`, and `Generosity`

4. **Categorical Analysis**
   - Frequency distribution of `Region`
   - Average happiness by region

5. **Correlation & Bivariate Analysis**
   - Correlation heatmap of features
   - Regression plots (`GDP vs Happiness`, `Life_Expectancy vs Happiness`)
   - Pairplots for main factors

6. **Regional & Country-Level Analysis**
   - Average scores per region
   - Top & bottom 10 countries by each factor
   - Scatterplots grouped by `Region`

---

## Key Insights

- **Top Factors Influencing Happiness:**
  - Strongest positive correlation with **GDP**, **Social support**, and **Life Expectancy**
  - **Freedom** contributes positively but slightly less
  - **Generosity** and **Corruption** show weaker, more variable relationships (cultural/perceptual influences)

- **Regional Trends:**
  - **Western Europe & North America/ANZ** have the highest scores across Happiness, GDP, and Freedom
  - **Sub-Saharan Africa & South Asia** consistently show the lowest scores

- **Country Highlights:**
  - **Finland, Denmark, Switzerland** are among the happiest countries
  - Countries with weaker economies and lower life expectancy rank lower

---

## Conclusion

The analysis clearly shows that **economic prosperity, strong social networks, and health** are the key drivers of happiness worldwide.
While ethical/cultural factors like generosity and corruption also play a role, their influence is less direct and varies significantly by region.

---

تحب أجهزلك كمان نسخة مختصرة من الكود كـ `src/eda.py` بحيث يكون reusable (functions لتنضيف الداتا، plotting) ولا تخليها Notebook فقط؟
```
