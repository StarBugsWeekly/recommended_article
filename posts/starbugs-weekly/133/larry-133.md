---
title: 第 133 期 MongoDB 推薦文章
date: 2022-05-10
author: larry

layout: layouts/post.njk
tags: [MongoDB]
---

## MongoDB

<!-- summary -->

### [MongoDB Schema 設計指南](https://blog.toright.com/posts/4483/mongodb-schema-%E8%A8%AD%E8%A8%88%E6%8C%87%E5%8D%97.html)

在使用像 MongoDB 這類 document-based 的 NoSQL 時，因為每筆資料的格式都是 JSON，而且 MongoDB 也支援很多跟 Object、Array 相關的功能，所以在設計 Schema 時會跟傳統的 SQL Database 有點不一樣，不能直接把 SQL 那套理論原封不動搬過來用哦。

<!-- summary -->

### [MongoDB Aggregation 優化](https://blog.myctw.cc/post/acdb.html)

用過 MongoDB 一陣子之後應該都會接觸到他的 aggregation，他可以把你想要做的一系列操作寫成一個落落長的 pipeline，譬如說先搜尋、統計、最後做排序。而這篇文章提到了在寫 pipeline 有一些要注意的小地方，雖然有些部分 MongoDB 會幫你最佳化，但還是要注意一下讓你的 aggregation 效能更好。

### [Do You Need Mongoose When Developing Node.js and MongoDB Applications?](https://www.mongodb.com/developer/article/mongoose-versus-nodejs-driver/)

有在 Node.js 中用過 MongoDB 的人應該都知道 Mongoose 這套 ODM，他最大的好處就是可以幫你做 schema validation，讓你的資料庫不會有一堆缺值、型別錯誤的資料。但現在的 MongoDB 內建的 schema validation 也逐漸成熟了，所以下個專案也許可以考慮不需要使用 Mongoose，直接用內建的就好。
