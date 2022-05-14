---
title: 第 133 期 DevOps 推薦文章
date: 2022-05-17
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Deleting Production in a Few Easy Steps (and How to Fix It)](https://thenewstack.io/deleting-production-in-a-few-easy-steps-and-how-to-fix-it/)

講解真實環境的災難還原之旅，起初 ArgoCD 因為 path 寫錯導致部署錯誤，而且剛好刪到最核心的業務。當下團隊直覺想到何不 revert 就好，但可惜的是該服務為 stateful 的，且 ArgoCD 會重新創建新的 instance 但會沒有使用者重要的 metadata。於是團隊開始著手災難復原，先把 backing service 裡的資料恢復（文章把相依關係和一些技巧寫的很詳細務必細讀），核心業務的服務暫時上線後先加大硬體和多開幾台應付暫時的大量流量，這趟災難復原總共花了 6 小時。<!-- summary -->

關於災難復原要做的好，除了平常的備份外，也要熟悉服務相依性、架構和細節才行，而且也得做事後檢討改善部署流程，像是改善生產 YAML 的方式、在生產 YAML 的時候偵測有沒有重複、把 ArgoCD 設定成不能刪除既有的 stateful 資源以及多個 ArgoCD 之間不能互相干涉彼此部署的服務。

### [Service mesh at scale: How Xbox Cloud Gaming secures 22k pods with Linkerd](https://www.cncf.io/blog/2022/05/10/service-mesh-at-scale-how-xbox-cloud-gaming-secures-22k-pods-with-linkerd%EF%BF%BC/)

文章描述 Microsoft Xbox 如何使用 service mesh 工具 Linkerd 減少維護的人力成本（令我訝異的是原來對延遲要求甚高的遊戲也會用 service mesh），團隊一開始考慮的工具有 Istio、Linkerd、Consul Connect 和其他工具，但最後還是選擇 Linkerd，原因如下：

* 容易設定 mTLS
* 因為有 Service Mesh Interface API 所以跟其他 CNCF 專案工具有很好的整合
* mTLS 是從 proxy level 下手，不用特別呼叫專門的 mTLS 服務可以減少 100ms 的延遲
* 更好的網路流量監控，而且很多功能都開箱即用

### [Build or Buy? Developer Productivity vs. Flexibility](https://thenewstack.io/build-or-buy-developer-productivity-vs-flexibility/)

設計架構時應該要選怎樣的工具？雲服務還是地端？高階語言還是低階語言做開發？自架還是託管服務？自己設計工具還是使用 SaaS？文章給了一個當開發時應該選擇用 library 還是 API 當作範例參考，在選擇的過程中，其中最大的兩個原則是這個專案是否跟核心業務有關，以及這個專案是否可以透過客製化獲得商業上的成功。