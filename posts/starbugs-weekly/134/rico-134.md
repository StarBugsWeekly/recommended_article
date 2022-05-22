---
title: 第 134 期 DevOps 推薦文章
date: 2022-05-24
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [The most important changes in Kubernetes 1.24 and why they matter](https://www.padok.fr/en/blog/new-kubernetes-changes)

作者幫大家重點整理了新版 Kubernetes 1.24 重要的 7 點改動。最知名的改動不外乎就是 Dockershim 正式的被移除了，雖然裡面寫 Docker 正式不能被使用，但事實上還是有辦法使用，Docker 有推出 cri-dockerd 版本，<!-- summary -->詳情可以參考我們 Starbugs 131 期寫的[文章推薦](https://weekly.starbugs.dev/2022/05/03/131-may-day/)。

還有其他重要的功能如：新的 OOM metric、指定 Load Balancer 類型可以改用 LoadBalancerClass 而不是難設定的 annotation、不能指定 Load Balancer 的 IP address（即便在某些商業需求下很好用）、service account token 為了安全將開始有些限制、RuntimeClass.Overhead 正式進入 stable version 讓 pod 可以設定 cpu + memory、以及 Kubernetes 團隊決定所有 beta 的 API 都不再是預設值（得另外 enable 才行）。

### [My First Honeypot](https://medium.com/@williamlaw2991/my-first-honeypot-f7bfb1d1079a)

作者自己架設了兩種 honeypot 程式來吸引網路上的攻擊並且加以分析，第一個工具 Cowrie 可以看出攻擊者會想要知道系統的基本硬體資訊如 cpu、memory 或硬碟大小等等，也會嘗試使用 Linux 常見的帳號和密碼登入，攻擊者會安裝 busybox 看能不能控制整台機器，當然想盡辦法安裝挖礦軟體也是不可少的，作者也分析攻擊者的 IP 國家位置。

第二種 honeybot 工具 ADBhoney 用來模擬 Android 裝置，像是手機或電視，可以看出攻擊者也會想要安裝挖礦程式、惡意程式，攻擊者也會偷寫檔案在系統裡來判斷這台機器攻擊過了沒，並且保持挖礦或惡意程式是否運作正常。

### [Why Run Postgres in Kubernetes?](https://containerjournal.com/kubecon-cnc-eu-2022/why-run-postgres-in-kubernetes/)

作者解釋普遍業界並不鼓勵直接把 Postgres 安裝在 Kubernetes，但是 Data on Kubernetes 2021 研究顯示 90% 的技術主管認為 Kubernetes 已經準備好跑 stateful 的程式，而且也可以在 Kubernetes 的各種機制上獲得好處，例如更低的災難復原時間，甚至 CICD 也可以有很好的 integration test 整合。
