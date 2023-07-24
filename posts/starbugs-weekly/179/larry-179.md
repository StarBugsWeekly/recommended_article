---
title: 第 179 期 Golang 推薦文章
date: 2023-07-25
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Caching Golang tests in CI](https://www.airplane.dev/blog/caching-golang-tests-in-ci)

這篇文章作者的公司 Airplane 用 Go 來開發產品，並且在每次有新 commit 時就在 Github Action 上跑單元測試。但因為單元測試跑得時間太久了（可能測試寫太多了，真是一間好公司XD），因此他們用了 cache 來大幅加速。如果你的公司也有測試太多要跑很久的問題，那也可以參考看看這篇文章的做法哦～

### [Built-in functions in Go 1.21](https://antonz.org/go-1-21-builtins/)

Go 從版本 1.21 開始又多了 min、max、clear 三個內建函數，這篇文章用很簡短的幾個例子帶你看看他們，以後寫程式的時候就可以直接拿來用啦！

### [Random testing in Go](https://bitfieldconsulting.com/golang/random-testing)

這一系列講 Go Fuzzing Test 的四篇文章終於寫完啦，看完這四篇，除了會對 Fuzzing Test 有基本的認識之外，應該也會知道怎麼用他來找出一些奇怪的 bug。如果你對 Go 的基本語法還有單元測試已經非常熟悉，那現在來學 Fuzzing Test 剛剛好。
