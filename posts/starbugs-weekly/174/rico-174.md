---
title: 第 174 期 DevOps 推薦文章
date: 2023-05-16
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [4 Core Principles of GitOps](https://thenewstack.io/4-core-principles-of-gitops/)

OpenGitOps 社群表示 GitOps 的四個核心原則：
<!-- summary -->

1. GitOps 是宣告式的
2. GitOps 是有版本控管且不可變動的。期望的狀態是要能夠歷史追蹤的
3. GitOps 的服務能夠自動拉式部署的（GitOps 很多都是 pull-based 的方式部署）。例如使用 Flux 持續且漸進部署解決方案，而且兼具資安、迅速和可靠
4. GitOps 的服務能夠持續性的和解（Reconciled）。能夠持續觀察系統狀態並且達到期望狀態，目前社群還在定義中，因為跟拉式部署的想法接近

### [Kubernetes Community: A Guide to Open Source Localization](https://thenewstack.io/kubernetes-community-a-guide-to-open-source-localization/)

軟體技術的確還是以英文為大宗，在推廣的過程中語言仍是個隔閡，除了打破語言的限制，在地化也十分重要，而 Kubernetes 在地化就給大家很好的例子學習。

### [Introducing "Implement DNS in a Weekend"](https://jvns.ca/blog/2023/05/12/introducing-implement-dns-in-a-weekend/)

作者用 Python 實作了 DNS 域名解析的小工具，從中複習 DNS 本身是怎麼運作的，而為了練習，只有用到標準的函式庫。作者也有開放大家下載程式碼，大約 200 多行。