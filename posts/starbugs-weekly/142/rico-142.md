---
title: 第 142 期 DevOps 推薦文章
date: 2022-07-26
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How Prometheus Querying Works (and Why You Should Care)](https://www.timescale.com/blog/how-prometheus-querying-works-and-why-you-should-care/)

深入 Prometheus 如何查詢資料細節的文章，本文是基於 2022 年歐洲 Prometheus Day 演講做的延伸，裡面有影片可以參考。從 Prometheus data model 以及 indexing 策略到最後的執行查詢，執行查詢有一步一步拆解整體的流程。<!-- summary -->

### [Prometheus vs. OpenTelemetry Metrics: A Complete Guide](https://www.timescale.com/blog/prometheus-vs-opentelemetry-metrics-a-complete-guide/)

究竟要使用 Prometheus 還是 OpenTelemetry 呢？本文給了詳盡的建議。此篇是系列文的最後一篇比較文，有興趣可以看前面兩篇介紹 Prometheus 和 OpenTelemetry。這兩個工具最大的差異在於 Prometheus 從收集、儲存和搜尋都做完了，而 OpenTelemetry 本身負責的事情只有收集而已，儲存和搜尋都是交給其他服務去做。

### [How to quickly (and successfully) onboard engineers](https://about.gitlab.com/blog/2022/07/21/quickly-onboarding-engineers-successfully/)

DevOps 文化的涉略範圍當然也包括加速新進人員的上手過程，時間軸上大致分為四個階段：從新進員工還沒開工前就要開始準備了、第一天的準備、第一週的目標以及一個月後持續的遞交價值。
