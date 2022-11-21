---
title: 第 159 期 IaC 推薦文章
date: 2022-11-22
author: smalltown

layout: layouts/post.njk
tags: [IaC]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## IaC
### [The top programming languages](https://octoverse.github.com/2022/top-programming-languages)

從最近 GitHub 發布的統計結果發現用來達成 IaC 的 HCL (HashiCorp Configuration Language) 成為過去一年來成長最快的語言，主要是由於 Terraform 此工具的普及，加上自動化管理與部署基礎設施成為被大家廣泛接受的最佳守則，雖然有人覺得他其實不算是一個語言 ([Reference](https://news.ycombinator.com/item?id=33556902))，但不可否認 HCL 在基礎設施的管理幫助大家節省不少時間與降低人為疏失

<!-- summary -->

### [Infrastructure as Code’s Broken Promises](https://levelup.gitconnected.com/infrastructure-as-codes-broken-promises-4c9dc86f909c)

此篇文章的作者常常聽到 Infrastructure as Code 的好處就是採用之後可以解決掉所有管理基礎設施的問題，比起手動管理來的更簡單，寫出來的 IaC 可以被拿來測試，除此之外也可以節省更多的時間；但作者覺得總是有不預期的緊急事件會發生，環境會發生偏移，綜合他自己的經驗來說，基礎設施對比於一般靜態的應用程式就像是活著的生物一般，讓他覺得導入 IaC 之後人生也沒有變得比較簡單，要維護 IaC 反而讓一切變得更複雜而且要花更多的時間

留言提出不少正向的看法與建議，希望作者不要放棄 IaC XD
- 作者對於 IaC 有了錯誤的期待，IaC 並不是要讓任何人的生活變得更簡單，它是要讓基礎設施的管理工作有辦法被重複化，進而變得更可靠，最終提高擴展性
- 對待 IaC 也需要跟其他的程式語言一樣，你必須要有單元測試和整合測試，而且不要去接受環境偏移的發生，當因為緊急事件的發生不得以手動處理後，你要盡快讓一切的管理工作再次回到 IaC 的管控之下
- 雖然短期要花費比較多的時間和感到痛苦，但長期來說，你的基礎設施會變得更可靠，更容易被管理，進而讓你的團隊可以更專注在開發新的功能上

### [5 common pitfalls in Infrastructure as Code](https://itnext.io/5-common-pitfalls-in-infrastructure-as-code-3637ab6b02e0)

這篇文章作者跟大家分享使用 IaC 時常見五個陷阱，讓大家避免掉這些陷阱，讓 IaC 的管理更加順利

- Pets vs Cattle: 避免像對待伺服器或是基礎設施的固定資源一般，例如給予特定的名字與 IP；而是要將它們視為可以被快速替換的資源，這樣才能讓你的基礎設施更像是應用程序而不是實體伺服器
- Virtualized Data Center: 不要把實體資料中心的概念移植到 IaC 來，很多問題是雲端供應商自己要去擔心的，你應該 100% 的虛擬化的去使用它，例如可以使用多個供應商，根據需求來增加或減少資源達到成本最佳化，將服務的負載量分散到第三方服務去
- Not understanding relation between infrastructure and data: 因為害怕會遺失或是損害資料而導致 IaC 的採用率低下，其實可以透過簡單的分析來得知 IaC 要怎麼安全地應用在有正式環境資料的情境之下
- Breaking Dev and Ops: 透過 IaC 來打破 Dev 與 Ops 的藩籬，讓他們可以一起合作，擁有持續不間斷且自動化的流程
- Using IaC as fancy deployment scripts: IaC 並不是花俏的腳本語言，要從 IaC 中獲取最大的好處，就是要嘗試像對待一般的應用程式語言一樣來對待他，例如要有版本控制，它也要有自己的 CI/CD Pipeline