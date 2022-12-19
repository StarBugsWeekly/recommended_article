---
title: 第 163 期 Git 推薦文章
date: 2022-12-20
author: smalltown

layout: layouts/post.njk
tags: [Git]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## Git

### [Monorepo Build Tools](https://earthly.dev/blog/monorepo-tools/)

最近在軟體開發的圈子中，使用 Monorepos 來管理程式碼有變流行的趨勢，Monorepos 指的是單一個 Repository 中包含著許多相關但是不同專案的程式碼，他有不少優點，但這樣的管理方式也帶來不少的挑戰，假設一個 Repo 中有數百個服務，彼此之間存在著相依性，當其中一個服務有變動時，如何讓其他的服務不會全部都被重新測試，編譯和部署？這時就可以依靠 Monorepos 專屬的工具來解決這個問題，在評估相關類型的工具時，通常會需要考慮以下幾個因素：
<!-- summary -->

- Programming Language Support: 確認選擇的工具支援你目前以及未來所使用的程式語言
- Learning Curve: 每個工具的學習成本各有不同，評估工具的複雜度，確認是否適合你的團隊
- Caching: 一個理想的建構工具，對於同一個 Build 不應該被執行兩次，應該要選擇具備在遠端分散式環境執行與支援快取的工具
- Build Introspection: 能夠洞察被構建服務的流程和相依關係，允許工程師去查看構建圖，構建時哪個環節效率不佳，或是變更牽涉到哪一些專案
- Versatility: 構建以外的附加功能，例如相依套件如何被安裝？整合測試如何運行？測試資料庫如何被還原？換句話說，除了從程式碼構建 Artifact 之外的其他問題都需要被考慮進去

而目前在這個領域中，作者介紹了四個工具供大家選擇，底下根據上面提的選擇要點來做比較 (不過這篇文章是 Earthly 所撰寫，所以不能全信XD):

- Bazel: 
    - Programming Language Support: Java, C++, Python...等
    - Learning Curve: 四個工具中最複雜
    - Caching: 支援遠端快取和分散式執行 (開源 & 商用版本)
    - Build Introspection: 透過 `bazel query` 和其他相關指令提供強大的 Introspection 功能
    - Versatility: 相當受限，只可以在 run 的階段執行整合測試，至於環境設定和自動構建方面則是被認為不在此工具的支援範圍內

- Pants:
    - Programming Language Support: Go, Python, Java...等 (沒有 JavaScript)
    - Learning Curve: 透過 Static Introspection，使得他比 Bazel 更易用一些
    - Caching: 支援遠端快取和分散式執行 (開源 & 商用版本)
    - Build Introspection: 透過 `pants dependencies` 指令提供良好的 Introspection 功能
    - Versatility: 相當受限，環境設定和自動構建方面也是被認為不在此工具的支援範圍內
- NX:
    - Programming Language Support: Javascript, Go, Rust，還有 iOS 和 Android 執行器
    - Learning Curve: 對於 JavaScript 開發者來說學習曲線最低
    - Caching: 支援遠端快取和分散式執行 (商用版本)
    - Build Introspection: 提供一些 Introspection 功能
    - Versatility: 透過 npm 腳本支援不可快取的步驟和一次性的構建任務

- Earthly:
    - Programming Language Support: 任何可以運行在 Linux 環境的東西
    - Learning Curve: 有點類似 Dockerfile，使用一連串的 RUN 指令來構建，學習曲線最低
    - Caching: 支援遠端快取和分散式執行 (開源 & 商用版本)
    - Build Introspection: 受限的 Introspection 功能
    - Versatility: 透過包裝現有的工具來提供環境設定和自動構建的功能

### [The Wordcel's Guide to Shape Rotation using the Git Commit Graph](https://www.dolthub.com/blog/2022-12-14-wordcels-guide-to-git/)

活在 2022 年快要結束的這個當下，應該沒有人會質疑 Git 在軟體開發領域的地位，幾乎每個人都需要使用它，但不一定每個人都真的了解他，這篇文章的作者坦承他一開始費了很大的勁去使用 Git，透過了很長時間的研究和練習之後才總算比較會使用一些，也才有辦法分享這篇文章給對於 Git 還不熟的人；文章中使用淺顯的例子加上容易理解的示意圖來解釋了 Git 常用的功能與知識，如 Git Commit, Branch, Merging, 至於 Rebase 呢？作者在最後説 Rebase 一個不被信任的黑暗工具，請大家使用 Merge 就好XD

### [How to Close a Pull Request - Merge Commit vs Squash vs Rebase on GitHub](https://leonardomontini.dev/close-pr-strategy-merge-commit-squash-rebase/)

當要把 Pull Request Branch 合併到 Main Branch 的時會看到三個選項，分別是 **"Create a merge commit"**, **"Squash and merge"** 以及 **"Rebase and merge"**，這三個選項分別會如何將 PR Branch 合併到 Main Branch 呢？而究竟哪一個選項是最好的呢？

- Create a Merge Commit: Merge Commit 是在 GitHub 最常用也是預設的選項，也是執行 `git merge` 時的預設行為，PR Branch 中的所有 Commit 歷史都完整地被保留在 Main Branch 中，然後會有一個額外的 Commit 將 PR Branch 的所有變更內容合併到 Main Branch；優點就是可以很容易追蹤到被修改的那一行程式碼是在哪一個 Commit 中，缺點就是當有很多的 Commit 在很多不同的 Branch 時，最終整個 Commit 的歷史紀錄會變得很雜亂，追蹤變更軌跡會是個相當大的挑戰

- Squash and Merge: 但你真的需要追蹤每一個變更的 Commit 嗎？包含打錯字，漏掉檔案，格式錯誤...等，假如答案是否定的，那你應該考慮使用 Squash Merge，他會忽略掉 PR Branch 中所有的 Commit，然後將所有的變更內容合併成一個 Commit 合併到 Main Branch 中，如此一來，你可以放心的在 PR Branch 中提送任何你想要的 Commit，因為最終只會有一個 Commit 被合併到 Main Branch 中

- Rebase and Merge: 當你不需要一個額外的 Commit 來得知 Merge 的發生時，而且希望最終所有的 Commit 都線性在單一個 Branch 中時，就可以使用 Rebase and Merge，他會保留所有的 Commit，而且在合併時不會有額外的 Commit；缺點就是在 Rebase 遇到合併衝突時，很容易在無意間遺失部分的程式碼，而且假如你需要追趕上多個 Commit 時，你最後可能需要為每一個 Commit 解決合併衝突，而不像其他的 Merge 選項，只需要解決一次合併衝突

而究竟要選擇哪一個比較好，作者覺得假如 PR Branch 不會開著很久的話，那麼 Squash Merge 是個不錯的選擇，而他本身並不是 Rebase 的粉絲，因為他覺得使用 Rebase 很容易造成失誤，但是在決定要採用哪一個之前，可以先想想看自己和團隊需要去看歷史 Commit 的頻率有多高，團隊中有多少個成員，使用的 CI 工具是否需要完整的 Commit 歷史