---
title: 第 149 期 DevOps 推薦文章
date: 2022-09-13
author: rico

layout: layouts/post.njk
tags: [DevOps]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

## DevOps

<!-- summary -->
### [The 2-minute test for Kubernetes Pod security](https://www.cncf.io/blog/2022/09/06/the-2-minute-test-for-kubernetes-pod-security/)

本文示範了如何 2 分鐘使用 Kubernetes Pod Security Standards 來檢查 pod 的資安，而且完全不用在 Kubernetes cluster 內安裝多餘的東西，只需要靠 kuberctl 安裝 Kyverno 後掃描 cluster 或 namespace 就可以知道結果了。<!-- summary -->

### [Avoiding the Top 10 NGINX Configuration Mistakes](https://www.nginx.com/blog/avoiding-top-10-nginx-configuration-mistakes/)

本文介紹了如何避免 Nginx 10 個常見的設定錯誤：
1. 每個 worker 的 file descriptors 預設值太低，可以調高，跟連線數有關
2. 預設 error_log 是不會儲存的，建議可以開啟
3. 正常設定下每個新請求都要三向交握且會佔用 ports，所以建議開啟 keepalive
4. 使用者常常忘記個別 path 下的設定會 override 全域的設定
5. 建議 proxy_buffering 使用預設的打開選項，只有很少數的情境才需要關閉
6. 避免設定 if 時使用不當
7. 避免過度地使用 health checks
8. 避免以不安全的方式存取 metrics，建議使用簡單的帳號密碼和許可或阻擋名單做一定程度的阻擋
9. 建議在同個 /24 網段下不要使用 ip_hash 演算法，因為它只看前三個八位元組，會無法分散流量，建議使用 hash 演算法。
10. 應該活用 upstream{} 的好處做全域的設定

### [How a Cloud Skills Shortage Is Affecting Multi-Cloud Adoption](https://www.hashicorp.com/blog/how-a-cloud-skills-shortage-is-affecting-multi-cloud-adoption)

Hachicorp 統計了組織在採用多雲策略時會遇到的阻礙，而平台團隊（platform team）負責什麼任務，同不同意多雲環境自動化的重要性，哪些自動化功能可以幫助多雲策略。