---
title: 第 166 期 DevOps 推薦文章
date: 2023-01-24
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Multi-cluster management for Kubernetes with Cluster API and Argo CD](https://aws.amazon.com/blogs/containers/multi-cluster-management-for-kubernetes-with-cluster-api-and-argo-cd/)

Cluster API 是個專門用來管理多種 Kubernetes 叢集的 CNCF 專案，而本篇介紹使用 Cluster API 和 Argo CD 管理多個 Kubernetes 叢集，示範的架構為在本機 Docker 裡建立 Kind 後安裝 Cluster API 和 Argo CD，並由它們管理背後多個 Kubernetes 叢集。裡面解釋了 AWS IAM 是怎麼授權、CNI 安裝情況以及最後部署簡單的 app。<!-- summary -->

### [Why Managing WAFs at Scale Requires Centralized Visibility and Configuration Management](https://www.nginx.com/blog/why-managing-wafs-at-scale-requires-centralized-visibility-and-configuration-management/)

現在越來越多企業等級的資訊團隊需要集中化式的 Web Application Firewall（WAF）管理監控工具，而 F5 NGINX Management Suite 可以快速以視覺化的方式排查分析，例如最嚴重的攻擊方式、機器人攻擊程度、使用的工具、被攻擊的機器或 CVEs 等等，除了分析外也可以快速集中式的部署新的 Policy 來阻擋攻擊。

### [Source Code Management Best Practices](https://devops.com/source-code-management-best-practices/)

Source Code Management（SCM）已經是老生常談了，但還是再談一次最佳實踐給大家溫習。
- 多 commit
- 確保 repository 都是最新的
- 詳細寫 commit message
- 在 commit 之前先好好審視所有變更
- 自動化 workflow 要設計好：前贅字要用 `feat` 或 `fix` 等等、使用者權限控管、誰有權限放行可以合併 commit
- 資安的設計也不能馬乎：基本的使用者權限、視覺化呈現使用者活躍紀錄、災難復原計畫等等