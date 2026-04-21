# 🚢 Titanic Data Cleaning and Visualization

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/senapathi402-star/data_cleaning_and_visualizing_titanic_dataset/blob/main/Titanic_data_cleaning_And_visualization.ipynb)

## 📌 Project Overview

This project performs **data cleaning** and **exploratory data analysis (EDA)** on the Titanic dataset using Python. The goal is to handle missing values, understand the data structure, and extract meaningful visual insights about the passengers and survival rates.

---

## 🗂️ Dataset

- **Source:** Seaborn built-in Titanic dataset
- **Size:** 891 rows × 15 columns
- **Features:** `survived`, `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `class`, `who`, `adult_male`, `deck`, `embark_town`, `alive`, `alone`

---

## 🧹 Data Cleaning Steps

| Column | Issue | Solution |
|--------|-------|----------|
| `age` | 177 missing values | Filled with gender-wise mean (Female ≈ 28, Male ≈ 31) |
| `embarked` | 2 missing values | Filled with mode (`S`) |
| `embark_town` | 2 missing values | Filled with mode (`Southampton`) |
| `deck` | 688 missing values | Filled with pclass-wise mode |
| `age` | Float dtype | Converted to integer |

> **Note:** 116 duplicate rows were identified but **not removed**, as without passenger names, identical rows may represent genuinely different individuals.

---

## 📊 Visualizations

### Univariate Analysis
- Passenger class distribution (bar chart)
- Deck distribution (count plot)

### Bivariate Analysis
- Survival count by deck (grouped bar chart)
- Survival rate by gender (pie chart)
- Fare vs. Age (scatter plot)
- Fare distribution (box plot)
- Age distribution (box plot)

---

## 🔍 Key Insights

- **Class 3** had the highest number of passengers (491 out of 891)
- **Deck F** was the most occupied deck after imputation
- Decks **F and G** had the lowest survival rates — likely because they are located at the bottom of the ship
- **52.53%** of males died; only **9.09%** of females died
- **26.15%** of females survived vs. **12.23%** of males — consistent with the *"women and children first"* policy
- Most ticket fares ranged between **$20–$50**
- Majority of passengers were aged **25–35 years**
- **Outliers** exist in `fare` (premium-priced tickets) and `age` (entries with age = 0)

---

## ✅ Conclusion

The cleaned dataset reveals clear patterns in survival rates based on gender, passenger class, and deck location. Female passengers had significantly higher survival rates than males. Duplicates were intentionally retained due to insufficient identifying information (no passenger names). Outliers in fare and age were preserved for analysis integrity.

---

## 🛠️ Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 🚀 How to Run

1. Click the **Open in Colab** badge above, or
2. Clone this repository and run the notebook locally:

```bash
git clone https://github.com/senapathi402-star/data_cleaning_and_visualizing_titanic_dataset.git
```

---

## 📁 Project Structure
