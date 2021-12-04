---
title: 第 110 期 DevOps 推薦文章
date: 2021-12-07
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [AWS re:Invent 2021 Adam Selipsky Keynote Summary](https://beabetterdev.com/2021/12/01/aws-reinvent-2021-adam-selipsky-keynote-summary/)

今年 AWS re:Invent 恢復在拉斯維加斯實體舉辦，這次一樣推出許多的新功能，例如之前我一直苦惱要怎麼把公開 Image 同步到，自己家裡的功能，[現在在 ECR 裡面就可以辦到](https://aws.amazon.com/blos/aws/announcing-pull-through-cache-repositories-for-amazon-elastic-container-registry/)，而且[推出 AWS 自有的 Kubernetes AutoScaler - Karpenter](https://aws.amazon.com/blogs/aws/introducing-karpenter-an-open-source-high-performance-kubernetes-cluster-autoscaler/)，當然這只是今年推出功能中的冰山一角！而在最重要的 Keynote 中又宣布的什麼大事呢？

- 當然就是 AWS 自家的新一代處理器 Graviton3，更快的運算速度而且更省能源，而且新的 Instance Type C7G 就會使用這顆新的處理器；除此之外也宣布了專門為訓練模型而最佳化的 Instance Type **TRN1**

- 再來則是為了金融相關產業所推出的遷移工具 AWS Mainframe Modernization，讓開發者將過時的 Infrastructure 搬遷到 Cloud 時更方便，AWS 甚至可以自動化從標準的 Cobol 程式碼產生 Java 程式碼

- 再來這應該是最屌的發佈功能了 - AWS Private 5G！他讓顧客可以使用 AWS Infrastructure 去架設跟擴展 5G 網路，AWS 提供硬體，組態，沒有限制任何可連接裝置的數量，跟其他 AWS 服務一樣，只要付錢就可以使用！

- 其他還有...Lake Formation Row and Cell Level Security, Lake Formation Transactions, 更多 Serverless 服務，Sagemaker Canvas，Goldman Sachs Financial Cloud For Data, AWS IoT Twinmaker, AWS IoT FleetWise 多到我連複製貼上都覺得累XD 有興趣的人可以再花點時間詳細研究

<!-- summary -->
### [Kubernetes 1.23 – What’s new?](https://sysdig.com/blog/kubernetes-1-23-whats-new/)

除了 AWS re:Invent 大爆炸之外，Kubernetes 也即將推出 1.23 版本更新，這次帶來 45 個功能改善，雖然相對於 1.21 (50) 和 1.22 (56) 來說比較少，但其中幾個還滿有感的，例如 [kubectl events](https://sysdig.com/blog/kubernetes-1-23-whats-new/#1440) 指令，支援 [OpenAPI v3](https://sysdig.com/blog/kubernetes-1-23-whats-new/#2887) , [gRPC probes](https://github.com/kubernetes/enhancements/issues/2727), 同時也可以看到 [CSI Drivers](https://sysdig.com/blog/kubernetes-1-23-whats-new/#2317) 和 [Windows Support](https://github.com/kubernetes/enhancements/issues/2802) 這兩個大專案的持續進展，而且也有不少功能抵達 GA 階段，有興趣的人可以閱讀原文獲得更多且詳細的資訊！ 

<!-- summary -->
### [Visualizing Kubernetes Clusters with Navigate](https://medium.com/@brkg_/visualizing-kubernetes-clusters-with-navigate-e340e5419c19)

這兩天發現有一個叫做 Navigate 的免費開源專案，他可以用來視覺化 Kubernetes Cluster 的各種資源，也可以顯示即時的 Log，範例圖看起來滿潮的，而且其中一個功能是可以從本地端的 YAML 檔案把即將部署到 K8s 中的資源也是進行視覺化呈現，讓開發者可以事先知道自己要部署到 K8s Cluster 中的組態長什麼樣子，感覺還滿不錯的，有機會再來試用看看！