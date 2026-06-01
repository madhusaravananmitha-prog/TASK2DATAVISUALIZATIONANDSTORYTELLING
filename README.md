# TASK2DATAVISUALIZATIONANDSTORYTELLING
# Customer Churn Analysis and Prediction using Power BI

## Project Overview

This project focuses on analyzing customer churn data and building an interactive dashboard using Power BI to identify factors influencing customer retention and churn behavior. The dashboard provides valuable insights into customer demographics, contract types, service usage, tenure, and churn trends, enabling data-driven business decisions.

---

## Objectives

* Analyze customer churn patterns and trends.
* Identify key factors contributing to customer attrition.
* Visualize customer demographics and behavior.
* Create an interactive dashboard for business insights.
* Support customer retention strategies through data analysis.

---

## Tools and Technologies

* Power BI Desktop
* Power Query Editor
* DAX (Data Analysis Expressions)
* Customer Churn Dataset

---

## Dataset Information

The dataset contains customer-related information, including:

* Customer ID
* Gender
* Senior Citizen Status
* Partner Status
* Dependents
* Tenure
* Internet Service
* Contract Type
* Payment Method
* Monthly Charges
* Total Charges
* Churn Status

---

## Data Preparation

### Data Import

* Imported the customer churn dataset into Power BI.
* Verified column names and data types.

### Data Cleaning

* Removed null and blank values.
* Removed duplicate records.
* Converted data types appropriately.
* Trimmed unwanted spaces from text fields.
* Standardized text formatting.

### Data Transformation

* Created **Senior Citizen Status** column.
* Created **Tenure Category** column:

  * New Customers (<12 months)
  * Regular Customers (12–24 months)
  * Loyal Customers (>24 months)

---

## DAX Measures Created

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS('Customer_Churn_Data'),
        'Customer_Churn_Data'[Churn] = "Yes"
    ),
    COUNTROWS('Customer_Churn_Data')
) * 100
```

### Total Customers

```DAX
Total Customers =
COUNTROWS('Customer_Churn_Data')
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    COUNTROWS('Customer_Churn_Data'),
    'Customer_Churn_Data'[Churn] = "Yes"
)
```

### Active Customers

```DAX
Active Customers =
CALCULATE(
    COUNTROWS('Customer_Churn_Data'),
    'Customer_Churn_Data'[Churn] = "No"
)
```

### Average Monthly Charges

```DAX
Average Monthly Charges =
AVERAGE('Customer_Churn_Data'[MonthlyCharges])
```

### Average Tenure

```DAX
Average Tenure =
AVERAGE('Customer_Churn_Data'[tenure])
```

### Total Revenue

```DAX
Total Revenue =
SUM('Customer_Churn_Data'[MonthlyCharges])
```

---

## Dashboard Components

### KPI Cards

* Churn Rate
* Total Customers
* Churned Customers
* Active Customers
* Average Monthly Charges
* Average Tenure
* Total Revenue

### Customer Demographics Analysis

* Gender Distribution (Pie Chart)
* Dependents vs Churn (Stacked Bar Chart)

### Customer Tenure Analysis

* Tenure Distribution Histogram

### Payment Method Analysis

* Customer Count by Payment Method

### Contract Type Analysis

* Contract Distribution (Donut Chart)
* Contract Type vs Churn (Stacked Bar Chart)

### Internet Service Analysis

* Internet Service vs Churn

### Monthly Charges Analysis

* Monthly Charges vs Churn (Scatter Plot)

### Interactive Filters (Slicers)

* Gender
* Contract Type
* Internet Service
* Churn Status

---

## Key Insights

* The overall churn rate is approximately **26%**, indicating a significant customer attrition rate.
* Customers with **Month-to-Month contracts** exhibit higher churn compared to long-term contracts.
* Customers using **Fiber Optic Internet Service** show relatively higher churn rates.
* Longer-tenure customers demonstrate better retention.
* Payment methods influence customer retention patterns.

---

## Skills Demonstrated

* Data Cleaning and Transformation
* Data Modeling
* DAX Calculations
* Dashboard Development
* Data Visualization
* Business Intelligence Reporting
* Customer Behavior Analysis
* Analytical Thinking

---

## Outcome

Developed a fully interactive Power BI dashboard that enables stakeholders to monitor customer churn trends, understand customer behavior, and make informed business decisions aimed at improving customer retention and reducing churn.

---

**Author:** Madhu Mitha
**Role:** Computer Science and Business Systems Student | Data Analytics Enthusiast
