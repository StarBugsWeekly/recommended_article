---
title: 第 141 期 後端開發 推薦文章
date: 2022-07-19
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Backend

<!-- summary -->
### [7 Best Practices for Speeding Up Code Reviews](https://hackernoon.com/7-best-practices-for-speeding-up-code-reviews)

Code Review 可能會很痛苦，軟體開發工程師經常會抱怨 Review 的流程緩慢，導致其他相關的任務也跟著被延遲，而且也造成自己在新開的 PR 和下個工作任務之間來回切換；Review 出來的結果也可能會充滿吹毛求疵的回饋，這對所有參加 Code Review 的人來說都是很糟糕的體驗
<!-- summary -->

甚至有人建議將 Code Review 直接取消，不過這種作法可能對新創小公司還適合，但作者認為這樣的做法不適合所有的組織，尤其是企業級的大公司，所以作者想要透過這篇文章提出七個關於 Code Review 的最佳實踐，PR Submitter 和 Reviewer 在 Code Review 的過程有更好的體驗

### [pocketbase](https://github.com/pocketbase/pocketbase)

PocketBase 是一個開源的 Go 後端框架，可以用來構建後端應用，他由以下元件所組成：即時訂閱功能，檔案和使用者管理，方便的管理員 UI，和 REST-ish API，Client 端 API SDK，讓開發者可以輕鬆地開發後端應用

### [tproxy](https://github.com/kevwan/tproxy)

當作者在開發後端服務和 [go-zero](https://github.com/zeromicro/go-zero) 時，常常會需要去監控網路流量，例如監控 gRPC 何時需要連線或是重新連線，監控 MySQL 的 Connection Pool 有多少，以及監控目前有多少的 TCP 連線，這些都是很麻煩的事情，因此作者想要提供一個簡單的工具，可以讓開發者即時監控這些網路相關數據，專注在程式邏輯的開發上面