---
title: 第 127 期 DevOps 推薦文章
date: 2022-04-05
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [CNCF Argo Project 2022 User Survey Results](https://blog.argoproj.io/cncf-argo-project-2022-user-survey-results-f9caf46df7fd)

作者帶大家看 CNCF 2022 年使用者對 Argo 專案的社群回饋報告，樣本數為 147 份，其中 92 份來自 CD/Rollouts，55 份為 Workflows/Events：
<!-- summary -->

Argo CD/Rollouts：

* 所有的調查回覆中有 80% 已經把 Argo CD 用於生產環境超過 6 個月
* NPS 分數（Net Promoter Score，調查的方法類似為 0-10 分你有多推薦 Argo CD）為 74，比去年還多 4 分

Argo Workflows/Events

* 所有的調查回覆中有 75% 已經把 Argo Workflows 用於生產環境，50% 表示在生產環境超過 6 個月
* NPS 分數落在 48 分

另外也有描寫什麼角色會使用這些工具、生產環境的詳細使用時間、使用數量、生態等等。

### [Why Let’s Encrypt is a really, really, really bad idea…](https://medium.com/swlh/why-lets-encrypt-is-a-really-really-really-bad-idea-d69308887801)

Let’s Encrypt 雖然方便，但其實當全世界的網站把雞蛋放在同一個籃子裡是有風險的，在資安的角度來看，CAs 的碎片化——也就是說憑證散落在各個供應商是件好事，而非 bug 一樣的存在。如果想要改善的話可以從三點著手：

1. 網站架設完就完全不用煩惱憑證的方案是不存在的，盡量避免「免費」或「方便」的方案
2. 要注意憑證商負責保護網站的哪些部分，且使用憑證供應商的工具發出 CSR（certificate signing request）
3. 可以考慮向憑證供應商保保險

### [3 Must-Haves When Implementing DevSecOps](https://devops.com/3-must-haves-when-implementing-devsecops/)

DevSecOps 這個詞已經不陌生了，但實踐時要注意哪些呢？作者講解和秀出例子來佐證 DevSecOps 的重要性，並表示要順利的導入組織必須要有三大要點，教育、流程和工具都要到位才行。
