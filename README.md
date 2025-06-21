# 🏃 Aerofit Treadmill Customer Analysis Case Study

## 🏢 About Aerofit

**Aerofit** is a leading brand in the fitness equipment industry, offering treadmills, exercise bikes, gym equipment, and fitness accessories. With a focus on catering to diverse customer needs, the company’s product range includes:

- **KP281**: Entry-level treadmill ($1,500)
- **KP481**: Mid-level treadmill for regular runners ($1,750)
- **KP781**: Advanced treadmill with premium features ($2,500)

## 🎯 Business Problem

The **Market Research team at Aerofit** wants to understand what kind of customers are buying which treadmill model. The aim is to **profile the audience segments** and build **conditional/marginal probabilities** for each product. This will help in:

- Recommending the right treadmill to new customers
- Building targeted marketing strategies
- Expanding product reach across key demographics

## 📂 Dataset Overview
### 📥 Dataset: [Aerofit_treadmill.csv](https://drive.google.com/file/d/1c4Gs-X_azmpp8o0Ls2Sk532uVBEa8cBr/view?usp=drive_link)

The dataset includes purchase data for 180 customers collected over 3 months.

| Column         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `Product`      | Treadmill model purchased (KP281, KP481, KP781)                            |
| `Age`          | Customer’s age                                                              |
| `Gender`       | Male or Female                                                              |
| `Education`    | Years of education                                                          |
| `MaritalStatus`| Single or Partnered                                                         |
| `Usage`        | Planned weekly usage of the treadmill                                       |
| `Income`       | Annual income in USD                                                        |
| `Fitness`      | Self-rated fitness level (1 to 5)                                           |
| `Miles`        | Expected weekly distance (miles)                                            |



## 🎯 Core Exploratory Goals

- Understand demographic patterns by product type.
- Detect outliers and distribution skews.
- Compute **marginal and conditional probabilities** (e.g., what % of males buy KP781?).
- Profile customers by age, gender, income, and usage.
- Recommend strategies based on probability tables and visual analytics.


## 📊 Key Analysis

### 1. 🔍 General & Preprocessing
- Dataset: 180 rows × 9 columns.
- No missing values. Data types validated and consistent.
- Outlier detection using boxplots and comparison of mean vs. median.

### 2. 📊 Categorical Variables Analysis
- Countplots and cross-tabulations for `Product`, `Gender`, and `MaritalStatus`.
- Majority buyers for KP281 are **partnered**, while KP781 is favored by **single males**.

### 3. 📈 Bivariate Insights
- Boxplots and histograms show:
  - **KP781** buyers are younger, higher income, more frequent users.
  - **KP281** appeals to casual, lower-income, and less-fit customers.

### 4. 📋 Probability Tables
- **Marginal Probabilities**:
  - KP281: 44.4%  
  - KP481: 33.3%  
  - KP781: 22.2%
  
- **Conditional Probabilities**:
  - High probability of KP781 purchase among **males**, **single customers**, and those with **fitness rating ≥ 4**.
  - KP281 more likely among **females**, **partnered customers**, and lower fitness scores.

### 5. 🔥 Correlation Analysis
- Strong correlation among `Fitness`, `Usage`, and `Miles`.
- Moderate positive correlation between `Education` and `Income`.

## 👥 Customer Profiles

### KP281 – Entry Level
- **Age**: < 30
- **Income**: < $70,000
- **Usage**: 2–4 times/week
- **Fitness**: Level 2–3
- **Miles**: < 100 miles/week
- **Gender**: Balanced
- **Marital**: Popular among partnered individuals

### KP481 – Mid-Level
- **Age**: Around 30
- **Income**: $40,000–$70,000
- **Usage**: Moderate
- **Fitness**: Level 3–4
- **Miles**: 80–120
- **Gender**: Balanced

### KP781 – Premium
- **Age**: 25–40, males > 40
- **Income**: > $70,000
- **Usage**: > 4 times/week
- **Fitness**: Level 4–5
- **Miles**: > 120 miles/week
- **Gender**: Primarily male

## 💡 Recommendations

### 📦 Product Strategy
- **KP281**: Promote as a budget-friendly option for light users and fitness beginners  
- **KP481**: Position as a value option for moderately active individuals  
- **KP781**: Target premium, fitness-focused segment with high-income levels

### 🎯 Marketing Tactics
- Use **income** and **fitness level** as primary segmenting features
- Focus on **partnered households** for KP281 and **single males** for KP781
- Customize campaigns for different **usage levels and education brackets**

### 📈 Feature Development
- Introduce **smart fitness tracking** for KP781 to attract data-driven athletes
- Offer **bundle deals** (with accessories) for KP281 to increase conversions

### 💬 Continuous Optimization
- Monitor feedback regularly  
- Run A/B campaigns based on user profiles  
- Train sales staff for **profile-based product recommendations**

## 🛠️ Tools Used

- Python (Pandas, Matplotlib, Seaborn)
- Statistical analysis using NumPy
- Visualizations: Countplot, Boxplot, Scatterplot, Crosstab, Heatmap

## 📄 Output Report

📎 All code, charts, and insights are compiled in the attached PDF:  
**[aerofit_case_study_akansha_saini.pdf](https://drive.google.com/file/d/11R-kOx4-UjTUQduAchUJhVSj6DI55c9l/view?usp=drive_link)**

## 📌 Notes
* Data was normalized using clipping between percentiles to reduce skew from outliers.
* Cross-tabulated distributions used for all conditional probability computations.
* Strategic insights backed by EDA, statistical summaries, and multivariate visualizations.
