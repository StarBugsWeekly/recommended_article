---
title: 第 154 期 Kubernetes 推薦文章
date: 2022-10-18
author: smalltown

layout: layouts/post.njk
tags: [Kubernetes]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Kubernetes

<!-- summary -->
### [Learn Kubernetes - The Easy Way](https://programmingpercy.tech/blog/learn-kubernetes-the-easy-way)

假如你是一個軟體開發人員，應該時常會聽到 Kubernetes，畢竟他已經成為整個產業中 Container Orchestrator 的標準，作者當初剛開始學習 Kubernetes 時覺得很困難，因為其中有很多的東西需要學習，所以沒多久他就想要放棄了，也因為這個理由，所以他嘗試寫這篇教學文章來慢慢地將整個 K8s 需要知道的知識用簡單且好理解的方式一步一步給走過一輪，最終將可以完成一個提供 API 運行有資料庫的應用程式！
<!-- summary -->

### [Kubernetes Authentication Sidecars: A Revelation in Microservice Architecture](https://betterprogramming.pub/kubernetes-authentication-sidecars-a-revelation-in-microservice-architecture-12c4608189ab)

身為一位軟體開發人員，我們總是花費大把的時間在設定 Authentication 或是除錯有關於 Authentication 的問題，你一定曾經卡在 Authentication 無法符合預期運作的坑裡，而隨著 MicroServiers 的大量採用，有越來越多的服務需要去實作 Authentication，而這篇文章想要跟大家介紹如何透過利用 Sidecar 的方式來統一處理 Authentication 的需求

### [Securing CI/CD pipelines through security gates with Kubescape ](https://www.cncf.io/blog/2022/10/14/securing-ci-cd-pipelines-through-security-gates-with-kubescape/)

DevOps 的概念讓程式碼透過更完善且自動化的 CI/CD 提升了服務的品質，然而在 Security 越來越重要的今天也有更多的 Zero-Day 威脅與錯誤的組態配置被引入到正式環境的系統當中，而在 CI/CD Process 越來越自動化的今天，如何在此過程中加入 Security Gate 來檢查與驗證系統的安全性就變得非常重要，而這篇文章就想要跟大家介紹如何在 CI/CD 的 Process 中透過 Kubescape 來檢查 Kubernetes 的安全性