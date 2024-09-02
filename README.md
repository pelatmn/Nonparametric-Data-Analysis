# Nonparametric-Data-Analysis

# 📊 Statistical Analysis of Dependent and Independent Non-Parametric Datasets

## 📋 Overview

This project focuses on the statistical analysis of dependent and independent non-parametric datasets. The analysis includes various tests such as the Mann-Whitney test, Wilcoxon Signed-Rank test, Kruskal-Wallis test, Friedman test, and Mann-Kendall trend test. The data sets are analyzed to determine if there are significant differences between groups or trends over time.

## 🏗️ Project Structure

### 1. 📝 Datasets

- **Independent Data Set:** 
  - A study with 15 participants divided into three groups to measure strength gains after different treatments.
  - **Objective:** To determine if there is a significant difference in strength gains between the different treatment methods.

- **Dependent Data Set:**
  - A study analyzing the effects of animal companionship on the quality of life of 10 elderly male participants over four weeks.
  - **Objective:** To observe the impact of animal companionship over time on participants' life satisfaction.

### 2. ⚙️ Statistical Tests

#### 2.1. 📊 Independent Data Analysis

- **Normality Test:** 
  - Shapiro-Wilk test was used to assess the normality of the data.
  - Results indicated that for one of the treatment methods, data does not follow a normal distribution.

- **Descriptive Statistics:** 
  - Mean, standard deviation, variance, skewness, and kurtosis values were calculated.
  - Box plots, Q-Q plots, and histograms were used for visualization.

- **Statistical Tests:**
  - **Sign Test and Wilcoxon Signed-Rank Test:** Used to compare medians of a selected group against a specific value.
  - **Mann-Whitney Test:** Conducted to compare differences between two independent groups.
  - **Kruskal-Wallis Test:** Used to compare differences between three independent groups.

#### 2.2. 🔍 Dependent Data Analysis

- **Normality Test:** 
  - Shapiro-Wilk test was used to assess the normality of the data for each week.
  - Results varied, with some weeks showing non-normal distributions.

- **Descriptive Statistics:** 
  - Summary statistics such as mean, standard deviation, and variance were calculated.
  - Visualizations included histograms and box plots.

- **Statistical Tests:**
  - **Wilcoxon Signed-Rank Test:** Used to compare differences between two dependent groups (e.g., week 1 vs. week 2).
  - **Friedman Test:** Conducted to compare differences across multiple dependent groups (e.g., weekly data).

#### 2.3. 🎯 Trend Analysis

- **Mann-Kendall Test:**
  - Applied to detect trends over time in a dataset of Euro exchange rates for the year 2023.
  - The test indicated a significant positive trend in the exchange rates.

## 🛠️ Code Snippets

- **Data Import and Preparation:**
  ```python
  import pandas as pd
  data = pd.read_excel('path_to_file.xlsx')
