---
title: 第 119 期 DevOps 推薦文章
date: 2022-02-08
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Scaling Kubernetes to Over 4k Nodes and 200k Pods](https://medium.com/paypal-tech/scaling-kubernetes-to-over-4k-nodes-and-200k-pods-29988fad6ed)

PayPal 目前主要的 Workload 運行在 Mesos，而在準備把部分的 Workload 搬遷到 Kubernetes 前，他們需要先測試看看 K8s 的擴展性有沒有辦法滿足他們的需求，他們一開始運行 2,000 Pod 在 1,000 Node 中，接著增加到 16,000 Pod 在 32,000 Node 中，然後跳到 150,000 Pod 在 4,100 Node 中，最後透過增加每台 Node 的 CPU，讓 Pod 的個數上升到 200,000，在這個過程中他們遇到一些挑戰，而這篇文章中描述的他們如何面對且克服這些挑戰的過程 (看起來主要都是在 Control Plane 上的調校)，有興趣的人請詳閱內文

<!-- summary -->

### [Kubernetes Vault Integration via Sidecar Agent Injector vs. CSI Provider](https://www.hashicorp.com/blog/kubernetes-vault-integration-via-sidecar-agent-injector-vs-csi-provider)

HashiCorp Vault 算是目前開源軟體圈內，數一數二的密碼管理工具，而官方這邊跟 Kubernetes 的整合方式有兩種，本文將比較這兩種方式有何不同，根據結論來看的話，第一種方式功能比較齊全，詳細比較的可以參考內文

1. The Vault Sidecar Agent Injector

透過 [vault-k8s](https://github.com/hashicorp/vault-k8s) 這個 Project 所實作的 Side Car 模式，讓 K8s mutating webhook controller 將機敏資料注入到 Pod 中

2. The Vault Container Storage Interface (CSI) provider

透過 [Vault CSI provider](https://www.vaultproject.io/docs/platform/k8s/csi) 讓 Pod 可以直接去使用暫時性的 [CSI Secrets Store](https://github.com/kubernetes-sigs/secrets-store-csi-driver) 空間

### [Decoupled Microservices Architecture with Materialize](https://dev.to/bobbyiliev/decoupled-microservices-architecture-with-materialize-2l67)

目前有數種方式可以用來處理 Microservice Architecture 中的資料，本文想要介紹幾種分散式資料庫的做法，而作者主要講解的東西是構築於 [Houssem Dellai](https://www.youtube.com/channel/UCCYR9GpcE3skVnyMU8Wx1kQ) 的影片 - [Data in a Microservice Architecture](https://www.youtube.com/watch?v=31AD6Nobt1o) 之上，文中假設有一個電子商務網站，並且由兩個 Microservice 所構成 (Catalog Service & Basket Service)，兩個服務前面由 API Gateway 負責接收請求，並且有各自的資料庫，而且為了讓 Basket 可以跟 Catalog 溝通，所以中間還有實作 Restful API，這個架構最大的問題就在於 Basket 對於 Catalog 的高耦合，所以有不少缺點，那要如何改善這樣的架構呢？答案就在文中！