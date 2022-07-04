---
title: 第 139 期 Golang 推薦文章
date: 2022-07-05
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [A Closer Look at Go’s sync Package](https://teivah.medium.com/a-closer-look-at-go-sync-package-9f4e4a28c35a)

知道怎麼啟動 goroutine 之後，下一個問題是怎麼讓多個 goroutine 分工合作，這時候就會用到 sync 裡面的 Mutex 或是 WaitGroup。這篇文章詳細介紹了 sync package 裡面的東西，先把這篇看完再開始用 goroutine 一定會大有幫助哦

### [Custom GitHub Action with Go](https://thedevelopercafe.com/articles/custom-github-action-with-go-29d9ce66e5a8)

Github Action 已經推出好一段時間了，應該有不少人都用過了。那有沒有想過要自己寫一個 action 呢？這邊有一篇簡單的教學，只要跟著做很快就可以寫出來哦～

### [CSP vs Actor model for concurrency](https://dev.to/karanpratapsingh/csp-vs-actor-model-for-concurrency-1cpg)

寫 Go 的人應該都知道 Go 的 goroutine 跟 channel 是 CSP model 的具體實現，而有另外一種 concurrency model 叫 actor model 則是可以在 Elixir 中看到，有興趣可以來了解一下他們的差異～
