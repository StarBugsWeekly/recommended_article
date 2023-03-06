---
title: 第 169 期 資料庫 推薦文章
date: 2023-03-07
author: larry

layout: layouts/post.njk
tags: [Database]
---

## Database

### [淺談 Database Partition. Centralized and Distributed.](https://homuchen.com/posts/what-is-database-partition-sharding/)

不得不說資料庫這領域真的是有很多學問，好幾年前我對資料庫還不太了解時，一直以為 sharding 跟 replication 是一樣的東西，反正就是開好幾台 DB instance 共同存放那些資料嘛XD。是後來慢慢深入了解後才知道兩個在概念上是完全不同的，如果你對 sharding、replication、partition 這些名詞還有點模糊的話，這篇文章解釋得很好哦～

### [Database 一代代的演化和傳承](https://tachunwu.github.io/posts/db-history/)

早在電腦發明以前，就已經有儲存資料的需求，因此關於資料庫的理論從好幾十年前就開始有了。如果你對資料庫的演進有興趣的話，這篇文章會從 1980 年代的資料庫開始介紹起，一直講到近幾年比較新的資料庫，讓你知道每個時代的資料庫系統想要解決什麼問題，以及又有什麼相對應的優缺點。

### [Is offset pagination dead? Why cursor pagination is taking over](https://uxdesign.cc/why-facebook-says-cursor-pagination-is-the-greatest-d6b98d86b6c0)

如果你有在後端實作過分頁功能，那你應該會知道有分成 offset based 跟 cursor based 兩種做法，這兩種做法各有他們的優缺點，如果你跟他們還不太熟悉的話，這篇文章有各種示意圖跟圖表，保證你看完就懂哦（這篇文真的寫得很好，但他是 member-only 的文章，所以可譨會需要開無痕模式來讀）


