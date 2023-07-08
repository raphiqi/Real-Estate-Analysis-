# Real-Estate-Price Modeling through Multi-linear Regression
Finding out the analysis process of determining house sales from various variables and predictors through Multi Linear Regression
# Business Understanding
A brief overview of the business focusing on conducting regression analysis for house sales.
It aims to explain the importance of regression analysis in understanding the factors that influence house prices and predicting future trends like waterfront and views.
Highlighting the value that the business brings to clients by providing data-driven insights and accurate predictions.
Conducts a market analysis to identify the target market for the regression analysis services.
Analyze the demand for real estate market insights and the need for accurate predictions
Business Understanding
# a.) Introduction
The business specializes in providing regression analysis services for house sales. It understands the importance of utilizing data-driven insights to understand the factors that influence house prices and predict future trends accurately. By conducting thorough market analysis, the business identifies the target market and the demand for real estate market insights and predictions.
Overall, the business understands the significance of regression analysis in the context of house sales. It leverages data, statistical expertise, and predictive modeling to provide valuable insights to clients, enabling them to make informed decisions in the dynamic real estate market in Northwestern county.
# b.) Problem Statement
The real estate industry faces the challenge of accurately understanding the factors that influence house prices and predicting future trends. Many stakeholders, including buyers, sellers, investors, and lenders, seek reliable insights to make informed decisions. However, the complexity of the market and the multitude of variables involved make it difficult to obtain accurate predictions and data-driven insights.

There is a need for a specialized business that comprehends the intricacies of house sale regression analysis. Such a business should possess a deep understanding of the real estate market, employ robust methodologies for data collection and analysis, develop accurate regression models, and deliver clear and understandable reports to clients.

By addressing these challenges, the business can provide reliable predictions of house prices, identify significant factors influencing the market, and offer actionable insights to clients. This will empower stakeholders to make informed decisions, mitigate risks, optimize investments, and maximize returns in the dynamic real estate industry.

# c.) Main Objective
The primary focus is on delivering value to clients by:

Predicting House Prices: Developing robust regression models that consider various factors such as location, size, amenities, and market trends to accurately predict house prices. The objective is to provide clients with reliable estimates of property values, empowering them to make informed buying, selling, or investment decisions.

Identifying Market Influencers: Analyzing the data to identify significant factors that impact the real estate market, such as economic indicators, neighborhood characteristics, interest rates, and supply and demand dynamics. The objective is to help clients understand the key drivers of property values and recognize emerging trends.

Ensuring Data Accuracy and Reliability: Implementing robust data collection, cleaning, and preprocessing methodologies to ensure the accuracy and reliability of the data used in the regression analysis. The objective is to provide clients with reliable and trustworthy insights to support their decision-making processes.

Building Strong Client Relationships: Prioritizing client needs and fostering strong relationships to understand their specific requirements and tailor analysis and insights accordingly. The objective is to provide personalized services and cultivate long-term collaborations and repeat business.

# d.) Specific Objective
Providing Actionable Insights: Presenting findings and insights in clear and understandable reports, customized based on client requirements. The objective is to provide clients with actionable recommendations that enable them to optimize their real estate strategies, mitigate risks, and maximize returns.
# e.) Experimental Design
Data Collection
Data cleaning
Training the data
Modelling and Analysis
Conclusions and Recommendations

# 
Data Understanding
This project uses the King County House Sales dataset, which can be found in kc_house_data.csv in the data folder in this git respiratory . The description of the column names can be found in column_names.md in the same folder. As with most real world data sets, the column names are not perfectly described so will figure out how to access this as we continue

Lets ignore some or all of the following features:

- date
- view
- sqft_above
- sqft_basement
- yr_renovated
- zipcode
- lat
- long
- sqft_living15
- sqft_lot15

# Final Multi-Linear Regression Model Results

OLS Regression Results                            
==============================================================================
Dep. Variable:                  price   R-squared:                       0.514
Model:                            OLS   Adj. R-squared:                  0.513
Method:                 Least Squares   F-statistic:                     5545.
Date:                Sat, 08 Jul 2023   Prob (F-statistic):               0.00
Time:                        16:50:15   Log-Likelihood:            -2.1887e+05
No. Observations:               15762   AIC:                         4.377e+05
Df Residuals:                   15758   BIC:                         4.378e+05
Df Model:                           3                                         
Covariance Type:            nonrobust                                         
===============================================================================
                  coef    std err          t      P>|t|      [0.025      0.975]
-------------------------------------------------------------------------------
const         6.86e+04   8155.577      8.411      0.000    5.26e+04    8.46e+04
sqft_living   316.9197      3.633     87.242      0.000     309.799     324.040
bathrooms    6491.4498   4150.903      1.564      0.118   -1644.796    1.46e+04
bedrooms    -5.968e+04   2729.552    -21.866      0.000    -6.5e+04   -5.43e+04
==============================================================================
Omnibus:                    10819.360   Durbin-Watson:                   1.971
Prob(Omnibus):                  0.000   Jarque-Bera (JB):           409070.539
Skew:                           2.812   Prob(JB):                         0.00
Kurtosis:                      27.316   Cond. No.                     9.33e+03
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
[2] The condition number is large, 9.33e+03. This might indicate that there are
strong multicollinearity or other numerical problems.

# Results
R-squared and Adjusted R-squared:

R-squared: 0.514 This value represents the proportion of variance in the dependent variable (price) that can be explained by the independent variables (sqft_living, bathrooms, and bedrooms). In this case, approximately 51.4% of the variance in house prices can be explained by the predictors in the model. Adjusted R-squared: 0.513 The adjusted R-squared takes into account the number of predictors and sample size. It provides a more accurate measure of the model's goodness of fit. Coefficients and Standard Errors:

const (intercept): 6.86e+04 This represents the estimated average house price when all the predictors (sqft_living, bathrooms, and bedrooms) are zero. sqft_living: 316.9197 For every one unit increase in square footage, the estimated average house price is expected to increase by 316.92 dollars. bathrooms: 6491.4498 This coefficient represents the expected change in the average house price for each additional bathroom. For each additional bedroom, the estimated average house price is expected to decrease by 59,680 dollars. P-values:

P-values provide information about the statistical significance of each coefficient. A p-value less than 0.05 is typically considered statistically significant. In this model, the coefficients for the intercept and bedrooms are statistically significant (p < 0.001), while the coefficient for bathrooms is not statistically significant (p = 0.118).

# Conclusions and Next steps
Interpretation and Insights:
Dig deeper into the regression results to extract valuable insights and interpret the coefficients of the predictors in the context of your project. Identify the most influential factors affecting house prices based on the magnitude and statistical significance of the coefficients.Conduct hypothesis testing.

Communication and Reporting:
Prepare a comprehensive report summarizing your regression analysis, including the methodology, findings, and recommendations. Clearly communicate the limitations and assumptions of the model. Further Analysis and Exploration:

Explore additional research questions or hypotheses related to the housing market.
Investigate the relationships between other variables or factors and house prices to gain a deeper understanding of the market dynamics.Explore other machine learning approaches.
