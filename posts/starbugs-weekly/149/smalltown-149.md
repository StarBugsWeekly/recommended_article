---
title: 第 149 期 Git 推薦文章
date: 2022-09-13
author: smalltown

layout: layouts/post.njk
tags: [Git]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Git

<!-- summary -->
### [GIT Branching Strategies in 2022](https://faun.pub/git-branching-strategies-in-2022-83938c5784d8)

Git 這套版本管理系統賦予軟體開發者能力去追蹤，管理和組織他們的程式碼，但是 Git 本身並沒有提供一個明確的分支策略，這將會導致相對大型的團隊在建立分支及合併程式碼時容易搞的一團亂，因此開發者必須自己去決定如何使用 Git 分支。本文將介紹幾種不同的分支策略，並且提供一些建議，讓你可以選擇最適合你的分支策略。

- GitFlow
- GitHub Flow
- GitLab Flow
- Trunk-based development
- Scaled Trunk-Based Development
- Release Flow

<!-- summary -->

### [Sign your Git commits with 1Password](https://blog.1password.com/git-commit-signing/)

1Password 除了對一般使用者體驗來說還不錯之外，自己覺得他在近年來也一直推出對於 Developer 很友善的功能，例如之前支援了 [SSH](https://developer.1password.com/docs/ssh/) 還有 [VIsual Studio Code](https://blog.1password.com/1password-visual-studio-code)；而 [GitHub 於近期宣布支援透過 SSH Key 去對 Git Commit 做簽章驗證](https://github.blog/changelog/2022-08-23-ssh-commit-verification-now-supported/) (之前只支援 GPG Key)，1password 這篇文章便是介紹了如何將 SSH Key 儲存於其中，並對 Git Commit 做簽章驗證。

### [Merging two GitHub repositories without losing commit history](https://hacks.mozilla.org/2022/08/merging-two-github-repositories-without-losing-commit-history/)

自己是有把 Git Repository 搬來搬去的經驗，但是把兩個 Repository 合併在一起的經驗卻是第一次，這篇文章介紹了如何將兩個 Repository 合併在一起，並且保留原本的 Commit History。先筆記下來，搞不好將來有一天自己也會使用到