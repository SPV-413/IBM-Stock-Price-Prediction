# IBM Stock Price Prediction (Time Series Forecasting)
This project focuses on time series forecasting for predicting IBM stock prices using machine learning models. The dataset includes historical stock prices up to December 2023. Accurate predictions can assist investors, financial analysts, and traders in making informed decisions, optimizing trading strategies, and managing risks. Additionally, this project serves as a practical application of machine learning in finance, demonstrating the effectiveness of different predictive models while providing insights into stock market behavior.

## Dataset Overview
- **Source**: IBM
- **Rows**: 5282
- **Columns**: 7  (including the target variable)
- **Target Variable**:
  - **Close** (The final price of the stock at the end of the time period)
- **Features**:
  - **Date** (The timestamp representing when the stock price data was recorded)
  - **Open** (The price at which the stock starts trading at the beginning of the time period)
  - **High** (The highest price the stock reached during the time period)
  - **Low** (The lowest price the stock dropped to during the time period)
  - **Adj Close** (The adjusted closing price after considering corporate actions like dividends or stock splits)
  - **Volume** (The total number of shares traded during the time period, indicating market activity)

## Project Workflow
### 1. **Feature Engineering**
- convert the date column to datetime format and set it as the index
- Sorting the index
- Checking missing values
- Checking duplicates
- Identifying & Handling the outliers
  - Boxplot & Winsorize
- Feature scaling (`StandardScaler`)
- Splitting dataset into training & testing sets (`train_test_split`)

### 2. **Machine Learning Models**
The project implements multiple machine learning models & one deep learning model for regression:
- **XGBoost Regressor**
- **SVR**
- **KNeighborsRegressor**
- **Multi-layer Perceptron (MLP) Regressor**

### 3. **Model Evaluation**
- **R2 Score**
- **Mean Squared Error**       
- **Mean Absolute Error**
- **Root Mean Squared Error**
- **cross_val_score** (To check overfitting)

## Installation & Usage

### Prerequisites
Ensure you have the following installed:
- Python 3.10 and above
- Jupyter Notebook
- Required libraries (`pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`)

### Running the Notebook
1. Clone the repository:
   git clone https://github.com/SPV-413/IBM-Stock-Price-Prediction.git
2. Navigate to the project folder:
   cd IBM-Stock-Price-Prediction
3. Open the Jupyter Notebook:
   jupyter notebook IBM Stock Price Prediction.ipynb

## Results
- For this specific dataset and task, the **XGBoost Regressor** is the most effective model. Suggests it captures the underlying patterns in the data most accurately.
- XGBoost Regressor model achieving a 97% R-squared score on IBM stock price prediction (up to December 2023) without overfitting, and the plot of actual vs predicted values shows a very close alignment.

## Contact
For any inquiries, reach out via GitHub or email.






