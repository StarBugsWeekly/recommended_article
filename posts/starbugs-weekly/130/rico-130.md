---
title: 第 130 期 DevOps 推薦文章
date: 2022-04-26
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [New Wave for Helm!](https://medium.com/wriketechclub/new-wave-for-helm-b9800733587f)

作者原本使用 helmfile 來管理 Kubernetes 的部署，也很喜歡裡面的諸多的功能，不過作者依舊尋找更好的工具。作者認為 helmwave 除了常見的 everything as code 的功能外，還有循序部署、即時追蹤 Kubernetes resources、不需要額外的工具就可以直接使用 helmwave，很多測試工具如 kube-linter、Kubeval、Pluto 都可以整合，還有一個特色就是使用體驗跟 docker-compose 很像。<!-- summary -->

### [Stop Using Branches for Deploying to Different GitOps Environments](https://medium.com/containers-101/stop-using-branches-for-deploying-to-different-gitops-environments-7111d0632402)

此推薦文章和下篇是同一系列，作者講述很多組織在使用 GitOps 如何在同一個 release 前進到下一個環境是大家一直探討的，因為答案有很多種，所以作者就索性說明哪些我們應該避免：

1. 依環境分 git branches 只適用於 legacy applications（這裡指的是傳統 git-flow），採用 trunk-based 並且用依環境用 feature flag 來控制，application code 和 configuration code 也建議放在不同 repository
2. 前進到下個環境從來不是只有 git merge 這麼簡單，兩次的 merge 都修改同一個地方時有可能會被忽略而 merge 進去了，hotfix 時的 cherry-picks 也得小心使用
3. 依照環境分 branches 不太適合 Helm/Kustomize，因為它們並不會知道 git branches、git merge 或 pull request，因為他們都是靠檔案做環境分類

### [How to Model Your Gitops Environments and Promote Releases between Them](https://medium.com/containers-101/how-to-model-your-gitops-environments-and-promote-releases-between-them-ff40fd3008)

接續上篇，作者持續探討 GitOps 如何順利地 release 在各個環境中：

1. 要先了解你維護的服務
2. 五個範例來解釋每次的變更對環境的互動
3. 如何初始化新的部署
4. 對照不同環境的設定
5. 要如何 release 在不同的 GitOps 環境
6. 更改設定就要改全部的環境
7. 環境依照資料夾來分的好處
8. 如何在 GitOps 環境中使用 Helm
9. 大型組織可以考慮依環境分 repository
10. 環境分類請愛用資料夾，而非 branches
