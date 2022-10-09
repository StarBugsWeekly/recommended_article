---
title: 第 153 期 前端開發 推薦文章
date: 2022-10-11
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 前端開發
<!-- summary -->

### [The Future of the Web is on the Edge](https://deno.com/blog/the-future-of-web-is-on-the-edge)

文章標題上的 edge 是指你的網站或 APP 同時給在世界各地的 server 託管，讓 server 可以更靠近使用者一點，算是物理上的拉近使用者與 server 的距離，使得使用者能夠更快的得到 server 的回應，文章中除了比較各地的 TTFB 時間，還針對以下幾點解說 edge 的特性：

* 更靠進使用者的 Caching
* 更少的 servers，更多的 serverless
* 更佳的性能
* 更好的安全性
* 更棒的開發體驗

<!-- summary -->

### [A Deep Dive Into CSS Grid minmax()](https://ishadeed.com/article/css-grid-minmax/)

CSS 的 grid 排版相當好用！且在 grid 系統裡面有個作者認為非常強大 `minmax()` 特性，使他寫了一篇文章，來當作一份完整的 `minmax()` 使用指南。在文章裡，程式碼、圖片、影片全都有！可以花一些時間慢慢看完。

### [在 reduce 使用點點點 spread operator 是效能上的 anti-pattern](https://jason-memo.dev/posts/spread-in-reduce-is-a-perf-antipattern/)

在一些 reduce 中，常常會為了使每個 object 都是 immutable 的而使用 spread operator 語法產生另一個新的 object，但也因為這樣會導致時間複雜度從 O(n) 變成 O(n^2)，雖然在大部分情況下，這麼做是不會顯著的影響到效能，但在真的需要優化的時候，還是可以注意一下這種寫法所產生出來的額外效能耗損。
