---
title: 第 146 期 Terraform 推薦文章
date: 2022-08-23
author: smalltown

layout: layouts/post.njk
tags: [Terraform]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Terraform

<!-- summary -->
### [How to manage multiple environments with Terraform](https://blog.gruntwork.io/how-to-manage-multiple-environments-with-terraform-32c7bc5d692)

一開始使用 Terraform 來部署開發環境時可能沒有多想，東西也都可以正常運行，但當環境開始變多時，問題開始接踵而來，例如一堆重複的程式碼，環境之間的隔離性不足，很難去做 Debug 的工作...等，所以 Gruntwork 的 Co-founder 準備了三篇文章，分別解釋如何使用 [Terraform Workspace](https://blog.gruntwork.io/how-to-manage-multiple-environments-with-terraform-using-workspaces-98680d89a03e), [Git Branches](https://blog.gruntwork.io/how-to-manage-multiple-environments-with-terraform-using-branches-875d1a2ee647) 和 [Terragrunt](https://blog.gruntwork.io/how-to-manage-multiple-environments-with-terraform-using-terragrunt-2c3e32fc60a8) 來達成分離環境的做法，讓大家可以對這個主題有個全面的了解

<!-- summary -->

### [Manage your terraform like a container](https://medium.com/@dugouchet.a/manage-your-terraform-like-a-container-d2acbc46d7d4)

這篇文章繼續聊 Terraform 環境切分的問題，他覺得部署 Terraform 就像是使用 Container 一樣，大家應該已經習慣同樣一個 Container Image 建置出來之後供所有不同的環境一起使用，然後透過環境變數讓 Container 可以在不同的環境裡面運行成功；其實 Terraform 應該也要是一樣的做法，Terraform Module 要可以讓不同的環境一起使用，只透過不同環境的組態檔案就可以讓他去建置與管理不同環境與帳號的雲端資源

### [Design by Contract in Terraform](https://betterprogramming.pub/design-by-contracts-in-terraform-63467a749c1a)

在軟體開發中有一種設計方式稱為 Design by Contract (DbC)，這種方法要求軟體設計者為軟體組件定義正式的，精確的並且可驗證的介面，這樣，為傳統的抽象資料類型又增加了先驗條件、後驗條件和不變式。這種方法的名字裡用到的「契約」或者說「契約」是一種比喻，因為它和商業契約的情況有點類似 ([Wiki](https://zh.wikipedia.org/zh-tw/%E5%A5%91%E7%BA%A6%E5%BC%8F%E8%AE%BE%E8%AE%A1))；而 Terraform 在 v0.13 加入加了輸入參數的驗證功能，在最新 v1.2 也將 precondition 和 postcondition 這兩個功能給加了進來，如此一下在撰寫 Terraform Module 就可以使用 Design by Contract 的設計方式，詳細做法與範例可以參閱此文章


