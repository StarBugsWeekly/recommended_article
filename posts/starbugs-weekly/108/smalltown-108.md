---
title: 第108期 DevOps 推薦文章
date: 2021-11-23
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

### [CRISP: Critical Path Analysis for Microservice Architectures](https://eng.uber.com/crisp-critical-path-analysis-for-microservice-architectures/)

Uber 的後端系統算是 MicroService 架構的榜樣，其中有數千個 MicroService 透過 RPC 的方式跟其他服務進行溝通，所以當服務請求發生時，就很像是網路傳遞時會有數個 hops 一樣，當數個 MicroService 都正常時，這個服務請求才能夠運行成功，其過程是相當複雜的，可能隱含很多的動作，非同步..等，所以當要追查一個服務請求點到點的品質時，可以想像是相當困難的，所以 Uber 開發了一個叫做 CRISP 的工具，用來解決追蹤複雜服務請求中到底是哪一個環節出了問題，CRISP 主要使用 Jaeger 這個 RPC 的追蹤工具，對於此主題有興趣的人，可以查看原文獲得更仔細的資訊
<!-- summary -->
### [cloudquery](https://github.com/cloudquery/cloudquery)

CloudQuery 可以將在雲端的資源資訊給萃取出來，將其轉化為 PostgreSQL Table 的資料，主要的使用情境有底下三種：

- Search: 使用標準的 SQL 語法去搜尋雲端資源 
- Visualize:將資料透過 BI 或是視覺化工具呈現出來，例如 Grafana, QuickSight...等
- Policy as Code: 將 Security 和 Compliance 規則寫成 SQL 語法用以達成 PaC
<!-- summary -->
### [Prometheus announces an Agent to address a new range of use cases](https://www.cncf.io/blog/2021/11/16/prometheus-announces-an-agent-to-address-a-new-range-of-use-cases/)

一直以來 Prometheus 都是使用 Pull 的模式，透過 Prometheus Server 把來自各方的資料做彙整，而最近宣佈了新的模式 Agent Mode，Prometheus Agent 跟 Prometheus Server 其實有點像，他還是透過 Pull 去抓取 HTTP 所暴露的 Metric 資料，然後使用 Remote Write 的方式將資料送到遠端的 Prometheus Server，不過 Metric 資料並不會儲存在本地端，送出去後就會立即移除掉，希望可以應用在某些應用情境上，例如 Edge Networks 和 IoT