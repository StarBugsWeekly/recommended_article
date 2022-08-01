---
title: 第 143 期 DevOps 推薦文章
date: 2022-08-02
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How Kubernetes Reinvented Virtual Machines (in a good sense)](https://iximiuz.com/en/posts/kubernetes-vs-virtual-machines/)

這篇文章以實際面的角度切入加上圖片解釋了為什麼要有 Kubernetes 的存在，從最一開始的 VM 遇到的難題開始到 container 解決了什麼問題，以及 container 不能解決的問題，最後延伸到 Kubernetes pod 的特別之處，作者比喻 pod 類似 VM 的概念，所有 container 共享同一個 namespace。當然不免俗的還是要簡單介紹 Kubernetes 常見的 object 例如：Deployment、ReplicaSet 和 Service。<!-- summary -->

### [Core DevOps Practices to Secure Your Infrastructure as Code](https://dzone.com/refcardz/iac-security-1)

IaC 已經是顯學了，但是 IaC 還是有許多 security 挑戰需要克服，IaC 在 hybrid-cloud 和 multi-cloud 會增加管理 security 的難度；或者 infra 持續的增長但是管理的支出不變或更少；業務上的需求說變就變，infra 必須要跟著因應而增加複雜度。IaC 靜態分析可以讓 security 有所提升，與其讓 developer 自己檢查，還不如用靜態分析來做，況且每家 cloud provider 的機制都不太一樣，文章的最後也有提及怎麼做好 security IaC for multi-cloud。
文章也提及 IaC security 除了 IaC CICD pipeline 的整合外，還需要重視使用後的 feedback；把 alerts 做好分類和願意承受的風險，不然團隊很快就會陷入疲勞；另外除了 infra，app 也必須做好靜態和動態的分析。

### [Expand the Power of Traefik Proxy with Custom Plugins](https://traefik.io/blog/expand-the-power-of-traefik-proxy-with-custom-plugins/)

Traefik proxy 是目前很受歡迎的 cloud-native application proxy 之一，其支援使用者安裝另外客製化的 plugin，不論從 dashboard 或從設定檔都可以輕鬆安裝，甚至也會直接給你 YAML 範例讓使用者方便複製貼上，而且這些 plugin 不用特別編譯且跨平台支援。目前看到很有意思的 plugin 有 ldapAuth、DenyIP、Rewrite Body 等等，最後官方也有完整的文章教學怎麼寫一個客製化的 plugin。