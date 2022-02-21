---
title: 第 121 期 DevOps 推薦文章
date: 2022-02-22
author: smalltown

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [Introducing Opta: Terraform on Rails](https://www.cncf.io/blog/2022/02/18/introducing-opta-terraform-on-rails/)

[Opta](https://github.com/run-x/opta) 是一個 IaC Framework，讓你可以使用高階語法來建構雲端架構，而不會迷失在低階的雲端設定組態當中，它提供使用者大量的函式庫來建立出理想中的架構，而且更棒的是他的底層使用 Terraform，所以使用者不會被鎖定在某個平台上，使用者永遠可以撰寫客製化的 Terraform，甚至是將 Opta 直接整合 Terraform 來使用

而它主要目標是希望除了業務邏輯跟 Unit Testing 由 Developer 去負責之外，其他諸如 Provision, Deployment, Observatility, Multiple Envs, Security 都由他來完成， Opta 目前支援三大主要公有雲 (AWS, GCP 跟 Azure)，現在主要有底下幾個 Module:

- Microservices (powered by Kubernetes)
- Databases - Postgres, MySQL, Redis
- Serverless workloads
- Networking - VPCs, Subnets, Load balancers
- CDN (Content Delivery Network)
- Object storage (S3, GCS)

除此之外他也將一些 Best Practice 融合近來，例如：

- Observability (Datadog, LogDNA)
- SOC2 compliance
- Continuous Deployment
- Hardened network and security configurations (AWS, GCP, Azure)
- Auto-scaling and high availability (HA)

### [Introducing a Google Cloud architecture diagramming tool](https://cloud.google.com/blog/topics/developers-practitioners/introducing-google-cloud-architecture-diagramming-tool)

相較於上面的 Opta 使用 YAML 檔案格式來描述雲端架構，GCP 這邊則是推出了 Google 雲端架構繪圖工具，讓使用者可以再將想要的雲端架構圖透過該工具繪製完成後，透過指標點一下，就直接將該架構在 GCP 內給部署出來，看來以後在 IaC 的世界裡，搞不好畫圖比寫 Code 來得重要了 😂

### [HashiCorp Terraform AWS Provider Introduces Significant Changes to Amazon S3 Bucket Resource](https://www.infoq.com/news/2022/02/terraform-aws-provider-s3/)

看完高階的 IaC，接著來看低階一些的，HashiCorp 最近釋出 Terraform AWS Provider 4.0，在這個更新版當中，在 S3 Bucket 這個資源中包含了巨大且不可向下相容的變更，因此沒有鎖定 AWS Provider 版本的人，在最近使用的時候要注意一下，假如發生不意外的錯誤，就有可能是因為這次的更新所造成的，看是要降板，或是捲起袖子來修改一番了💪

### [Include diagrams in your Markdown files with Mermaid](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)

上週情人節時 GitHub 宣佈一個新功能，就是以後可以在 Markdown 檔案格式中透過 Mermaid 來增加圖像了！這樣一來以後想要在 Markdown 檔案中加入流程圖的話就可以不用特地畫一張圖，然後再把圖片轉成 JPG/PNG 檔之後加到 Repository 中，然後再讓 Markdown 去引用他，可以省下不少時間 🕒