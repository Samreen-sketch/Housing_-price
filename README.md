# Housing_-price
Analysis of Housing Data

Dataset
The dataset is downloaded from Kaggle. This data includes the following characteristics:

Feature	Type
Price	Numerical
Area	Numerical
Bedrooms	Numerical
Bathrooms	Numerical
Stories	Numerical
Main road	Numerical
Guestroom	Numerical
Basement	Object
Hot-water heating	Object
Air conditioning	Object
Parking	Numerical
Prefer area	Object
Furnishing status	Object


Business Value of Housing Dataset Analyses:
Analyzing housing datasets can unlock valuable business insights that drive smarter decisions across real estate, construction, and investment sectors. Identifying undervalued properties, high-growth areas, and optimal rental pricing ensures profitable investments.
Most Commonly Used Model for Predicting Housing Price:
1.	Linear Regression
2.	Decision Tree Regressor
3.	Random Forest Regressor
4.	XGBoost
 
Why Choose Random Forest Regressor:
•	Reduces overfitting in decision trees.
•	Handles missing values, categorical data, and feature importance effectively.
# Import Libraries
This project uses Python with the following libraries:
-pandas, numpy: For data handling
- matplotlib, seaborn: For visualization
- scikit-learn: For machine learning (Random Forest Regressor, model evaluation)
  # Dataset
The project uses a dataset named `Housing.csv` containing housing-related features for prediction or analysis.
The data is loaded using `pandas.read_csv()` into a DataFrame.
![image](https://github.com/user-attachments/assets/4fb60e5d-058d-48af-9ae4-86299e0aefc1)
 # Data Preprocessing (using Wrangler)

The heart disease dataset (`hd.csv`) was loaded using `pandas.read_csv()`.

In **Wrangler**, string values such as `"Yes"` and `"No"` were converted to **Boolean** (`True`/`False`) to make the data machine learning-ready.

This preprocessing step ensures that all categorical values are in the correct format for analysis and model training.
![image](https://github.com/user-attachments/assets/1f87e33e-2fd1-406e-9a30-cd0619423ac0)Feature and Target Separation

# 	Separate features and target

- The feature variables (independent) were separated from the target variable (`price`).
- `pandas.drop()` was used to remove the `price` column from the features.
-  Train-Test Split

# To evaluate model performance:

- The dataset was split into training and testing sets using `train_test_split` from `scikit-learn`.
- 80% of the data was used for training and 20% for testing.
- `random_state=42` was set to ensure reproducibility.
# Model Initialization

A **Random Forest Regressor** from `scikit-learn` was used to predict housing prices.

- `n_estimators=100`: Uses 100 decision trees in the ensemble
- `max_depth=None`: No maximum tree depth (trees are fully grown)
- `random_state=42`: Ensures consistent and reproducible results during training

Random Forest was chosen for its ability to handle non-linear relationships and its robustness against overfitting
# Model Training

The `RandomForestRegressor` was trained using the `fit()` method with the training data:
![image](https://github.com/user-attachments/assets/ccd89171-09b7-47e0-852b-589f5e2ab7ff)
# Model Prediction and Evaluation

After training, the model was evaluated on the test dataset using the following metrics:
# Mean Absolute Error (MAE)

Measures the average magnitude of errors between predicted and actual values.
# Mean Percentage Absolute Error (MPAE)
Measures average error as a percentage, useful for understanding relative error
![image](https://github.com/user-attachments/assets/c1f57e90-3f7e-4acb-8c84-dd6ba38ce87d)
 # 	Visualization:
Correlation Map:
![image](https://github.com/user-attachments/assets/5737ca69-8f5c-4d37-a172-2cbf886f9214)
# Box Plot
# Preferred Area vs. Price
![image](https://github.com/user-attachments/assets/5e873365-84cc-4657-8630-eb9647676cb9)
i.	Most properties in desired locations cost between ~₹3.5M and ₹6.5M (35-65 lakhs).

ii.	The median price is approximately ₹4.5 million (45 lakhs).

There are a number of extreme outliers above ₹9M and even up to ₹13M (1.3 crores), suggesting a few luxury properties.

# 	Stories vs. Price
![image](https://github.com/user-attachments/assets/3b841a3c-7760-43ed-a033-768fa26b3bf6)
i.	The number of stories is an essential factor in predicting house prices.
ii.	Multi-story homes may be more valuable to buyers because of their size, improved views, or additional amenities.
iii.	Outliers indicate that there are some extremely expensive houses on the market, particularly in the two- and four-story categories.
# 	Bedrooms vs. Price
![image](https://github.com/user-attachments/assets/a3b18f10-8fc8-470c-b4c4-63da17d3fb65)
i.	Positive correlation between number of bedrooms and house price, up to 5 bedrooms.
ii.	With the highest number of outliers, properties with four or five bedrooms are priced significantly higher than average.
# Conclusion:
Mean Absolute Error (MAE): ₹11,25,108

This indicates that the average difference between the actual and model-predicted home values is about ₹11.25 lakhs.
Example:

In comparison to the actual prices, the model-predicted property prices are often wrong by about
₹11.25 lakhs.













- 




  
