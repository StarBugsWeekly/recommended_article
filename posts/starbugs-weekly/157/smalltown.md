---
title: 第 157 期 Coding 推薦文章
date: 2022-11-08
author: smalltown

layout: layouts/post.njk
tags: [Coding]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Coding

<!-- summary -->
### [Git commit messages are useless](https://blog.trunk.io/git-commit-messages-are-useless-c2f3c46f678e)

作者覺得 Git Commit Message 根本就不被需要，就像沒有人在乎你早餐吃了什麼一樣XD 作者的論述與推薦作法如下，(但 Main Branch 的 Commit Message 還是相當重要的) 大家是否也這樣覺得呢？這篇文章的回覆滿多人不認同作者的觀點的，大家可以去看看。
<!-- summary -->

- 因為 Commit Message 在 PR Branch 其實沒有太大的意義，讓 PR 最後被 squash-merged 到 Main Branch 就好，這時設定 GitHub 以 PR 名稱當成 Commit Message 就可以了，而且程式本身的註解才是重點
- Git CLI 最近也添加了一個可以讓開發者不需要寫 Commit Message 的 Flag `--allow-empty-message`，推薦大家可以使用 command alias 的功能來設定 git commit 指令 `git config --global alias.nccommit 'commit -a --allow-empty-message -'`
- 最後就是要記得設定 GitHub Branch Protection 不允許任何人直接 Commit 到 Main Branch

### [m1guelpf/auto-commit](https://github.com/m1guelpf/auto-commit)

auto-commit 是一個可以根據你寫的程式碼自動產生 Commit Message 的小工具 (其使用 Rust 開發且利用了 OpenAI Codex)，這樣一來就可以不用再去掰要寫什麼 Commit Message 了XD

### [Want Cleaner Code? Use the Rule of Six](https://betterprogramming.pub/want-cleaner-code-use-the-rule-of-six-c21635ee2185)

每個人都想要寫出 Clean Code，也有不少書籍在談論這個主題，不過你不用急著把書看完才能夠寫出 Clean Code，這篇文章提供了簡單的規則 (Rule of Six) 與詳細範例，讓開發者輕易寫出不令人感到混淆的程式碼

- 一行程式碼盡量只做一件事
- 拆解太複雜的程式碼成多行 (SIMPLE: Split Into Multiple Lines)
- 將功能一樣的程式碼寫成函示 (MORE: Move Out and Rewrite as a Function)
- 多練習同時使用 SIMPLE 與 MORE 來撰寫程式碼