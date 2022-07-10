---
title: 第 140 期 DevOps 推薦文章
date: 2022-07-12
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [List of DevOps Blogs and Resources for Learning](https://devopscube.com/list-of-devops-blogs-and-resources/)

這篇目前是我看過最厲害的 DevOps 資源整理，從課程、Github repository（光是這個水就很深）、書籍、blog、social media、podcast、知名人士、白皮書、必看的工程文章 blog、討論區。可以看得出來這篇整理都是精挑細選的，想要精進自己這邊是很好的入口，更不用說筆者我之後的 DevOps 推薦文章也會從裡面找。<!-- summary -->

### [Understanding data transfer costs for AWS container services](https://aws.amazon.com/blogs/containers/understanding-data-transfer-costs-for-aws-container-services/)

這篇解釋在 AWS 上使用 container 服務所花的資料傳輸費用。例如 container deployment 的不同而很難注意到花費，container image registry 是否為 public or private、是否同個 region 都會影響資料傳輸費用。有些 AWS container 服務的特殊性，地端的 nodes 需要跟 AWS 雲上的 control plane 做溝通也會有傳輸費用，更不用說 AZ 之間的傳輸費用。甚至要注意的是 Kubernetes 的設定是不是流量直接到適當的 node 上而不用再請 kube-proxy 轉送。

### [Advanced Features of Kubernetes’ Horizontal Pod Autoscaler](https://betterprogramming.pub/advanced-features-of-kubernetes-horizontal-pod-autoscaler-536ebd7893ad)

本文用 KinD 做測試環境示範進階的 HPA（Horizontal Pod Autoscaler），基本 HPA 常見的基準就是 CPU or memory 使用量，於是作者就示範客製 Prometheus metric 來觸發 HPA，而且可以從 `Pods` 和 `Service` 這兩層看情況收集。除了從 application 本身獲取 metric 之外，也可以從它的 backing service 下手，例如 DB 或 queue service。另外也介紹較為特殊的功能如：HPAScaleToZero、HPAContainerMetrics、LogarithmicScaleDown。
