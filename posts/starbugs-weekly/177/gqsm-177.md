---
title: 第 177 期 前端開發 推薦文章
date: 2023-06-27
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [Reducing Complexity in Front End Development](https://css-irl.info/reducing-complexity-in-front-end-development/)

這篇文章主要是在分享作者在 [All Day Hey](https://heypresents.com/conferences/2023) 裡面最喜歡的一個議程 [Abstractions, complexities and off-ramps](https://heypresents.com/talks/abstractions-complexities-and-off-ramps)，議程內容主要是在說，現代開發都會傾向於尋找現有的解決方案，然後從 npm 把第三方套件下載下來使用，但如此一來前端的專案其實是失去掌控的，因為在那些第三方套件中有太多複雜性，你不確定他何時和什麼原因會使專案出錯。此議程會帶你分析這些複雜性，以及提供你能夠逐步解決的方式。推薦大家可以點進文章看看！如果有時間也可以看完整個議程！ 🙌

### [useHooks](https://usehooks.com/)

相信有在使用 React 的開發者，對於自己寫 hooks 來說應該是家常便飯了，而這個意外看到的 repository 就是將各種常用的操作，像是 debounce、toggle、mouse 等等，然後把它們的邏輯包成方便使用的 Hooks！且網站中的每個 hooks 都有對應的 Demo 和程式碼，如果不想要下載整個套件也可以直接複製到專案用！

### [👋 Say Goodbye to Spread Operator: Use Default Composer](https://aralroca.com/blog/default-composer)

在 JavaScript 裡面使用解構產生新的物件賦值是很常見的操作，還能夠用一個有預設值的物件搭配有值的物件做到組合的效果，產生出一個「有更新值就用新值，沒有的話就用預設值」的物件出來，但如果是單層的物件還好操作，如果是巢狀的物件就會有點麻煩了，這篇文章就是在介紹 [default-composer](https://github.com/aralroca/default-composer) 這個第三方套件，讓我們可以更容易地做到相同的事情。
