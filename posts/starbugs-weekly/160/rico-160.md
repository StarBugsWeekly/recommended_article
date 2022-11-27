---
title: 第 160 期 DevOps 推薦文章
date: 2022-11-29
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Twitter Architecture 2022 vs. 2012](https://twitter.com/alexxubyte/status/1594008281340530688)

因 Elon Musk 把 Twitter 架構圖公開，作者就整理了 2022 和 2012 的架構圖讓大家一窺其內部運作。<!-- summary -->

### [How Zapier uses KEDA](https://keda.sh/blog/2022-03-10-how-zapier-uses-keda/)

Zapier 分享他們的 backend worker 原本是靠 CPU loading 做水平擴展，但是此 worker 有很多 blocking I/O 的功能，所以工作量很多時但 CPU 使用量還是很低。也因此團隊開始轉用 [KEDA](https://keda.sh/) 這個 event-driven autoscaling 專案來偵測 RabbitMQ queue 的數量和原本的 CPU loading 來做水平擴展。

### [X.509 Certificate Management with Vault](https://www.hashicorp.com/blog/certificate-management-with-vault)

Vault 可以選不同的 secret engine 而千變萬化，這次介紹的是 PKI（Public Key Infrastructure） certificate，可以生產短期的 certificate 後再搭配 Vault agent 可以做到自動更新與撤銷過期 certificates，也可以審計當時發行和撤銷的 certificates。