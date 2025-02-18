# **Big-Mart-Sales-Prediction**

## 1) Problem Statement

The data scientists at BigMart have collected sales data from 2013 for 1559 products across 10 stores in different cities. Along with this, certain attributes of each product and store have been defined. The goal of this data science project is to build a predictive model that estimates the sales of each product at a given store.

- **Business Goal:**  
  The objective is to use the model to understand the factors (properties of products and stores) that are key drivers in increasing sales.

- **Problem Type:**  
  This is a supervised learning problem.

- **Target Feature:**  
  The target variable for prediction is `Item_Outlet_Sales`.

1. **Problem Statement**
2. **Loading Packages and Data**
3. **Exploratory Data Analysis (EDA)**
4. **Label Encoding**
5. **One-Hot Encoding**
6. **Data Preprocessing**
7. **Modeling**
8. **Linear Regression**
9. **Regularized Linear Regression**
10. **Random Forest**
11. **XGBoost**
12. **Predictions & Summary**
13. **Saving the Final Model**
14. **Hyperparameter Tuning with RandomizedSearchCV**
15. **Evaluating RandomizedSearchCV Tuned Models**
16. **Final Predictions Using Best RandomizedSearchCV Model**
17. **GridSearchCV for Hyperparameter Tuning**
18. **Evaluating GridSearchCV Tuned Models**
19. **Final Predictions Using Best GridSearchCV Model**
20. **Saving the Final GridSearchCV Model Predictions**

---

## Data Dictionary

We have two datasets: **train** and **test**. The **train dataset** contains both input and output variables, while the **test dataset** only includes input variables for which sales need to be predicted.

### Train Dataset (8523 rows)

| Variable                  | Description                                                              |
|---------------------------|--------------------------------------------------------------------------|
| `Item_Identifier`          | Unique product ID                                                        |
| `Item_Weight`              | Weight of the product                                                     |
| `Item_Fat_Content`         | Whether the product is low fat or not                                    |
| `Item_Visibility`          | Percentage of total display area allocated to the product in a store    |
| `Item_Type`                | The category the product belongs to                                      |
| `Item_MRP`                 | Maximum Retail Price (list price) of the product                        |
| `Outlet_Identifier`        | Unique store ID                                                          |
| `Outlet_Establishment_Year`| The year in which the store was established                              |
| `Outlet_Size`              | The size of the store in terms of ground area covered                    |
| `Outlet_Location_Type`     | The type of city in which the store is located                           |
| `Outlet_Type`              | Whether the outlet is a grocery store or a supermarket                   |
| `Item_Outlet_Sales`        | Sales of the product in the store (target variable)                     |

### Test Dataset (5681 rows)

| Variable                  | Description                                                              |
|---------------------------|--------------------------------------------------------------------------|
| `Item_Identifier`          | Unique product ID                                                        |
| `Item_Weight`              | Weight of the product                                                     |
| `Item_Fat_Content`         | Whether the product is low fat or not                                    |
| `Item_Visibility`          | Percentage of total display area allocated to the product in a store    |
| `Item_Type`                | The category the product belongs to                                      |
| `Item_MRP`                 | Maximum Retail Price (list price) of the product                        |
| `Outlet_Identifier`        | Unique store ID                                                          |
| `Outlet_Establishment_Year`| The year in which the store was established                              |
| `Outlet_Size`              | The size of the store in terms of ground area covered                    |
| `Outlet_Location_Type`     | The type of city in which the store is located                           |
| `Outlet_Type`              | Whether the outlet is a grocery store or a supermarket                   |

---

## Submission File Format

To submit your predictions, the output file should be structured as follows:

| Variable               | Description                                                   |
|------------------------|---------------------------------------------------------------|
| `Item_Identifier`       | Unique product ID                                             |
| `Outlet_Identifier`     | Unique store ID                                               |
| `Item_Outlet_Sales`     | Predicted sales of the product in the particular store       |

