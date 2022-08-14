---
title: 第 145 期 DevOps 推薦文章
date: 2022-08-16
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [My Istiod Pod Can’t Communicate with the Kubernetes API Server!](https://thenewstack.io/my-istiod-pod-cant-communicate-with-the-kubernetes-api-server/)

作者示範以 Cilium 和 Istio 防止多個服務之間未經授權的連線，這次展示兩個不同版本的服務不應該能夠互相連線，基本上這個功能靠 Cilium 的 L4 network policy 就可以做到了。於是作者示範假如 pod 無法跟 Kubernetes API 溝通時怎麼辦？這時可以看到 Istio 的 L7 authorization policy 會擋下連線。另外這個示範在本機即可執行。<!-- summary -->

### [4 Ways to Optimize Your Workflows with Docker Extensions](https://thenewstack.io/4-ways-to-optimize-your-workflows-with-docker-extensions/)

Docker 桌面版最新釋出的擴充功能可以讓開發更加強大，受歡迎的擴充功能有：硬碟使用量、Tailscale（可以讓外網連線自己在內網環境本機的 container）、Logs Explorer 和 Slim.Ai（分析 container image），眾多擴充都可以在 Docker Marketplace 找到。

### [Dashboards as code: A new approach to visualizing AWS APIs](https://aws.amazon.com/blogs/opensource/dashboards-as-code-a-new-approach-to-visualizing-aws-apis/)

Steampipe 提供 Dashboard as Code 的概念讓使用者可以客製化 AWS dashboard，像是可以定義多個 regions 或多個 AWS accounts。文章裡示範如哪些 iam user 的 access key 的已經超過 90 天沒換，S3 在各個 regions 的數量，IAM user、group 和 policy 的關係，以及合規測試的 dashboard。