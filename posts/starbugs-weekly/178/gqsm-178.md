---
title: 第 179 期 前端開發 推薦文章
date: 2023-07-25
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [The case against self-closing tags in HTML](https://jakearchibald.com/2023/against-self-closing-tags-in-html/)

作者喜歡 Prettier，但他對於 Prettier 中的自我關閉 `/>` 感到相當不認同，認為這並非純 HTML 下的產物，只是因為歷史沿革而產生的一種通融，也對於其他人支持的「`/>` 讓初學者不必學習哪種標籤為自動關閉」的意見回應了自己的看法，也用了較相似了例子 JSX 進來比較，或是從編譯的角度來看待 `/>`。是一篇很有趣的文章！

### [How React 18 Improves Application Performance](https://vercel.com/blog/how-react-18-improves-application-performance)

文章一開始會先從 JavaScript 的 Main thread 和 Long tasks 開始說起，解釋有哪些因素會影響到效能，也有稍微介紹一些 web 指標，將讀者帶入效能對使用者的影響層面。接著就開始介紹 React 18 做的 Transitions、Suspense 和 React Server Components 等相關功能是如何提高應用程序性能的！文章裡面的圖片遠遠大於範例的程式碼內容，非常容易理解！

### [Tailwind CSS Tips and Tricks Worth Knowing](https://www.builder.io/blog/tailwind-css-tips-and-tricks)

這篇文章會提到許多在使用 tailwind CSS 的一些技巧，和你可能採到坑的部分，我覺得非常適合剛剛在學習 tailwind CSS 的讀者閱讀！像是文章一開始提到的動態顏色，因為 tailwind 會幫你移除沒用到的樣式名稱，讓 CSS 在打包過後的 size 較小，所以動態顏色就不能這麼做 `className={`bg-${color}-500`}`，你必須得讓完整的樣式名稱能夠被 tailwind 抓到。