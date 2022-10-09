---
title: 第 153 期 Golang 推薦文章
date: 2022-10-11
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [乾淨的 Golang 編碼 (Clean Go code) 系列](https://datapool.tw/2022/09/11/%e8%89%af%e5%a5%bd%e7%9a%84%e4%b9%be%e6%b7%a8%e7%9a%84-golang-%e7%b7%a8%e7%a2%bc-clean-go-code1/)

把程式碼寫得乾淨漂亮從來不是一件容易的事，這一系列文章以 Go 為例分享了怎麼把程式跟註解都寫得更漂亮，讓你的 codebase 更好維護～

### [Concurrency isn’t Always Faster in Go](https://link.medium.com/9fVkvAzOktb)

因為有 Goroutine 的關係，在 Go 裡面很輕易就可以做到併發（Concurrency），但併發並不完全就代表高效能，如果沒有搞清楚各個 thread 什麼時候會執行，那可能還會比 sequential 執行來得更慢哦

### [A practical approach to structuring Golang applications](https://dev.to/firdavs_kasymov/a-practical-approach-to-structuring-golang-applications-1cc2)

每次要開新專案時，都很煩惱資料夾的結構應該要怎麼拆分，而這篇文章介紹了一種還不錯的方法，大家可以參考看看
