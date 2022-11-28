---
title: 第 160 期 Go 推薦文章
date: 2022-11-29
author: larry

layout: layouts/post.njk
tags: [Golang]
---

## Golang

### [Modern API design with Golang, PostgreSQL and Docker](https://bognov.tech/modern-api-design-with-golang-postgresql-and-docker)

如果你最近剛開始學 Go，那你可以看看這篇文章怎麼用 Go, PostgreSQL 跟 Docker 寫出一個簡單又好部署的 API Server。對於 Go 的寫法有點概念之後，再學其他 library 也會更得心應手～

### [Struct Composition in Go](https://medium.com/@muhammadarifineffendi/struct-composition-in-go-80492bd447bd)

因為 Go 裡面沒有繼承的語法，如果想在 Go 裡面做到其他 OOP 語言的繼承，那可以試試看用 Struct Composition 的方式，雖然剛開始用可能會不太習慣，但用久了會覺得這樣的設計其實也滿好的～

### [奔放的 Golang，卻隱藏著有紀律的架構！- Clean Architecture 實作篇](https://ithelp.ithome.com.tw/articles/10240228)

最近在寫 Go 的時候對於各個 package 之間的 boundary 不太確定該怎麼拿捏、還有 interface 該怎麼設計，好像怎麼樣都切不乾淨的感覺。查了一些資料後發現由 Uncle Bob 提出的 Clean Architecture 剛好有講到各個 Layer 之間要怎麼分工才能比較好測試，如果你還沒聽過 Clean Architecture 的話可以看看這系列文的 Day6 到 Day8，也許會有意外的收穫哦。
