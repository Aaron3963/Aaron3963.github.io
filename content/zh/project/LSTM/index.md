---
title: 用于股票价格预测的 Attention LSTM 模型
weight: 10
summary: 一篇关于结合 LSTM 与自注意力机制来预测英伟达股票价格的结课论文。
tags:
  - 量化研究
  - 深度学习
  - LSTM
  - Transformer
  - PyTorch

date: '2025-06-14'

# 项目的可选外部链接（会替代项目详情页）。
external_link: ''

image:
  caption: 改良版 LSTM 单元
  focal_point: Smart

# links:
#   - name: 完整项目
#     url:

url_code: 'https://github.com/Aaron3963/LSTMs_for_Stock_Prediction/'
url_pdf: 'uploads/Attention_LSTM_for_Stock_Forecasting_Using_Macro_and_Commodity_Features.pdf'
# url_slides:
# url_video: 
---

在这篇项目论文中，我提出了一种结合自注意力机制的 LSTM 模型，用于预测个股价格，具体目标为英伟达（Nvidia，NVDA）。我的动机是通过引入注意力机制动态赋予重要时间步更高权重，从而改进传统 LSTM，并帮助模型捕捉标准 LSTM 往往难以充分识别的长期依赖关系。我也强调了特征工程的重要性，不仅纳入 OHLCV 数据，还加入了与英伟达供应链相关的宏观经济指标和大宗商品价格，例如锂、铜和黄金。

我的实验比较了三种模型：基准 LSTM、一个源自 AMV-LSTM 的变体，以及我提出的 Attention LSTM。尽管该变体在训练集上表现最好，F1 分数达到 0.891，但它出现了严重过拟合，并在测试集上崩溃，F1 分数仅为 0.094。相比之下，我的 Attention LSTM 取得了最高的测试集 F1 分数 0.629，比基准模型高出 2%，并展现出更好的泛化能力。我还发现，仅使用 OHLCV 数据训练的模型表现并不优于随机猜测，这进一步证明了多维特征对于该任务至关重要。

我的结论是，将 LSTM 与注意力机制结合，为股票预测提供了一个有前景的方向，尤其是在引入多样化的宏观经济与大宗商品数据后。未来工作可以探索更深层的注意力增强架构，并纳入新闻情绪等语义信息，以进一步提升预测表现。