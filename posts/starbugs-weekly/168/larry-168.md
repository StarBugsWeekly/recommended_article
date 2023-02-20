---
title: 第 168 期 Golang 推薦文章
date: 2023-02-21
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [把 Github Issue 當成資料庫來用](https://www.evanlin.com/go-github-issue/)

想要自己寫一個 Go Application 但又不想花錢租資料庫嗎？這邊提供一個把 Github Issue 拿來當資料庫的方法。只要你的流量不高，對於 DB read/write  的速度也不要太計較，那真的可以用 Github Issue 來當資料庫XD。

### [Go 1.20 in a nutshell](https://appliedgo.com/blog/go-1-20-in-a-nutshell)

前幾週有分享一篇文章講 Go 1.20 有哪些新 feature，但那篇文章比較長，如果你懶得看太多細節，只想看懶人包了解一下 Go 1.20 的話XD，那可以看看這篇文章～

### [Go 1.20 Experiment: Memory Arenas vs Traditional Memory Management](https://pyroscope.io/blog/go-1-20-memory-arenas/)

Go 在 1.20 推出的實驗性 feature - Memory Arenas 究竟能不能幫我們改善記憶體管理以及 GC 的效率呢？如果懶得自己研究的話，那我們來看看別人研究完的結果。結論是 Memory Arenas 在某些極端的情況下，確實可以幫你減少很多 overhead，但因為 Memory Arenas 仍然是實驗性的功能，如果要用在 Production 上的話還是要自己評估看看。
