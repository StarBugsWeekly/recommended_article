---
title: 第 139 期 系統監控 推薦文章
date: 2022-07-05
author: smalltown

layout: layouts/post.njk
tags: [Monitoring]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Monitoring

<!-- summary -->
### [A set of modern Grafana dashboards for Kubernetes](https://medium.com/@dotdc/a-set-of-modern-grafana-dashboards-for-kubernetes-4b989c72a4b2)

作者在 2018 年擔任 DevOps Engingger 負責多個運行在 GKE 的 Go 微服務效能測試時，便開始使用 Grafana 來視覺化 K8s 運算資源的使用狀態。從那時起他便深深的愛上有關 K8s 相關監控技術而且從未停止鑽研他，也正因為如此才會有今天要介紹的 Grafana Dashboard 開源專案
<!-- summary -->

在這個 Grafana Dashbord 開源專案中，作者希望可以做出一系列可以幫助自己快速解決每天維運問題的 Dashboard，他並不想要把所有的 Metric 都放進來，而是希望做出有用且直覺的 Dashboard，因此最後做出了以下幾個可以搭配一起使用的 Dashboard，從範例圖看起來還滿不賴的，感覺滿值得安裝來試試看的

- Kubernetes / Views / Global
- Kubernetes / Views / Namespaces
- Kubernetes / Views / Nodes
- Kubernetes / Views / Pods
- Kubernetes / System / API Server
- Kubernetes / System / CoreDNS
- Kubernetes Addons / Trivy / Starboard Operator

### [Vault Logging and Alerting on Day 1](https://www.hashicorp.com/blog/vault-logging-and-alerting-on-day-1)

Vault 可以算是開源界 Credential Management 的第一把交椅，他可以很安全地保護機敏資料，不過他本身也是一個應用服務，要如何收集分析他的 Log？以及怎麼知道哪一些訊息表示他出問題了，需要有 Alert 通知我們呢？官方的這篇文章提供了一個簡單且免費的解決方案，讓使用者運行此方案在 AWS 環境中，就可以讓 Vault 服務可以簡易的處理 Log 與具備有 Alert 通知功能，有使用 Vault 的人千萬不要錯過了

### [OpenTelemetry Roadmap and Latest Updates](https://horovits.medium.com/opentelemetry-roadmap-and-latest-updates-a389144f3812)

OpenTelemetry 目前是 CNCF 第二活躍的專案，在 KubeCon Europe 2022 中關於他的最大新聞應該就是 OpenTelemetry Metrics 已經到了 RC 階段，使用 Java, .Net 和 Python 實作的相關 API 和 SDK 也都趨於穩定，OpenTelemetry Protocol 也是越來越穩定，同時他也全面支援 Prometheus，不管是要匯出或是匯入 Prometheus 格式的 Metric 都可以，更多關於 OpenTelemetry 近期更新可以參考詳細內文