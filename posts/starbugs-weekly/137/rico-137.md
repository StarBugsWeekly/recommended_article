---
title: 第 137 期 DevOps 推薦文章
date: 2022-06-21
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [A deep dive into OpenTelemetry metrics](https://www.cncf.io/blog/2022/06/08/a-deep-dive-into-opentelemetry-metrics/)

OpenTelemetry 相信大家都不陌生，此篇文章從基本開始分享起，並且解釋收集 metrics 流程的細節，也有解釋同步與非同步的實作上的差異，另外文章裡的各種分類表和 OpenTelemetry SDK 範例也十分受用。<!-- summary -->

### [Troubleshooting Amazon EKS API servers with Prometheus](https://aws.amazon.com/blogs/containers/troubleshooting-amazon-eks-api-servers-with-prometheus/)

文章以圖文並茂的方式教大家怎麼 troubleshooting EKS API。其中提到的 LIST 和 WATCH 的差異，使用 WATCH 可以讓 Kubernetes 規模更大，不過當 object 或 worker nodes 越多也是有負擔，本文也有寫解決方法，另外當有些服務使用過多的 LIST 呼叫時務必加上 limit。維運人員也要注意服務詭異的行爲像是讀跟寫的次數不一致是否是預期的？API 優先程度可以根據服務有所調整，這樣就可以避免有些服務影響到 API server。

### [Why Is Everyone Ignoring the Day 2 Kubernetes Problem?](https://thenewstack.io/why-is-everyone-ignoring-the-day-2-kubernetes-problem/)

單純使用 Kubernetes 的 Deployment、Service 或 Ingress 並不難，最難的是如何持續的維運 cluster，比起技術上的使用，更多的是要了解 Kubernetes 的生態圈，然後在各個面向選擇適合組織的工具。例如：如何標準化 Kubernetes 的更新管理、使用者的權限管理與隔離、監控、審計以及如何整合第三方工具等等。