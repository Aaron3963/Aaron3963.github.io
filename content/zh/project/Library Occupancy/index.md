---
title: 图书馆人流量与天气分析
weight: 10
summary: 一个数据科学项目，旨在探索 UCSD Geisel 图书馆和 WongAvery 图书馆的人流量趋势，并尝试回答天气是否会影响人们前往图书馆的意愿。
tags:
  - 数据科学
  - 数据可视化
  - Scikit-learn
  - Pandas
  - Seaborn

date: '2023-12-01'

# 项目的可选外部链接（会替代项目详情页）。
external_link: ''

image:
  caption: 我们展示文稿的封面
  focal_point: Smart

links:
  - name: 完整项目
    url: https://aaron3963.github.io/COGS-108-Project/

url_code: 'https://github.com/Aaron3963/COGS-108-Project'
# url_pdf: 
# url_slides:
url_video: 'https://youtu.be/s202-BIAFj8'
---

{{% callout note %}}
该项目已在线完全渲染，可在[这里](https://aaron3963.github.io/COGS-108-Project/)查看。
{{% /callout %}}

在这个项目中，我们研究了天气条件是否会影响 UCSD 图书馆的学生人流量模式，具体分析对象为 Geisel 图书馆和 WongAvery 图书馆。我们将图书馆的小时级入口计数数据与 NOAA La Jolla 气象站的天气数据相结合，覆盖时间为 2022-2023 学年。在进行了大量数据清洗、去除异常值、周末以及夜间时段后，我们将两个数据集合并用于分析。

我们的探索性分析揭示了一些有趣的模式：Geisel 图书馆的人流量在整个学期内相对稳定，即使在期末考试周也没有出现明显激增——这与普遍认知相反。我们还发现，周五和周末的人流量始终较低。在研究气温与图书馆访问量之间的关系时，我们观察到秋季学期和春季学期存在较弱但为正的线性相关关系，这表明较温和的天气可能会鼓励更多学生前往图书馆。然而，冬季学期并未表现出明确关系，因为学生似乎无论气温如何都会前往图书馆。

总体而言，虽然我们找到了一些证据支持“天气会影响图书馆人流量”这一假设，但这种关系较为有限。许多其他因素——例如学术日程、期中考试以及个人学习习惯——可能发挥着更重要的作用。我们还发现 WongAvery 数据存在质量问题，并将其从最终分析中排除，这也强调了未来工作中进行稳健数据收集的重要性。