---
title: 第 164 期 Node.js 推薦文章
date: 2022-12-27
author: larry

layout: layouts/post.njk
tags: [Node.js]
---

## Node.js

### [Popular Node.js patterns and tools to re-consider](https://practica.dev/blog/popular-nodejs-pattern-and-tools-to-reconsider/)

在 Node.js 的生態系中，有很多我們慣用的第三方 package 或是常寫的一些 pattern，他們當初可能是為了解決某些問題才出現，但現在已經有點不合時宜。因此這篇文章列出了幾個在採用之前應該重新考慮的模式和工具，讓你在 npm install 之前想想是不是真的需要，或者有更好的替代方案。

### [Guidelines for choosing a Node.js framework](https://simonplend.com/guidelines-for-choosing-a-node-js-framework/)

近年來 Node.js 用來寫 API Server 的框架越來越多了，除了最知名的 Express/Koa 之外，還有 Fastify、Hapi 等等強調速度、易用性的框架。而這篇文章並沒有直接跟你說要選什麼框架，而是跟你說在選擇的時候該考慮哪些問題，譬如說你需不需要 Websocket、有沒有打算用 TypeScript 等等，這些都會決定哪一個框架最適合你

### [Best practices for creating a modern npm package](https://snyk.io/blog/best-practices-create-modern-npm-package/)

現在要發佈一個可靠的 npm package，可不是把幾個 function 包一包傳上去就好了，你可能還需要加上單元測試、同時支援 ESM 跟 CJS、做安全性檢查等等，這篇文章搜集了這些 best practice（順便推銷他們自己家的工具XD），讓你做為一個專案的維護者，可以發佈出更高品質的 package。

