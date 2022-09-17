---
title: 第 150 期 DevOps 推薦文章
date: 2022-09-20
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [6 Best Practices to Manage Pull Request Creation and Feedback](https://doordash.engineering/2022/08/23/6-best-practices-to-manage-pull-request-creation-and-feedback/)

建立好的 PR（Pull Request，或者也可以說 Merge Request）可以減少開發時間，除了要保持簡單、結構完整且一致性以及做好測試這三大基本要素之外，還建議以下幾點：<!-- summary -->
1. 命名時需要點敘述性和一致性
2. PR 名稱要清楚和描述
3. PR 的變動越小越好
4. PR 有爭議時請直接詢問對方，減少溝通時間
5. 動手做之前先做好功課來避免整個 PR 重寫
6. 多找一些人審查 PR

### [7 CNCF Projects For Building Cloud-Native Networks](https://containerjournal.com/features/7-cncf-projects-for-building-cloud-native-networks/)

本篇介紹 7 個用於建立 Cloud Native 類型網路的 CNCF 專案：
1. Antrea - 建立在 Open vSwitch 上的 Kubernetes 網路
2. Cilium - 基於 eBPF 的網路、資安和觀測的專案
3. Container Network Interface (CNI) - 專門用於 container 的 interface
4. CNI-Genie - 讓多個 CNI plugins 可以在運行時同時存在
5. Kube-OVN - 適用於大型企業的 Kubernetes 網路構造
6. Network Service Mesh - 混合多雲架構的 service mesh
7. Submariner - 可 `Pod` 或 `Service` 直接在不同 Kubernetes cluster 或不同雲之間互連

### [How Many Nodes for Your Kubernetes Control Plane?](https://thenewstack.io/how-many-nodes-for-your-kubernetes-control-plane/)

自架 Kubernetes control plane 需要幾個節點比較洽當？以 etcd 做為叢集狀態儲存工具時，2 個節點比 1 個節點還糟，因為很可能發生腦裂的情況，官方建議 3 或 5 個節點，超過 7 個可能有延遲問題。最後作者分別對 3、5、7、9 個節點做壓測證明延遲問題，以及假如有節點壞了，建議先移除之後再增加新的節點；但如果是節點沒壞，先增加新的節點之後再移除舊的。