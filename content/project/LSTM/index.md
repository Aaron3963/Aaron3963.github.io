---
title: Attention LSTM for Stock Price Prediction
weight: 10
summary: Paper about combining LSTM with Self-Attention mechanism for predicting Nvidia stock prices.
tags:
  - Quant Research
  - Deep Learning
  - LSTM
  - Transformer
  - PyTorch

date: '2025-06-14'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Custom LSTM Cell
  focal_point: Smart

# links:
#   - name: Full Project
#     url:

url_code: 'https://github.com/Aaron3963/LSTMs_for_Stock_Prediction/'
url_pdf: 'uploads/Attention_LSTM_for_Stock_Forecasting_Using_Macro_and_Commodity_Features.pdf'
# url_slides:
# url_video: 
---

In this project paper, I proposed an LSTM model with a self-attention mechanism for predicting individual stock prices, specifically targeting Nvidia (NVDA). My motivation was to improve upon traditional LSTMs by integrating the attention mechanism's ability to dynamically weight important time steps, which helps capture long-term dependencies that standard LSTMs often miss. I also emphasized the importance of feature engineering, incorporating not just OHLCV data but also macroeconomic indicators and commodity prices—such as lithium, copper, and gold—that are relevant to Nvidia's supply chain.

My experiments compared three models: a baseline LSTM, a variant derived from AMV-LSTM, and my proposed Attention LSTM. While the variant performed best on training data with an F1 score of 0.891, it severely overfitted and collapsed on the test set with a score of only 0.094. In contrast, my Attention LSTM achieved the highest test F1 score of 0.629, outperforming the baseline by 2% and demonstrating better generalization. I also found that models trained with only OHLCV data performed no better than random guessing, confirming that multi-dimensional features are crucial for this task.

I conclude that combining LSTM with attention mechanisms offers a promising direction for stock forecasting, particularly when augmented with diverse macroeconomic and commodity data. Future work could explore deeper attention-augmented architectures and incorporate semantic information like news sentiment to further enhance predictive performance.