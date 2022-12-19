---
title: 第 163 期 DevOps 推薦文章
date: 2022-12-20
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How DoorDash Secures Data Transfer Between Cloud and On-Premise Data Centers](https://doordash.engineering/2022/11/29/how-doordash-secures-data-transfer-between-cloud-and-on-premise-data-centers/)

處理底層網路一直都不是簡單的事，DoorDash 因為業務需要跟供應商做介接，但因為供應商敏感的資料不適合暴露於公開的網路，所以評估 AWS Site-to-Site VPN 和 Direct Connect。確定使用 Direct Connect 的實體光纖線路後，發現供應商防火牆的規則會擋掉所有來自內網的 CIDR 範圍，<!-- summary -->例如 10.0.0.0 到 10.255. 255.255 (Class A) 172.16.0.0 到 172.31. 255.255 (Class B) 192.168.0.0 到 192.168. 255.255 (Class C)，確保流量是來自外部。於是 DoorDash 只好使用 NAT Gateway 嘗試解決，但發現在 Virtual Private Gateway 時沒辦法抓到 NAT Gateway 的 Elastic IP，所以最後使用 [Private NAT Gateway](https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/private-nat-gateway.html) 才得以解決。然後 DoorDash 在靠 AWS Transit Gateway 把 Direct Connect 的環境以中心點串到各個 AWS 帳號去。

### [Kubernetes CI/CD Pipelines Explained](https://thenewstack.io/kubernetes-ci-cd-pipelines-explained/)

我想大家或許對 Kubernetes CI/CD 工具已經很熟了，但本篇依舊介紹不錯的工具之外，也介紹了最佳實踐，以及推薦自動化、團隊合作、資安和監控工具。是一篇要入門建置 Kubernetes CI/CD pipeline 很不錯的起點文章。

### [How to Build a Fintech App: Approach, Architecture, and Scalability](https://mobidev.biz/blog/how-to-build-fintech-app-approach-architecture-scalability)

做金融科技的服務要如何選架構？地點決定法規、商業模式影響系統負載、是否很在意延遲、服務需不需要即時性和系統可靠性容錯率有多少，又或者單體架構（Monolith）、服務導向架構（service-oriented architecture）或微服務架構（Microservices）。作者是建議業務一開始可以循序漸進，因為微服務架構會花很多開發時間，等腳步穩了再改進即可。