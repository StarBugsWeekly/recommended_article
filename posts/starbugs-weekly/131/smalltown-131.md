---
title: 第 131 期 後端開發 推薦文章
date: 2022-05-03
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [SQuriL: Generate and Store Your GraphQL Schemas](https://medium.com/@michael-a-trapani/squril-generate-and-store-your-graphql-schemas-ae38af229701)

GraphQL 是讓 API 對既有資料實現強大搜尋功能的語言與 Runtime，他提供了一個相對於 RESTful 的替代方案，讓開發者可以使用單一個請求來對多個資料來源獲取資料；雖然 GraphQL 的優勢顯而易見，但有許多的公司尚未將查詢語言整合到既有的技術棧當中，對於這類公司來說要採用 GraphQL 的門檻相對地高，SQuriL 就是為了解決類似問題而生的解決方案，他是一個開源的 GraphQL Schema 生成和儲存工具，可以從 PostgreSQL URI 來產生客製化且具備可以 Production 環境使用的 GraphQL Schema 給 Node.js 和 TypeScript 相容環境使用，有興趣的人可以參考這篇文章看看如何使用它

<!-- summary -->

### [Improving Query Performance by 10000x](https://betterprogramming.pub/improving-query-performance-by-10000x-79b84c80fbaf)

當你嘗試從系統中獲得更多資訊時，你的應用程式是不是也變得更慢了？你並不孤獨，雖然有人說過不要過早去優化系統，但在某些時候，你還是必須要花點時間去研究看看如何提高系統效能，作者所在的 Sky Ledge 最近遇到類似的問題...一個簡單的 Query 本來預期在 1 秒內就要跑完，但在 Staging 環境花了將近 30 秒才取得回應，作者後來花了兩個多小時將問題解決掉！文中巨細彌遺地慢慢解釋他怎麼用科學方式去分析找到問題的過程還滿值得參考一下的

### [System Design — Design a Monitoring System](https://gongybable.medium.com/system-design-design-a-monitoring-system-f0f0cbafc895)

如何設計一個監控系統？這個問題應該滿常會在面試中被提問到，首先必須考量的點在於如何收集 Metric，是要用 Pull 或是 Push 模式，假如使用 Pull 模式的話要怎麼去設計 Exporter；而一個監控系統應該要具備擴展性，那麼要如何達成？儲存資料的 DB 要怎麼設計...等，這一連串的問題，作者用一篇文章來含括與回答，讓大家可以更清楚的理解監控系統的設計