---
title: 第106期 Testing 推薦文章
date: 2021-11-09
author: larry
# description: 這篇文章將從 AOP 的核心思想談到目前主流實現 AOP 的不同策略並比較他們的差異，適合了解 Java 語言或者有稍微玩過 AOP 但是不清楚其原理的人閱讀。
layout: layouts/post.njk
tags: [Software Engineering]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Testing

### [一次搞懂單元測試、整合測試、端對端測試之間的差異](https://blog.miniasp.com/post/2019/02/18/Unit-testing-Integration-testing-e2e-testing)

大家都知道測試可以確保程式的正確性，但根據不同的目的，測試又可大略分成單元測試、整合測試、端對端測試三種，因此在真的開始寫測試之前，務必要先搞清楚你需要的是哪種測試，才不會花了一堆時間結果沒測到最重要的部分哦～

### [What's in a Story?](https://dannorth.net/whats-in-a-story/)

身為工程師，在跟 PM 溝通需求時最怕的就是 PM 以為他講清楚了，工程師也以為自己聽懂了，結果做出來後得到的回覆卻是「這不是我要的！」。所以在真的開始實作之前，雙方可以用 User Story 把各種 scenario 一一列出來，雙方都同意之後這些 scenario 也可以直接寫成測試，真的是非常省時間的一套方法

### [Mocks and explicit contracts](http://blog.plataformatec.com.br/2015/10/mocks-and-explicit-contracts/)

寫測試寫到一定程度之後，為了方便建立測試專用的環境，一定會需要用到 mock。而這篇文章雖然已經是多年前發表的，但我覺得他在講怎麼正確使用 mock 講得非常好，尤其是他內文有講到 mock 應該當作名詞而非動詞來用，看完之後覺得又更了解怎麼用 mock 跟 interface 了