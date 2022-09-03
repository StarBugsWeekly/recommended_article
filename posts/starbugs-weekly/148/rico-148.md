---
title: 第 148 期 DevOps 推薦文章
date: 2022-09-06
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How to Handle Kubernetes Health Checks](https://doordash.engineering/2022/08/09/how-to-handle-kubernetes-health-checks/)

DoorDash 在黑色星期五因為 readiness health check 而導致服務不正常，他們一開始從 metrics 和 tracing 做調查但因 health check request 導致呈現的資訊很雜，最後不得已才去 log 抓出問題。因用 Spring Boot Framework 預設的 health check，而預設它會一次檢查很多地方，其中一個就是 Redis 且剛好檢查的 path 已經是 legacy 的狀態了，所以服務延遲增加導致危機。最後他們有探討應該深度了解 health check 的行為，以及觀測服務應該要消除 health check 雜訊。<!-- summary -->

### [Kubernetes Removals and Major Changes In 1.25](https://kubernetes.io/blog/2022/08/04/upcoming-changes-in-kubernetes-1-25/)

Kubernetes 1.25 重要的變動有 PodSecurityPolicy 正式被移除因為使用體驗容易讓人困惑，其功能將被 Pod Security Asmission 取代；In-tree CSI （意思是指和 Kuberentes 專案寫在一起的 CSI 功能）將拆出來交給其他專門做儲存廠商的專案；IPTables 裡這些 `KUBE-MARK-DROP`、`KUBE-MARK-MASQ` 和 `KUBE-POSTROUTING`  chains 照理上來說只限於給 Kubernetes 使用才對，但是卻有些工具卻會依賴這些 chains 的行為，所以現在要漸漸改成這些 chains 只給 Kubernetes 內部情境使用。

### [Kubernetes 1.25: cgroup v2 graduates to GA](https://kubernetes.io/blog/2022/08/31/cgroupv2-ga-1-25/)

Kubernetes 1.25 版本的 cgroup v2 邁向 GA（general availability），新版本有更好的資源配置外，升級也十分輕鬆，只要 worker node 的作業系統 cgroup v2 是預設的、以及 container runtime 也有支援以及 kubelet 和 container runtime 設定使用 cgroup driver 就可以無痛升級了（強烈建議 cgroup driver 使用 systemd 來運行）。另外升級完畢後也務必更新監控或開發語言的版本以便支援 cgroup v2。
