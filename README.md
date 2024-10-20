

# Retail Sales Prediction Project 

### Project Overview
This project aims to develop a machine learning model to predict retail sales using the Big Mart dataset. Accurate sales predictions will enable retailers to manage inventory, optimize stock levels, and make informed decisions regarding promotions and product placements.

### Objective
The main objective is to create a predictive model that accurately estimates future sales of products across various stores. This will enhance Big Mart's ability to manage inventory and develop effective sales strategies.

### Dataset
- **Source:** Big Mart sales data
- **Entries:** 8,523
- **Features:** 12 columns, including product and store attributes.

### Key Features
- **Item_Identifier:** Unique product ID
- **Item_Weight:** Weight of the product
- **Item_Fat_Content:** Indicates if the product is low fat or regular
- **Item_Visibility:** Display area percentage for the product
- **Item_Type:** Category of the product (e.g., Dairy, Soft Drinks)
- **Item_MRP:** Maximum Retail Price
- **Outlet_Identifier:** Unique store ID
- **Outlet_Establishment_Year:** Year the store was established
- **Outlet_Size:** Size of the store (small, medium, large)
- **Outlet_Location_Type:** City type (e.g., Tier 1, Tier 3)
- **Outlet_Type:** Type of store (e.g., Grocery Store)
- **Item_Outlet_Sales:** Target variable representing sales

### Data Preprocessing
1. **Handling Missing Values:**
   - Filled missing `Item_Weight` values with the mean.
   - Filled missing `Outlet_Size` values using the mode based on `Outlet_Type`.

2. **Encoding Categorical Variables:**
   - Standardized the `Item_Fat_Content` categories.
   - Applied Label Encoding for categorical features.

### Data Analysis
- Summary statistics and visualizations were performed to understand distributions and relationships among features.
- **Insights:**
  - Some `Item_Visibility` values were zero, which may be unrealistic.
  - The target variable (`Item_Outlet_Sales`) showed significant variance.

### Machine Learning Models

1. **XGBoost Regressor**
   - **R² Score (Training):** 0.876
   - **R² Score (Testing):** 0.502
   - **RMSE:** 1,538,210.92
   - **MAE:** 866.26

2. **Random Forest Regressor**
   - **R² Score (Testing):** 0.552
   - **Mean Absolute Error (MAE):** 824.26
   - **Root Mean Squared Error (RMSE):** 1,382,432.00

### Data Visualization
Visualizations were created to understand the distribution of numerical features and relationships between various variables, such as `Item_Weight`.



### Conclusion
The developed models provide a foundation for predicting retail sales. The project can be extended with more sophisticated feature engineering, hyperparameter tuning, and model evaluation techniques.

### Requirements
- **Python 3.x**
- **Libraries:** numpy, pandas, seaborn, matplotlib, scikit-learn, xgboost

### Usage
Clone this repository and run the Jupyter Notebook to explore the data and models.

### Future Work
- Improve model performance with additional feature engineering.
- Experiment with different regression algorithms.
- Conduct hyperparameter tuning for optimal model settings.

