# Unit 6: Analytics for Planning and Forecasting

## Overview

This unit delves into advanced data analytics techniques crucial for effective marketing planning and forecasting. Key topics include understanding the sales funnel, distinguishing between descriptive and predictive metrics, evaluating return on ad spend (ROAS) and return on investment (ROI), calculating customer lifetime value (CLV), and employing linear regression for forecasting.

---

## 1. The Sales Funnel & Descriptive Marketing Metrics

### The Sales Funnel

- **Definition**: The sales funnel is a model that illustrates the journey potential customers take from becoming aware of a product or service to making a purchase and beyond. It helps visualize and manage the customer journey to optimize each stage and improve conversion rates.
  
- **Stages**:
  - **Awareness**: Potential customers first learn about the brand or product through marketing activities such as advertising, content marketing, or social media.
  - **Interest**: Potential customers express interest by engaging with the brand, such as signing up for newsletters or following on social media.
  - **Consideration**: Customers evaluate the product or service by comparing it with competitors and considering how well it meets their needs.
  - **Decision**: The customer decides to purchase the product or service. This stage may involve negotiations or special offers.
  - **Retention**: Post-purchase efforts focus on keeping customers engaged and encouraging repeat purchases through follow-up communication, customer support, and exclusive offers.

### Descriptive Marketing Metrics

- **Definition**: Descriptive metrics summarize historical data to understand past performance. They do not predict future outcomes but provide insights into what has happened.
  
- **Key Metrics**:
  - **Website Traffic**:
    - **Page Views**: Total number of pages viewed on the website.
    - **Unique Visitors**: Number of distinct individuals visiting the site over a given period.
    - **Bounce Rate**: Percentage of visitors who leave the site after viewing only one page.
  - **Conversion Rates**:
    - **Conversion Rate**: Percentage of users who complete a desired action (e.g., purchase, sign-up) out of the total number of visitors.
  - **Engagement Metrics**:
    - **Social Media Engagement**: Measures interactions such as likes, comments, shares, and retweets on social media platforms.
    - **Email Engagement**: Metrics such as open rates, click-through rates, and response rates for email campaigns.

---

## 2. Descriptive vs. Predictive Metrics

### Descriptive Metrics

- **Purpose**: To provide a snapshot of past performance and understand historical trends.
  
- **Applications**:
  - **Campaign Analysis**: Reviewing past marketing campaigns to identify successful strategies and areas for improvement.
  - **Trend Analysis**: Observing historical trends in metrics such as website traffic or sales to understand patterns over time.

### Predictive Metrics

- **Purpose**: To forecast future outcomes based on historical data and trends.
  
- **Applications**:
  - **Sales Forecasting**: Predicting future sales based on historical data, seasonal trends, and other influencing factors.
  - **Customer Behavior Prediction**: Estimating future customer actions, such as the likelihood of purchasing or churn, based on past behavior patterns.

---

## 3. Return on Ad Spend (ROAS) and Return on Investment (ROI)

### Return on Ad Spend (ROAS)

- **Definition**: ROAS measures the revenue generated for every dollar spent on advertising.
  
- **Formula**: 
  **ROAS** = (Revenue from Ads / Cost of Ads)
  
- **Purpose**: To determine the profitability of ad campaigns and evaluate their impact on revenue generation.
  
- **Example**: If a campaign costs $1,000 and generates $5,000 in revenue, ROAS = 5. This means that for every dollar spent on ads, five dollars in revenue were generated.

### Return on Investment (ROI)

- **Definition**: ROI measures the overall profitability of an investment by comparing the net profit to the cost of the investment.
  
- **Formula**: 
  **ROI** = (Net Profit / Cost of Investment) × 100
  
- **Purpose**: To assess the overall success of marketing investments and their impact on business profitability.
  
- **Example**: If an investment costs $2,000 and generates a net profit of $6,000, the ROI is calculated as follows:
  
  **ROI** = ((6,000 - 2,000) / 2,000) × 100 = 200%
  
  This means the investment generated a 200% return on the initial cost.

---

## 4. Customer Lifetime Value (CLV) and Why It Matters

### Customer Lifetime Value (CLV)

- **Definition**: CLV represents the total revenue a business can expect from a customer over the entire duration of their relationship with the brand.
  
- **Formula**: 
  **CLV** = Average Purchase Value × Purchase Frequency × Customer Lifespan
  
- **Purpose**: To understand the long-term value of customers and guide strategies for customer acquisition, retention, and loyalty.
  
- **Example Calculation**:
  - **Average Purchase Value**: $50
  - **Purchase Frequency**: 4 purchases per year
  - **Customer Lifespan**: 5 years
  - **CLV** = $50 × 4 × 5 = $1,000

### Why CLV Matters

- **Resource Allocation**: Helps businesses allocate resources effectively by focusing on high-value customers.
- **Retention Strategies**: Guides efforts to retain valuable customers through personalized offers and loyalty programs.
- **Customer Acquisition**: Determines how much to invest in acquiring new customers based on their projected lifetime value.

---

## 5. Introduction to Linear Regression

### Linear Regression

- **Definition**: Linear regression is a statistical method used to model and analyze the relationship between a dependent variable and one or more independent variables. It predicts the dependent variable based on the values of the independent variables.
  
- **Purpose**: To understand and quantify the relationship between variables, and to forecast future outcomes based on this relationship.
  
