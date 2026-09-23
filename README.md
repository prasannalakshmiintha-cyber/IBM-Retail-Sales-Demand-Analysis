# Retail Sales and Demand Analysis with Sales Prediction

## 1. Project Overview

**Retail Sales and Demand Analysis with Sales Prediction** is an IBM SkillsBuild Data Analytics with AI Internship Project.

The project analyzes historical retail sales transactions using data analytics, exploratory data analysis, feature engineering, and machine learning. The objective is to understand sales patterns, customer and product-related information, returns, and other factors, and to build regression models for predicting **Sales Amount**.

## 2. Problem Statement

Retail businesses generate large amounts of sales data every day. Simply storing sales data is not enough. Businesses need to understand sales patterns, identify products with high and low demand, analyze factors affecting sales, and estimate sales values to support business decisions.

This project analyzes historical retail sales data using data analytics and machine learning techniques. The project includes data cleaning, exploratory data analysis, feature engineering, machine learning model development, model evaluation, and sample sales prediction.

## 3. Objectives

- Understand and analyze historical retail sales data.
- Clean and preprocess the dataset.
- Analyze sales, profit, product, customer, channel, monthly, and return patterns.
- Identify important relationships between sales and other variables.
- Create useful visualizations to understand sales patterns.
- Prepare relevant features for machine learning.
- Build regression models to predict Sales Amount.
- Evaluate the models using MAE, RMSE, and R².
- Analyze feature importance and test the trained model with a sample transaction.

## 4. Dataset Description

### Dataset Name

**Sales Transactions 2022–2025**

### Dataset Source

The dataset used for this project is available on Kaggle:

https://www.kaggle.com/datasets/danielsowah123/retail-sales-dataset

### Dataset Details

The dataset contains **18,045 transactions and 36 columns**. It includes customer information, product information, sales and cost values, discounts, payment methods, delivery details, returns, ratings, inventory levels, and order-year information.

Important variables include:

- Customer_Age
- Customer_Gender
- Customer_Segment
- Order_Date
- Order_Time
- Sales_Channel
- Store
- Country
- Region
- City
- Product_Category
- Product_Subcategory
- Quantity
- Unit_Price
- Discount_Percentage
- Sales_Amount
- Cost_Amount
- Profit
- Payment_Method
- Order_Status
- Shipping_Method
- Delivery_Days
- Return_Flag
- Return_Reason
- Customer_Rating
- Inventory_Level

### Local Dataset Files

```text
sales_transactions_2022_2025.csv
sales_data_dictionary.csv
```

## 5. Technologies Used

| Technology / Library | Purpose |
|---|---|
| Python | Main programming language |
| Jupyter Notebook | Development and execution environment |
| NumPy | Numerical operations |
| Pandas | Data loading, cleaning, and analysis |
| Matplotlib | Data visualization |
| Seaborn | Statistical and exploratory data visualization |
| Scikit-learn | Machine learning, model training, and evaluation |

## 6. Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Data Cleaning & Preprocessing
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Train-Test Split
   ↓
Linear Regression + Random Forest Regression
   ↓
Model Evaluation
   ↓
Feature Importance
   ↓
Sample Sales Prediction
   ↓
