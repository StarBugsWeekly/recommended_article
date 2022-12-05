---
title: 第 161 期 Kubernetes 推薦文章
date: 2022-12-06
author: smalltown

layout: layouts/post.njk
tags: [Kubernetes]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## Kubernetes

### [Kubernetes 1.26 – What’s new?](https://sysdig.com/blog/kubernetes-1-26-whats-new/)

K8s 1.26 也差不多要正式發佈了，讓我們跟著 sysdig 來看看這一版有什麼重要更新吧！ 這一版有 37 個增強功能，對比於 1.25 有 40 個，1.24 有 46 個，這 37 個裡面有 11 個會升到穩定版本，10 個的功能還需要持續改善，16 個全新的功能，其中底下幾個是 sysdig 覺得比較重要的更新，更詳細內容可以參閱內文：

<!-- summary -->

- 儲存功能: 透過 VolumeSnapshot 功能，從不同 Namespace 的儲存快照建立新的儲存空間
- 驗證功能: 構築於 1.25 引進用來驗證 CRD 的 Common Expression Language (CEL)，現在 admission controller 多了一個 ValidatingAdmissionPolicy 型別，讓使用者可以在沒有 webhook 的情況下達成驗證機制
- 監控功能: 不再需要透過 Prometheus Exporter，可以直接在 /metrics/slis 提供 Kubernetes 的 SLI Metric
- 監控功能: 開始從 CRI API 來獲取 Container 的資訊 (例如 CPU, Memory 使用量)，而不是 cAdvisor，這也意味著會慢慢的將 cAdvisor 給淘汰掉，畢竟 Container Runtime 才是最清楚知道 Container 運行狀況的角色
- 管理功能: 既有的 Resource Management 只能針對 CPU 和 Memory 去設定 Limit 和 Request (之後還可以針對 Storage)，不過對於需要做初始化和清理的硬體資源，如 FPGA，或是想要限制硬體資源被存取，如共享的 GPU，這次新增了新的 ResourceClaimTemplate 和 ResourceClass 物件來達成這些需求，讓資源更動態地去分配
- 管理功能: 讓 Topology Manager 對於 multi-NUMA (NUMA: non-uniform memory access) 的 Kubernetes 節點有更好的控制權，例如透過控制使用哪一顆實體的 CPU 核心來避免 Memory 在不同晶片暫存或是 Socket 間跳躍，用以獲得大幅度的效能改善
- 管理功能: StatefulSet 多了掌控起始 Replica 數目的設定 (spec.ordinals.start)，主要的應用情境會是在跨 Namespace 或是叢集搬遷 StatefulSet 可以達成 0 Downtime 的需求 (建議同時搭配 PodDistruptionBudgets 去做使用)
- 管理功能: 讓 Kubernetes 的使用者可以透過 Auth API 獲得自己的使用者資訊，例如有什麼樣的權限，位於哪一些群組...等
- 效能改善: 讓 kubernetes-apiserver 提供 API 的完整清單，這樣一來呼叫 kubernetes-apiserver 的 client 就不用自己去查找有哪一些 API 和這些 API 有哪一些版本可以使用

### [Kubernetes Labels: Expert Guide with 10 Best Practices ](https://cast.ai/blog/kubernetes-labels-expert-guide-with-10-best-practices/)

透過 Kubernetes 於資源內所下的 Label，可以讓管理者更快地查找問題，一次將組態變更集體套用到多個資源，用來監控資源的使用狀況與成本，所以這篇文章要跟大家介紹 10 個使用 Label 的最佳實踐

