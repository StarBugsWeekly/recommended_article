---
title: 第 146 期 DevOps 推薦文章
date: 2022-08-23
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How Blockchain Tech Can Improve DevOps Practices in Web3](https://dzone.com/articles/how-blockchain-tech-can-improve-devops-practices-i)

這篇介紹了 DevOps 精神可以幫到 Web3 哪些層面，以 Ethereum 為例，把 DevOps 八字環的回饋、開發、測試、整合、CICD、監控以及維運對應的工具都寫出來，以及區塊鏈特性的關係我們要注意的地方，可以一次窺探 Web3 技術生態系的文章。<!-- summary -->

### [When docker images stop being portable](https://mental-reverb.com/blog.php?id=37)

作者把 CI 伺服器從 Ubuntu 16.04 升級到 20.04 發現 gnulib 有 path 太長的 bug 導致 container image 無法下載。後來發現這個 bug 一直都有，唯一的變動是 docker 的儲存驅動（Storage Driver）從 aufs 變成 overlay2，就因為 overlay2 比 aufs 多四個字導致 path 超過 4096 bytes 的限制。本文可以看到作者重現 bug 詳細的心路歷程。

### [Is it time to migrate from Lens to OpenLens to manage your Kubernetes clusters?](https://medium.com/dev-genius/is-it-time-to-migrate-from-lens-to-openlens-75496e5758d8)

Lens IDE 是 Kubernetes 生態好用的工具之一，不過最近越來越商業化了，所以作者就介紹 OpenLens 這個工具，以及 Lens 與 OpenLens 的關係。使用 OpenLens 有兩個方法，使用社群提供的檔案或者自己安裝，但是不論哪一種都會遇到 Windows 或 macOS 程式碼簽章（Code Signing）的問題，自己個人下載基本上都可以用，但是有些組織的電腦會有資安的要求，運行的軟體必須要有程式碼簽章才可以，所以可以自己跟 Windows 或 Apple 買開發方案，或者捐款給社群讓他們可以付開發方案的費用。