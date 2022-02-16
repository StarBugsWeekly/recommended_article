---
title: 第 120 期 DevOps 推薦文章
date: 2022-02-15
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Why you should NOT use Service Mesh](https://medium.com/google-cloud/when-not-to-use-service-mesh-1a44abdeea31)

Service Mesh 已經變成雲端架構中滿重要的一環，因為假如你使用正確的話，確實可以帶來很多好處，並且解鎖很多功能來讓你的團隊更省時省事，Service Mesh 要不要使用會建議在專案比較早期的階段就決定會比較好，而很多人決定的方式都是...要更安全，所以要 mTLS，所以要 Service Mesh，然後就用了，但作者認為不能這麼草率地去做這樣的決定，他提出幾個需要考慮的<!-- summary -->要素，讓使用者可以更謹慎的評估要不要去使用 Service Mesh

- 組織內是否具備擁有 Service Mesh 知識與經驗的人員？
假如團隊內沒有人知道 Service Mesh 甚至是 Kubernetes 就貿然使用的話，將會對專案造成負面的影響，尤其是當服務發生中斷或是遇到問題時，沒有人有辦法去除錯自己不懂的東西，所以必須確保有人員至少了解 Service Mesh 是什麼，以及他的基本概念

- 準備好面對採用 Service Mesh 將增加的技術債了嗎？
在 Production 環境使用 Service Mesh 當然比 Get Started 裡面的範例來的複雜很多，例如要怎麼自動化的部署 Service Mesh，怎麼去監控跟追蹤他是否正常，遇到問題的時候要怎麼去除錯跟找出原因，換句話說採用 Service Mesh 需要做的事情會比想像來得多，會有更多的設定需要在架構面落實，並且可能因此引入更多的工具並且也需要去維護它，這些都將有可能導致技術債的增加

- Service Mesh 是否與組織的應用程式相容嗎？
假如是自己開發的應用程式應該是不用擔心跟 Service Mesh 有相容問題，但第三方工具可就不一定了，例如作者發現他在 Argo Workflows 裡面加上 Service Mesh 之後，導致運行時間跟過時的機率增加，也增加了資源的使用，所以必須要先做過實驗才能知道自己想要使用的工具會不會跟 Service Mesh 八字不合

### [Akamai acquires Linode for $900M](https://techcrunch.com/2022/02/15/akamai-acquires-linode-for-900m/)

聽到 Akamai 這間公司應該都是聯想到 CDN，但其實他也有提供安全和邊緣運算的相關服務，他在今天宣布將使用 9 億美金併購 Linode，Akamai 預估 Linode 可以為他在 2022 年就帶來 1 億美金的收入，Akamai 宣稱此併購可以讓 Linode 不管是在雲端或是邊緣運算方面變成世界上最分散的運算平台，而在併購後 Linode 將會保持跟以往一樣的運作方式為大家服務

### [How to Use the Linux cut Command](https://www.howtogeek.com/775824/how-to-use-the-linux-cut-command/)

大家或多或少應該都會需要在 Terminal 處理有規則的字串，例如使用 kubectl get pod 後，想把某一些 Pod 給刪除掉，這時候可以先透過 `grep` 過濾資料，但該如何把 Pod 的名稱從過濾完的資料內再萃取出來呢？這時候就可以使用 Linux 裡面一個很強大的 `cut` 指令，他可以幫你把結構化資料的特定欄位給抓取出來，透過這篇文章可以詳細的知道如何使用它來讓自已日常工作事半功倍

### [spongebob-cli](https://github.com/trakBan/spongebob-cli)

當一直在 Terminal 做事情做到感覺有點疲憊時，該如何讓自己放鬆一下呢？！答案就是下指令 `spongebob-cli` 看一集海綿寶寶 🤣 自己滿喜歡看海綿寶寶的，因為裡面有很多大人才看得懂的劇情，沒想到有同好竟然把觀看海綿寶寶做成了 CLI 工具，透過該指令還可以選擇要看哪一集，喜歡海綿寶寶的人不要錯過了!

