---
title: 第 132 期 前端開發 推薦文章
date: 2022-05-10
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 前端開發
<!-- summary -->

### [You Don’t Need A UI Framework](https://www.smashingmagazine.com/2022/05/you-dont-need-ui-framework/)

這篇標題滿聳動的，但是作者其實是從「客製化的設計」、「節省時間」和「可用性和可訪問性」幾個面向，逐一讓讀者去思考，真的任何時候都需要選擇 UI Framework 嗎？也許自己花在把 UI Framework 所提供的樣式，調整成自己成專案所需求樣式的時間，都早就超過直接完成需求的時間了，我想這應該也是 [Tailwind CSS](https://tailwindcss.com/) 那麼深受開發者喜愛的原因之一。

<!-- summary -->

### [Memoization in JavaScript](https://parthasarma.hashnode.dev/memoization-in-javascript)

在需要反覆執行一些長時間運算的方法時，我們可以自己實做一個 memoization function，去紀錄 function 在什麼參數執行下會回傳什麼結果，並在下一次以相同參數執行的時候，就不需要再重複運算，只需要直接從紀錄中找到結果直接回傳就好。這個概念也有點像Design Pattern 裡的 Proxy Pattern。

### [Most common mistakes of (not only) JavaScript developers](https://blog.thecode.xyz/most-common-mistakes-of-not-only-javascript-developers#comments-list)

作者在文中舉出幾個剛學習 JavaScript 時會沒留意到的幾個小地方，比較常見的包含 `==` 和 `===`、`null` 的 type 是 Object 或是寫 `switch` 的時候要記得考慮 default 狀況等，算是一篇初階且容易閱讀的文章。
