# claude.md｜Asset Allocation Lab 期末作業工作規範

> 每次開工先讀本檔與 `log.md`。本檔控制在一頁內，修改時請精簡。

## 1. 目標
用 vibe coding（Claude Code）做一個**個人財務規劃 × 資產配置互動模擬網頁**。使用者輸入收入、支出、資產、負債與人生目標，網頁以視覺化與情境模擬呈現不同配置與決策的影響。**不推薦個別金融商品**；所有報酬率、通膨等數字都是教學假設，不是預測。

## 2. TA（目標使用者）
**主要 TA（2026-11-25 鎖定）：25–40 歲的台灣上班族**，有一些存款但沒有系統化配置過，想同時兼顧買房、育兒和退休。網頁的預設範例、問卷與用語以這群人為準（月薪、房貸／車貸、勞保勞退、ETF 定期定額）。流程：**人生目標 → 現金流 → 資產負債**，再談配置。

次要族群（之後再擴充）：剛出社會只想先存預備金的新鮮人、已有投資想檢查集中度的人、接近退休者。

資產類別：現金、股票、債券、黃金、REITs（其他如不動產、虛擬資產為次要）。

## 3. 資料夾結構（第一層）
| 路徑 | 內容 |
|---|---|
| `claude.md`、`log.md` | 本規範與變更日誌 |
| `Asset_Allocation_Lab_產品計畫書_v0.1.md` | 產品計畫書：六大模組、MVP 分期 |
| `Asset Allocation Lab Wiki 知識庫 v1.0.md` | Perplexity 整理的資料（FIN/GOAL/TVM/PORT/RISK/MGMT/SCEN/QUANT/TW 共 30 篇），**之後用來補 wiki** |
| `Claude_work/LLM_Wiki/` | 既有 wiki 專案（有自己的 `CLAUDE.md` 與 git） |
| `MM_DD截圖過程/`（如 `11_25截圖過程/`） | 作業過程截圖，**只留本機、不上傳 GitHub**（已列入 `.gitignore`） |
| `.obsidian/` | Obsidian 設定，不要動 |

## 4. Wiki 結構（`Claude_work/LLM_Wiki/`）
- `raw/`：原始來源，**只讀不改**；新來源先放 `raw/inbox/`。
- `wiki/`：知識層，含 `index.md`、`log.md`、`overview.md` 及 `concepts/`、`strategies/`、`asset-classes/`、`entities/`、`taiwan/`、`sources/`、`syntheses/`、`my-portfolio/`。
- `templates/`：頁面模板；`research/`：研究筆記與簡報產出。
- 補 wiki 時依該資料夾的 `CLAUDE.md` 規範（frontmatter、連結、來源標註）。預計新增「個人財務規劃、人生目標、貨幣時間價值、風險評估、情境模擬」等主題頁。

## 5. 命名規則
- Wiki 頁面檔名：英文小寫 kebab-case（如 `emergency-fund.md`），H1 用繁體中文，必要時括號附英文。
- 來源摘要頁：`sources/web-YYYY-MM-DD-短題.md`；研究資料夾：`research/YYYY-MM-DD-短題/`。
- 第一層文件：`名稱_v版本.md`（如 `產品計畫書_v0.2.md`），改版不覆蓋舊版。
- 日期一律 `YYYY-MM-DD`。網頁程式碼放 `web/`（單一 `index.html`，Chart.js 由 CDN 載入）。

## 6. 工作規則
1. **每次變動都要記到 `log.md`**（新增、修改、刪除、搬移檔案皆算），依日期記錄，每筆 1–3 行，只能往下追加。
2. 動手前先確認範圍；使用者沒要求的事（補 wiki、寫網頁）不主動做。
3. 不修改 `raw/` 與 Perplexity 原始資料；要引用就摘要並標註來源。
4. 台灣制度（稅、勞退、勞保）要註明查核基準日與適用年度。
5. 全部使用繁體中文；財務術語首次出現可附英文。
6. 計算公式以知識庫 v1.0 的口徑為準（例如支出與債務還款分開計）。
7. GitHub repo：`xuwei5820-human/asset-allocation-lab`。截圖、`.obsidian/`、`Claude_work/` 不上傳；新增截圖資料夾須符合 `.gitignore` 的 `*截圖過程/` 規則。
