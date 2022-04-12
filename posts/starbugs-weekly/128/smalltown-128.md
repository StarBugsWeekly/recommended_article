---
title: 第 128 期 後端開發 推薦文章
date: 2022-04-12
author: smalltown

layout: layouts/post.njk
tags: [Backend]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## 後端開發

<!-- summary -->
### [How to design a system to scale to your first 100 million users](https://levelup.gitconnected.com/how-to-design-a-system-to-scale-to-your-first-100-million-users-4450a2f9703d)

如何設計一個可以服務增加到 1 億使用者的系統？作者使用很淺顯易懂的例子，跟精美的架構圖，一步一步帶著使用者去理解怎麼設計出一個可以服務 一億個使用者的系統，大概會提到的範圍如下：
<!-- summary -->

- 首先從把所有的東西都塞在同一台機器裡面為例
- 分析什麼叫做 Scaling Out 與 Scaling Up
- 解釋為什麼要把 Web Server 和 Database 拆開來
- 如何讓 Web Server 可以達成 Scaling Out
- 如何讓 Database 可以達成 Scaling Out
- 怎麼去選擇 NoSQL 或是 SQL
- 最後提到怎麼去利用 CDN 來幫助自己的系統服務使用者

### [7 tools for visualizing a codebase](https://lmy.medium.com/7-tools-for-visualizing-a-codebase-41b7cddb1a14)

想要撰寫文件但是卻不知道該從何開始嗎？假如有這樣困擾的話，可以考慮直接在文件中加入圖片，畢竟有圖有真相 😂 而此篇文章的作者推薦了幾個可以從程式碼或是組態，直接視覺化的工具

- docker-compose-viz: 將 docker-compose.yml 檔案轉換成圖片
- Code2flow: 將 Python, Javascript, Ruby 和 Ruby 程式碼內函式的呼叫關係轉換成圖片
- pycallgraph, pyan: 跟 Code2flow 一樣的功能，但是特別針對 Python 語言做處理
- Bazel: 他是一個用來 Build Java, C++, Go, ANdroid, iOS...等其他語言的工具，而他剛他剛好也可以將程式與其使用到的函式庫相依性用視覺化呈現出來
- pipdeptree: 跟 Bazel 可以達到同樣的效果，不過是針對 Python 語言
- depgraph-maven-plugin: 跟 Bazel 可以達到同樣的效果，不過是針對使用 Maven 的 Java 程式
- Gource, CodeSee: 假如不是想要撰寫文件，只是想要快速瞭解某個 Code Repo的話，可以試試看這兩個工具

### [6 Algorithms Every Developer Should Know](https://medium.com/dare-to-be-better/6-algorithms-every-developer-should-know-f78b609c7e7c)

作者自己並不是一個很喜愛研究資料結構和演算法的工程師，但他現在在他的工作生涯中經歷過的大大小小專案之後，發現有 6 個演算法是每個工程師都應該要知道的，因為這 6 個演算法幾乎可以解決開發流程中的每個問題，每個演算法的詳細介紹可以參閱內文

- Sorting Algorithm (排序演算法)
- Searching Algorithm (搜尋演算法)
- Dynamic Programming (動態規劃)
- Recursion Algorithm (遞迴演算法)
- Divide and Conquer (分治法)
- Hashing (雜湊函式)
