# Univariate LSTM Stock Prediction Model

## Project Overview
This project demonstrates the application of a univariate Long Short-Term Memory (LSTM) model to predict stock prices using historical closing price data. The model utilizes the closing prices from the previous three days to predict the next day's closing price of a stock.

## Goal
The aim of this project is to explore the effectiveness of LSTM networks in capturing the temporal dependencies of stock price movements. This can provide insights into potential future trends based on historical data, which is crucial for making informed investment decisions.

### Data Source
The stock price data was obtained from Yahoo Finance's historical data section for NVIDIA Corporation (NVDA), which can be accessed [here](https://finance.yahoo.com/quote/NVDA/history). To explore other stocks, simply navigate to Yahoo Finance, search for the desired company under the "Quote Lookup" feature, and download the historical stock data from the 'Historical Data' tab for that specific stock. Replace the dataset in the project with your chosen stock data to run new predictions.

## Model Details
- **Model Type**: Univariate LSTM
- **Input**: Previous three days' closing prices
- **Output**: Predicted closing price for the next day

### Model Architecture
The model is structured as follows:
- **Input Layer**: Accepts input shape of (3, 1) which corresponds to 3 days of stock prices.
- **LSTM Layer**: A Long Short-Term Memory layer with 64 units.
- **Dense Layers**:
  - First Dense layer with 32 neurons and ReLU activation.
  - Second Dense layer also with 32 neurons and ReLU activation.
  - Third Dense layer with 16 neurons and ReLU activation.
- **Output Layer**: A single neuron with a linear activation function to predict the next day's closing price.
- **Compilation**: The model is compiled with the Mean Squared Error (MSE) loss function and uses the Adam optimizer with a learning rate of 0.001. Metrics include mean absolute error.

## Libraries and Tools
- Python
- Keras
- TensorFlow
- Pandas
- NumPy
- Matplotlib (for visualization)
