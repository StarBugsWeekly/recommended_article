---
title: 第 123 期 DevOps 推薦文章
date: 2022-03-08
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Workshops as code](https://www.gitpod.io/blog/workshops-as-code)

自己也蠻喜歡參加或者舉辦 workshop 所以對這篇很有感觸，以前 workshop 在真正體驗核心技術之前就得花很多時間做前置環境設定，作者就提及之前 2019 年舉辦 NixOS workshop 攏長的前置過程，創虛擬機看似簡單但每個人的環境都不一樣，出問題很難 debug。<!-- summary -->而 Gitpod 正好解決上述的問題，我們可以把 workshop 環境標準化寫成 code，藉由 container 的重複使用和重複再製的特性，以及 Gitpod 基本上是跑在雲端上的，就讓所有參加者的環境確保一模一樣。

現在你可以直接在網頁按個按鈕就有 NixOS 的環境了，作者也有提供 [gitpod-io/template-nixo](https://gitpod.io/#https://github.com/gitpod-io/template-nixos) 給大家嘗試。

### [The Best DevOps Blogs](https://dev.to/karllhughes/the-best-devops-blogs-1bn5)

雖然這篇文章有點舊了，但其中分享 blogs 的評分非常實用，作者依照 5 個角度去評分這個 blog，分析的依據有：

1. 文章品質
2. 一致性
3. 文章有效壽命
4. 技術深度
5. 用途廣泛程度

有些偏向新聞或者文件、有些像是論壇、有些不免俗的會寫自家產品的 DevOps 解決方案或者累積的經驗談，作者也是給經驗談最高的分數。除了文字之外，裡面也有 podcast 的形式，適合通勤的時候聽。

### [How many AWS Accounts do I need?](https://medium.com/geekculture/how-many-aws-accounts-do-i-need-d54261a0ab04)

我想當 AWS 使用久了就會有這個煩惱，作者就以這些面向去探討，幫讀者分析自己要怎麼設計多個 AWS 帳號的用途。

* 未來商業發展與團隊
  * 例如以 Infrastructure、Network、Security、Application 和 Data Warehouse 等等不同的團隊做 AWS 帳號的區分。
* Domain Driven Design（領域驅動設計，俗稱 DDD）
  * 依照不同的商業領域做區分，要注意的判斷哪些 services 應該在同個 AWS 帳號，哪些可以分開。
* 環境
  * 同一個 service 依照不同的環境分 AWS 帳號，如果本身環境很多的確可以考慮把多個環境合併在一個 AWS 帳號裡。
* 災難恢復
  * 為了減少 service 恢復的時間，可以把全部或者部分的 service 複製到另外一個 AWS 帳號。
* 多個 region
  * 這邊比較特別的是作者是以非技術的角度作切入的，每個地理位置的資料隱私政策都不一樣，為了提供更好的使用體驗而做不同 region 和不同 AWS 帳號的決策。
* 沙盒/測試
  * 跟環境分帳號不一樣的是這需求純粹做類似 infrastructure PoC，或者測試串接多個 AWS 帳號 VPC 網路，或者同個 service 以不同的沙盒環境做測試而區分 AWS 帳號。
* 正確使用 CI/CD Pipeline 的 AWS 帳號
  * 這也是很有挑戰性的設計，CICD pipeline 要如何「觀察」你的 infrastructure 和 services 在不同的環境、region 和 AWS 帳號之後再做部署。