---
title: 第 138 期 資料庫 推薦文章
date: 2022-06-28
author: larry

layout: layouts/post.njk
tags: [Database]
---

## 資料庫

### [How the N+1 Query Can Burn Your Database](https://betterprogramming.pub/how-the-n-1-query-can-burn-your-database-3841c93987e5)

N+1 問題是資料庫領域非常知名的問題，這篇文章詳細解釋了 N+1 問題的成因，以及該如何解決，如果才剛開始碰資料庫或是後端開發，建議可以讀讀看哦～

### [Herding elephants: Lessons learned from sharding Postgres at Notion](https://www.notion.so/blog/sharding-postgres-at-notion)

應該很多人都聽過 Notion 這個筆記軟體，隨著使用者跟資料量越來越多，他們決定要對 PostgreSQL 建的資料庫做 sharding，這篇文章說明了他們是怎麼做的、過程中遇到什麼困難，非常不錯的文章（但有點長讀起來有點累XD）

### [Hosting SQLite databases on Github Pages](https://phiresky.github.io/blog/2021/hosting-sqlite-databases-on-github-pages/)

你一定知道 SQLite 這個資料庫，但你有想過他可以被架在 Github page 上嗎。這篇的作者先把 SQLite 編譯成 WebAssembly，接著再弄一個 file system 讓他去幫忙抓資料。雖然實用性不高但還滿有趣的XD

