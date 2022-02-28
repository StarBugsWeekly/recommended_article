---
title: 第 122 期 DevOps 推薦文章
date: 2022-03-01
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [[DevOps] Create your first CI/CD pipeline!!](https://faun.pub/devops-create-your-first-ci-cd-pipeline-ed054ba1404f)

CI/CD Pipeline 要將新版本軟題發佈所必須要執行的一連串步驟，它透過監控和自動化來改善應用程式開發的流程，特別是在整合跟測試的階段，當然還有交付跟部署，雖然 CI/CD 的所有步驟都可以手動執行，但 CI/CD 真的的價值需要透過自動化才能體現，所以作者將自身經驗和詳細設定過程透過這篇文章<!-- summary -->介紹分享給大家

主要使用到的工具為 Ubuntu EC2, Java, Jenkins, Maven, Tomcat, Docker, Jira 和 DefectDojo，談到 Build, Test, Release, Deploy 以及 Validation 和 Compliance，過程鉅細彌遺，很適合初學者跟著一起試試看


### [Chaos Mesh moves to the CNCF Incubator](https://www.cncf.io/blog/2022/02/16/chaos-mesh-moves-to-the-cncf-incubator/)

CNCF Committee 最近投票通過接受 Chaos Mesh 成為 CNCF Incubating 專案，Chaos Mesh 是一個功能眾多的 Chaos Engineering 平台，讓 Chaos 可以在 Kubernetes 的環境中實驗，自從在 2020 年七月成為 CNCF Sandbox 之後，他已經釋出兩個主要大版本更新 (v1.0 和 v2.0) 和 30 幾個次要更新，這些改動讓他在觀測，功能和安全性上帶來重大的改善，感覺是個滿有前景的專案，可以投資一點時間在上面

### [1Password for SSH & Git (Beta)](https://developer.1password.com/docs/ssh/)

自己本來就有購買 1Password 供個人使用，不然不好做到不同網站的密碼又複雜又相異，兩天看到 1Password 的文章發現竟然釋出 SSH 的功能，以後就可以把 SSH Key 也存在 1Password 裡面，都過他去存取 Git 或是 SSH 到其他的伺服器內，目前已經有支援 Mac, Linux 跟 Windows，有使用 1Password 的人可以趕緊一起來使用看看 😊
