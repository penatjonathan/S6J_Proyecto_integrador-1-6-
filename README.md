# 🎮 Sprint 6 Project — Ice Video Game Sales Analysis (Integrated Project)

---

🧠 **Project Overview**  
In this sprint, I worked as a data analyst for **Ice**, an international online video game store.  
The company provided historical data on **game sales, genres, platforms, critic and user reviews**, and **ESRB ratings**.  
My mission was to identify patterns that determine whether a game is likely to succeed — helping the marketing team detect promising projects and plan advertising campaigns effectively.

For this project, I used open-source data up to **2016**, simulating that I was preparing a marketing plan for **2017**.  
The goal was to apply all the statistical and analytical skills developed throughout the previous sprints in one integrated, end-to-end case study.

---

## 🎯 Project Objectives  
- Clean and preprocess the dataset.  
- Analyze sales by platform, genre, and region.  
- Explore the impact of critic and user ratings on sales performance.  
- Identify trends in platform lifecycles (growth and decline).  
- Profile user preferences across North America, Europe, and Japan.  
- Test hypotheses on user rating differences between platforms and genres.  
- Draw business insights to guide 2017 marketing strategy.  

---

## 📁 Dataset  

**File:** `/datasets/games.csv`  

| Column | Description |
|---------|--------------|
| `name` | Game title |
| `platform` | Gaming platform (e.g., Xbox, PlayStation) |
| `year_of_release` | Release year |
| `genre` | Game genre |
| `na_sales` | North America sales (in millions USD) |
| `eu_sales` | Europe sales (in millions USD) |
| `jp_sales` | Japan sales (in millions USD) |
| `other_sales` | Sales in other regions (in millions USD) |
| `critic_score` | Critics’ score (out of 100) |
| `user_score` | Users’ score (out of 10) |
| `rating` | ESRB age rating (e.g., E, T, M) |

---

## 🧩 Project Steps  

### Step 1 – Data Loading & Inspection  
- Imported `games.csv` and reviewed its structure.  
- Checked data types, missing values, and overall consistency.  
- Noted that **TBD** entries represent “to be determined” values and required special handling.  

### Step 2 – Data Preparation  
- Converted column names to lowercase.  
- Adjusted data types (e.g., `year_of_release` → `int`, scores → `float`).  
- Replaced or imputed missing values as appropriate and documented reasons.  
- Added a `total_sales` column = `na_sales + eu_sales + jp_sales + other_sales`.  
- Verified data accuracy after transformations.  

### Step 3 – Exploratory Data Analysis  
- Analyzed game release trends by year to determine data relevance.  
- Compared total sales across platforms and identified top-performing ones.  
- Examined lifecycle patterns — when platforms rise and decline in popularity.  
- Focused analysis on **recent and relevant years** to predict 2017 trends.  
- Created boxplots of global sales per platform to identify outliers and variability.  
- Studied correlations between **critic/user reviews** and **sales** on top platforms.  
- Compared performance of the same titles across multiple platforms.  
- Assessed the profitability of different genres.  

### Step 4 – Regional User Profiling  
For each region (**NA**, **EU**, **JP**):  
- Identified the **top 5 platforms** and **top 5 genres**.  
- Compared market shares and consumer preferences across regions.  
- Evaluated whether **ESRB ratings** influence sales differently per region.  

### Step 5 – Hypothesis Testing  
**Hypothesis 1:**  
- **H₀:** Average user ratings for Xbox One and PC games are equal.  
- **H₁:** Average user ratings differ between Xbox One and PC games.  

**Hypothesis 2:**  
- **H₀:** Average user ratings for Action and Sports genres are equal.  
- **H₁:** Average user ratings differ between Action and Sports genres.  

- Set significance level **α = 0.05**.  
- Applied **independent two-sample t-tests** (`scipy.stats.ttest_ind`).  
- Interpreted p-values and drew conclusions on statistical significance.  

### Step 6 – Conclusion  
- Summarized which **platforms and genres** are most profitable.  
- Highlighted how **critic and user scores** impact sales.  
- Provided insights for **marketing and inventory planning** for 2017.  

---

## 💡 Key Analytical Questions  
- Which gaming platforms are gaining or losing popularity?  
- What genres deliver the highest total sales?  
- How do critic and user ratings influence success?  
- Do sales patterns differ significantly between regions?  
- How should Ice allocate advertising efforts based on 2016 data?  

---

## 💼 Skills Developed  
- Data Cleaning & Preprocessing (`pandas`, `numpy`)  
- Exploratory Data Analysis (EDA)  
- Correlation Analysis & Visualization  
- Hypothesis Testing (`scipy.stats`)  
- Regional Market Profiling  
- Strategic Insights from Data  

---

## 🧰 Tools & Technologies  
`Python` | `Pandas` | `NumPy` | `Matplotlib` | `Seaborn` | `SciPy` | `Jupyter Notebook`

---

## 👤 Author  
*Project completed by [Jonathan Peña] as part of Sprint 6 — Integrated Data Analysis Project.*
