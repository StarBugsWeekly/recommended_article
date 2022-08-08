---
title: 第 144 期 DevOps 推薦文章
date: 2022-08-09
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [SRE From Theory to Practice: What's Difficult About On-Call?](https://dzone.com/articles/sre-from-theory-to-practice-whats-difficult-about)

造成 on-call 困難的原因不外乎是沒有完好的文件、責任歸屬不清、透明度不足和花在 on-call 時間上的比例等等，要如何實踐健康的 on-call 機制可以從這三點上改善：
* 內部的 on-call 要跟影響到客戶的外部 on-call 一樣重要，建議可以從 SLIs 和 SLOs 上著手
* 客戶們的使用情況可以分析不同服務的重要性，另外不確定服務的運作原理不必感到挫折或羞恥地尋求幫助！
* 如上所述，營造無究責的文化（blameless culture）非常重要<!-- summary -->

### [Top 25 Nginx Tips and Tricks From Practical Experience](https://hackernoon.com/top-25-nginx-tips-and-tricks-from-practical-experience)

本文介紹 Nginx 的基本程式架構，解釋為什麼改設定的時候可以讓使用者察覺不到，並且提供許多作者實際工作上好用的 Nginx 使用訣竅，對於維運工程師是個很實用的文章，工作常用的設定都有。

### [What is a Platform Orchestrator?](https://www.cncf.io/blog/2022/08/04/what-is-a-platform-orchestrator/)

本文介紹 platform orchestrator 的精髓與要解決的痛點，其本質是建立在 Declarative Application Model 上，也是大家熟悉的 pull model，這些是可以動態更新的。而最主要解決的原先的是以靜態的方式建立 application，例如靜態設定很容易在不同環境中飄移，很難維護且很難標準化。最後還有假如要建立 platform orchestrator 的話會遇到的細節整理。
