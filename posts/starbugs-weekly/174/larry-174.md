---
title: 第 174 期 Golang 推薦文章
date: 2023-05-16
author: larry

layout: layouts/post.njk
tags: [Golang]
---
## Golang

### [The Go 1.19 Atomic Wrappers and why to use them](https://medium.com/@deckarep/the-go-1-19-atomic-wrappers-and-why-to-use-them-ae14c1177ad8)

自從 Go 1.19 開始，就有像是 `atomic.Int64` 這樣的型別，可以防止有人對變數做不是 atomic 的操作。譬如程式碼中有一個 `var counter atomic.Int64`，但你的同事忘記這個 `counter` 會被多個 goroutine 共用，所以他寫了 `counter++`，這時候 Go compiler 就會噴錯告訴你不可以這樣用，要乖乖寫 `counter.Add(1)` 才可以避免 data race，真的是很不錯的新功能～

### [6 Tips on High Performance Go — Advanced Go Topics](https://link.medium.com/H1s1blbsJzb)

想要寫出更高效能的 Go 程式碼嗎？這篇文章講了幾個技巧跟工具，譬如說內建的 profiling tool 跟 benchmark，幫助你找出 Go 程式中潛在的效能問題。如果想讓你的 Go 功力更上一層樓，那可以看看這篇文章。

### [Go Generic Repo](https://link.medium.com/RNYVq0x56yb)

Go 從 1.18 開始支援泛型，但在實務上還是不常看到泛型的運用。而這篇文章給了一個很不錯的例子，用非常少的程式碼寫出一個通用的 Repository 跟 Model，不只寫起來漂亮，而且也非常好維護呢～
