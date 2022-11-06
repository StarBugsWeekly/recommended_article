---
title: 第 157 期 DevOps 推薦文章
date: 2022-11-08
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [How to Install and Run Jenkins With Docker Compose](https://www.cloudbees.com/blog/how-to-install-and-run-jenkins-with-docker-compose)

現在已經有很多 CICD 工具讓人很好上手，但不能否認的是，Jenkins 在業界還是佔有一席之地。假如想要在自己的電腦快速搭建一個 Jenkins 實驗環境該怎麼辦呢？專門提供 Jenkins 服務 CloudBees 公司寫了一篇圖文並茂的以 docker-compose 快速建立環境的文章，方便讓大家做快速的測試。<!-- summary -->

### [Automate Terraform documentation like a pro!](https://medium.com/google-cloud/automate-terraform-documentation-like-a-pro-ed3e19998808)

當 Terraform module 開發完畢時總得寫些文件讓其他團隊知道如何使用，於是作者介紹 [terraform-docs](https://terraform-docs.io/) 可以快速生成 Makrdown 或者 AsciiDoc 文件，最好的情況就是把這工具整合進 CI 的流程裡。

### [How DoorDash Ensures Velocity and Reliability through Policy Automation](https://doordash.engineering/2022/09/20/how-doordash-ensures-velocity-and-reliability-through-policy-automation/)

DoorDash 分享了他們 Infrastructure as Code 和 Policy as Code 而工具就是 [Terraform](https://www.terraform.io/) 和 [OPA](https://www.openpolicyagent.org/) 使用的經驗。OPA 內容會使用 [Conftest](https://www.conftest.dev/) 做檢查，在使用 Policy as Code 的建議有：
- 重要的 resources 改動應該要給不同相關的團隊做程式碼審查
- Terraform modules 的改動影響 infra 是可以接受的，只要工程師依照 cloud resource 規定就可以讓批准自動化
- 特定的操作只能限定在特定的 resources 內
- 程式改動必須要有資安團隊審視過
- 確保 cloud resources 的 tags 都有被使用到
- 成本上的設定可以對 infra 做更改
- 對 resource type 做審核，確保工程師寫 IaC 時可以使用到 reserved instances 或者折扣方案
