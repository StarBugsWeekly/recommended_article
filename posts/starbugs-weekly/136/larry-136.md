---
title: 第 136 期 Security 推薦文章
date: 2022-06-14
author: larry

layout: layouts/post.njk
tags: [Security]
---

## Security

<!-- summary -->

### [Implementing Two-Factor Authentication with NodeJS and otplib](https://soshace.com/implementing-two-factor-authentication-with-nodejs-and-otplib/)

看完 TOTP 2FA 的原理之後覺得很有趣，想要幫自己的服務也加上 TOTP 的功能嗎？這邊有一篇教學教你怎麼用現在的 node package otplib 來實作 TOTP，就算沒有想自己做也可以看一下，會對於 TOTP 的內部實作更有概念哦

<!-- summary -->

### [聽說不能用明文存密碼，那到底該怎麼存？](https://medium.com/starbugs/how-to-store-password-in-database-sefely-6b20f48def92)

身為一個服務提供者，除了支援 TOTP 外，在儲存使用者密碼時也必須多注意才行，所以這邊講解了到底該用什麼方式儲存使用者的密碼，才是最安全的

### [[Security] SSL — HTTPS 背後的功臣](https://medium.com/starbugs/security-ssl-https-%E8%83%8C%E5%BE%8C%E7%9A%84%E5%8A%9F%E8%87%A3-df714e4df77b)

大家都知道網站要有 HTTPS 才安全，但你知道他背後的功臣 SSL 是怎麼運作的嗎？如果你好像知道，但又有點不太確定是怎麼樣，那就趕快來讀讀文章複習一下吧～
