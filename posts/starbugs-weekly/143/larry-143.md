---
title: 第 143 期 Elixir 推薦文章
date: 2022-07-26
author: larry

layout: layouts/post.njk
tags: [Elixir]
---

## Elixir

### [用 Elixir 學習後端煉金術 系列文](https://ithelp.ithome.com.tw/articles/10235287)

最近一直被同事推坑 Elixir，前幾天去 Coscup 又被推一次，越聽越不錯決定花點時間來看看XD，然後就找到了這篇講 Elixir 跟 Phoenix 框架的系列文，有興趣的話也一起來學學新語言吧～

### [46 年老技術與 Web 的新火花 - Actor Model in Web](https://blog.techbridge.cc/2019/06/21/actor-model-in-web/)

Elixir 因為建立在 Erlang 之上，所以也是使用 Actor Model 來進行平行處理。雖然 Actor Model 比較冷門一點，但他的設計概念其實非常好，除了可以將灌注點分離，而且在平行處理時完全不需要上 lock，可以很好的解決需要平行運算的問題。

### [CSP vs Actor model for concurrency](https://dev.to/karanpratapsingh/csp-vs-actor-model-for-concurrency-1cpg)

如果你也有寫 Go 的話，應該會聽過另一個 concurrency model 叫 CSP，其實我覺得 Actor model 跟 CSP 都是很好的想法，比 multi-thread 共用變數然後上 lock 還要好非常多XD。有興趣可以看這篇文章複習一下這兩個 model，也順便看看他們到底哪裡不一樣～
