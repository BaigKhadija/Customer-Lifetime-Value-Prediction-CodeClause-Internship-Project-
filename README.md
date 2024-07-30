# Customer Lifetime Value Prediction (CodeClause Internship Project)

## Project Overview
The aim is to accurately predict CLV for customers of the auto insurance company. The project includes:

- **Exploratory Data Analysis (EDA)**: To examine how CLV relates to other features.
- **Statistical Analysis**: Using techniques such as Ordinary Least Squares (OLS) for numerical features and Mann–Whitney U and Kruskal-Wallis tests for categorical variables to assess feature significance.
- **Supervised Regression Models**: Implementing models like Linear Regression, Ridge Regression, Lasso Regression, Decision Tree Regression, Random Forest Regression, and AdaBoost Regression.
- **Model Tuning**: GridSearchCV was employed with Random Forest Regression to achieve the best performance metrics.

## Dataset Description

The dataset includes 24 features and 9134 records, representing the CLV of customers from an auto insurance company in the United States.

## Exploratory Data Analysis

#### Univariate Analysis
![CLV](/CLV.png "Customer Lifetime Value")
CLV: Displays a strong right skew.
![location](/location.png "Location")
-Location: Most customers are located in suburban areas.

#### Bivariate Analysis
![Bivariate Analysis](/bi.png "Bivariate Analysis of CLV and Monthly Premium")
- **CLV vs. Monthly Premium Auto**: Positive correlation and linear relationship.

#### Multivariate Analysis
![Heatmap](/Heatmap.png "Heatmap")
- **Heatmap Analysis**:
  - Positive correlation between CLV and Monthly Premium Auto.
  - Slight positive correlation between Total Claim Amount and CLV.
  - Minimal correlation between Income and CLV.

## Evaluation Metric

The models were evaluated using RMSE (Root Mean Squared Error) and R^2 score.

## Supervised Models Used

| Model                       | R^2 Score | RMSE   |
|-----------------------------|-----------|--------|
| Linear Regression           | 0.25      | 0.5772 |
| Ridge Regression            | 0.21      | 0.5925 |
| Lasso Regression            | 0.19      | 0.5992 |
| Decision Tree Regression    | 0.84      | 0.2668 |
| Random Forest Regression    | 0.90      | 0.2047 |
| AdaBoost Regression         | 0.89      | 0.2181 |
| Random Forest with GridSearchCV | 0.91  | 0.1956 |

## Final Model

Among the models tested, Random Forest Regression optimized with GridSearchCV provided the best performance in terms of both RMSE and R^2 score.

## Conclusion

Key features for predicting CLV include the number of policies, monthly premium, total claim amount, months since policy inception, income, months since the last claim, number of open complaints, coverage type, employment status, and offer type. Customers with more policies and higher premiums are more valuable. Interestingly, the type or size of the vehicle does not significantly affect CLV. Therefore, insurance agents should focus their advertising efforts on customers with more policies to maximize CLV.
