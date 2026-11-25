# log.md｜變更日誌

> 依日期記錄，每筆 1–3 行，新紀錄往下追加。格式：`- [類型] 內容`（類型：新增／修改／刪除／搬移）

## 2026-11-25
- [新增] 建立 `claude.md`（專案目標、TA、資料夾與 wiki 結構、命名規則、工作規則）與 `log.md`。
- 本次未改動 wiki 與其他既有檔案；尚未補 wiki、尚未開始寫網頁。
- [新增] 依 Perplexity 知識庫 v1.0 補 wiki：新增 1 來源頁、21 概念頁、3 台灣制度頁；原檔複製一份到 `LLM_Wiki/raw/articles/`（第一層原檔不動）。
- [修改] 更新 15 個既有 wiki 頁（MPT、相關性、再平衡、風險承受度、順序風險、債券、現金、稅務等）及 index、overview、wiki/log.md；30 則案例已驗算。
- [待查] 原檔標頭稱 27 篇、實際 30 篇（本檔 claude.md 也寫 27）；稅率級距、勞保請領年齡表等缺口已在 wiki 標「待查」，未自行補數據。
- [修改] `claude.md` 知識庫篇數 27 改為 30（依使用者指示）。
- [修改] 緊急預備金改採劉玉皙老師說法（至少 6 個月，引中央社書摘）：新增 wiki 來源頁 1 頁，修改 emergency-fund、cash、index、wiki/log.md；一般情境說法待使用者提供資料。
- [新增] 建立 `web/index.html`：單頁資產配置 MVP（四步驟：目標與收支、資產負債與緊急預備金、風險問卷、股債金 REITs 現金建議配置），Chart.js 動態圖表，數值改變即時更新。
- [待確認] 緊急預備金預設 6 個月、必要生活費只算伙食＋固定成本＋醫藥雜支（劉玉皙老師說法，查證中），程式與畫面皆標「待確認」，月數可調；範例組合與衝擊幅度為教學假設。
- [新增] 建立 .gitignore（排除 .obsidian、Claude_work），初始化 git 並推送到 GitHub repo https://github.com/xuwei5820-human/asset-allocation-lab（目前為私人，待使用者改公開）。
- [修改] 截圖資料夾不上傳 GitHub：加入 .gitignore、從 repo 最新版移除（本機檔案保留；舊 commit 歷史仍含截圖，待處理）；claude.md 補記此規則與 web/ 規則。
- [修改] repo 改為公開（使用者於 GitHub 設定）：https://github.com/xuwei5820-human/asset-allocation-lab
