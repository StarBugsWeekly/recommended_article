---
title: 第 113 期 DevOps 推薦文章
date: 2021-12-28
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [SLICK: Adopting SLOs for improved reliability](https://engineering.fb.com/2021/12/13/production-engineering/slick/)

相信大家或多或少應該都有聽過 SLO (service-level objectives) 與 SLI (service-level indicator)，Meta (Facebook) 為了能夠中心化管理與定義 SLI 與 SLO，他們建立一個叫做 SLICK 的工具，讓大家可以更簡單查詢與理解所有服務的可靠性；在使用 SLICK 之前，SLO 或是其他有關服務效能的 Metrics 通常儲存在客製化的儀表板，文件或是其他的工具內，假如你想要衡量一個團隊的 SLO，可能需要花上一個小時去搜尋，或是找人問東問西，而且 Meta 以前儲存 Metric 的系統並沒有保留太久的資料，導致幾乎不可能去分析週期比較長的 SLO，但自從使用 SLICK 之後可以達到四個目標：

1. 使用統一的方式對所有的服務定義 SLO
2. 擁有精準度為每分鐘且保存兩年的 Metric 資料
3. 對於 SLI/SLO 的 Metric 可以有一套標準的視覺化與搜尋方式
4. 提供週期性的可靠性報告給內部成員，讓團隊可以用來做可靠性檢查

更多詳細做法可以參考內文，看他還有提供一些 UI 截圖出來，比較可惜的是看起來並不是開源專案

<!-- summary -->
### [GitHub may replace DockerHub](https://levelup.gitconnected.com/github-may-replace-dockerhub-a5da5e547f01)

過去數年來 Docker 的崛起，讓大家一度以為 Linux Container 就叫做 Docker，因為他讓大家很輕易地就可以發布 Container 到免費的 DockerHub，不過作者認為將 DockerHub 視為 Container Image 唯一 Repository 的時代已經過去了，他覺得 GitHub 將會把這個第一名的寶座搶到手，因為 GitHub 目前算是開源專案的不二選擇，所有的開發者幾乎被他握在手中，而且他持續不斷地在加強 CI/CD 功能，改善 Issues, Documentation 還有架站功能，除此之外，近期對於 Package 儲存功能也越來越完整...等，因此他覺得 DockerHub 最後將會被 GitHub 所取代，大家也是這樣覺得嗎？


### [Web 1.0, Web 2.0 & Web 3.0 Explained](https://dev.to/narottam04/web-10-web-20-web-30-explained-591n)

最近 Web 3.0 這個詞彙突然很熱門！他究竟是什麼呢？這篇文章從 Web 1.0 Beta -> Web 1.0 -> Web 2.0 的定義開始解釋起，並且提出 Web 2.0 的缺點，也就是所有的使用者資料都集中在大公司手上，例如 Google, Facebook，他們靠著販賣大家的資料來賺大錢，而 Web 3.0 主要就是想要建立一個去中心化又安全的網路環境，讓人類可以使用它安全的交換金錢與資訊，而不再需要中介者或是大型科技公司，所以資料不再像 Web 2.0 集中儲存在單一資料庫內，而是像運行在區塊鏈內，Peer to Peer 的節點內的感覺，有人甚至預測在 Web 3.0 的架構下，每個人都會是內容擁有者，公司將會變成由去中心化的團體所運行，又稱為 DAO (Decentralized Autonomous Organization)，而不再需要 CEO 或是任何公司的高層管理組織，而且每個人都是匿名存在於 Web 3.0 中

有人認為 Web 3.0 只是加密貨幣交易者建立的騙局，然而也有人相信他是可能實現的想法，不過和 Blockchian 一樣，Web 3.0 都還在很早期的階段，所以未來會發展成什麼樣子還很難說...目前也還有很多未解決的問題，因此還有很長的一段路要走，更多參考資訊請參考文章內容