---
title: 第 135 期 Kubernetes 推薦文章
date: 2022-05-31
author: smalltown

layout: layouts/post.njk
tags: [Kubernetes]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Kubernetes

<!-- summary -->
### [Automate All the Boring Kubernetes Operations With Python](https://betterprogramming.pub/automate-all-the-boring-kubernetes-operations-with-python-7a31bbf7a387)

隨著 K8s 的普及度越來越高，大家日常工作上使用到的時間應該也越來越多，因此這篇文章介紹了如何利用 Python K8s Client Library 自動化一些日常維運 K8s 常常會做的操作

<!-- summary -->

### [Kubernetes ephemeral container security](https://www.cncf.io/blog/2022/05/24/kubernetes-ephemeral-container-security/)

假如你需要除錯一個 K8s Pod 但是基於安全考量不能夠在其中任意安裝除錯工具，那該如何怎麼辦呢？！好加在 Kubernetes 介紹了一個叫做 Ephemeral Container 的概念來應付此種狀況，透過這篇文章的介紹來了解如何使用此功能

### [Don't Write Your Own Kubernetes YAML Generator](https://matduggan.com/tips-for-making-kubernetes-yaml-less-annoying/)

維運 K8s 的人其實不太需要撰寫程式，但一定會許要撰寫 YAML 檔案來對 K8s Cluster 進行配置，這篇文章在開頭便提出作者為什麼不建議使用 YAML Generator 來做這件事情，而是可以準備好簡易的 YAML 檔案之後，再透過 yq, Kustomize 去做修改，甚至可以透過 client libary 來配置 K8s Cluster