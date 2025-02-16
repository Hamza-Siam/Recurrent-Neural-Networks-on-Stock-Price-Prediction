# Recurrent Neural Networks on Stock Price Prediction

* <h4><b> Overview </b></h4> 

  In this project, the application of Recurrent Neural Networks (RNNs) for stock price prediction is explored using historical stock data of AMP (ASX). The project focuses on building and evaluating three types of RNN architectures: the traditional RNN, Long Short-Term Memory (LSTM), and Gated Recurrent Units (GRU). Each model is trained to predict the stock's closing prices using the past 60 days of data. The models are then tested on recent data, with performance assessed using Mean Squared Error (MSE). The findings provide a comparison of the prediction accuracy between the three models, with visualizations showing the predicted stock prices against the actual values. The project demonstrates the potential of RNN-based architectures in time series forecasting, while also highlighting the challenges of predicting highly volatile stock prices. 

* <h4><b> Key Findings </b></h4> 

  - <b> RNN, LSTM, and GRU models all predict stock prices: </b> The three models—RNN, LSTM, and GRU—were able to predict AMP stock prices based on historical data, but with varying levels of accuracy. Each model was able to approximate stock price movements, but the LSTM and GRU generally performed better due to their ability to capture long-term dependencies.
  - <b> RNN model struggles with long-term dependencies: </b> The traditional RNN model faced difficulties in learning long-term dependencies within the stock price data. This was reflected in the relatively higher Mean Squared Error (MSE) compared to LSTM and GRU models.
  - <b> LSTM model offers improved prediction accuracy: </b> The LSTM model performed significantly better than the RNN model, showing a lower MSE. This is likely due to LSTM's ability to handle long-term dependencies more effectively through its gating mechanism, improving stock price forecasting.
  - <b> GRU model provides comparable results to LSTM: </b> The GRU model, with fewer parameters than LSTM, showed similar performance to LSTM. It was able to predict stock prices with accuracy close to the LSTM model while being computationally more efficient.
  - <b> Test data predictions align with actual stock trends: </b> All three models showed reasonable alignment between predicted and actual stock prices during the test phase, with the GRU and LSTM models providing predictions that followed the actual stock price trend more closely, especially during volatile periods.
 
* <h4><b> Insightful Details </b></h4> 

  - <b> Data Preprocessing for Stock Price Input – </b> The code uses MinMaxScaler to normalize stock prices within the range of 0 to 1. This scaling technique ensures that the RNN models receive inputs within a consistent range, improving the model's ability to learn efficiently and avoid issues related to differing feature scales.
  - <b> Sliding Window for Time-Series Prediction – </b> The project implements a sliding window approach (using the past 60 days) to create input features for the models. This allows the models to learn patterns based on previous stock prices, which is crucial for time-series forecasting like stock prices.
  - <b> Dropout Regularization to Avoid Overfitting – </b> Dropout layers are included in all three models (RNN, LSTM, GRU) with a rate of 0.2. This helps prevent overfitting by randomly setting some neuron outputs to zero during training, forcing the model to generalize better and not memorize the training data.
  - <b> Model Comparison Through MSE Evaluation – </b> The Mean Squared Error (MSE) is used as the primary metric for model evaluation. By comparing the MSE values of RNN, LSTM, and GRU, the project provides clear insights into the prediction accuracy of each model. Lower MSE values correlate with better predictive performance, highlighting the strengths of LSTM and GRU.
  - <b> Prediction Visualization for Model Comparison – </b> The code generates plots comparing actual stock prices with the predicted prices from all three models. This visualization helps assess how well the models track stock price trends, and it is especially useful for understanding the impact of using different RNN architectures (RNN, LSTM, GRU) in capturing stock market behavior.
  
* <h4><b> Challenges </b></h4> 

   - <b> Difficulty in Capturing Long-Term Dependencies – </b> Despite using RNNs, the models may struggle with capturing long-term dependencies in the stock price data due to the vanishing gradient problem. This makes it hard for traditional RNNs to learn patterns over long sequences, requiring more complex models like LSTM and GRU to handle longer time horizons more effectively.
   - <b> Overfitting Risk with Small Training Data – </b> With the sliding window approach, the model is trained on a limited set of data (60 past days), which can cause overfitting. The model might memorize patterns from the training set and perform poorly on unseen data, especially when the training data is small compared to the variability of the stock market.
   - <b> Noise in Stock Market Data – </b> Stock prices are often noisy and affected by many external factors (such as economic events, market sentiment, etc.) that are difficult to capture with time-series models. The presence of such noise complicates model training, as it can lead to inaccurate predictions despite well-constructed models.
   - <b> Choice of Model Architecture and Hyperparameters – </b> Tuning the hyperparameters (e.g., number of units, number of layers, learning rate, batch size) can be challenging, as these choices have a significant impact on model performance. Determining the optimal architecture for stock price prediction requires experimentation, and improper tuning can result in models that underperform.
   - <b> Scaling Issues in Real-Time Prediction – </b> While the model works well on historical data, applying it to real-time stock price prediction can be difficult due to the need for constant updates to input data. Real-time scaling and managing batch updates (especially with stock market fluctuations) can be computationally expensive and time-sensitive, limiting the model's practical application.

* <h4><b> Data Files </b></h4> 

  - <b> Dataset for the project – </b> Downloaded from Yahoo Finance for AMP.AX from 2000-01-01 to 2020-06-01
  - <b> Code for the project – </b> [View Code](https://github.com/Hamza-Siam/Hamza-Siam/blob/main/Recurrent%20Neural%20Networks%20on%20Stock%20Price%20Prediction.pdf)
