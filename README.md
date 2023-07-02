# Black-Friday-Sales-Prediction-Regression-Analysis 👾

### Requirements

**The project was developed with:**
 - Jupyter notebook
 - Python
 - Matplotlib
 - Scikit-learn
 - pandas
 - numpy

### ✔ Purpose and Aim of This Assignment

- The goal is to predict the purchase amount of a customer based on various features given in  a dataset of sales transaction on Black Friday
Performing a regression analysis on this data set and improving base model by achieving the lowest RMSE.
- In order to achieve this task, we perform;
  - various data preprocessing, 
  - feature engineering steps,
  - trying different regression models 
- Hyperparameter tuning using grid search

### ✔ Data Preprocessing and Feature Engineering

- Checking first for null values in the data and filling the null values in the dataset.
- Converting the categorical attributes to numerical using a dictionary (label encoding). Either with the help of lambda function or with labelEncoder package as stated in notebook.
- In handling outliers’ part, the IQR method is used to detect and remove outliers from the Purchase column to get rid of outliers.
- Then, splitting the data for training. Purchase is an output data that is why it is uninvolved from X.
- Feature scaling helps to improve model's performance. Make sure that features are on the same scale.  Fit the transform using StandartScaler method with columns that contains numerical data.
- Lastly, randomly created two new attributes: Total_Products_by_User and Avg_Purchase_by_City. These will help to model task clearly. They provide additional features that capture information about each user's purchasing behavior and used as predictors.

### ✔ Regression Models

Four regression models are used:
- Decision Tree -> MSE: 3482.0864492025125
- ExtraTreesRegressor -> MSE: 3137.623884258123
- XGBRegressor -> MSE: 2795.779971892693
- LinearRegression -> MSE: 3624.547078823614

We know that the lowest MSE is capable of producing more accurate predictions on the dataset. So, XGBRegressor is performing the best.


### ✔ Model Tuning and Performance

- The base model provided to us had an RMSE score of 3061.42. 
- In the model tuning part of my notebook, I have used XGB as an model and defined the hyperparameters to search over using GridSearchCV like model’s max depth, learning rate and min child weight. 
- Best parameters became 0.5, 7, 50, respectively.
- RMSE is 2768.1450270884225 which shows that base model’s score is improved.



