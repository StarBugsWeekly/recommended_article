---
title: 第 162 期 TypeScript 推薦文章
date: 2022-12-13
author: larry

layout: layouts/post.njk
tags: [TypeScript]
---

## TypeScript

### [Migrating millions of lines of code to TypeScript](https://stripe.com/blog/migrating-to-typescript)

大家應該多少有聽過 Stripe 這間公司，他們在今年把他們最大的 JS codebase 總計數百萬行的程式碼從 Flow migrate 到 TypeScript。這篇文章簡單分享了他們為何要這麼做、以及他們 migration 的過程和結果，如果你手上也有專案在考慮要不要為了好維護 migrate 到 TypeScript，這篇文章可以當作一個參考。

### [Use TypeScript Record Types for Better Code](https://itnext.io/use-typescript-record-types-for-better-code-ce1768c6cb53)

其實我以前跟 TypeScript 裡面的 Record/Pick/Omit 那些對型別進行運算、運算的 utility 很不熟，是前陣子仔細去讀了 TypeScript 的官方文件後才發現這些東西真是太好用了。而這篇文章就是介紹了 Record 的用法，推薦給跟我一樣的型別苦手們。

### [Type-Safe TypeScript With Type Narrowing](https://betterprogramming.pub/type-safe-typescript-with-type-narrowing-649450d708df)

TypeScript 寫久了，遲早有一天會覺得 TypeScript 怎麼那麼笨，「我這邊明明就不可能是 XX 型別啊，你一直噴錯是怎樣？」。別氣別氣，只要你懂 TypeScript 的型別推論，你就可以用 type narrowing 把你的程式碼變得更加安全、而且可讀性也更高。不過這算是比較進階的技巧，如果你對 TypeScript 的型別還不是很熟悉，那可以先把這篇文章存起來，過個一年半載再回來看。

