---
title: 第 168 期 DevOps 推薦文章
date: 2023-02-21
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Back to Basics: Installing NGINX Open Source and NGINX Plus](https://www.nginx.com/blog/back-to-basics-installing-nginx-open-source-and-nginx-plus/)

想必不少人對 Nginx 的設定依舊一知半解，官方提供的基礎影片以有結構的方式介紹 Nginx 本身與使用，是時候重溫基本功了。除了 open source 版本，也順便介紹 Nginx Plus 的付費版本。

<!-- summary -->

### [How do you gracefully shut down pods in kubernetes](https://itnext.io/how-do-you-gracefully-shut-down-pods-in-kubernetes-fb19f617cd67)

當你從 terminal 裡下達 kubectl delete pod 時會發生什麼事？發出 request 到 kube-apiserver 後移除 etcd 裡 IP 和 port 的網路資訊，etcd 再通知 CoreDNS、kube-proxy 或 Nginx-ingress 等等也要移除網路資訊。之後節點上的 kubelet 也會收到刪除 pod 的通知開始動作，會先看 preStop 、SIGTERM 最後才強制使用 SIGKILL。

### [Secrets Management](https://dzone.com/articles/secrets-management-1)

密碼管理永遠是令人頭痛的點，此篇介紹一些該注意的點，不論是生產、測試、內部環境甚至服務本身以及 DevOps 相關的工具全部建議要有 RBAC、使用專門的密碼軟體和時常更新密碼，而且一個密碼軟體不太可能支援所有使用情境，所以選用正確的密碼軟體對應適當的情境。