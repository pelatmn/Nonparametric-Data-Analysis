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

### 2. ⚙️ Statistical Tests and Results

#### 2.1. 📊 Independent Data Analysis

- **Normality Test:** 
  - Shapiro-Wilk test was used to assess the normality of the data.
  - **Results:**
    - **Treatment 1:** p-value = 0.829 > 0.05, data is normally distributed.
    - **Treatment 2:** p-value = 0.855 > 0.05, data is normally distributed.
    - **Treatment 3:** p-value = 0.044 < 0.05, data is not normally distributed.

- **Descriptive Statistics:** 
  - **Overall Results:**
    - **Mean:** 10.20
    - **Standard Deviation:** 9.84
    - **Variance:** 96.88
    - **Skewness:** 
      - Treatment 1: 0.298 (approximately symmetric)
      - Treatment 2: 0.261 (approximately symmetric)
      - Treatment 3: 1.300 (positively skewed)
    - **Kurtosis:**
      - Treatment 1: -1.317 (platykurtic)
      - Treatment 2: -1.101 (platykurtic)
      - Treatment 3: 0.004 (mesokurtic, close to normal distribution)

- **Visualization:**
  - **Q-Q Plots, Histograms, and Box Plots** were generated to visualize the data distributions and assess normality. 
    - **Q-Q Plot Results:**
      - Treatment 1 and 2 show data points aligned with the normal line, indicating normality.
      - Treatment 3 shows deviation from the normal line, indicating non-normality.
    - **Histogram Results:**
      - Treatment 1: Slightly positively skewed.
      - Treatment 2: Slightly negatively skewed.
      - Treatment 3: Significantly positively skewed.
    - **Box Plot Results:**
      - Treatment 3 has outliers, indicating non-normality.
      - Median lines of Treatment 1 and 2 overlap, suggesting no significant difference between them. However, Treatment 3's median does not overlap with others, suggesting a potential difference.

- **Statistical Tests:**
  - **Sign Test and Wilcoxon Signed-Rank Test:** Used to compare medians of Treatment 3 against a specific value.
    - **Results:**
      - **Sign Test:** p-value = 0.3125 > 0.05, median of Treatment 3 is not significantly different from 9.
      - **Wilcoxon Signed-Rank Test:** p-value = 0.1726 > 0.05, median of Treatment 3 is not significantly different from 9.
  - **Mann-Whitney Test:** Conducted to compare differences between Treatments 1 and 3.
    - **Result:** p-value = 0.1547 > 0.05, no significant difference between Treatments 1 and 3 in terms of strength gains.
  - **Kruskal-Wallis Test:** Used to compare differences across all three treatments.
    - **Result:** p-value = 0.2566 > 0.05, no significant difference between any of the treatments in terms of strength gains.

#### 2.2. 🔍 Dependent Data Analysis

- **Normality Test:** 
  - Shapiro-Wilk test was used to assess the normality of the data for each week.
  - **Results:**
    - **Week 1:** p-value = 0.0038 < 0.05, data is not normally distributed.
    - **Week 2:** p-value = 0.0980 > 0.05, data is normally distributed.
    - **Week 3:** p-value = 0.6737 > 0.05, data is normally distributed.
    - **Week 4:** p-value = 0.7167 > 0.05, data is normally distributed.

- **Descriptive Statistics:** 
  - **Overall Results:**
    - **Mean:** 
      - Week 1: 9.90
      - Week 2: 10.60
      - Week 3: 10.10
      - Week 4: 10.20
    - **Standard Deviation:** 
      - Week 1: 4.07
      - Week 2: 5.56
      - Week 3: 3.87
      - Week 4: 4.02
    - **Variance:** 
      - Week 1: 16.54
      - Week 2: 30.93
      - Week 3: 14.99
      - Week 4: 16.18
    - **Skewness:** 
      - Week 1: 1.642 (positively skewed)
      - Week 2: 0.429 (slightly negatively skewed)
      - Week 3: -0.528 (slightly positively skewed)
      - Week 4: 0.235 (slightly negatively skewed)
    - **Kurtosis:**
      - Week 1: 1.845 (leptokurtic)
      - Week 2: -1.450 (platykurtic)
      - Week 3: 0.220 (mesokurtic)
      - Week 4: -0.970 (platykurtic)

- **Visualization:**
  - **Q-Q Plots, Histograms, and Box Plots** were generated to visualize the data distributions.
    - **Q-Q Plot Results:**
      - Week 1 deviates from the normal line, indicating non-normality.
      - Weeks 2, 3, and 4 show alignment with the normal line, indicating normality.
    - **Histogram Results:**
      - Week 1: Positively skewed distribution.
      - Week 2: Symmetric distribution.
      - Week 3: Negatively skewed distribution.
      - Week 4: Negatively skewed distribution.
    - **Box Plot Results:**
      - Week 1 has outliers, and Weeks 2, 3, and 4 show varying levels of dispersion.

- **Statistical Tests:**
  - **Wilcoxon Signed-Rank Test:** Used to compare differences between Week 1 and Week 2.
    - **Result:** p-value = 0.4228 > 0.05, no significant difference between Week 1 and Week 2.
  - **Friedman Test:** Used to compare differences across all four weeks.
    - **Result:** p-value = 0.9232 > 0.05, no significant difference in quality of life across the four weeks.

#### 2.3. 🎯 Trend Analysis

- **Mann-Kendall Test:**
  - Applied to detect trends over time in a dataset of Euro exchange rates for the year 2023.
  - **Results:**
    - **Kendall Tau Correlation:** 0.909, indicating a strong positive trend.
    - **p-value:** 1.47e-06, confirming that the trend is statistically significant.

## 🛠️ Code Snippets

- **Data Import and Preparation:**
  ```python
  import pandas as pd
  data = pd.read_excel('path_to_file.xlsx')

## 📚 References

- **Data Source:** 
  - Euro exchange rates from [Investing.com](https://tr.investing.com/currencies/eur-try-historical-data) (Accessed on January 6, 2024).
- **Literature:**
  - Corder, G. W., & Foreman, I. D. (2014). *Nonparametric Statistics*. Wiley.

#### 📫 How to Contribute
Contributions are welcome! Feel free to open an issue or submit a pull request with improvements or additional analyses.

## 🔧 Appendix: Code Snippets

### Independent Data Analysis

#### Importing Data and Initial Analysis
```python
import pandas as pd

# Load independent data
data = pd.read_excel('path_to_file.xlsx')

# Display first few rows
print(data.head())
