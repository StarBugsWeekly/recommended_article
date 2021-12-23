---
title: 第 112 期 DevOps 推薦文章
date: 2021-12-21
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Kubernetes-in-Kubernetes and the WEDOS PXE bootable server farm](https://kubernetes.io/blog/2021/12/22/kubernetes-in-kubernetes-and-pxe-bootable-server-farm/)

或許有的人正在想怎麼把應用服務搬遷進到 Kubernetes 中，但你知道現在有個專案叫做 Kubernetes-in-Kubernetes，直接把 Kubernetes 也搬遷到 Kubernetes 中 (好繞口令)，作者會有這樣的構想是因為藉由使用 K8s 的話，其實不只可以像寫程式語言一樣宣告你的應用服務，也可以像寫程式一樣去定義整個 Infrastructure，所以作者就想利用這個特性，將 Multi-Cluster K8s 運行在一個大的 Kubernetes Cluster 中，有興趣了解怎麼做到的人可以參考內文，想要試試看的人也可以透過 Helm 跟幾個簡單的指令部署看看

<!-- summary -->
### [A brief history of code search at GitHub](https://github.blog/2021-12-15-a-brief-history-of-code-search-at-github/)

GitHub 算是工程師平日生活不可或缺的網站之一，而他們最近宣布新的程式碼搜尋功能用以提升開發者的工作效率，例如更容易找到需要的結果，而且可以再搜尋時使用正規表示式，在搜尋時透過 `org:` 或是 `repo:` 來限縮限縮搜尋的範圍，或是使用邏輯運算元如 OR, NOT 來做搜尋...等功能，有興趣的人可到[封測網站註冊](https://cs.github.com/)；而在新功能推出的同時，也撰寫了這篇文章分享 GitHub 搜尋功能的歷史故事，讓大家知道他們想要達成的目標與進展過程～

<!-- summary -->
### [Improving platform efficiency, reliability, and performance in one week with Linkerd](https://www.cncf.io/blog/2021/12/13/improving-platform-efficiency-reliability-and-performance-in-one-week-with-linkerd/)

Salt Security 是一間提供 API 防護功能的公司，所以他們的服務不能夠容忍任何的 Down Time, 因為顧客不會有停止遭受攻擊的時候，他們一開始將微服務運行於 Kubernets Cluster 中，而隨著規模越來越大，他們開始想要遷移到使用 gRPC 的架構，但是遇到 K8s 沒有支援 Load Balancing 的問題，所以發現了 Linkerd 這個專案，因為他不僅可以讓 gRPC 具備 Load Balancing 的功能之外，而且也提高了整個平台的效率，可靠性和整體效能，文章中對於他們的每一個技術方案選擇做出詳細的解釋，有遇到一樣問題的人，或是徬徨要不要導入 Linkerd 的人可以參考看看這篇文章