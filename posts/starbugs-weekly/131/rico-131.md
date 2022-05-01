---
title: 第 131 期 DevOps 推薦文章
date: 2022-05-03
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [New Relic Report Shows Lots of Java Apps Running in Containers](https://containerjournal.com/features/new-relic-report-shows-lots-of-java-apps-running-in-containers/)

[2022 年 New Relic 報告](https://newrelic.com/resources/report/2022-state-of-java-ecosystem)指出許多組織 Java 服務逐漸轉換成 container，而且每個服務有變微服務的趨勢。整體而言，Java 11 佔將近 48%，然而 Java 8 依舊佔了 46%。另外 Java Development Kit（JDK）也有增加的趨勢，在 AWS 上跑的 Java 服務 JDK 佔了 22% 而 Oracle 佔了 35%，與 2020 年相比，Oracle 曾經有 75% 的佔比。<!-- summary -->除了 Java 程式本身，也討論了大型企業雖然很慢但還是有在做變化甚至從地端轉化到雲上，幸好許多 Cloud Native 工具像是 OpenTelemetry 可以幫助組織監控服務的狀態，讓企業轉化可以更順利，並且以後 Open Source 跟商用軟體混用會更盛行。

### [Kubernetes volume backup for disaster recovery](https://medium.com/@amitabhprasad/kubernetes-volume-backup-for-disaster-recovery-56a5facee7fe)

作者解釋 Kubernetes 災難復原雖然已經有 Velero 備份 volume，但是 Velero 每次都是完整的備份，當資料越來越多時恐會影響到復圓所需的時間（RTO）。作者幫大家複習 PV、PVC、StorageClass 以及比較新的 VolumeSnapshotContent、VolumeSnapshot 和 VolumeSnapshotClass 技術概念，之後 demo 如何在兩個不同 region 的 Cluster 之間靠 snapshot 複製 volume。

### [Dockershim not needed: Docker Desktop with Kubernetes 1.24+](https://www.docker.com/blog/dockershim-not-needed-docker-desktop-with-kubernetes-1-24)

自從 Kubernetes 宣布棄用 Docker 後震驚業界，社群開始考慮其他替代方案，但其實 Docker 還是有推出新的 cri-dockerd 版本，也就是使用標準的 CRI 所做的 interface，這樣 Docker 跑起來跟其他替代方案無異了，以前的流程是：

kubelet -> cri-dockerd -> dockershim -> docker

新的版本則是可以不用 dockershim 了：

kubelet -> cri-dockerd -> docker
