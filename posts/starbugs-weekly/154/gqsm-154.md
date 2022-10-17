---
title: 第 154 期 前端開發 推薦文章
date: 2022-10-18
author: gqsm

layout: layouts/post.njk
tags: [Front-end]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 前端開發
<!-- summary -->

### [The Web’s Next Transition](https://www.epicweb.dev/the-webs-next-transition)

Web 開發的每個架構都有屬於他的好處以及痛點，而就是那些痛點促使我們不斷的進入到下一個新的架構。在文章會一一以下每種架構的優缺點：

* Multi-Page Apps (MPAs)
* Progressively Enhanced Multi-Page Apps (PEMPAs)
* Single Page Apps (SPAs)

目前最流行的是 Single Page Apps，但我們正進入到另一個新架構的過渡期當中！

<!-- summary -->

### [【MVVM】如何手刻 Vue 的 Text Interpolations 與 Data Binding](https://medium.com/codememo/mvvm-%E5%A6%82%E4%BD%95%E6%89%8B%E5%88%BB-vue-%E7%9A%84-text-interpolations-%E8%88%87-data-binding-4f4f8442d1a6)

作者會在文章中解釋如何用原生的 JavaScript 實作目前前端框架常見的資料綁定，其中會涉及到以下幾個知識和技術點：

1. 如何將 data 編譯到 HTML 的標記上 {{ expression }}
2. 如何使用 Array.reduce() 對 template 標記取值
3. 如何使用 Proxy API 監聽 data 的 setter 以實現響應式數據綁定
4. 使用訂閱/發佈模式的概念，收集需編譯的依賴文本對象
5. 使用閉包 (Closure) 的概念，紀錄依賴對像
6. 如何使用遞迴進行深層遍歷
7. 如何做到「指哪打哪」的響應式

### [TypeScript: Type Guards](https://www.robinwieruch.de/typescript-type-guard/)

前一陣子在讀 TypeScript 文件的時候有讀到 this-based type guards，和這篇文章一樣都是用 `XXX is Type` 檢查使用者自己定義的型別，以確保經過 type guard 的 value 型別。
