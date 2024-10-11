# Financial Data Analytics Final Project

I created these Jupyter Notebooks for my team as part of the final project in my graduate-level Financial Data Analytics course (FI8090) at Georgia State University in the Fall Semester of 2022. This project was completed in collaboration with my teammates. Notably, I took on all coding responsibilities since my team members were not experienced programmers. Our work was presented to and evaluated by executives at QNBT and our professor.

The goal of the project was to perform analysis of a 50,000+ record dataset using Tableau and Python. Our goal was to create a model to predict and understand the drivers behind customer attrition. This analysis leveraged various machine learning models to maximize prediction accuracy and insights into customer behaviors.

## Overview of the Analysis

### 1. Data Preparation and Exploration
- **Initial Tools**: Before diving into Python, I used **Excel** and **Tableau** to clean and manipulate the data, identify trends, and explore initial insights. This early-stage work helped us understand the dataset's structure and provided a foundation for further modeling.
- **Data Sources**: The dataset was obtained from a financial institution and consisted of customer demographics, account balances, product usage (e.g., credit cards, loans), and behavioral metrics such as overdraft fees and service charges.
- **Data Cleaning**: Imported data into Python, examined null values, and removed/handled missing or inconsistent entries. Verified data types and corrected where necessary to ensure consistency.
- **Visualizations**: Utilized **Matplotlib** and **Seaborn** to generate key visualizations, such as histograms of customer tenure, heatmaps of feature correlations, and bar charts of customer churn distribution.

![Feature Correlation Heatmap](images/heatmap.png)

### 2. Data Balancing and Feature Engineering
- **Class Imbalance**: The dataset had a significant imbalance between churned and non-churned customers. Applied **undersampling** to balance the dataset and prevent biased model performance.
- **Feature Engineering**: Created several new features, such as customer tenure groups (e.g., Millennials, Gen Z), and combined related attributes to enhance model performance. Features like **experience-based status** and **transaction activity** were refined for better interpretation.

### 3. Predictive Modeling
- **Logistic Regression**: Built several **logistic regression models** to predict customer churn based on different combinations of variables:
  - **Churn & Years as a Customer**: Explored the relationship between tenure and churn. Found a negative relationship indicating that longer-tenured customers were less likely to churn.
  - **Churn & Transaction Count**: Modeled churn as a function of the number of transactions. Observed a weak but statistically significant effect on churn probability.
  - **Churn & Credit Card Flag**: Analyzed the impact of credit card ownership on churn, noting that having a credit card slightly reduced churn likelihood.
  - **Full Model**: Built a comprehensive logistic regression model including all available features, yielding a **pseudo R-squared of 0.126**.

![Logistic Regression Summary](images/logistic_regression_summary.png)

- **Model Evaluation**: Evaluated model performance using metrics such as **accuracy**, **confusion matrix**, and **pseudo R-squared** values. The **full logistic regression model** achieved an accuracy of 66.9%, and detailed models were created to isolate the influence of specific features.
- **Negative Experience & Exposure Model**: Combined negative customer experiences (e.g., overdraft charges, service charges) and exposure variables (e.g., transactions, bill payments). This resulted in a **pseudo R-squared of 0.082** with a test accuracy of **62.7%**.

### 4. LASSO Regression for Feature Selection
- **LASSO Model**: Built a **LASSO regression model** using negative experience and exposure variables to perform feature selection and regularization. This technique helped refine the most impactful factors contributing to customer churn by penalizing less relevant variables.

### 5. Key Insights
- **Customer Experience**: Factors such as **overdraft charges**, **service charges**, and **negative experiences** significantly increased the probability of churn, particularly for younger customers (e.g., Millennials).
- **Customer Exposure**: High usage of services like mobile app activity showed a nuanced impact, where active engagement helped retain customers, while negative financial behaviors contributed to increased churn.
- **Impact of Credit Cards**: Customers with credit cards exhibited slightly lower churn rates, which might indicate better engagement or satisfaction with financial services.

## Summary of Analysis
- Analyzed customer churn data by combining **initial exploration in Excel and Tableau** with **detailed Python-based modeling** to derive insights into customer behavior.
- Applied **logistic regression** and **LASSO regression** to predict churn and identify key drivers.
- Significant factors impacting churn included **overdraft fees**, **negative financial experiences**, and **customer tenure**.
- This project demonstrated skills in **data preparation**, **feature engineering**, **machine learning modeling**, and **model evaluation** in a finance context.

