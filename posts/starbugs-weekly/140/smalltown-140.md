---
title: 第 140 期 Kubernetes 推薦文章
date: 2022-07-12
author: smalltown

layout: layouts/post.njk
tags: [Monitoring]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Kubernetes

<!-- summary -->
### [How Virtual Kubernetes Clusters Can Speed Up Your Local Development](https://loft-sh.medium.com/how-virtual-kubernetes-clusters-can-speed-up-your-local-development-e5645614a3c5)

[vcluster](https://github.com/loft-sh/vcluster) 是 Loft 的一個專案，他可以將一個虛擬的 K8s Cluster 建立在實體 K8s Cluster 的一個 Namepsace 中 (感覺好像在繞口令)，換句話說就是 Host K8s Cluster -> Namespace -> Virtual K8s Cluster！而這篇文章則是要跟大家介紹如何利用 vcluster 來加速本地端開發流程
<!-- summary -->

### [How to scale down Kubernetes cluster workloads during off-hours](https://tanmay-bhat.medium.com/how-to-scale-down-kubernetes-cluster-workloads-during-off-hours-fe4bc477ed51)

K8s 有沒有可能根據時間把叢集變小？為什麼會想要這樣做呢？因為作者所為維護的服務其實在下班時間沒有什麼流量，尤其在週末更是慘澹，所以假如可以根據時間把 K8s Cluster 縮小的話，就可以解省很多的經費，所以他想要跟大家介紹一個叫做 [Kubernetes Downscaler](https://codeberg.org/hjacobs/kube-downscaler) 的開源專案，讓 K8s 可以根據使用者需求節能省碳

### [Cubernetes](https://www.justingarrison.com/blog/2022-07-06-cubernetes/)

有在研究自架 K8s 的人應該有聽過 [Amazon EKS Anywhere](https://aws.amazon.com/blogs/containers/getting-started-with-eks-anywhere-on-bare-metal/)，而作者就利用這個專案花了幾個月的時間自幹的一座 K8s Cluster，並將其取名為 Cubernetes，文中詳細地描述了如何完成這台機器的詳細過程，看起來滿酷的，會有人也想要跟作者一樣也自己來一台嗎XD