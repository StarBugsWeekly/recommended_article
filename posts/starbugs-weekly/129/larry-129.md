---
title: 第 129 期 MongoDB 推薦文章
date: 2022-04-19
author: larry

layout: layouts/post.njk
tags: [Back-end]
---

## MongoDB
<!-- summary -->

### [該用 MySQL 或 MongoDB？選擇資料庫前你該了解的事](https://tw.alphacamp.co/blog/mysql-and-mongodb-comparison)

在剛開始學習使用資料庫時，第一個會先碰到的問題就是要使用 MySQL/PostgreSQL 還是 MongoDB，但要使用什麼資料庫跟你的應用場景其實有很大的關係，如果還不知道怎麼選的話來看看這篇的分析吧

<!-- summary -->

### [MongoDB 不懂 ESR 別說你會用 Index !!](https://blog.myctw.cc/post/d50d.html)

在 MongoDB 中進行 query 時，如果希望盡量吃到 index，那在設計 index 以及進行搜尋、排序時就要遵守 ESR(Equality, Sort, Range) 原則，但不知道為什麼這個原則並沒有寫在官方文件裡XD，所以如果你有在用 MongoDB 卻沒聽過 ESR 的話趕快來這邊補一下

### [Getting started with MongoDB explain()](https://www.dbkoda.com/blog/2017/11/12/MongoDBExplain)

在使用資料庫時，為了加快搜尋的速度我們都會使用 index，但怎麼知道你建立的 index 是不是真的有被吃進去呢，總不能憑感覺吧，所以這時候就要把 explain 請出來，看看 Mongo 是不是真的有照你想的去使用建出來的 index

