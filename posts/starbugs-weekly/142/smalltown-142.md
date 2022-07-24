---
title: 第 142 期 Terraform 推薦文章
date: 2022-07-26
author: smalltown

layout: layouts/post.njk
tags: [IaC]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Terraform

<!-- summary -->
### [Four Great Alternatives to HashiCorp’s Terraform Cloud](https://medium.com/@elliotgraebert/four-great-alternatives-to-hashicorps-terraform-cloud-6e0a3a0a5482)

Infrastructure as Code 也是程式碼，所以當然也需要 Continuous Integration，而大家應該馬上就會想到 Terraform Cloud 這個由 HashiCorp 所推出的服務，不過除了他之外還有其他的選擇嗎？有些人或許還知道一個開源的工具叫做 Atlantis，這篇文章介紹了其他幾個替代方案，分別是 Spacelift, Env0, Scalr, 和 Cloudify，從各個角度來做筆記與詳細介紹，對於 IaC 的 CI 有興趣的人，千萬不要錯過這篇文章！
<!-- summary -->

### [Terraform — Best Practices](https://medium.com/devops-mojo/terraform-best-practices-top-best-practices-for-terraform-configuration-style-formatting-structure-66b8d938f00c)

這篇文章介紹撰寫 Terraform 時建議的最佳實踐，從檔案架構開始談起，接著討論 Module 的結構，如何利用不同的資料夾來分離應用服務與環境，檔案命名規則，提高安全性的作法...等超多撰寫 Terraform 需要注意的地方，不管是剛開始學習 Terraform 或是已經接觸過 Terraform 的人，這篇文章都相當的實用！

### [How Terraform Works : Modules Illustrated](https://awstip.com/terraform-modules-illustrate-26cbc48be83a)

這篇文章透過清楚的圖片來說明 Terraform Module 是如何的運作，從 Root Module 和 Child Module 如何一起運行，Output 如何被 Module 所使用，都用詳細的圖解做說明，對於 Module 還不太熟悉的人可以透過此篇文章好好深入了解一下！
