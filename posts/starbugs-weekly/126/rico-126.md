---
title: 第 126 期 DevOps 推薦文章
date: 2022-03-29
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Prometheus - Investigation on high memory consumption](https://source.coveo.com/2021/03/03/prometheus-memory/)

作者先幫讀者複習一次 Prometheus 的名詞解釋和運作原理，之後循序漸進分析出記憶體幾乎是用在哪裡，最後得出的結論是 Prometheus label 比 metric 本身還要消耗記憶體，拿掉作者認為不重要的 `id` label 後，生產環境的記憶體使用量減少了 75%。
<!-- summary -->

### [Prometheus rate function](https://www.metricfire.com/blog/understanding-the-prometheus-rate-function/)

Prometheus alert rule 在網路上常常看到 `rate()` function 的範例，但個人覺得官方文件解釋稍微抽象了一點。於是找到這篇作者除了解釋 `rate()` 原理外，也說明跟 `irate()` 的差異，並且分享了實際的使用心得建議，甚至提供了 alert rule 和 SLO 計算的範例，另外作者也提醒 `rate()` function 計算期間沒有 scrape 到資料的話會失真。

### [Getting started with Grafana dashboard design](https://grafana.com/go/webinar/guide-to-dashboard-design/)

這篇以影片為主，主要是 Grafana dashboard 展示的確以影片的傳達媒介較佳。這次 webinar 說明在設計 dashboard 時要注意的人類瀏覽的行爲、顏色的使用、觀看者是誰以及 panel 呈現的優先度等等。後半段也有大量 dashboard 火力展示和 Q&A，Q&A 內容可以看到一些精彩的示範，例如從 50:12 主持人回答如何在同一個時間點對比 metric 和 log。