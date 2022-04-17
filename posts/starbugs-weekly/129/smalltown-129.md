---
title: 第 129 期 後端開發 推薦文章
date: 2022-04-19
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [30 Coding Concepts I Learned After Reading “Clean Code”](https://betterprogramming.pub/thoughts-on-clean-code-d373c0d93ea4)

作者本身喜愛將自己所讀完的書給記下來，因此在讀完 Uncle Bob 所撰寫的 Clean Code 之後，將讀完此書學到的 30 個概念給整理出來，首先講述 Clean Code 的整體思想與概念，然後再深入探討這三十個概念的細節，策略與實作相關訊息，假如沒有太多時間來讀這本書的話，可以考慮花個 15 分鐘閱讀此篇整理文章
<!-- summary -->

### [1,000,000 Concurrent Connections](https://josephmate.github.io/2022-04-14-max-connections/)

作者最近看到不少文章有一個錯誤的觀念，述說著一台伺服器最多只能接受 65,000 個連線，作者首先提出一些證據來打臉，首先是 WhatsApp 所使用到的 Phoenix Web Framework 早就演示過可以在單一個 Port 上接受數百萬的連線，再來要是任何人假如不相信的話，可以使用簡單的 Java 在自己的機器做個實驗就可以了；但為了證實自己所說，作者還是詳細的做了個 PoC 將結果展示給大家看，結果顯示在 Mac 就可以接受到將近八萬個連線，並且將可能遇到的問題給記錄下來

### [CQRS Software Architecture Pattern: The Good, the Bad, and the Ugly](https://betterprogramming.pub/cqrs-software-architecture-pattern-the-good-the-bad-and-the-ugly-e9d6e7a34daf)

Command and Query Responsibility Segregation (CQRS) 是一種專門用來將資料的讀與寫分離開來的架構，其中的 Queries 就是負責來讀取資料的模型，Commands 就是用來負責更新資料的模型；這篇文章將會詳細的介紹 CQRS 的架構，並且詳細地說明如何實作 CQRS，以及他的優缺點，跟可能會遇到的問題