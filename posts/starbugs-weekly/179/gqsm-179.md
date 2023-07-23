---
title: 第 178 期 前端開發 推薦文章
date: 2023-07-11
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [The End of Front-End Development](https://www.joshwcomeau.com/blog/the-end-of-frontend-development/)

近幾年來 AI 急速成長，有許多前端工程師都會認為自己會被 AI 所取代，因為他們甚至能夠根據畫在紙上的 UI，產生對應的 HTML、CSS 和 JavaScript，這聽起來非常可怕，也讓許多前端工程師開始焦慮自己是否要繼續走下去。但是作者在這篇文章中指出，早在 CSS 誕生後的兩年內，第一個號稱不需要寫任何程式碼就能建構網站的 Homestead 就誕生了，但是現在前端工程師絕種了嗎？並沒有。而作者也有從其他面向去討論 AI 對軟體工程師的影響，最推薦的是最後一段寫給有熱忱的開發者的一段話。早上醒來看完這篇文章，心裡的暖都分不清到底是來自於作者的文字還是夏天的太陽。

### [The modern way of serving images](https://kurtextrem.de/posts/modern-way-of-img)

文章中一開始用數據表示，從 HTTP Archive 收集到的資訊當中，至少 70% 的網站都利用當作網站裡最吸引人的部分，但只有 34% 使用了 `<img srcset>` 建立響應式和高效能的圖片顯示。作者會在文章中解釋為什麼我們會需要建立響應式的圖片，以及我們要如何利用 `<img srcset>` 和 `<picture>` 改善顯示或載入圖片時，在網頁遇到的常見問題以及使用者體驗！

### [Zedux: Is this the one?](https://omnistac.github.io/zedux/blog/zedux-is-this-the-one)

Zedux 是為最自由的 React 所建立的狀態管理工具，它潛伏了 5 年多仔細研究 React 狀態管理工具的生態，然後將各種狀態管理工具的優點全部 all for one 到自己身上。Zedux 中的 atom 參考了 Recoil，也吸收了 React Query 擁有簡單版本的 query 和 mutation，其中也包含 Redux 和 Jotai 的所有功能。那看來只要學習這套，之後怎麼鬼轉其他狀態管理工具都沒問題了。 😂
