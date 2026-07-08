---
title: 机器学习因子回测平台
weight: 10
summary: 一个一体化回测管线，使用户能够轻松测试简单的由机器学习算法生成因子生成量化交易策略。
tags:
  - 量化开发
  - 回测
  - Scikit-learn
  - Backtrader

date: '2025-12-30'

# 项目的可选外部链接（会替代项目详情页）。
external_link: ''

image:
  caption: 报告示例
  focal_point: Smart

links:
  - name: 回测结果
    url: https://aaron3963.github.io/SimpBackTest/
url_code: 'https://github.com/Aaron3963/SimpBackTest'
# url_pdf: 
# url_slides:
# url_video:
---

该项目是一个回测流水线，使用户能够轻松测试简单的算法交易策略。它包含回测所需的所有必要步骤，包括数据获取、特征生成、模型选择、信号生成和报告生成。该项目高度模块化，并兼容 sklearn 和 pandas，因此用户可以在几乎没有额外负担的情况下修改或导入策略。

交易信号会被保存并加载到 Backtrader 中进行回测，而 quantStats 负责生成 HTML 报告，其中包含所有测试指标以及如下所示的图表。此外，项目还包含一个自动化的 GitHub Actions 工作流，用于生成一个[静态网页](https://aaron3963.github.io/SimpBackTest/)，其中汇总了所有生成的报告。