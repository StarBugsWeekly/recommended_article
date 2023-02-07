---
title: 第 167 期 前端開發 推薦文章
date: 2023-02-07
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [High Definition CSS Color Guide](https://developer.chrome.com/articles/high-definition-css-color-guide/)

先說文長注意。CSS color 4 帶來了許多用來管理和處理顏色的工具，作者它寫了一篇指南涵蓋了這些新的功能。在指南中會學習到以下幾點：

* 什麼是色域？
* 人類的視覺範圍。
* 什麼是色彩空間？
* 如何使用更多顏色、新空間和嘗試結果。
* 回顧典型的色彩空間。
* 認識新的 Web 色彩空間。
* 加權平均顏色。
* Gamut clamping（不知道怎麼翻 🥲）
* 選擇色彩空間。
* 轉換到 HD CSS 顏色。
* 檢查色域和色彩空間支持。
* 使用 Chrome DevTools 嘗試顏色。

<!-- summary -->

### [Why React isn't dying](https://tkdodo.eu/blog/why-react-isnt-dying)

文章中作者談論為何現在推特上正出現一些關於 React 正在枯萎，或是其他 Framework 比 React 更好的討論，其實比起文章我更喜歡第一則留言說，如果你不能放棄 100% 的向下相容，那你就會慢慢失去動力，這就是大家認為 React 已死的原因（遠望 Vue3）。

### [You’ve Got Options for Removing Event Listeners](https://www.macarthur.me/posts/options-for-removing-event-listeners)

相信大家看到標題都直覺的想到了可以用 `removeEventListener` 來移除監聽的事件，但除此之外，文章裡還介紹了其他 3 種方法：

* 使用 `addEventListener` 的第三個參數可以設置 once options。
* 複製和替換整個節點。
* 使用 `AbortController` 可修改複數的監聽事件。

文末也有以上 4 種方式的選擇時機，大家可以參考看看！
