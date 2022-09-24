---
title: 第 151 期 Cloud 推薦文章
date: 2022-09-27
author: smalltown

layout: layouts/post.njk
tags: [Cloud]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Cloud

<!-- summary -->
### [AWS vs GCP reliability is wildly different](https://freeman.vc/notes/aws-vs-gcp-reliability-is-wildly-different)

雖然公有雲用起來讓人覺得它像是不存在一般，例如你可以隨時開關一台機器，而且只需要根據使用量付費，彷彿就像是背後有無窮無盡的資源一樣，但其實事實並非如此，他背後也是實體機房，也會受到晶片短缺的影響才對 (尤其是 GPU)，作者在 GCP 遇到機器開很慢的狀況之後，就想要來試試看同時對 AWS 與 GCP 做開大量 GPU 機器的壓力測試

實驗方式為在兩週內兩個平台都各自開了 3,000 T4 GPUs，假如開啟時間超過 200s 就算 Timeout，實驗結果 AWS 大勝，平均一個 GPU 在 15秒內 (平均 11.4 秒)，GCP 在 45 秒內 (平均 42.6 秒)，AWS 在兩週內遇到一次明顯的開機 Timeout，而 GCP 則是 84次，結論就是 AWS 的開機時間比 GCP 快 66% 並且少 84 倍遇到開機 Timeout 的機會

<!-- summary -->

### [Why you should keep using CPU limits on Kubernetes](https://dnastacio.medium.com/why-you-should-keep-using-cpu-limits-on-kubernetes-60c4e50dfc61)

大家應該都知道 K8s 的 Workload 可以設定資源的限制，Memory 比較沒有問題，但是對於 CPU 的 Limit 到底要不要設定？前一陣子有一篇文章請大家停止設定 CPU Limit 引起熱烈迴響，文章一開頭就提到在大多數情況之下，設定 CPU Limit 利大於弊 ([For the love of god, stop using CPU limits on Kubernetes (updated)](https://home.robusta.dev/blog/stop-using-cpu-limits/))；過了一個月之後，也就是這篇文章的作者則是提出反面的看法，他認為 CPU Limit 仍然是有其必要性的，並且提出了一些理由，大家覺得究竟要不要設定呢？

### [Best Tools to Visualize your Terraform](https://medium.com/@mike_tyson_cloud/best-tools-to-visualize-your-terraform-d4b537f091dc)

很多人目前都是使用 Terraform 來做雲端資源做管理，不過畢竟人類是視覺性的動物，所以如果能夠將 Terraform 的資源以視覺化的方式呈現出來，那麼就能夠更容易的理解資源的關係，這篇文章介紹各種可以將 Terraform 程式碼視覺畫的工具，讓大家可以將 Terraform 的資源以視覺化的方式呈現出來

- Brainboard
- Terraform 原生指令
- Blast radius
- Terraform Visual
- Inframap
- Rover
- Diagrams codes
- Structurizr
- Diagrams Mingrammer
- Cloud discovery