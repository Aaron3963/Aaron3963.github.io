---
title: 基于新闻标题情绪分析的 S&P 500 交易策略
weight: 50
summary: 使用自定义 Transformer 模型和来自多个来源的新闻标题，构建了一个针对 S&P 500 的交易策略，在 6 个月内获得了 10% 的收益。
tags:
  - 量化研究
  - 算法交易
  - 情绪分析
  - PyTorch
  - Scikit-learn

date: '2024-12-06'

# 项目的可选外部链接（会替代项目详情页）。
external_link: ''

image:
  caption: 我们的投资组合收益与基准表现的对比
  focal_point: Smart

links:
  - name: 完整项目
    url: https://aaron3963.github.io/CSE_151A_Project/

url_code: 'https://github.com/Aaron3963/CSE_151A_Project'
# url_pdf: ''
# url_slides:
# url_video: 
# Slides（可选）。
#   将此项目与 Markdown 幻灯片关联。
#   只需输入幻灯片文件名，不包含扩展名。
#   例如，`slides = "example-slides"` 会引用 `content/slides/example-slides.md`。
#   否则，将 `slides = ""`。
# slides: example
---
{{% callout note %}}
该项目已在线完全渲染，可在[这里](https://aaron3963.github.io/CSE_151A_Project/)查看。
{{% /callout %}}

在这个项目中，我们旨在构建一个能够根据每日新闻标题预测 S&P 500 指数上涨或下跌的模型。我们收集并分析了来自 CNBC、The Guardian 和 Reuters 的三年多新闻标题数据，时间跨度从 2017 年末到 2020 年中，并将其与对应的每日 S&P 500 交易数据结合。我们的探索性数据分析揭示了不同数据集规模的差异、标题中常见停用词占据主导，以及 2020 年初 COVID-19 导致的显著下跌；我们预计这些因素可能会影响模型表现。

我们首先使用基于 TF-IDF 特征的逻辑回归模型作为基准，其准确率仅约为 51%–55%。随后，我们实现了基于 Transformer 的分类器，并进行了大量超参数调优实验，包括调整注意力头数量、应用学习率衰减，以及测试多种文本预处理策略。表现最好的模型移除了停用词，并取得了 61.5% 的测试准确率——虽然提升有限，但高于随机猜测。

我们将该模型转化为一个量化交易策略：当模型预测市场偏空时做空市场。该策略在六个月内产生了超过 10% 的毛收益，显著优于简单的买入并持有策略。尽管结果令人鼓舞，但我们也承认，金融市场受到新闻情绪之外众多因素的影响。我们认为，未来使用 LSTM 或 BERT 等模型可能进一步提升预测表现。