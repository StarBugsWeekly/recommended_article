---
title: 第 109 期 DevOps 推薦文章
date: 2021-11-30
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Infrastructure as Code: the next big shift is here](https://itnext.io/infrastructure-as-code-the-next-big-shift-is-here-9215f0bda7ce)

軟體架構一直在演進，不管是在 Provision，Delivery 或是 Maintenance 的方式都一直在進化中，而 Infrastructure as Code 尤其是如何，他可以將整個架構視覺化並且去補助服務的運行，而且這一切可以透過任何的語言，並且將其儲存在 Version Control 的 Repository 之中，而究竟 IaC 是如何走到今天這樣的面貌的呢？作者認為有幾個重要的階段，分別為...，文章中透過生動可愛的漫畫對每一個階段做詳細地說明

- Virtualization
- Containerisation and containers orchestration
- Public Cloud Infrastructure
- DevOps Culture

<!-- summary -->
### [How To Level Up Your Kubernetes Game](https://itnext.io/how-to-level-up-your-kubernetes-game-96f8f7ea50b9)

根據 Cloud Native Survey 2020 的調查顯示 Container 在 Production 環境的使用成長的三倍，因此 Kubernetes 的使用率只會升不會降，但使用 K8s 和擴展他是兩回事，K8s 設計是用來構建平台的平台，他的不僅僅只是用來管理 Container 而已，他的 API 和 Contril Plane 都是可擴展的，例如 K8s 的 Operator 和 Control Loop 都可以用來擴展 K8s，所以這篇文章想要介紹 Operator Pattern，讓大家一起學習如何適當地使用 Opertoar，並探索 Operator 的架構


### [dstp](https://github.com/ycd/dstp)

當有辦公室有人跟你說某個網站不能連時，你下意識會做什麼事情？使用 nslookup 或是 curl 嗎？現在你有更好的選擇 - dstp！這個 CLI 小工具可以幫你幫目標網站做常見的網路測試，包含 ping, DNS, TLS 和 HTTP 的檢查，讓你使用單一個工具就可以做完所有的檢查，不用在使用多個工具東查西查的