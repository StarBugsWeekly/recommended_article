---
title: 第 145 期 Security 推薦文章
date: 2022-08-16
author: smalltown

layout: layouts/post.njk
tags: [Security]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## Security

<!-- summary -->
### [Cloud Native Security Whitepaper version 1.0 audiobook release](https://www.cncf.io/blog/2022/08/12/cloud-native-security-whitepaper-version-1-0-audiobook-release/)

CNCF 的 Security Technical Advisory Group 最近推出了 Cloud Native Security Whitepaper 的第二版 ([GitHub 下載連結](https://github.com/cncf/tag-security/tree/main/security-whitepaper))，除此之外還特別準備了 Cloud Native Security Whitepaper 的第一版的 audiobook ([前往聆聽](https://soundcloud.com/user-769472014/sets/cncf-tag-security-cloud-native-security-whitepaper-version-v1)) 讓使用者聽到第一版的講解

<!-- summary -->
### [Dependabot now alerts for vulnerable GitHub Actions](https://github.blog/2022-08-09-dependabot-now-alerts-for-vulnerable-github-actions/)

一個安全的 CI/CD 流程對於開發團隊來說是相當重要的一環，GitHub Action 除了讓開發者存放於 GitHub 的程式碼具有原生 CI/CD 的能力之外，最近官方也宣布現在會針對易受攻擊的 GitHub Actions 發出 Dependabot 的告警，用來協助開發者修復 CI/CD 流程中的安全問題

### [Amazon Detective Supports Kubernetes Workloads on Amazon EKS for Security Investigations](https://aws.amazon.com/blogs/aws/amazon-detective-supports-kubernetes-workloads-on-amazon-eks-for-security-investigations/)

AWS Detective 是 AWS 於 2020 所推出的服務，它可以用來偵測來自 Amazon GuardDyty, AWS Cloudtrail 和 AWS VPC 的嘗試登入事件，API 存取，和網路流量...等，現在他將可以支援 Kubernetes 工作流程，並且支援 AWS EKS 的安全偵測，現在只要開啟這個功能，他就會開始檢查 EKS 的 Audit Log，允許使用者可以快速偵測到運行於 EKS 中的服務是否有潛藏的惡意行為

