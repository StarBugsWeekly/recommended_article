---
title: 第 161 期 DevOps 推薦文章
date: 2022-12-06
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How We Use Terraform At Slack](https://slack.engineering/how-we-use-terraform-at-slack/)

Slack 使用 Terraform 時也是早期從單一個 AWS 帳號逐漸擴展，也會把大型服務拆成多個 Terraform state files 管理，也會分配不同 AWS IAM 權限來提供 sandbox 環境，使用文法檢查工具來輔助 Terraform 多版本讓環境可以逐一升級<!-- summary -->，Terraform module 從原本相對路徑逐漸改成用 git 抓下來到最後開發工具只可惜更難做測試，也開發了 Terraform Smart Planner 讓還沒 merge 的測試結果印出 output 讓 reviewer 更好審視。這篇文章的結語也說們的 Terraform 之旅離完美還很遠，也不忘在文章最後偷偷徵才。

### [How to Mentor Interns to Become Skillful Engineers](https://slack.engineering/how-to-mentor-interns-to-become-skillful-engineers/)

如何讓讓實習生快速進入狀況也是 DevOps 的一環，Slack 就分享除了要注意分配給實習生要做什麼專案外，他的 onboarding 流程跟資源是否能讓他快速進入狀況？如何測量實習生的實習成效是成功的？如果實習生有多位 mentors 該怎麼確保他可以溝通順暢？文章對於制定這些計畫有個詳細的紀錄，即使用在正職員工上也很受用。

### [A Day in the Life of a Cloud Engineer at Slack Australia](https://slack.engineering/a-day-in-the-life-of-a-cloud-engineer-at-slack-australia/)

在澳洲的 Slack 的雲端工程師分享他的一天行程，Slack 的雲端團隊有三種分別是 Foundation、VM 和 containers，在 VM 團隊的他表示在每週開會時可以了解其他團隊的事務。公司的溝通風格基本上還是以非同步為主，code review 也是如此，這也有助於跟北美的同事做溝通。