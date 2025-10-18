# House Price Prediction

This project is an end-to-end machine learning solution for predicting house prices. It involves data cleaning, exploratory data analysis (EDA), feature engineering, model comparison, and final model deployment.

The primary goal is to build a regression model that accurately predicts the **totalprice** of a property based on its features, such as location, size (sqft), and number of bedrooms (BHK).

## Project Workflow

  1.  **Data Loading:** The dataset (**HouseDetails.csv**) is loaded into a **pandas** DataFrame.
  2.  **Exploratory Data Analysis (EDA):**
          * Analyzed data types, checked for missing values, and examined the unique values for each feature.
          * Visualized the distribution of the target variable (`**totalprice**) using a histogram.
          * Used a boxplot to understand the relationship between the number of **bhk** and the **totalprice**.
  3.  **Data Preprocessing:**
          * **Encoding:** Categorical features (**propertytype** and **location**) were converted into numerical values using **sklearn.preprocessing.LabelEncoder**.
          * **Feature Scaling:** All features were normalized using **sklearn.preprocessing.StandardScaler** to ensure that all variables contribute equally to the model's performance.
  4.  **Model Training & Evaluation:**
          * The dataset was split into training (80%) and testing (20%) sets.
          * Five different regression models were trained and compared:
              * Linear Regression
              * K-Neighbors Regressor
              * Decision Tree Regressor
              * Random Forest Regressor
              * Gradient Boosting Regressor
          * Models were evaluated using **Mean Absolute Error (MAE)**, **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, and **R² Score**.
  5.  **Results:**
          The **Gradient Boosting Regressor** provided the best performance on the test set.
  
  6.  **Model Saving:**
          The best-performing model (**GradientBoostingRegressor**), the **StandardScaler**, and the **LabelEncoders** were saved using **joblib** for future use in a prediction pipeline.

## Technologies Used

  * Python
  * Pandas
  * NumPy
  * Scikit-learn
  * Matplotlib
  * Seaborn
  * Jupyter Notebook
  * Joblib
