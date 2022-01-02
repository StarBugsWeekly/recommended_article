---
title: 第 114 期 DevOps 推薦文章
date: 2022-01-04
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps



<!-- summary -->
### [11 Things I Learned After Becoming a Coding Interviewer](https://betterprogramming.pub/11-things-i-learned-after-becoming-a-coding-interviewer-b951370ebda7)

大家這次的年終有超過 40 個月嗎？要是沒有的話是不是要準備看新的工作機會啦 (大誤)，身為一個工程師擔任應徵者的機會通常比面試官來得多，作者在他將近七年的職涯中參加過 40 次的面試，他通常會因為感到緊張，尷尬和沒自信，而在 Coding 的面試階段失敗，他總是覺得面試官就像神一樣，隨時要對他宣判什麼，而最近他的職位變得相對資深，所以開始需要規律的當面試官，所以他想要分享 11 件事情給準備參加面試的人

01. 面試官並不會將履歷鉅細彌遺地看過，過往的工作經驗也不代表目前的 Coding 技巧有多強，所以不用花太多時間去準備自我介紹的部分
02. 面試官可能也跟應徵者一樣緊張，因為兩者都在做一件不是日常工作會做的事情，面試官也會怕被應徵者問倒
03. 多說一點話可以幫助自己，畢竟一面試就馬上開始寫程式有點怪，總是需要暖機一下，例如利用前面提到沒那麼重要的自我介紹，然後再真的寫程式時，可以多跟面試官確定問題，解釋為什麼要這樣寫...等，讓彼此融入在面試的過程中，這將會使面試官留下較好的印象
04. 寫程式的技能不是唯一的衡量標準，溝通能力是一個更重要的決定因素，所謂的溝通不只是在於你說了什麼，你如何去表達也很重要，例如發音，語速，面部表情...等
05. 尋求協助並不丟臉，假如你在寫程式的過程中卡關了，可以適時地尋求協助，不要花太多時間讓自己一個人卡在某個點，因為面試官通常也都很樂意給出一些提示
06. 一個問題並總是會有完美的答案，其實有時候面試官更想要看到應徵者，講答案逐步組織起來的流程，雖然這筆直接講出某個直接的答案要花時間
07. 記得要選擇自己熟悉的語言，而不是工作要求裡面的，因為在面試的時候會特別容易被看破手腳，自己熟稔的語言比較不會出包
08. 通常使用 Google 是可以被允許的，雖然一開始不會明說，但假如應徵者卡關覺得有需要的話，可以對面試官提出請求
09. 當面試官再打字或是看別的地方時，可能是在做筆記或是看面試小抄，不一定是一邊工作一邊參加面試
10. 當面試官不說話時，並不表示給應徵者吃閉門羹，因為有時候閒聊會讓應徵者受到影響，面試工程師職務時，還是會以技術相關的內容為衡量依據，其他的不用多想
11. 面試官比應徵者更希望你可以獲得這份工作，因為招募是很昂貴的流程，因為招募一個人要花很多的時間，假如面試沒有通過就整個要再重來一次

<!-- summary -->
### [GitHub’s top 10 blog posts of 2021](https://github.blog/2021-12-28-githubs-top-10-blog-posts-of-2021/)

在跨入到 2022 之後，好像沒有看到太多 2021 的技術回顧文章，最近好像只有看到這篇 GitHub 回顧自己在 2021 最熱門的十大技術文章，前三名分別是 [GitHub’s Engineering Team has moved to Codespaces](https://github.blog/2021-08-11-githubs-engineering-team-moved-codespaces/)，[Behind GitHub’s new authentication token format](https://github.blog/2021-04-05-behind-githubs-new-authentication-token-formats/) 和 [Introducing GitHub Copilot: your AI pair programmer](https://github.blog/2021-06-29-introducing-github-copilot-ai-pair-programmer/)，這樣的排名結果會讓你覺得出乎意料之外嗎？對於其他十大技術文章有興趣的人可以參閱內文

<!-- summary -->
### [Spotify System Architecture](https://medium.com/interviewnoodle/spotify-system-architecture-6bb418db6084)

目前市面上有很多的音樂串流服務，例如 Spotify, Apple Music, Pandora, Soundcloud 和 Tidal，而今天作者想要跟大家解釋更多有關於  Spotify 這個音樂串流服務，首先從他的系統功能需求開始分析起，例如可以下載歌曲，發現音樂，Spotify Connect...等，接著預估他的 Scale 有多大，例如有多少使用者，歌曲的串流品質需要的頻寬，可以下載多少首歌，支援多少種語言...等，然後根據這些要點將系統架構給勾勒出來，並且逐步分析每一個元件使用的技術，函式庫與演算法...等，讓讀者可以跟著文章一步一步去做一次完整的系統架分析