---
title: 第 175 期 DevOps 推薦文章
date: 2023-05-30
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [4 Tools that Make it Easy to manage your Kubernetes Cluster](https://medium.com/@onai.rotich/4-tools-that-make-it-easy-to-manage-your-kubernetes-cluster-be252847cd85)

作者介紹了四個 Kubernetes 工具，K8sgpt、K9s、Lens 和 Rancher。其中最吸引的莫過於 K8sgpt，他會掃描整個 Kubrenetes 叢集後給予人性化的 troubleshooting 解答，也可以讓非維運人員看懂哪裡出問題。
<!-- summary -->

### [Recover your Amazon EC2 instance when SSH key pair is lost](https://awstip.com/recover-your-amazon-ec2-instance-when-ssh-key-pair-is-lost-fd0626d02c19)

新手剛開始使用 AWS 有很高機率遺失 ssh key，這篇文章一步一步帶著讀者怎麼挽救，原理就是把原本機器上的硬碟掛載到另外一台機器上（中間有許多小障礙文章都有解法），之後把新的 .ssh/authorized_keys 複製到硬碟上，再把硬碟掛載回舊的機器即可用新的 ssh key 連線到舊機器了。

### [How to Learn Linux Shell Scripting for DevOps?](https://devopscube.com/linux-shell-scripting-for-devops/)

Linux shell script 是到哪裡都很萬用的工具，作者彙整了有關 shell script 學習資源、現實場景的範例、可能需要 shell script 的場景或面試時可能會遇到的問題。
