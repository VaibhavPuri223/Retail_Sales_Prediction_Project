# Retail_Sales_Prediction_Project
Predict daily retail store sales using historical sales, promotion, holiday, store, assortment, and competition information.


Retail_Sales_Prediction_Project (1).ipynb
File
create readme  file for this project

I’ve created a README.md file for your Retail Sales Prediction project based on your Jupyter Notebook.

📄 Download your README file

📌 What's included?
Project overview and objectives

Dataset description

Tools and technologies used

Random Forest Regressor algorithm

Data cleaning and feature engineering

Model evaluation: MAE, RMSE, and R²

Instructions to install dependencies and run the notebook

Generated CSV output files

Business use cases and project limitations

📂 How to add it to GitHub
Download the README file.

Rename it to README.md if necessary.

Open your Retail Sales Prediction project repository on .

Click Add file → Upload files.

Upload README.md and commit the changes.

Important: Your notebook requires two CSV datasets: Salesdata-DS DATA.csv and store-DS DATA.csv. Make sure these files are available in your project folder before running the notebook. 



README_Retail_Sales_Prediction.md


Retail Sales Prediction Using Machine Learning
Project Overview
This project uses historical retail sales data and store-level information to predict daily sales for stores. It combines data cleaning, exploratory data analysis (EDA), date-based feature engineering, and a Random Forest Regressor model.

The project is designed to help retailers understand sales patterns and support planning for inventory, staffing, and promotions.

Objectives
Explore historical sales and store information.

Clean and merge sales and store datasets.

Analyze sales patterns across days, months, promotions, holidays, and store types.

Create calendar and competition-related features.

Train a Random Forest regression model to predict sales.

Evaluate predictions using MAE, RMSE, and R².

Generate store-wise predictions and save the output as CSV files.

Dataset
The notebook expects these two CSV files in the same directory as the notebook:

Salesdata-DS DATA.csv — daily store-level sales records.

store-DS DATA.csv — store characteristics and related information.

The target variable is Sales. The Store column is used to join the two datasets.

Note: The CSV datasets are required to run the notebook and are not included unless uploaded separately.

Tools and Technologies
Python

Jupyter Notebook

Pandas and NumPy

Matplotlib and Seaborn

Scikit-learn

Machine Learning Approach
The notebook uses a Random Forest Regressor.

Data preparation and features
The workflow includes:

Loading and inspecting the sales and store datasets.

Checking missing values and duplicate records.

Cleaning the data and merging the datasets using Store.

Exploring sales patterns with visualizations.

Extracting calendar features from Date, including year, month, day, week of year, quarter, and weekend indicator.

Preparing store, promotion, holiday, assortment, and competition-related features.

One-hot encoding selected categorical features.

Training and validating the model using a chronological split, with earlier observations for training and more recent observations for validation.

Customers is deliberately excluded from the model features because future customer counts may not be available when making a sales forecast. The notebook also models records where the store is open.

For faster training on large datasets, the notebook samples up to 200,000 training rows when needed, using a fixed random seed. The validation set remains untouched.

Model Evaluation
The notebook calculates these regression metrics:

MAE (Mean Absolute Error): Average absolute difference between actual and predicted sales. Lower is better.

RMSE (Root Mean Squared Error): Gives greater weight to larger prediction errors. Lower is better.

R² (Coefficient of Determination): Indicates how much variation in sales is explained by the model. Higher is generally better.

It also compares actual and predicted sales visually.

Outputs
After the notebook runs successfully, it saves:

store_wise_sales_predictions.csv — predicted sales by store and date.

model_comparison.csv — evaluation metrics for the Random Forest model.

The notebook also displays store-level prediction summaries, including predicted days, average predicted daily sales, and total predicted sales.

How to Run
Download or clone this project repository.

Place the notebook and both required CSV files in the same folder.

Install the required Python packages:

pip install numpy pandas matplotlib seaborn scikit-learn jupyter
Start Jupyter Notebook:

jupyter notebook
Open Retail_Sales_Prediction_Project (1).ipynb and run the cells from top to bottom.

Business Use Cases
Support inventory and replenishment planning.

Help managers plan staffing for expected demand.

Understand how promotions and holidays relate to sales.

Compare sales patterns across store types and time periods.

Review store-wise predicted sales for operational planning.

Limitations
Prediction quality depends on the quality and coverage of the supplied datasets.

The notebook's validation metrics should be reviewed before using predictions for business decisions.

Historical patterns may not capture unexpected events or sudden changes in customer behavior.

This is a notebook-based forecasting workflow, not a deployed production service.

Author
Vaibhav Puri

This project was developed for retail sales analysis and machine-learning practice.

