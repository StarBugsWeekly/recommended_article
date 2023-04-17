---
title: 第 171 期 Go 推薦文章
date: 2023-04-04
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Defer your mutex Unlocks](https://www.ribice.ba/defer-mutex-unlocks/)

不得不說 Go 的 defer 真的是一個很好用的功能，除了避免不小心忘記釋放資源，如果 function 在執行的過程中意外發生了 panic，defer 還是會在正確的時間執行，所以不管在什麼情況下，只要是要釋放資源，都推薦使用 defer。

### [Uber Go Style Guide](https://github.com/uber-go/guide/blob/master/style.md)

想知道大組織怎麼管理他們的程式碼風格嗎？這份文件是 Uber 在公司內實施的 Go guideline，透過這些規範可以讓他們避免一些常見的可讀性以及效能問題。

### [SOLID Principles: Explained with Golang Examples](https://dev.to/ansu/solid-principles-explained-with-golang-examples-5eh)

SOLID 原則應該大家都聽過，但如果要應用到 Go 裡面，會有哪些地方需要注意呢？這篇文章舉了非常多例子，教你怎麼寫出 SOLID 的 Go 程式碼。為了在三個月後還看得懂自己寫的程式碼，當然要趕快學起來！
