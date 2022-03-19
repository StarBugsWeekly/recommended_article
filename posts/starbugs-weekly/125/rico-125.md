---
title: 第 125 期 DevOps 推薦文章
date: 2022-03-22
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [A better alternative for Docker Desktop?](https://medium.com/@oribenhur/a-better-alternative-for-docker-desktop-3e8fa38d618)

我想不少公司應該有認真考慮過 Docker Desktop license 付費的問題，這篇分享作者在使用多個方案後決定使用 Rancher Desktop，選擇的理由不外乎社群活耀度、支援 docker 和 contained、支援 docker-cli 和 nerdctl、支援 Apple M1 以及支援 build-in local volume mounts，會特別強調 local volume mounts 是因為 Podman 不太支援這點。
<!-- summary -->
作者介紹了兩種安裝 Rancher Desktop 的方法，一個是從 shell script 安裝，另外一種比較簡單許多，直接下載 .dmg 檔案。

### [Replace Docker Desktop with lima](https://medium.com/itnext/replace-docker-desktop-with-lima-88ec6f9d6a19)

這篇介紹另外一個取代 Docker Desktop 的選擇 Lima，作者也表示他嘗試了一下 Podman 發現 local volume mount 的問題（而且這個 issue 從 2020 就已經有了）。Lima 安裝的 script 看似很複雜但其實只是一些簡單的設定，例如：為了連線而改 hostname、設定 rootless container 以及必要的 healthcheck 等等。

附帶一提的是，不論是 Rancher Desktop 或 Lima 都有支援 docker-compose。

### [5 unusual Docker container use cases](https://medium.com/itnext/5-unusual-docker-container-use-cases-547804d64c35)

介紹 5 種平常不會用到的 container 用法，不過老實說這 5 種我就蠻常用其中 3 種，讓我們來看看哪些你也中了吧：

* 跑真正有 UI 的 container
  * 裡面舉例了相片管理軟體 [digikam](https://www.digikam.org/)、瀏覽器或 Libre Office 等等都可以跑 container。
* 跑 Linux 桌面版的 container
  * 跟上一個用法有點雷同，Linux 桌面是從網頁去看的，也剛好有 Youtuber 拍實際跑起來的[影片](https://youtu.be/Gd9bvdkIXOQ)。
* 把 container 當作指令
  * 個人蠻常用的，畢竟有的時候不會想要安裝太多在自己的電腦裡。不過作者在這裡描述的是想要更高客製化的執行環境，他的[另外一篇文章](https://itnext.io/portable-kubernetes-management-with-kubectl-in-docker-cb861a2c3c02)裡就有寫為了執行 kubectl 所安裝的一系列環境。
* 把 container 當作開發環境
  * 也算是很常用的場景，畢竟 Apple M1 還是處處受限制，也剛好有 Gitpod 這個 SaaS 選擇。
* 把 container 當作 Kubernetes 環境
  * 有在使用 Kubernetes 的人一定不陌生這個使用方法，雖然不比真實的 Kubernetes，但是可以快速驗證一些基本的想法或除錯。