- 使用 Kubernetes 本身推薦的 Label ([Reference](https://kubernetes.io/docs/concepts/overview/working-with-objects/common-labels/#labels)) 來對物件分群: K8s 推薦使用 app.kubernetes.io/name 和 app.kubernetes.io/instance 來代表應用程式的名稱和實例；假如是公司內部的應用服務，就可以使用自己公司的 subdomain 來取代 app.kubernetes.io 然後來客製化對應的 Label
- 注意 Label 的語法正確性: Label 是 Key Value 的組合，你必須使用 `<Prefix>/<Name>` 的格式來命名，其中 Prefix 是選擇性的，但假如要使用的話，要注意它必須是 DNS Subdomain 的格式，字數限制為 253 個字元，他可以讓團隊使用多個 Label 而不會產生命名衝突 (試想那些存在於第三方套件的 Label...)，其中 kubernetes.io 和 k8s.io 是 Kubernetes 針對內部核心元件所保留的 Prefix；Name 就是 Label 屬性名稱，例如可以使用 environment 來代表運行的環境，值得部分就可以用 production 或是 testing，Name 有一些使用需求，例如他不能是空的，字數限制為 63 個字元，開頭和結尾必須使用字母與數字 ([a-z0-9A-Z])，中間可以使用字母與數字和 -, _, . 符號混合
- 標準化的 Label 命名規則: 不同的團隊間必須要使用一致性的命名規則，不然花在維護 Label 的努力將會白費掉
- 避免不必要的 Label 變更: Label 是用來識別和選擇 K8s 中的資源用以達成排程，部署或是管理的目的，所以變更 Label 會造成深遠和不可預見的影響，例如你把某一群 Pod 的 App Label 從值 frontend 修改成 backend，K8s 就會認為你要把這些 Pod 重新部署到 backend 的節點上，這有可能會造成這些 Pod 開始 Crach，最終無法被存取；所以只要在絕對必要時才去修改 Label，並且在進行任何修改之前仔細的評估可能造成的後果，避免遭遇到不可預期的狀況
- 使用 Label Selector 來選擇資源: 透過使用相等性或是集合的操作來對資源做選擇，以相等性來說， = 和 == 都代表相等，!= 代表不相等，也可以透過逗號 , 將添加的多個 Label 區隔開來一起使用；而集合的操作有點像是 SQL 語法中的 IN，例如 app in (frontend, backend) 代表 app Label 擁有 frontend 或是 backend 的資源都會被選擇出來
- 不要將應用程式的資訊寫入 Label: K8s Label 主要是用來儲存物件的 Metadata，而不是用來當作應用程式的資料儲存區，因為 K8s 的資源的使用時間通常很短，而且跟應用程式沒有緊密的關係，Label 很快就會變的不同步而毫無用處
- 不要將機敏資訊寫入 Label: 假如有心人士可以存取你的 K8s 叢集，而你又把諸如密碼， API Credential 或是其他的機敏資訊寫入了 Label，那麼這些資訊就可以在明碼的情況下被輕易取得；建議應該要存放在 K8s Secret 而不是 Label 內，因為在 Secret 內至少是被編碼過的，而且只有需要的 Pod 才能夠去取得它，這樣一來，即使有心人士可以存取你的 K8s 叢集，也不會有機會直接看到這些儲存於 Secret 的機敏資訊 (自己覺得 K8s Secret 還是不夠安全，建議整合第三方的 Secret Management 工具，如 HashiCorp Vault)
- 將 Label 加到 Pod Template: 將必要的 Label 添加到運行資源的 Pod Template 中，如此一來 K8s Controller 便可以如你所期望地建立 Pod；目標是只建立對團隊可以帶來價值的 Label 就好，而不是浮濫的建立一堆沒有用處的 Label，建議從小處著手，一開始先在 Template 中建立一個必要 Label 的清單，例如用來識別資源的擁有者，資源運行的環境以及發布資訊
- 將 Label 的添加過程自動化: 自動化可以節省大量時間，當然對於標籤的管理也不例外，假如平常就有在使用 CI/CD Pipeline 的話，就可以輕鬆自動化為某些 Label 做橫向的管理工作；使用 CD 工具來添加 Label 是很明智的選擇，因為它可以確保 Label 的一致性，並且提高工程師的生產力，除此之外，也建議通過 CI 工作來檢查 Label 是否正確無誤，當 Label 遺失時就應該讓 CI 工作失敗並且通知相關負責的團隊來處理
- 使用 Label 來做成本監控: 標籤對於了解 K8s 的雲端使用成本很有幫助，其實不管是成本監控，資源分配和管理其實都仰賴著妥切的 Label 策略；當多個團隊共享同一個 K8s Cluster 時 (Multi-Tenant)，你就會需要使用相關 Label 來建立成本分佈報告，因為這樣做才可以獲知特定團隊，服務或是應用服務所耗費的成本，這對調查突然激增的使用成本相當地有幫助

### [Deploying Kubernetes resources in a specific order using Helm or werf](https://blog.werf.io/deploying-kubernetes-resources-in-a-specific-order-using-helm-or-werf-f8eb8c1a08)

假如希望部署 K8s 資源時可以使用某種順序去部署的話，通常是有點挑戰性的，有時候甚至必須要等待外部資源準備完成，假設今天你要部署一個應用服務好了，那就要先等一個外部的 Operator 建立好動態的 K8s Secret，再來開始初始化和設置資料庫，最後才能夠部署應用服務，這篇文章就要跟大家介紹如何使用 Helm 或是 werf 來解決這個問題

- 使用 Helm: 主要是透過 initContainers 來達成，透過 init container 來讓不同的元件之間有順序性的部署，講白話一點就是有個插入一個 until xxx; do sleep 1 done 的 shell script，這個 script 會一直去檢查某個相依資源是否存在，如果存在就會可以部署主體資源，如果不存在就會一直等待，直到相依資源存在為止，這樣就可以達到等待某個相依資源的目的
- 使用 werf: 首先必須要在 K8s 資源定義中加入 werf 相關的 annotations，這些 annotations 會告訴 werf 這些資源的權重，werf 會根據這些權重來決定資源的部署順序，這樣就可以達到資源部署的順序性