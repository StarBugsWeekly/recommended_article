---
title: 第 106 期 DevOps 推薦文章
date: 2021-11-09
author: smalltown
layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps
<!-- summary -->
### [Just 7 Remarkable K8S Tools Boosting Up Your Effectiveness](https://getbetterdevops.io/7-essential-tools-to-be-more-efficient-on-kubernetes/)

Kubernetes 是目前負責管理 Container 和微服務的的主要平台，一般人在開始學習跟 K8s 互動時都是透過 `kubectl`，它的確也真的扮演著很重要的角色，不過不知道使用者是否發現透過他一直在重複著一樣的動作，因而浪費掉寶貴的時間，所以這篇文章要介紹 7 個可以幫助使用者增進效率的工具：
<!-- summary -->
1. [Kube-shell](https://github.com/cloudnativelabs/kube-shell): 透過顯示豐富的資訊和提示來減少使用 kubectl 時可能產生的錯誤並且加快操作速度
2. [Kubectx - Kubens](https://github.com/ahmetb/kubectx): 管理 Multi-Cluster 的必備工具，協助使用者切換不同的 Cluster
3. [Kubetail](https://github.com/johanhaleby/kubetail): 功能有點像是 `kubectl logs -f`，但可以一次將多個 Pod 的 Log 同時顯示
4. [Kubetree](https://github.com/ahmetb/kubectl-tree): K8s 的某些資源間其實是有親子關係的，透過此工具可以將資源間的關係視覺化呈現出來
5. [K9S](https://github.com/derailed/k9s): K9S 應該就不用多說了，強大的 K8s Terminal UI，讓你可以輕易地與 K8s Cluster 互動
6. [Kube-Capacity](https://github.com/robscott/kube-capacity): 顯示 K8s Cluster 中 Resource 的 Request, Limit 和使用程度
7. [Lens](https://k8slens.dev/): Lens 應該也是大家都耳熟能響的 K8s UI 工具，可以運行在各種系統中 (Windows, Linux 和 Mac)，讓使用者可以透過類似 IDE 的感覺來跟 K8s 互動

### [Compliance in a DevOps Culture](https://martinfowler.com/articles/devops-compliance.html)

將 Compliance Control 和 Audit 整合進 CI/CD 的流程，對於想要在 DevOps 文化中滿足 Security Compliance 是滿直覺的作法，但根據不同的組織大小會遭遇到不同的挑戰，了解透過不同的實作方式所可能造成的影響是導致成功與否的重要關鍵，文中從理論開始談起 (講解得很細)，隨後提到各種模式，例如：Manual Compliance, Pipeline Compoiance, Composition Compliance 和 Point-of-Change Compliance，對於這塊領域有興趣的人可以參考看看

### [Anatomy of a Terminal Emulator](https://www.poor.dev/blog/terminal-anatomy/)

Terminal 是一個無所不在的平台，多年來一直相當穩定地存在著，雖然目前有大量的資源可以用來理解 Terminal 的內部運作方式，但其中大多數要嘛相當的神秘，或是需要特定領域的深入知識，所以這篇文章希望提供一個平易近人且相對廣泛容易了解的內容，來讓大家知道要開發一個 Terminal Emulator 平台時需要具備的知識
