---
title: 第 141 期 系統設計 推薦文章
date: 2022-07-19
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## 系統設計

### [CAP定理101—分散式系統，有一好沒兩好](https://medium.com/%E5%BE%8C%E7%AB%AF%E6%96%B0%E6%89%8B%E6%9D%91/cap%E5%AE%9A%E7%90%86101-3fdd10e0b9a)

最近 Larry 我在找工作，所以又重新讀了很多基礎的理論，意外發現這篇很不錯的文章。這篇從為什麼會出現 Partition 開始講起 CAP 定理，一步一步探究為什麼 CAP 三者不可能同時被滿足，最終再解釋 eventually consistency 這個妥協後的解法。

### [Unique Id generation in distributed systems](https://medium.com/nerd-for-tech/unique-id-generation-in-distributed-systems-6f7aaa39c9af)

你有想過在分散式系統中，如果讓不同機器生出不同的 ID 嗎？因為 UUID 實在太長了不符合這篇文章的情境（要讓使用者輸入 ID），所以作者參考了 Twitter snowflake 的設計理念，設計出自己的一套絕對不重複的 ID，很有趣的一篇文章。

### [System Design — Top K Trending Hashtags](https://mecha-mind.medium.com/system-design-top-k-trending-hashtags-4e12de5bb846)

如果要你實作一個系統，用來統計近 24 小時內 Instagram 上最熱門的十個 hashtag，那你會怎麼做設計呢？如果想不到的話可以來看看這篇文章，他從資料量跟使用者人數開始進行分析，並且提供了一個簡單（好像也不是那麼簡單？）的解法。




