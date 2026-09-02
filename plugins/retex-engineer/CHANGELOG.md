# retex-engineer 更版歷程

本文件記錄 `retex-engineer` plugin 的版本異動，供後續維護參考。版號對應 `.claude-plugin/plugin.json` 的 `version` 欄位。

## 1.1.5

- `senior-engineer` skill 新增前綴條件：若使用者訊息以`開發`、`除錯`、`[開發]`、`[除錯]`、「開發」或「除錯」開頭，一律強制觸發此 skill
- 起因：加強觸發方式並減少因提示詞撰寫問題導致沒觸發
- 
## 1.1.4

- `senior-engineer` skill 新增鐵則：開發必須完全依照設計規格執行；規格標示「待確認」或本身含糊不清的部分，只能寫 `TODO` 註解說明待確認事項，不能自行猜測數值或邏輯冒充已實作。
- 完工報告新增「規格待確認 / 未實作項目」章節，強制列出因規格不明確而未實作的部分。
- 起因：`SpecCompletionTool` 評分報告發現實作端擅自把規格要求的「平台代碼」替換成「平台名稱」，並在一個標註 TODO（待客戶確認批號定義）的欄位上自行補了一個沒有依據的固定值，導致 L3 視覺符合度未達門檻。

## 1.1.3

- 更新 `doc-to-markdown` skill 的轉換作法。
- （此版本歷經 revert/reapply 修正，最終內容以此版為準。）

## 1.1.2

- 版號調整，無功能異動。

## 1.1.1

- `senior-engineer` skill：使用者訊息以「開發」或「除錯」開頭時強制觸發 skill。

## 1.1.0

- 新增 `doc-to-markdown` skill。
- 調整 plugin 內部資料夾結構。

## 1.0.0

- 初始版本，提供 `senior-engineer` skill（規劃 → 開發 → 驗證 → 資安檢測四段式開發/除錯流程）。
