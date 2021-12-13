---
title: 第 111 期 前端開發 推薦文章
date: 2021-12-14
author: Andy

layout: layouts/post.njk
tags: [Front-end]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 前端開發
<!-- summary -->
### [A Complete Guide To Incremental Static Regeneration (ISR) With Next.js](https://www.smashingmagazine.com/2021/04/incremental-static-regeneration-nextjs/)

在 Next.js 中有一個相當重要的設定叫：Incremental Static Regeneration (ISR)，拜 ISR 所賜假如只有該頁面需要更新內容，可以只重 build 該頁面即可，不需要重 build 整個專案，對於 SSG 渲染方式來說可說是相當好用的一把利器，想要了解 Next.js ISR 的完整介紹，不妨可以參考這篇文章。
<!-- summary -->

### [Keeping things fresh with stale-while-revalidate](https://web.dev/stale-while-revalidate/)

stale-while-revalidate (SWR) 可以說是相當重要的一個 cache 處理機制，有了這套機制可以讓使用者在面對一個內容確定過期的頁面不會在一開始進入過長的等待，瀏覽器會先從 cache 返回之前的內容，並同時更新要顯示的正確內容，待下次使用者重新進入此頁面時就會是最新的內容了，有興趣了解 SWR 機制的可以參考看看這篇文章。

### [Learnings from React Conf 2021](https://dev.to/alexeagleson/learnings-from-react-conf-2021-17lg)

React 每年都會有一場盛大的 conference，這次的 conference 又介紹了相當多好用的工具，有興趣的讀者可以參考別人整理好的筆記。(所以我說那個 React 18 什麼時候才要正式上線呢XD
