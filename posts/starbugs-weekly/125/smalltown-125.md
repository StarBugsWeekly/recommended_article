---
title: 第 125 期 後端開發 推薦文章
date: 2022-03-22
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [System Design Basics: Proxy vs. Reverse Proxy](https://medium.com/interviewnoodle/system-design-basics-proxy-vs-reverse-proxy-90d48da385be)

在一個分散式的系統中，我們時常會聽到 Proxy 跟 Reverse Proxy，這兩個詞總是令人感到混肴，這兩者其中最大的不同之處在哪裡？而在什麼樣的情況之下會需要使用到它們？使用之後可以獲得什麼好處？這篇文章使用動畫圖來說明當 Proxy 代替 Client 送出請求到 Server 端，如何去達成 Caching, Anonymity, Traffic Control, Logging 等功能；同樣透過動畫去解釋 Reverse Proxy 將最終接受請求的 Server 對 Client 隱藏起來的同時，又是怎麼樣去 Caching, Anoymity, Load Balancing, Experimentation, Router/Ingress，對於這兩個詞彙也常常感到混肴的人，可以參考一下這篇文章

<!-- summary -->

### [PostgreSQL: Lessons Learned While Optimising Query Performance](https://betterprogramming.pub/postgresql-lessons-learned-while-optimising-query-performance-56e1652ecd86)

作者在去年學到很多關於如何去優化 PostgreSQL 效能的知識，所以想要透過這篇文章跟大家分享如何充分利用 Database 的關鍵點，他覺得有兩點特別重要，並且使用圖示詳細說明為什麼以及如何改善，對於 Tuning Database 底層有興趣的人可以參考看看

1. 最常造成 Database 效能問題的原因通常在於 Index 並沒有被包含在搜尋中，或是建出來的 Index 並沒有被使用到
2. 不知道目前 Database 到底是好是壞，例如怎麼找到目前最慢的三個查詢語法？

### [How Do I Resolve Merge Conflicts?](https://dev.to/github/how-do-i-resolve-merge-conflicts-5438)

作者剛從 coding boot camp 畢業時其實還不會處理 Git Merge Conflict，他的當時的解決方式是直接重開一個新的 Git Repository，不過他在 2019 年作為一個軟體工程師跟著團隊一起工作之後，他不可能再透過開啟新的 Git Repository 來解決問題，所以他在那一年常常解 Merge Conflict 解到泛淚，不過在經歷那段時間之後，他現在已經很有信心自己去解決 Merge Conflict，雖然還是會有點感到壓力XD 所以他想要提供一些小技巧給大家，首先可以從了解為什麼 Merge Conflict 發生開始，接著提到如何去解決 Merge Conflict，內容講得滿詳細的，推薦給對於解決 Merge Conflict 也感到苦惱的人