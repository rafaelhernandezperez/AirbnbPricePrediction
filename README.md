🏠 Airbnb Price Prediction

A machine learning project exploring the Spanish short-term rental market and developing a predictive model for Airbnb listing prices.

The project combines exploratory data analysis, geographic and market analysis, feature engineering, statistical testing and machine learning to understand the factors influencing rental prices and predict listing prices based on property and market characteristics.

🎯 Objectives

The project focuses on several key questions:

* What factors have the greatest influence on Airbnb listing prices?
* How do prices differ across Spanish cities and regions?
* How do property characteristics, location and host attributes affect pricing?
* Can machine learning be used to accurately predict the price of an Airbnb listing?

🌍 Markets Analyzed

The exploratory analysis covers Airbnb listings across several Spanish destinations:

* Barcelona
* Madrid
* Málaga
* Mallorca
* Menorca
* Valencia
* Euskadi

Barcelona was selected as the primary market for developing and evaluating the machine learning model.

🔎 Exploratory Data Analysis

The project performs extensive exploratory analysis of the Airbnb datasets, including:

* Dataset structure and data-quality analysis
* Missing-value detection
* Duplicate analysis
* Price distribution analysis
* Outlier detection and treatment
* Property and room-type comparisons
* Geographic analysis of listings
* Host characteristics
* Review and rating analysis
* Correlation between listing characteristics and price
* Comparison of market characteristics across Spanish cities

Geospatial analysis and interactive maps were also used to explore how listing location relates to pricing.

⚙️ Data Preprocessing & Feature Engineering

The raw Airbnb data required several transformations before being suitable for machine learning.

The preprocessing workflow includes:

* Removal of irrelevant and high-dimensional variables
* Missing-value handling
* Price conversion and normalization
* Outlier treatment
* Conversion of percentage variables
* Transformation of date variables into numerical features
* Encoding of categorical variables
* Numerical feature scaling
* Feature selection

A Scikit-learn pipeline was used to ensure consistent preprocessing during model training and evaluation.

🤖 Machine Learning

Two regression approaches were initially evaluated:

Random Forest Regressor

An ensemble tree-based model capable of capturing nonlinear relationships between listing characteristics and price.

Support Vector Regression

A regression implementation of Support Vector Machines used as an alternative approach for comparison.

Both models were evaluated using cross-validation before selecting the best-performing approach.

🏆 Model Selection

The Random Forest Regressor substantially outperformed Support Vector Regression during cross-validation and was selected for further optimization.

Initial Random Forest cross-validation performance:

* R²: ~0.71
* MAE: ~35.1
* MSE: ~3,445

Feature importance was subsequently analyzed to identify which variables contributed most strongly to price predictions.

🔧 Hyperparameter Optimization

The Random Forest model was optimized using RandomizedSearchCV with 5-fold cross-validation.

The search explored combinations of:

* Number of estimators
* Maximum tree depth
* Minimum samples required to split a node
* Minimum samples per leaf

The best configuration identified was:

n_estimators: 200
max_depth: 30
min_samples_split: 6
min_samples_leaf: 1

📊 Final Performance

After hyperparameter optimization, the Random Forest achieved the following performance on the held-out test dataset:

Metric	Result
MAE	33.50
MSE	3,058.09
RMSE	55.30
R²	0.737
Explained Variance	0.737

The model therefore explains approximately 74% of the variance in Airbnb listing prices in the test dataset.

💡 Key Insights

The analysis highlights the importance of combining multiple types of information when estimating short-term rental prices.

Property characteristics, geographic location, accommodation capacity, host attributes and listing characteristics all contribute to price differences.

The results also demonstrate that tree-based ensemble methods such as Random Forest can effectively capture nonlinear relationships within rental-market data.

🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* SciPy
* Statsmodels
* Folium
* GeoPy
* Jupyter Notebook


📚 Context

This project was developed as an academic data science project focused on applying exploratory data analysis, statistical techniques and supervised machine learning to a real-world pricing problem.
