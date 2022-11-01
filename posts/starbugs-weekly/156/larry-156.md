---
title: 第 156 期 Golang 推薦文章
date: 2022-11-01
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Golang for JavaScript developers](https://deepu.tech/golang-for-javascript-developers-part-1/)

最近想學 Go 的人越來越多了，這邊推薦這一系列文章，主要是在介紹 Golang 跟 JavaScript 的差異，如果你原本就會寫 JavaScript，而且想要開始想要學習 Go，那這兩篇文章可以幫助你快速上手 Go～

### [Build a Tic-Tac-Toe Game In the GitHub README.md File](https://betterprogramming.pub/play-tic-tac-toe-from-github-readme-md-file-754539603380)

這篇文章很有趣，主要是在說要怎麼用 Markdown 跟 Go 在 Github 專案的 README 裡面寫一個真的可以玩的圈圈叉叉遊戲。如果只想玩玩看不想看文章的話，也可以直接滑到文章最底下的 [Frontend — Readme.md](https://github.com/sridhar-sp/tic-tac-toe)，然後直接點進去玩玩看。

### [How to Write Accurate Benchmarks in Go](https://teivah.medium.com/how-to-write-accurate-benchmarks-in-go-4266d7dd1a95)

在對 Go 的程式碼做 benchmark 的時候，其實有很多該注意的小地方，像是在設定好測試環境後應該要先重置 timer 才開始進行測試，或是在寫測試時要避免程式碼不小心被編譯器最佳化吃掉，如此一來才能得到真正準確的 benchmark 結果。
