---
title: 第 159 期 DevOps 推薦文章
date: 2022-11-22
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [5 New CNCF Projects To Watch In 2023](https://itnext.io/5-new-cncf-projects-to-watch-in-2023-af5234ba6e87)

介紹 5 款還不錯的 CNCF 新專案，分別為：<!-- summary -->
- [Teller](https://github.com/SpectralOps/Teller)，更安全的把敏感資訊避免錯誤地使用在 code、shell 或檔案裡，支援 Vault、Consul、AWS Secret Manager 或 Google Secret Manager 等等
- [OpenCost](https://github.com/opencost/opencost)，計算 K8s 所產生的費用，前身是 [kubecost](https://kubecost.com/)
- [OpenFuction](https://github.com/OpenFunction/OpenFunction)，在 K8s 上建立 FAAS（function as a code platform）
- [External-secrets](https://github.com/external-secrets/external-secrets)，讓外部的 secret 存入並且自動同步 K8s secret
- [Clusterpedia](https://github.com/clusterpedia-io/clusterpedia)，把多個 K8s clusters 的資源以 wikipedia 的方式呈現，可以使用進階的搜尋功能

### [AWS EBS Volumes gp2 vs gp3, io1 vs io2 which one to choose](https://devopslearning.medium.com/aws-ebs-volumes-gp2-vs-gp3-io1-vs-io2-which-one-to-choose-7177e59fff3c)

AWS EBS 類型的選擇是維運人員該注意的，gp2 和 gp3 衡量過後評估要換的話，gp2 是可以直接不用關機改成 gp3 的，只是要注意其會根據容量大小決定修改時間，而 io1 改成 io2 也以此類推。

### [Chaos engineering 101: Principles, process, and examples](https://learningdaily.dev/chaos-engineering-101-principles-process-and-examples-e94355e4e773)

Chaos Engineering 為現今許多大型組織的解決方案，本文簡單介紹一下其原理、工具、原則和流程、扎實的實際範例和如果要鑽研如何開啟下一步。