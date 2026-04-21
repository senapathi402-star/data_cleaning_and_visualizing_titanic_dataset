# 🚢 Titanic — Data Cleaning & Exploratory Data Analysis

> **Tools Used:** Python | Pandas | NumPy | Matplotlib | Seaborn
> **Dataset:** 891 Passengers | 15 Columns | Seaborn Built-in Dataset

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/senapathi402-star/data_cleaning_titanic/blob/main/Titanic_data_cleaning_And_visualization.ipynb)

---

## 📌 Objective

Perform **data cleaning** and **exploratory data analysis (EDA)** on the Titanic dataset to handle missing values, understand data structure, and extract meaningful insights about passenger survival rates.

---

## 🗃️ Dataset Structure

| Feature | Description |
|---------|-------------|
| `survived` | Survival (0 = No, 1 = Yes) |
| `pclass` | Passenger class (1, 2, 3) |
| `sex` | Gender |
| `age` | Age in years |
| `sibsp` | Siblings/spouses aboard |
| `parch` | Parents/children aboard |
| `fare` | Ticket fare |
| `embarked` | Port of embarkation |
| `deck` | Deck location on ship |
| `embark_town` | Town of embarkation |
| `alive` | Survived (yes/no) |

- **891 rows × 15 columns**

---

## 🧹 Data Cleaning Steps

| Column | Issue | Solution |
|--------|-------|----------|
| `age` | 177 missing values | Filled with gender-wise mean (Female ≈ 28, Male ≈ 31) |
| `embarked` | 2 missing values | Filled with mode (`S`) |
| `embark_town` | 2 missing values | Filled with mode (`Southampton`) |
| `deck` | 688 missing values | Filled with pclass-wise mode |
| `age` | Float dtype | Converted to integer |

> **Note:** 116 duplicate rows were identified but **not removed** — without passenger names, identical rows may represent genuinely different individuals.

---

## 📊 Visualizations Built

| Type | Chart | Insight |
|---|---|---|
| Univariate | Passenger class distribution | Class 3 dominates |
| Univariate | Deck distribution | Deck F most occupied |
| Bivariate | Survival by deck | Decks F & G lowest survival |
| Bivariate | Survival rate by gender | Pie chart — females survived more |
| Bivariate | Fare vs Age | Scatter plot — fare patterns |
| Distribution | Fare box plot | Most fares ₹20–₹50 |
| Distribution | Age box plot | Most passengers aged 25–35 |

---

## 🔍 Key Insights

| Metric | Value |
|--------|-------|
| 👥 Total Passengers | 891 |
| 🥉 Largest Class | Class 3 — 491 passengers (55%) |
| 🚢 Most Occupied Deck | Deck F (after imputation) |
| ♀️ Female Death Rate | 9.09% |
| ♂️ Male Death Rate | 52.53% |
| ♀️ Female Survival Rate | 26.15% |
| ♂️ Male Survival Rate | 12.23% |
| 💰 Typical Fare Range | $20 – $50 |
| 🎂 Typical Age Range | 25 – 35 years |

> **Key Finding:** Female passengers had nearly 3x higher survival rates than males — consistent with the *"women and children first"* policy.

> Decks **F and G** (bottom of ship) had the lowest survival rates.

---

## ✅ Conclusion

The cleaned Titanic dataset reveals clear survival patterns based on gender, passenger class, and deck location. Females had significantly higher survival rates. Duplicate rows were intentionally retained due to absence of passenger names. Outliers in fare and age were preserved for analysis integrity.

---

## 🛠️ Python Libraries Used

- `pandas` — data loading, cleaning, missing value treatment
- `numpy` — numerical operations and dtype conversion
- `matplotlib` — scatter plots, bar charts, box plots
- `seaborn` — count plots, distribution plots, styled visualizations

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `Titanic_data_cleaning_And_visualization.ipynb` | Full Jupyter Notebook |
| `README.md` | Project documentation |

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/senapathi402-star/data_cleaning_titanic.git
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Open the notebook in Jupyter or Google Colab and run all cells

---

## 👤 Author

**Senapathi Krishna Sai**
Data Analyst | SQL | Python | Tableau | Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/senapathi-krishna-sai-a54721388)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/senapathi402-star)
