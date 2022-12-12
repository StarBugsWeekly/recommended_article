---
title: 第 162 期 ChatGPT 推薦文章
date: 2022-12-13
author: smalltown

layout: layouts/post.njk
tags: [ChatGPT]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## ChatGPT

### [Awesome ChatGPT](https://github.com/humanloop/awesome-chatgpt)

有不少人已經開始把 ChatGPT 整合到既有的工具與服務中，例如 Python SDK, Chrome Extension 顯示跟 Google 搜尋結果的對比，GitHub Action 幫忙 Code Review，VSCode extension 幫忙寫程式，各種 Chat Bot 如 Telegram, WhatsApp, Twitter...來回覆對話，所以 Awesome 系列的 GitHub Repository 也有啦！之後可以跑來這個 Repository 看看有什麼有趣的 ChatGPT 專案又被實作出來了!

<!-- summary -->

### [ChatGPT for Google](https://github.com/wong2/chat-gpt-google-extension)

最近看到大家都一直在討論 ChatGPT，把各種問題丟給他去回答，很多人已經開始叫他寫程式了，感覺 Stack Overflow 的地位岌岌可危🤣 也有開發者想到其實我們現在還很常去找答案的方式就是去問 Google，所以有人寫了這個 Chrome Extension，讓搜尋字串也直接餵給 ChatGPT，不知道再這樣下去，以後 ChatGPT 的回答內容是不是要開始有業配文跟置入性行銷了?!

### [Introducing ChatGPT!](https://kozyrkov.medium.com/introducing-chatgpt-aa824ad89623)

Google 的 Chief Decision Scientist "Cassie Kozyrkov" 寫了一篇揭秘 ChatGPT 的文章，文章開頭先解釋了 ChatGPT 的技術原理為 GAN (Generative Adversarial Networks)，接著稍微提了 GAN 的運作原理，然後花了相對多的篇幅來講述 ChatGPT 的回答其實只是碰觸到了部分的現實，其他則是他想像出來的，這聽起來很像是缺點，但這也正是他的強項，因為他不會受限於現實，可以回答出充滿創造力與在框架外的答案，例如你問 ChatGPT 假如他的飛的話他會做什麼，他可能會回答 "我會像雄鷹一樣翱翔在天空，感受我翅膀下的風和飛行的自由"；緊接著提到利用 ChatGPT 寫程式的體驗

最恐怖的地方要來了，**上面的內容是由 ChatGPT 所產生的，而且是錯誤的**，作者是這樣跟 ChatGPT 說的 "請用 Cassie Kozyrkov 的風格寫一篇揭秘 ChatGPT 的部落格文章，解釋為什麼 ChatGPT 有用，跟 GAN 有什麼關係，以及為什麼 ChatGPT 的回答只是部分切合現實"；**但其實 ChatGPT 根本就不是使用 GAN 實作出來的，他是 Generative Pretrained Transformer**，但我相信假如不是對於這些背景知識很熟的人，應該都已經被騙了 🥲 沒錯，ChatGPT 所產生的部分回答是胡扯的，但他不算是騙子，因為所謂的騙子必須要先知道事情的真相並且去誤導人類，他只是不關心事情真相而胡說八道的角色，而這也是我們必須要先知道的最重要的重點

其實除了 ChatGPT 不是 GAN 所實作出來的之後，作者其他的論點都是真的，也就是一開始所提的 ChatGPT 的回答只有部分切合現實，因此可以想像我們在接下來的生活中會處在一個比以往都充斥著更多虛假內容的時代，所以會需要對於事實查核投入更多的精力；ChatGPT 確實讓作者留下了深刻的印象，佩服 OpenAI 所取得的非凡成就，而作者也鼓勵大家去使用它，因為他在各個應用領域中都具有相當大的潛力且值得去關注，換言之，吹牛胡扯的人是有用的，只要你知道他們是在吹牛的人就行了😂 但作者也對人類容易相信別人，導致 AI 將為人類帶來的坎坷之旅感到憂心，人類以後必須對於所有的線上資源採用不同的信任方式，避免獲取一堆有意人士製作出來的虛假內容...