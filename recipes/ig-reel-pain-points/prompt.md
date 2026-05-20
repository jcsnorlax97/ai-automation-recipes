# Prompt

```text
每天為 <account-handle> 蒐集可測試的 Instagram Reels 題材。目標受眾是 creators、freelancers、solopreneurs、small business owners，主題聚焦 ChatGPT、AI tools、prompt workflows、content creation、automation、metrics tracking。

這是一個 heartbeat automation：每天把 digest 回報到目前 Codex thread。不要嘗試直接寫入本機檔案或 Obsidian vault。使用者回來後，會再用 automation-vault-sync/capture/sync 流程把有價值的 digest 寫入 ai-work-log vault。

請使用公開網路來源搜尋最近的痛點、問題、抱怨、需求與熱門討論，優先參考 Reddit、Instagram/Threads/X 公開討論、YouTube 影片留言/標題、Product Hunt/AI 工具榜、AI 工具更新公告、創作者社群與小型企業社群。不要使用需要登入或無法公開存取的內容。

輸出請用繁體中文，格式如下：

1. 今日 5 個高潛力痛點
每個包含：pain point、來源類型、受眾、為什麼適合短影片。

2. 今日 10 個 Reel 測試題
每個包含：hook、prompt idea、要錄的 5 段畫面（AI 工具畫面 / prompt 範例 / Idea -> Prompt -> Draft -> Edit -> Publish workflow / metrics tracker / CTA: Follow <account-handle>）、預期觀眾收穫、建議追蹤 metric。

3. 今日優先拍的 3 支
用 1-10 分評估 visual clarity、usefulness、novelty，並說明排序理由。

4. 一個可直接貼進 ChatGPT 的 prompt 範例
讓使用者能立刻產生其中一支 Reel 的腳本或 workflow。

5. Sources
列出使用過的公開來源連結與一句話來源摘要。

6. Vault Sync Block
提供一段 markdown-ready 摘要，方便之後寫入 ai-work-log vault 的 `inbox/YYYY/MM/DD/automations/<automation-id>/`。格式請參考 `vault-sync-block-template.md`。注意：Vault Sync Block 外層使用 ```markdown fenced block；若 block 內需要包 prompt，請用 ~~~text fence，不要在 block 內再使用 ```text。

請避免泛泛題目，優先挑能用手機螢幕錄影清楚展示、3-5 秒一段、可在 20 秒內看懂結果的題材。
```
