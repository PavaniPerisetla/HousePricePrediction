# HousePricePrediction
🏠 House Price Prediction (Linear Regression)

This project implements a Linear Regression model to predict house prices based on features such as square footage (GrLivArea), number of bedrooms (BedroomAbvGr), and number of bathrooms (TotalBathrooms).
The dataset is based on the Kaggle House Prices - Advanced Regression Techniques competition.

📂 Project Structure
.
├── train.csv              # Training dataset (includes SalePrice)
├── test.csv               # Test dataset (no SalePrice)
├── sample_submission.csv  # Submission format from Kaggle
├── house_price.ipynb      # Jupyter/Colab notebook with code
└── README.md              # Project documentation

🚀 Workflow
Load and explore data
Train dataset contains house features + SalePrice (target).
Test dataset contains house features without SalePrice.

Feature selection
We use the following features:
GrLivArea → Above-ground living area (square feet)
BedroomAbvGr → Number of bedrooms above ground
TotalBathrooms → Total number of bathrooms (Full + Half + Basement)

Preprocessing
Handle missing values (e.g., fill NaN with median).
Select numerical features for regression.

Model training
Train a Linear Regression model using Scikit-learn.
Evaluate with Mean Squared Error (MSE) and R² Score.

Prediction & Submission
Use the trained model to predict house prices on test.csv.
Save results into my_submission.csv for Kaggle submission.

📊 Results
Evaluation Metrics (on validation set):
Mean Squared Error: ~2.62e9
R² Score: ~0.65

Example Predictions:

Id   GrLivArea  BedroomAbvGr  TotalBathrooms   PredictedPrice
1    1710       3             2.0             216927.60
2    1262       3             2.0             187340.12
3    1786       3             2.5             204560.77

📦 Requirements

Install the following dependencies:
pip install pandas numpy scikit-learn matplotlib seaborn

▶️ Usage

Clone the repository:

git clone https://github.com/PavaniPerisetla/HousePricePrediction.git
cd HousePricePrediction


Run the notebook:

Open HousePricePrediction.ipynb in Jupyter Notebook or Google Colab.

Generate predictions:

submission.to_csv("my_submission.csv", index=False)

Submit my_submission.csv to Kaggle.

📌 Future Improvements

Add more features (e.g., YearBuilt, OverallQual)
Try advanced models (Ridge, Lasso, Random Forest, Gradient Boosting)
Perform hyperparameter tuning
Feature engineering (log-transform skewed data, interaction terms)

🏅 Acknowledgements

Dataset: Kaggle House Prices Competition
Libraries: Pandas, NumPy, Scikit-learn
