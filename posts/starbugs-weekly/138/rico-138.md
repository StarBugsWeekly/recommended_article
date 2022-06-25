---
title: 第 138 期 DevOps 推薦文章
date: 2022-06-28
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Kubeconfig File Explained With Practical Examples](https://devopscube.com/kubernetes-kubeconfig-file/)

一開始接觸 Kubernetes 想必有很多人會疑惑自己的電腦到底是怎麼連線到 Kubernetes cluster API？其實就是靠 kubeconfig。這篇文章以實際的例子介紹 kubeconfig 的使用方法，例如：怎麼靈活運動 kubeconfig、如何 merge kubeconfig、如何生產 kubeconfig（很多 cloud provider 在這方面都把使用者體驗做得很好）以及一些 FAQs 讓讀者更了解 kubeconfig 知識。<!-- summary -->

### [Continuous Operations is the Unsung Hero of DevOps](https://thenewstack.io/continuous-operations-is-the-unsung-hero-of-devops/)

這篇文章的標題「持續維運（Continuous Operations）是 DevOps 文化裡的無名英雄」只要是身為第一線維運人員應該感同身受，其中的概念就提到應該把維運自動化到期望的設定狀態，讓維運人員可以專心在複雜的問題上，或者系統可以持續的掃描和修正錯誤。而持續維運可以解釋為 infrastructure 的持續交付（Continuous Delivery），如果使用 public cloud provider 和 Infrastructure-as-Code 就很容易，但是如果是 on-premises 環境就得花更多心力。

### [How to run untrusted containers in Kubernetes](https://blog.sighup.io/how-to-run-untrusted-containers-in-kubernetes/)

我們都知道 container 的隔離性還是有限，所以才會開始有在 Kubernetes 裡跑虛擬機的做法，只要虛擬機有按照 CRI（Container Runtime Iterface）的標準就可以。這邊介紹的 gVisor 可以提供虛擬機環境給 container，讓每個 container 的 kernel 都是獨立的，可以提供更好的獨立性。