---
title: 第 175 期 Golang 推薦文章
date: 2023-05-30
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Step up Your Go App Testing Game With the Testify Framework](https://semaphoreci.com/blog/testify-go)

如果你才剛開始在學 Go，那你絕對不能不知道 Testify 這個好用的 testing library，他幫你簡化了很多常用的操作譬如說 `assert.Equal` 跟 `assert.noError` 等等，讓你可以更快寫出正確的測試。除此之外，他也讓你可以輕鬆的造出一個 mock object，所以別猶豫，趕快讓 Testify 成為你的好幫手，讓你的測試寫起來更漂亮！

### [Go 當中的 sync pattern](https://code-pilot.me/synchronization-patterns-in-go)

這篇文章比較進階一點，文中從 Mutex、Semaphore 講到 Channel，帶你看看這些不同的 sync pattern 各自有什麼優缺點。看完這篇文章之後，你就會知道在 Go 裡面要怎麼解決各種 multi thread 的問題！

### [SwissMap: A smaller, faster Golang Hash Table](https://www.dolthub.com/blog/2023-03-28-swiss-map/)

SwissMap 聽起來像某一款高級巧克力的名字，但實際上，他是一個 Go 的 Hash Table package。他號稱比 Go 內建的 map 更快、記憶體的使用量也更少，是 Dolt 為了解決自身的問題而設計出來的。這篇文章講解了他們是怎麼設計跟實作 SwissMap，而且也提供了 Benchmark 給你參考，證明他們設計的這個 Hash Table 真的很不錯。
