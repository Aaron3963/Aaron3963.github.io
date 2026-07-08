---
title: Machine Learning Factor Backtest Pipeline
weight: 10
summary: An all-in-one backtesting pipeline that allows users to test simple algorithmic trading strategies with ease.
tags:
  - Quant Development
  - Backtest
  - Backtrader
  - Python
date: '2025-12-30'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Cover of our presentation
  focal_point: Smart

links:
  - name: Backtest Results
    url: https://aaron3963.github.io/SimpBackTest/
url_code: 'https://github.com/Aaron3963/SimpBackTest'
# url_pdf: 
# url_slides:
# url_video:
---

This project is a backtesting pipeline that allows users to test simple algorithmic trading strategies with ease. It contains all necessary steps for backtesting, including data fetching, feature generation, model selection, signal creation, and report generation. The project is highly modularized and compatible with sklearn and pandas, so users can modify or import strategies without overhead.

Trading signals are saved and loaded to Backtrader for backtesting, and quantStats is responsible for generating an HTML report that contains all testing metrics and graphs like the one below. There is also an automated Action workflow that generates a [static webpage](https://aaron3963.github.io/SimpBackTest/) which contains all the reports generated.