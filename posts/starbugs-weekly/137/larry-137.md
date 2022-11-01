---
title: 第 137 期 Golang 推薦文章
date: 2022-06-21
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Data Race Patterns in Go](https://eng.uber.com/data-race-patterns-in-go/)

Uber 的 Go 專案有超過五千萬行程式碼，工程師從以前到現在也修過超過一千個 data race（他們真的不考慮用 Rust 嗎XD）。而這篇文章就是他們修了這麼多 data race 之後，整理出來最可能犯錯的地方，非常值得讀的一篇文章～

### [Options Pattern in Golang](https://link.medium.com/BWX0EmRySqb)

Options pattern 是 Go 裡面很常見的寫法，在很多框架裡面都能見到他的蹤影，一起來看看什麼情況下可以使用這樣的 pattern，以及有什麼好處吧

### [Effective Error Handling in Golang](https://earthly.dev/blog/golang-errors/)

Go 內建的 error 跟很多語言不一樣，不僅不支援傳統的 try catch，甚至不包含 stack trace，所以用起來有一些不便，但也因此更輕量。如果才剛開始學 Go，來看看如何好好的使用 Go 的 error 吧
