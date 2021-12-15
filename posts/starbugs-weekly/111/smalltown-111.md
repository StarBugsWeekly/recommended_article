---
title: 第 111 期 DevOps 推薦文章
date: 2021-12-14
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Terraform 1.1 Improves Refactoring and the Cloud CLI Experience](https://www.hashicorp.com/blog/terraform-1-1-improves-refactoring-and-the-cloud-cli-experience)

HashiCorp 這幾天最大的[新聞](https://seekingalpha.com/article/4474505-hashicorp-could-be-the-worst-ipo-of-the-year)應該就是在 Nasdaq IPO 了！不過我們還是回歸技術面來看一下 Terraform 剛推出的 1.1 版有哪一些值得關注的內容:

- Terraform 使用久了之後，難免會遇到想要 ReFactoring 的狀況，例如把單一個 Module 拆成多個，這次在 1.1 推出了 `moved` statememt，讓使用者透過 plan 來預覽跟驗證 Refactoring 的動作，有興趣的人可以參考[官方教學文章](https://learn.hashicorp.com/tutorials/terraform/move-config)

- 改善在 Terraform Cloud 與 Enterprise 中的 CLI 體驗

<!-- summary -->
### [Karpenter vs Cluster Autoscaler](https://towardsdev.com/karpenter-vs-cluster-autoscaler-dd877b91629b)

上個月底 AWS re:Invent 推出了另外一套叫做 [Karpenter](https://github.com/aws/karpenter) 的 Kubernetes Cluster Autoscaler，而他跟目前大家使用的開源 [Cluster Autoscaler](https://github.com/kubernetes/autoscaler) 有什麼不一樣呢？就以 EKS 這個 Kubernetes 來舉例說明，它分成 Control Plane 和 Node Group，既有的開源 Cluster Autoscaler 會去偵測是否有 Pod 處於 Pending 的狀況，然後去叫控制 Node Group 的 AWS Auto-Scaling Group 根據需求增加多少台機器

而 Karpenter 可以根據 Pending Pod 所需要的資源跳過 Node Group，直接開適合的 EC2 出來，所以其實在時間跟資源的應用上都可以更有效率，例如突然有個需要使用超級多 Memory 的 Pod 處於 Pending 的狀態，在 AWS Auto-Scaling Group 裡面所定義的機器型別根本就都不適合此 Pod 運行，Karpenter 就可以直接協助開啟一台符合此 Pod 使用的 EC2 然後直接把 Pod 指派到這台新開的 EC2 上，所以對於 Kubernets Worker Node 的擴展性來說強大很多

### [Using ChatOps to help Actions on-call engineers](https://github.blog/2021-12-01-using-chatops-to-help-actions-on-call-engineers/)

在 GitHub 內常使用 ChatOps 來幫助合作更順利，使用的 Chatbot 為 Hubot，運行 ChatOps Command 很像是在 Terminal 運行自己的指令一樣，但不同之初在於所有的團隊成員都可以看到運行的成果，這讓合作時的溝通是即時的，特別是在處理 Incident 時，可以更快的恢復服務並且找出原因；而目前在 GitHub 內讓應用服務保持健康不再是某個神秘團隊的責任，而是落在建立該服務的工程師手上，因此除了幫 GitHub 建立力強大的功能之外，在 GitHub 的工程師也會貢獻他們時間在維護服務的健康上，此文便是講述前幾天一個新的 Actions on-call engineer: Mona 她處理 Incident 的經過，從其中可以看出 ChatOps 如何協助她快速且有效的處理事件
