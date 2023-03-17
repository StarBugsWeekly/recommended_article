---
title: 第 170 期 後端開發 推薦文章
date: 2023-03-21
author: larry

layout: layouts/post.njk
tags: [Backend]
---

## 後端開發

### [自動升級更新執行中的 Docker 容器解決方案 - watchtower](https://blog.wu-boy.com/2023/02/automating-docker-container-base-image-updates-cht/)

之前就有用過 watchtower 這個小工具，他會定期去幫你檢查 DockerHub（或其他 registry）是不是有新的 image 可以用，如果有的話他就會幫你拉下來重新啟動 container，所以他可以讓你的 container 隨時保持在最新的狀態。因此，我們可以用他來簡化部署流程：先把 watchtower 跑在你的 remote server 上，從此只要把新的 image 上傳到 registry 上，就會自動被部署到 production 上，真的很方便哦。

### [淺談各種資料庫cache策略: cache aside、read through、write through、write back](https://homuchen.com/posts/databse-chache-strategies/)

以前跟 cache 還不熟的時候，從來沒有想過後端的 cache 有這麼多種可能。這篇文章簡單介紹了 cache aside、read through、write through、write back 這四種策略，並且比較他們各自的優缺點（一致性、讀取效能、寫入效能等等），如果你已經用過 Redis/Memcached，想更深入了解他們在各種情境的使用方式，那這篇文章一定要看看！

### [The technology behind GitHub’s new code search](https://github.blog/2023-02-06-the-technology-behind-githubs-new-code-search/)

這篇文章的技術含量滿高的，在講 Github 後端是怎麼是怎麼做 code search 的功能，因為他們儲存了非常大量的程式碼，所以必須用特別的方式去儲存，才能很快地把結果搜尋出來～
