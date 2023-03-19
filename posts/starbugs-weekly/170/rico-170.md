---
title: 第 170 期 DevOps 推薦文章
date: 2023-03-21
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How to build, test and deploy your application using Azure and GitHub](https://devblogs.microsoft.com/devops/how-to-build-test-and-deploy-your-application-using-azure-and-github/)

當你使用的 git repository 是 GitHub、雲服務用 Azure 且剛好是用 Go 語言的話可以看看這篇入門部署教學，豐富詳盡的圖文手把手部署教學保證可以快速上手。

<!-- summary -->


### [Linkerd and ingress controllers: bringing the outside world in](https://www.cncf.io/blog/2023/03/15/linkerd-and-ingress-controllers-bringing-the-outside-world-in/)

Kubernetes Ingress 選擇繁多，為何 Linkerd 可以嶄露頭角呢？他帶來了無痛的 Service Mesh 使用體驗，但為了看到 client IP 我們還是得設定 `skip-incoming-ports` 不然就會看到 Linkerd 為連線的源頭。Linkerd 也會把封包送往 `Service` IP 而非 `Pod`，除非另外設定直接送往 `Pod` IP。文末也有提供 Linkerd 與其他受歡迎的 Ingress 工具比較，但不外乎都要設定的概念都大同小異。

### [How to use Kubernetes events for effective alerting and monitoring](https://www.cncf.io/blog/2023/03/13/how-to-use-kubernetes-events-for-effective-alerting-and-monitoring/)

Kubernetes `Events` 是常用但比較少探討的主題（就代表是直觀好用的設計），這些可以靠 Grafana agent + Loki 做監控，而 `Events` 常見的有：

1. 狀態改變：像是 `Pod` 有生成新的、pending、確定產生成功或失敗
2. 設定改變：像是節點水平擴張、垂直擴張的增加記憶體或硬碟等等
3. 調度：像是是否能夠下載容器 image、容器有沒有足夠的 cpu or memory 或容器 liveness or readiness 探針採樣失敗

Events 的種類則有：

1. 失敗
2. 驅逐
3. 調度失敗
4. 硬碟
5. 節點