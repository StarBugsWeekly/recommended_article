---
title: 第 163 期 前端開發 推薦文章
date: 2022-12-20
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
---

## 前端開發
<!-- summary -->

### [Optimize Interaction to Next Paint](https://web.dev/optimize-inp/)

Interaction to Next Paint (INP) 是用來測量回應速度的指標，如果使用者在網頁上進行操作但頁面沒有任何回應的話，那就這個使用者體驗就是差的。而 INP 就是要觀察頁面對使用者做的每一項操作回應的延遲時間。在這篇文章裡面會告訴你該如何測量、分析以及改善 INP 較差的問題。

<!-- summary -->

### [Vite 4.0 is out!](https://vitejs.dev/blog/announcing-vite4.html)

Vite 3 在發布之後，每週的下載量暴增到 250 萬，且根據今年 [Jamstack Conf](https://twitter.com/vite_js/status/1589665610119585793) 的問卷顯示，在社群內的使用率也提高到 32%，滿意度也維持在 9.7 高分。那在前作如此好評的狀況下，Vite 4 增修了以下幾點：

* 瀏覽器的支援度
* 將 .css 作為 string import
* 如果環境變數中有 # 或 ` 則需要用 " 包起來
* 減少打包後的尺寸
* 升級到 Vite Core

更詳細的內容就快點進去官方的公告看看吧！

### [Web Performance Calendar](https://calendar.perfplanet.com/2022/web-performance-apis-appreciation-post/)

這篇文章列舉了幾點在 Web 界用來處理效能的酷炫 API：

* [Render blocking status](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceResourceTiming/renderBlockingStatus)
* [OffscreenCanvas](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)
* [Async image decoding](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/decoding)
* [Image decode()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/decode)
* [loading=lazy](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/loading)
* [fetchpriority](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/fetchPriority)
* [103 Early Hints](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/103)

作者也有在每個 API 下快速介紹並附上目前的支援度，是一篇很好去吸收名詞的好文章！

