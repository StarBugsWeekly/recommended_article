---
title: 第 166 期 前端開發 推薦文章
date: 2023-01-24
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [A cure for React useState hell?](https://dev.to/builderio/a-cure-for-react-usestate-hell-1ldi)

在 React 裡面，如果要為 component 定義自身的狀態，通常都會直接使用 `useState`，但如果 state 裡面是保管著物件狀態的話，那在使用 `set*` 的時候就特別注意要使全新的物件，如果物件裡有許多欄位，那每次更新時都得要注意這件事情。而文章中提到了可以使用 `useReducer` 改善操作資料的複雜度，也可以在同個地方驗證是否要更新狀態。

<!-- summary -->

### [Applying SOLID principles to TypeScript](https://blog.logrocket.com/applying-solid-principles-typescript/)

SOLID 原則分別是：

1. 強調一個類只負責一件事的單一責任
2. 程式碼應該對擴展開放，但對修改封閉的開放封閉
3. 子類別要遵從父類別設計的里氏替換
4. 類別應該只實現它所需要的介面的介面隔離
5. 用抽象介面解除高低層次模組間依賴關係的依賴反轉

SOLID 是為了提高物件導向設計的可讀性，適應性，可擴展性和可維護性。文章裡使用 TypeScript 作為範例，說明如何將這幾個原則應用到 TypeScript 中。

### [A Complete Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

我知道你可能看過超過 100 篇在介紹關於如何使用 CSS 的 Gride 的文章，如果你沒有？那沒關係，我也是，但至少 10 篇應該也差不多了，但這篇關於 Grid 的推薦文章應該可以被稱作 Grid 百科，在文章中不只介紹基本用法、Gird 的一些專有名詞和屬性外，還包含程式碼、圖片和超過 60 篇的額外閱讀、6 篇影片和 9 個其他資源，建議存下來，然後可以拿來做前端外交，反正這大概是有生之年系列自己看也看不完。
