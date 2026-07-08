---
title: News Headline Based S&P500 Trading Strategy
weight: 50
summary: Used a custom transformer model and news headlines from various sources to make a trading strategy on S&P500. Back test results got 10% profit within 6 month.
tags:
  - Quant Research
  - Algorithmic Trading
  - Transformer
  - Sentiment Analysis
date: '2024-12-06'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Return of our portfolio compared with default
  focal_point: Smart

links:
  - name: Full Project
    url: https://aaron3963.github.io/CSE_151A_Project/

url_code: 'https://github.com/Aaron3963/CSE_151A_Project'
# url_pdf: ''
# url_slides:
# url_video: 
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---
{{% callout note %}}
This project is fully rendered online that can be found [here](https://aaron3963.github.io/CSE_151A_Project/).
{{% /callout %}}

In this project, we aimed to build a model capable of predicting whether the S&P 500 index would rise or fall based on daily news headlines. We collected and analyzed over three years of headlines from CNBC, The Guardian, and Reuters, spanning from late 2017 to mid-2020, and combined them with corresponding daily S&P 500 trading data. Our exploratory data analysis revealed varying dataset sizes, common stop words dominating headlines, and a significant COVID-19 dip in early 2020 that we anticipated might impact our model's performance.

We began with a logistic regression baseline using TF-IDF features, which achieved only around 51-55% accuracy. We then implemented Transformer-based classifiers and experimented extensively with hyperparameter tuning, including adjusting attention heads, applying learning rate decay, and testing various text preprocessing strategies. Our best-performing model, which removed stop words, achieved a 61.5% test accuracy—modest but above random guessing.

We translated this model into a quantitative trading strategy that used bearish predictions to short the market, generating over 10% gross profit in six months, significantly outperforming a simple buy-and-hold approach. While our results are encouraging, we acknowledge that financial markets are influenced by numerous factors beyond news sentiment, and we believe future work with LSTMs or BERT could further improve performance.