Conclusion
```

## 7. Data Preprocessing

The dataset was inspected for its dimensions, data types, missing values, and unusual observations.

The preprocessing included:

- Checking dataset dimensions and data types.
- Checking missing values.
- Handling missing categorical values by replacing them with `Unknown`.
- Handling missing numerical values such as Customer_Age, Delivery_Days, Customer_Rating, and Inventory_Level using median values.
- Examining potentially unusual observations.
- Inspecting negative quantities, customer ages above 100, and discounts above 100%.

## 8. Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the main patterns in the sales data.

The analysis included:

- Yearly sales and profit
- Product-category performance
- Sales channels
- Customer segments
- Top products
- Monthly trends
- Payment methods
- Returns
- Customer ratings
- Relationship between Sales Amount and Profit

### Selected Findings

- **Total transactions:** 18,045
- **Returned transactions:** 1,877
- **Return rate:** 10.40%
- **Average customer rating:** 3.99
- **Correlation between Sales Amount and Profit:** 0.92
- **Correlation between Discount Percentage and Profit:** -0.19
- **Correlation between Quantity and Sales Amount:** 0.43
- **2025 recorded the highest total sales** among the four years analyzed, with sales of approximately 2.30 million.

## 9. Machine Learning

The target variable for the machine learning task was:

```text
Sales_Amount
```

Feature engineering was performed using date information, including:

- Order_Month
- Order_Day
- Order_DayOfWeek

### Selected Features

- Customer_Age
- Quantity
- Unit_Price
- Discount_Percentage
- Cost_Amount
- Delivery_Days
- Customer_Rating
- Inventory_Level
- Order_Year
- Order_Month
- Order_Day
- Order_DayOfWeek

The dataset was divided into training and testing sets using an **80:20 split**.

Two regression models were developed:

1. **Linear Regression**
2. **Random Forest Regression**

## 10. Model Results

The models were evaluated using:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **R² (R-squared)**

### Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 33.68 | 83.06 | 0.9909 |
| Random Forest Regression | 11.42 | 54.49 | 0.9961 |

On the test split, the Random Forest Regression model produced lower MAE and RMSE and a higher R² than the Linear Regression model.

The Actual vs Predicted Sales visualization also showed that most predictions were close to the reference line.

## 11. Feature Importance

Feature importance was analyzed using the trained Random Forest Regression model.

This analysis helps understand the relative contribution of the selected input features to the model's Sales Amount predictions.

The detailed feature-importance output is available in the submitted Jupyter Notebook.

## 12. Sample Sales Prediction

A sample transaction was supplied to the trained Random Forest model.

The model produced a predicted:

```text
Sales Amount = 210.54
```

This is the prediction produced for the sample transaction used in the project.

## 13. Key Findings

The project demonstrates that historical retail sales data can be analyzed to identify useful patterns in:

- Sales
- Profit
- Products
- Customers
- Sales channels
- Monthly trends
- Returns
- Customer ratings
- Relationships between important variables

The machine learning analysis also demonstrates the use of regression models for Sales Amount prediction.

## 14. Business Applications

The project can support retail-related activities such as:

- Sales analysis
- Demand-related analysis
- Inventory planning
- Product performance analysis
- Customer and sales-channel analysis
- Return analysis
- Sales prediction
- Data-driven decision support

The model predictions should be treated as analytical outputs and should be considered together with other relevant business information when making real-world decisions.

## 15. Setup and Run Instructions

### Prerequisites

Install:

- Python 3.x
- Jupyter Notebook or Anaconda

### Install Required Libraries

Open Anaconda Prompt or Command Prompt in the project folder and run:

```bash
pip install -r requirements.txt
```

### Start Jupyter Notebook

Run:

```bash
jupyter notebook
```

Open the project `.ipynb` file.

### Run the Project

1. Keep the Jupyter Notebook and required CSV files available.
2. Open the notebook.
3. Run the cells from beginning to end.
4. Review the data analysis, visualizations, model results, feature importance, and sample prediction.

## 16. Project Files

The final project submission contains the following required files:

```text
IBM_Retail_Sales_Demand_Analysis/
│
├── Prasanna_RetailSalesAndDemandAnalysis.ipynb
├── requirements.txt
├── Prasanna_ProjectReport.docx
└── README.md
```

The GitHub repository may additionally contain:

```text
├── sales_transactions_2022_2025.csv
└── sales_data_dictionary.csv
```


## 17. Reproducibility

To reproduce the project:

1. Download the dataset from the Kaggle link provided above.
2. Place the required CSV files in the project directory.
3. Install the libraries listed in `requirements.txt`.
4. Open the Jupyter Notebook.
5. Run all notebook cells in order.
6. Review the generated analysis, visualizations, model evaluation results, feature importance, and sample prediction.

## 18. Future Scope

Possible future improvements include:

- Testing the models on future unseen sales data.
- Additional hyperparameter tuning and cross-validation.
- Including seasonal events, holidays, promotions, and other external factors.
- Developing an interactive sales analytics and prediction dashboard.
- Deploying the trained model as a web or mobile application.
- Extending the project toward product-demand forecasting using time-series methods.

## 19. Conclusion

This project analyzed **18,045 sales transactions from 2022–2025** using data analytics and machine learning techniques.

The dataset was cleaned and explored to identify sales patterns, customer behavior, product performance, sales channels, returns, and relationships between important variables. Feature engineering was then used to prepare the data for machine learning.

Two regression models, **Linear Regression** and **Random Forest Regression**, were developed to predict Sales Amount. Linear Regression achieved an MAE of **33.68**, RMSE of **83.06**, and R² of **0.9909**, while Random Forest Regression achieved an MAE of **11.42**, RMSE of **54.49**, and R² of **0.9961** on the test split.

The trained Random Forest model was also tested with a sample transaction and produced a predicted Sales Amount of **210.54**.

Overall, the project demonstrates how data analytics and machine learning can be applied to historical retail sales data to identify useful patterns and support sales prediction.

## 20. Author

**Name:** I.Prasanna lakshmi

**Program:** IBM SkillsBuild Data Analytics with AI Academic Internship Program

**Project:** Retail Sales and Demand Analysis with Sales Prediction
