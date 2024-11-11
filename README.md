# predict-FOREX-with-ML-Logistic-Regression
for step1 I've used logistic regression 

# EURUSD Price Prediction with Logistic Regression

This project demonstrates a simple machine learning model for predicting price movement (up or down) of the EUR/USD currency pair using logistic regression. The model is trained on historical data and predicts whether the price will increase or decrease based on recent features.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Requirements](#requirements)
- [Usage](#usage)
- [Model Evaluation](#model-evaluation)
- [Output](#output)

## Project Overview

The objective of this project is to create a binary classification model that predicts whether the EUR/USD exchange rate will go up or down based on historical OHLC (Open, High, Low, Close) and Volume data.

## Data Source

The model uses historical data for the EUR/USD currency pair, which is downloaded using the `yfinance` library from Yahoo Finance.

- **Data Range**: January 1, 2020 - January 1, 2023
- **Features**: Open, High, Low, Close, and Volume
- **Target**: Binary target indicating price movement (1 for up, 0 for down)

## Requirements

To run this project, you need the following Python libraries:

```bash
pip install yfinance pandas numpy scikit-learn
```

## Usage

1. **Clone the Repository**:

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. **Run the Script**:

   Execute the script in your preferred environment to download the data, train the model, and evaluate its performance.

   ```python
   python eurusd_prediction.py
   ```

### Code Description

1. **Data Download**:
   - The script downloads EUR/USD data from Yahoo Finance for the specified date range.

2. **Feature Engineering**:
   - Calculates daily price change and assigns a binary target (`1` if the price went up, `0` otherwise).

3. **Model Training**:
   - Splits the data into training and testing sets (80-20 split).
   - Trains a logistic regression model on the training data.

4. **Model Evaluation**:
   - Evaluates model performance using accuracy, classification report, and confusion matrix.
   - Provides a prediction for the latest available data point.

## Model Evaluation

The model’s performance is evaluated with metrics such as:

- **Accuracy**: The overall accuracy of the model on the test set.
- **Classification Report**: Precision, recall, and f1-score for both classes.
- **Confusion Matrix**: Confusion matrix of true vs. predicted labels.

### Example Evaluation

```
Accuracy: 0.51
Classification Report:
               precision    recall  f1-score   support

           0       0.50      0.99      0.67        78
           1       0.75      0.04      0.07        79

Confusion Matrix:
 [[77  1]
 [76  3]]
```

## Output

After running the script, the output includes the model's accuracy, a classification report, and the confusion matrix. Additionally, a prediction for the latest data point is made, indicating if the price is expected to go "Up" or "Down".


