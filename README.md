# Ethereum-Price-Prediction
Developed an LSTM-based predictive model to forecast Ethereum prices using historical data (2018–2024). Preprocessed and scaled data for effective time series modeling. Trained the model to predict price trends for 60 days. Visualized historical trends and predictions to evaluate accuracy and uncover key patterns.


# Ethereum Price Prediction with LSTM

This project uses machine learning to predict Ethereum prices based on historical data. The primary model is an LSTM (Long Short-Term Memory) network designed to capture sequential dependencies in time-series data.

## Table of Contents

1. [Introduction](#introduction)  
2. [Dataset](#dataset)  
3. [Data Preprocessing](#data-preprocessing)  
4. [Model Architecture](#model-architecture)  
5. [Training the Model](#training-the-model)  
6. [Evaluation](#evaluation)  
7. [Future Price Predictions](#future-price-predictions)  
8. [Results](#results)

---

## Introduction

This project explores the use of deep learning for financial forecasting. The Ethereum price data is analyzed, preprocessed, and modeled using an LSTM network. The goal is to predict future price trends and provide insights into the cryptocurrency market.

---

## Dataset

- **Source**: Ethereum daily price data (2018-2024).  
- **Columns**: `time`, `Open`, `High`, `Low`, `Close`, etc.  
- Data includes historical closing prices for Ethereum, which are used as the primary feature.

---

## Data Preprocessing

1. **Datetime Conversion**: The `time` column is converted to `datetime` and set as the index.  
2. **Visualization**: A plot of historical Ethereum closing prices.  
3. **Scaling**: The `Close` prices are scaled using Min-Max scaling for input to the LSTM model.  
4. **Sequence Generation**: Sequences of 60 days are created as input for the LSTM model.

---

## Model Architecture

The LSTM network consists of the following layers:

1. Input Layer: Accepts sequences of 60 days.  
2. Two LSTM Layers: With 50 units and dropout for regularization.  
3. Dense Layers: For output prediction.  
4. Optimizer: Adam optimizer with Mean Squared Error loss function.

---

## Training the Model

- **Training-Validation Split**: 80% training and 20% testing.  
- **Hyperparameters**:  
  - Epochs: 70  
  - Batch Size: 84  

The model is trained and validated using scaled data sequences.

---

## Evaluation

- **Metrics**: Mean Squared Error (MSE).  
- **Visualization**: Comparison of actual vs. predicted Ethereum prices.  

---

## Future Price Predictions

- **Horizon**: Predict the next 60 days of Ethereum prices.  
- **Method**: Sequential predictions using the trained LSTM model.  
- **Visualization**: Plot actual, predicted, and future prices.

---

## Results

| Metric                  | Value              |
|-------------------------|--------------------|
| Total Data Points       | *X*               |
| Training Data Points    | *Y*               |
| Testing Data Points     | *Z*               |
| Mean Squared Error (MSE)| *MSE Value*       |
| First Actual Price      | *Actual Start*    |
| First Predicted Price   | *Predicted Start* |
| Last Actual Price       | *Actual End*      |
| Last Predicted Price    | *Predicted End*   |
| Predicted Future Price  | *Future Price*    |

---

## Visualization

### Historical vs Predicted Prices
- Plot comparing actual and predicted prices for the test dataset.

### Future Price Predictions
- Plot extending predictions 60 days into the future.

---

