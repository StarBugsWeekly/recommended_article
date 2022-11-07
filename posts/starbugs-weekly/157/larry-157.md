---
title: 第 157 期 Golang 推薦文章
date: 2022-11-08
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [從 graphql-go 轉換到 gqlgen](https://blog.wu-boy.com/2020/04/switch-graphql-go-to-gqlgen-in-golang/)

有在 Go 上寫過 GraphQL Server 的朋友們可能都聽過 `graphql-go`，雖然他歷史比較悠久，但是他的維護狀況不是很好，所以作者就把他的專案轉移到 gqlgen 上面了，這篇文章就是他的心得分享，如果你也在用 graphql-go，可以參考看看

### [CRUD API with Go and PostgreSQL](https://dev.to/chetansj27/crud-api-with-go-and-postgresql-411n)

如果你才剛開始接觸 Go 的話，這篇文章是一個很簡單的 CRUD API 實作，用到的技術有使用 mux、Gorm 跟 PostgreSQL，如果你想要熟悉一下這幾個技術，可以看這篇文章來快速入門～

### [Processing Large Files with Go](https://medium.com/@snassr/processing-large-files-in-go-golang-6ea87effbfe2)

大家有使用 Go 來處理大檔案的經驗嗎？這篇文章講了一個處理巨大 csv 範例，而且在處理的過程中也善用了 Goroutine 來把效能榨乾，如果你也有處理大檔案的需求，可以看看這篇文章的實作方式
