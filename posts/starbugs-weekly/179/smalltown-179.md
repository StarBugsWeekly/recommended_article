---
title: 第 179 期 GenAI 推薦文章
date: 2023-07-25
author: smalltown

layout: layouts/post.njk
tags: [GenAI]
# image: /img/TheSpiritAndImplementationOfAOP/0____Bm36Dv5mm97e2vF.jpg
---

<!-- summary -->

## GenAI

### [假如生成式 AI 產生的程式碼都可以直接使用的話...](https://blog.blackhc.net/2022/12/llm_software_engineering/)

雖然自己有透 GitHub Copilot 和 ChatGPT 來增加生產力，但其實他產生出來的程式碼還是需要人工來檢查、修改，才能真正使用。最近看到一個叫做 LLM Strategy 工具提出來的想法滿不錯的，當工程師在撰寫 Python 時，只需要在程式碼上面加上 Decorator，例如: @llm_strategy(OpenAI(max_tokens=256))，那麼在接下來的 Class Method 中就只需要寫上需求註解，不需要撰寫程式碼，GenAI 就會幫你把需要的程式碼補完 (看附圖應該可以更好理解)
或許在不久的將來，當 GenAI 產生的程式碼都可以直接使用時，工程師就可以專注在需求上，而不需要花時間在撰寫程式碼上，寫程式的門檻也會更低！

<!-- summary -->

### [有沒有 On Premise 的 ChatGPT 啊？！](https://github.com/imartinez/privateGPT)

在雲端世界的解決方案中，企業常常因為資料安全性的考量，而不願意將資料上傳到雲端，這時候就會需要採購 On Premise 的版本，那在生成式 AI 的領域裡有沒有類似 ChatGPT 的 On Premise 的版本呢？
答案當然是肯定的，目前有看到幾個比較多人使用的專案，分別是 ColossalChat, privateGPT,  localGPT，其中 privateGPT 使用的 LLM 為 GPT4All，localGPT 則是使用 Vicuna-7B，推薦給有類似需求的人

- [ColossalChat](https://github.com/hpcaitech/ColossalAI/tree/main/applications/Chat) 
- [privateGPT](https://github.com/imartinez/privateGPT) 
- [localGPT](https://github.com/PromtEngineer/localGPT)

### [開發 AI 應用服務要怎麼抓蟲?](https://blog.langchain.dev/announcing-langsmith/)

一般來說，開發 Web 或是 Mobile App 時，都會使用諸如 Sentry 或是 Rollbar 的服務來協助追蹤程式遇到的問題，那在開發 AI App 時，要怎麼抓蟲和監控問題的發生呢?

在生成式 AI 開發框架中，相信不少人都是使用 #LangChain，而其實它也有推出類似的服務產品，也就是今天要提到的 #LangSmith，底下將介紹他所提供的重要功能

- Debugging: 視覺化使用者與 AI App 互動過程中每一個步驟輸入以及輸出 AI Model 的資訊，同時還會給出不預期的結果，錯誤，延遲時間，Token 的使用量，讓開發者有線索可以去找出可能是哪個地方出了問題；並且讓開發者可以直接從 LangSmith 的 UI 去做範例的測試，不用再複製貼上去 OpenAI Playground
- Testing: 軟體測試最直接的方式，不外乎就是修改程式碼，然後把資料丟進去後觀察輸出有沒有符合預期，而 AI App 測試時，會需要比較多的輸入資料，LangSmith 讓開發者可以快速從正在追蹤的問題，或是透過手動上傳的方式來建立資料集，開發者就可以立刻輕鬆的使用他們來測試撰寫的 Chain 和 Prompt 是否符合預期
- Monitoring: 程式當然不會再開發完成就結束了，當服務在線上持續運行時，時時刻刻監控其狀態是相當重要的，透過 LangSmith 可以去監控 AI App 的運行效能，例如延遲和成本，同時也要追蹤 Model 和 Chain 的運行效能，並且可以建立儀表板來了解目前使用者的使用狀況與體驗