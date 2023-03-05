---
title: 第 169 期 DevOps 推薦文章
date: 2023-03-07
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How Spotify Adopted and Outsourced Its Platform Mindset](https://thenewstack.io/how-spotlify-adopted-platform-engineering-culture/)


Spotify 的 Platform Mission 團隊把全公司 6000 工程師連結起來合作更有效率，讓新員工更上軌道的資料、文件和工具其實都不是 Platform Mission 團隊創造的，都是輔助其他部門撰寫，行銷團隊也會行銷內部工具促成團隊之間的合作。也有關於每位員工的職責是什麼的文件好讓跨團隊合作，甚至也有內部的使用者體驗調查。

<!-- summary -->

### [The Broker Pattern & how it works](https://blog.devgenius.io/clean-architecture-s-broker-pattern-10bc08f57753)

一個大型架構勢必會有 borker 的存在，此篇撰寫了 borker 介紹、使用時機、功能和優缺點。基本上 borker 在現在架構中扮演重要的角色，可以讓 client 和 server 之間做解藕，減少依賴性，增加擴充性。

### [Introducing Patcher, a new tool for keeping infrastructure code up-to-date!](https://medium.com/gruntwork/introducing-patcher-a-new-tool-for-keeping-infrastructure-code-up-to-date-e65b0c203b6b)

IaC 使用套件的管理是鮮少人探討的，例如 Terraform 使用的 modules，而 Gruntwork Patcher 會幫忙查找是否有新使用的套件版本後決定是否更新，之後使用者可以審視變更並且部署。
