---
title: 第 145 期 Golang 推薦文章
date: 2022-08-23
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Easy memory-saving tricks in Go](https://www.ribice.ba/golang-memory-savings/)

如果你想把程式跑在比較低階的機器上，譬如說樹莓派或是嵌入式的裝置，那你可能就會需要注意程式的記憶體使用量。這篇文章講了三種的方法來降低 memory usage，都非常簡單很容易就能做到哦～

### [GOMEMLIMIT is a game changer for high-memory applications](https://weaviate.io/blog/2022/08/GOMEMLIMIT-a-Game-Changer-for-High-Memory-Applications.html)

如果你的 Go 程式會用到很多 memory，三不五時就會 OOM(Out Of Memory)，那從 Go 1.19 開始可以用 GOMEMLIMIT 來限制 memory usage 了，他會在你的使用量在到達上限之前就幫你做 GC，讓你的程式不會因為不小心吃了太多記憶體，就直接被殺掉

### [打造 Go 语言最快的排序算法](https://blog.csdn.net/ByteDanceTech/article/details/124464192)

不知道大家有沒有聽說 Go 的 sorting 演算法從 1.19 開始變得更快了，這篇講的是這個更快的排序是怎麼被時做出來的，內容有點深，所以如果沒興趣的話不看也沒關係，只要記得趕快把 Go 升級到 1.19 就好～
