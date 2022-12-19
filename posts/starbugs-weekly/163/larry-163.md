---
title: 第 163 期 Golang 推薦文章
date: 2022-12-20
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [New in Go 1.20: wrapping multiple errors](https://lukas.zapletalovi.com/posts/2022/wrapping-multiple-errors/)

如果沒意外的話，Go 在明年二月就會發佈新版本 1.20。從 Go 1.20 開始，我們可以用 `errors.Join(err1, err2)` 把多個錯誤 join 成一個錯誤、而且 `fmt.Errorf` 也可以用來把多個錯誤格式化輸出成一個錯誤，讓 Go 的錯誤回傳、處理可以寫得更漂亮

### [Test parallelization in Go: Understanding the t.Parallel() method](https://engineering.mercari.com/en/blog/entry/20220408-how_to_use_t_parallel/)

維持寫測試的習慣固然是好事，但隨著專案中的測試越來越多，每次跑測試所需要的時間也會越來越久。這篇文章介紹了 Go 的平行化測試功能，如果每個測試都是完全獨立、且不影響彼此，那可以試試看用 `t.Parallel()` 來同時執行多個 test case！

### [Making a Go program run 1.7x faster with a one character change](https://hmarr.com/blog/go-allocation-hunting/)

在這篇文章中，作者介紹了他如何使用 Go 的 pprof 跟 flamegraphs 工具來分析效能，並且最後只改了一個字元（其實是兩個XD）就提升了 1.7 倍的效能。如果你已經有 Go 的開發經驗，又對效能最佳化感興趣，那麼這篇文章絕對值得一讀！
