---
title: 第 147 期 ArgoCD 推薦文章
date: 2022-08-30
author: smalltown

layout: layouts/post.njk
tags: [ArgoCD]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## ArgoCD

<!-- summary -->
### [ArgoCD ApplicationSet Generators](https://argocd-applicationset.readthedocs.io/en/stable/Generators/)

在 ArgoCD ApplicationSet 推出不久後就開始使用了，那個時候只有三個 Generator，分別是 Cluster Generator, Git Directory Generator 和 Git File Generator ([當時寫的 ArgoCD ApplicationSet 詳細介紹文](https://medium.com/starbugs/argo-cd-applicationset-controller-%E4%B8%96%E7%95%8C%E7%82%BA%E6%88%91%E8%80%8C%E8%BD%89%E5%8B%95-a837f9392298))，在經過一年多後，現在 Generator 多了不少類型，讓 ApplicationSet 變得更加完整且實用，底下稍微提一下這些新增的 Generator 分別可以達成什麼目的：<!-- summary -->

👉 Matrix Generator: 可以把兩種基礎 Generator 混合使用
👉 Merge Generator: 讓使用者先採用的基本 Generator，然後再透過其他 Generator 獲得的參數來做覆寫 (感覺使用時要小心)
👉 SCM Provider Generator: 用來產生 ArgoCD 所定義的 Repository 資源 (可以把同一個 Git Organization 底下的所有 Repository 都撈出來)
👉 Pull Request Generator: 當 Git Pull Request 開啟時，根據 PR 的內容產生測試環境出來
👉 Cluster Decision Resource Generator: 用來產生 ArgoCD 所定義的 Cluster 資源

其中 Pull Request Generator 是我最喜歡的一個，因為如此一來就可以讓 ArgoCD 輕易地達成 Git Pull Request 的開發流程，而 SCM Provider Generator 和 Cluster Decision Resource Generator 自己覺得雖然放在 ArgoCD ApplicationSet 裡面有點突兀，，因為他並不是用來產生 ArgoCD Application，但確實是很實用的功能；除此之外 Git Generator 現在可以對 Path 做 Exclude，自己目前已經使用它來解決 Prometheus CRD 遇到的問題 ([GitHub Issue](https://github.com/prometheus-operator/prometheus-operator/issues/4439))

### [2022 Argo external security audit: Lessons learned](https://blog.argoproj.io/2022-argo-external-security-audit-lessons-learned-951f80e0450d)

Argo 團隊和 CNCF 在 2022 年初開始和 Ada Logics 對 Argo 的四個 Project 進行安全稽核，結果確認了 26 個問題，其中 7 個在 Argo CD， 6 個在 Argo Workflow，13 個在 Argo Events

這些問題當中存在著 9 個 CVE，有 7 個 在 Argo CD 以及 2 個在 Argo Events，至於其他的則被當成 non-CVE，詳細的稽核報告與 CVE 細解可以參閱內文，其中不乏有風險等級來到 Critical 和 High 的 CVE，所以大家一定要記得將使用到的 Argo 相關 Project 進行升級

### [Solving ArgoCD Secret Management with the argocd-vault-plugin](https://itnext.io/argocd-secret-management-with-argocd-vault-plugin-539f104aff05)

GitOps 在 2017 由 Weaveworks 提出後，目前已經毫無疑問成為管理 Kubernetes 的主流方式，而每次在 GitOps 相關主題的討論，分享，演講...等，其中一定會被人提出來的問題就是在 GitOps 的架構下要如何去做 Secret Management，而作者的團隊當初選擇使用的 GitOps 工具為 ArgoCD，Secret Management 則為 HashiCorp Vault，在遍尋了既有的工具之後，發現採用的障礙都很高，甚至需要手動加密或是安裝其他的 Operator 來達成，並沒有找到符合自己團隊需求的解決方式

所以他們就決定自己建立自己的工具，也就是 argocd-vault-plugin，他們透過 ArgoCD 的 Custom Plugin Patten 來開發這個工具，透過他就可以從 HashiCorp Vault 取得 Secret，並將其注入到 Kubernetes 的 YAML 檔案內，實際安裝與使用方式可以參閱內文，這個工具在去年二月誕生，去年五月發布 V1.0 時也一併支援了 AWS Secret Manager([Reference](https://itnext.io/introducing-argocd-vault-plugin-v1-0-708433294b2d))，專案也持續活躍的更新當中 ([GitHub Repository](https://github.com/argoproj-labs/argocd-vault-plugin))，最近也有看到[其他人的文章](https://piotrminkowski.com/2022/08/08/manage-secrets-on-kubernetes-with-argocd-and-vault/)在分享這個工具，分享給有需要將 ArgoCD 與 HashiCorp Vault 整合在一起的人