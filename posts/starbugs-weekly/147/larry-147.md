---
title: 第 147 期 Golang 推薦文章
date: 2022-08-30
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Prevent Logging Secrets in Go by Using Custom Types](https://www.commonfate.io/blog/prevent-logging-secrets-in-go-by-using-custom-types)

在 Go 裡面進行 logging 時，如果一個不注意，可能會不小心把重要的 secret 輸出到 log。為了避免這種情況，這篇文章教你怎麼使用 custom types 來自動幫 secret 打碼，即便不小心輸出了，看起來也會是 ***** 的樣子。

### [Trying Clean Architecture on Golang](https://medium.com/easyread/golang-clean-archithecture-efd6d7c43047)

有點經驗的工程師應該都聽過所謂 Clean Architecture，因為 Clean Architecture 主要是一種概念而不是告訴你細節該如何實作，所以這篇文章嘗試用自己的方式去實現 Clean Architecture 的精神，而且也把程式碼公開出來給大家參考。

### [5 concurrency patterns in Golang](https://vietmle.com/posts/5_con_patterns_go/)

Go 身為一個很擅長做 concurrency 的語言，為了方便對開出來的 goroutine 進行管理，逐漸發展出一些很常見的 pattern，如果你正在煩惱要怎麼有效管理、整合各個 goroutine 的話，也許這篇文章能給你一些靈感。