- **Types**:
  - **Simple Linear Regression**: Analyzes the relationship between a single independent variable and a dependent variable.
  - **Multiple Linear Regression**: Analyzes the relationship between multiple independent variables and a dependent variable.

## Practical Session: Linear Regression and Multiple linear regression in Social Media Marketing 

### Simple Linear Regression

- **Objective**: Understand the impact of a single independent variable (e.g., marketing spend) on a dependent variable (e.g., sales).

- **Example**:
  - **Context**: Predicting sales based on social media ad spend.

- **Code**:
  
#### **1.1 Import Required Libraries**


To get started with the simple linear regression model, we need to import the following libraries:

- **`pandas`**: A library used for data manipulation and analysis. It provides data structures like DataFrames to work with tabular data.
- **`train_test_split`**: A function from `sklearn.model_selection` used to split data into training and testing sets.
- **`LinearRegression`**: A class from `sklearn.linear_model` for creating and training a linear regression model.
- **`mean_squared_error`**: A function from `sklearn.metrics` used to evaluate the performance of the regression model by calculating the mean squared error.
- **`matplotlib.pyplot`**: A library for creating visualizations such as plots and charts.

```python
  import pandas as pd
  from sklearn.model_selection import train_test_split
  from sklearn.linear_model import LinearRegression
  from sklearn.metrics import mean_squared_error
  import matplotlib.pyplot as plt
 ```

#### **1.2  Sample data**
- **This creates a DataFrame with sample data where MarketingSpend is the independent variable (feature) and Sales is the dependent variable (target).**
```python
  data = pd.DataFrame({
      'MarketingSpend': [1000, 1500, 2000, 2500, 3000, 3500, 4000],
      'Sales': [5000, 6000, 7000, 8000, 9000, 10000, 11000]
  })
 ```
#### **1.3 Features and target variable**
- **Features**: `X` includes the independent variable `MarketingSpend`.
- **Target Variable**: `y` is the dependent variable `Sales`.
```python
  X = data[['MarketingSpend']]
  y = data['Sales']
  ```

#### **1.4 Split data into training and test sets**
```python
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
 ```
#### **1.5 Initialize and train the model**
  ```python
  model = LinearRegression()
  model.fit(X_train, y_train)
 ```
#### **1.6 Make predictions and Evaluate the model**
 ```python
  y_pred = model.predict(X_test)
 

  mse = mean_squared_error(y_test, y_pred)
  print(f'Mean Squared Error: {mse}')
 ```
#### **1.7 Plotting**
```python
  plt.scatter(X, y, color='blue', label='Actual Sales')
  plt.plot(X, model.predict(X), color='red', label='Regression Line')
  plt.xlabel('Marketing Spend')
  plt.ylabel('Sales')
  plt.title('Marketing Spend vs Sales')
  plt.legend()
  plt.show()
 ```
#### Multiple Linear Regression 

- **Objective**
Analyze the impact of multiple independent variables (e.g., marketing spend, social media engagement) on a dependent variable (e.g., sales).

- **Example**
Predicting sales based on social media ad spend and engagement metrics.

- **Code**
Below is the Python code used for training and evaluating a Multiple Linear Regression model.
#### **1.1 Import Required Libraries**


To get started with the simple linear regression model, we need to import the following libraries:

- **`pandas`**: A library used for data manipulation and analysis. It provides data structures like DataFrames to work with tabular data.
- **`train_test_split`**: A function from `sklearn.model_selection` used to split data into training and testing sets.
- **`LinearRegression`**: A class from `sklearn.linear_model` for creating and training a linear regression model.
- **`mean_squared_error`**: A function from `sklearn.metrics` used to evaluate the performance of the regression model by calculating the mean squared error.
- **`matplotlib.pyplot`**: A library for creating visualizations such as plots and charts.

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
import matplotlib.pyplot as plt
 ```


#### **1.2  Sample data**
- **This creates a DataFrame with sample data where MarketingSpend is the independent variable (feature) and Sales is the dependent variable (target).**
```python
data = pd.DataFrame({
    'MarketingSpend': [1000, 1500, 2000, 2500, 3000, 3500, 4000],
    'SocialMediaEngagement': [200, 300, 400, 500, 600, 700, 800],
    'Sales': [5000, 6000, 7000, 8000, 9000, 10000, 11000]
 ```
#### **1.3 Features and target variable**
```python
- **Features**: `X` includes the independent variable `MarketingSpend`.
- **Target Variable**: `y` is the dependent variable `Sales`.
```python
X = data[['MarketingSpend', 'SocialMediaEngagement']]
y = data['Sales']
 ```


#### **1.4 Split data into training and test sets**
```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
 ```
#### **1.5 Initialize and train the model**
```python
model = LinearRegression()
model.fit(X_train, y_train)
 ```

#### **1.6 Make predictions and Evaluate the model**
```python
y_pred = model.predict(X_test)

mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print(f"Mean Squared Error: {mse}")
print(f"R^2 Score: {r2}")
 ```

#### **1.7 Plotting**
```python
plt.figure(figsize=(10, 6))
plt.scatter(y_test, y_pred, color='blue')
plt.plot([min(y_test), max(y_test)], [min(y_test), max(y_test)], color='red', linestyle='--')
plt.xlabel('Actual Sales')
plt.ylabel('Predicted Sales')
plt.title('Actual vs. Predicted Sales')
plt.show()
 ```
