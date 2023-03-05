---
title: 第 169 期 前端開發 推薦文章
date: 2023-03-07
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [CSS Tips for Better Web Development](https://www.builder.io/blog/css-tips-for-better-web-development)

這篇文章列出一些 CSS 技巧，可以幫助開發者進一步優化網頁的設計和性能。以下是文章中提到的一些重點：

1. 使用 `scroll-snap` 來實作絲滑般的滑動輪播效果
2. 使用 `position` 和 `grid` 處理網頁的 header 和 footer
3. 利用 `position` 的 `sticky` 在捲軸時固定畫面中的某個區塊
4. 透過 `backdrop-filter` 處理圖片的各種濾鏡
5. 使用 `:before` 和 `:after` 的組合，或是 `clip-path` 裁切元素的任何形狀

<!-- summary -->

### [Scroll Animation](https://css-tricks.com/books/greatest-css-tricks/scroll-animation/)

本文講解了如何只用一個 JavaScript 的語法來提供當前頁面捲動的百分比，就能透過 CSS 實現隨著捲軸移動產生的動畫效果。一開先介紹如何通過 JavaScript 來設置 CSS 自定義屬性 `--scroll`，並且將這個值用於 CSS 中。接著展示如何使用 `animation-delay` 來實現圖像的旋轉，並通過調整 CSS 中的動畫延遲來實現基於捲動位置的動畫效果。最後也提供了一個範例，示範在 `:root` 中設置 `animation-delay` 屬性，控制頁面上的所有動畫。

### [Debugging JavaScript Like a Pro: Tools and Techniques for Finding and Fixing Bugs](https://dev.to/iayeshasahar/debugging-javascript-like-a-pro-tools-and-techniques-for-finding-and-fixing-bugs-2lf5)

在文章裡提供了一些 JavaScript 的除錯工具和技巧，幫助開發者更快地找到和修復錯誤。作者分享的技巧和工具包括了瀏覽器開發者工具、console.log、debugger、linting 和單元測試等。除此之外還提到了常見的 JavaScript 錯誤，像是變數作用域、非同步問題等等，也提供解決這些問題的對應技巧。
