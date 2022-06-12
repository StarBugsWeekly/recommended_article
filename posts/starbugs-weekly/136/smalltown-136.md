---
title: 第 136 期 後端開發 推薦文章
date: 2022-06-14
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [Cache made consistent: Meta’s cache invalidation solution](https://engineering.fb.com/2022/06/08/core-data/cache-invalidation/)

Phil Karlton 曾說過在 Computer Science 領域最困難的兩件事情就是 **使暫存失效** 跟 **命名東西**，在 Meta 內部署著某些世界上最大的 Cache 系統，其中包含著 TAO 與 Memcache，而在過去幾年來，他們改善了 TAO 的暫存一致性，將其從 99.9999 % 提升到 99.99999999，對 Cache 改善有興趣的人不要錯過了

<!-- summary -->

### [Comparing Ceph, LINSTOR, Mayastor, and Vitastor storage performance in Kubernetes](https://blog.flant.com/kubernetes-storage-performance-linstor-ceph-mayastor-vitastor/)

作者說每一份工作總是會被要求對不同的 SDS 解決方案做基準測試，這次加入 Flant 後也不意外，所以這篇文章便是紀錄 Ceph, LINSTOR, Vitastor 和 Mayastor 在 Kuberneter 環境下大 PK 之後的結果，最後的冠軍為 LINSTOR，根據結果，作者覺得他是最成熟可以應用在正式環境的解決方案，詳細數據請參閱內文

### [Linux Memory: Buffer vs Cache](https://medium.com/geekculture/linux-memory-buffer-vs-cache-44d8a187f310)

在 Linux 系統內的 **Buffer** 和 **Cache** 有什麼不同呢？Buffer 會用來當做要寫到磁碟中資料的暫存空間，那麼他會用來暫存從磁碟讀取而來的資料嗎？Cache 是用來暫存從檔案讀取而來的資料，那麼他會用來暫存準備寫到檔案內的資料嗎？假如不知道這些問題答案的話，趕快看一看這篇文章就對了！
