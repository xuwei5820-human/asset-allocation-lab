# Asset Allocation Lab
## 個人財務規劃與資產配置互動模擬平台

**Product Proposal｜Version 0.1**  
**產品方向：** 財務規劃需求者 × 資產配置模擬器 × 視覺化互動網站  
**主要開發工具：** Claude Code

---

# 一、產品概念與定位

## 1.1 產品核心概念

Asset Allocation Lab 是一個以個人財務規劃為核心的互動式資產配置模擬平台。

使用者透過輸入個人財務資訊，包括收入、支出、資產、負債及未來人生目標，建立自己的財務輪廓。平台再透過動態視覺化、資產配置模擬及情境分析，讓使用者理解不同財務決策可能產生的影響。

產品不以直接推薦金融商品為主要目的，而是提供一個可以反覆調整變數、比較策略及理解財務取捨的決策環境。

**核心理念：**

> Don't just manage your money. Understand how your money shapes your future.

## 1.2 產品定位

| 項目 | 定位 |
|---|---|
| 產品類型 | Personal Finance & Asset Allocation Simulator |
| 主要使用者 | 有財務規劃需求的一般個人 |
| 核心需求 | 現金流管理、資產配置、人生目標規劃 |
| 主要特色 | 動態互動、情境模擬、視覺化 |
| 產品形式 | Responsive Interactive Website |
| AI 定位 | 金融知識解說、分析輔助、知識檢索 |
| 核心技術 | Deterministic Calculation + Graph Workflow |
| 開發工具 | Claude Code |

## 1.3 目標使用者

### Persona A：初入職場者
- 開始有穩定收入。
- 不清楚如何分配每月收入。
- 希望建立緊急預備金。
- 對股票、債券、ETF 有基本認識，但缺乏整體規劃。

### Persona B：具有一定投資經驗者
- 已持有股票、ETF、基金等金融資產。
- 缺乏完整的資產配置觀念。
- 想了解不同資產的風險與相關性。
- 希望檢視目前投資組合是否過度集中。

### Persona C：具有中長期財務目標者
- 有購屋、留學、退休等資金需求。
- 希望知道目前財務狀況能否支撐未來目標。
- 想比較不同儲蓄、投資及支出策略。
- 需要評估不同目標之間的資金分配。

---

# 二、核心產品功能

整個網站規劃為六大模組。

## Module 01｜Financial Profile：個人財務輪廓

建立使用者目前的財務狀況。

### 輸入資訊

**收入**
- 每月薪資收入。
- 額外收入。
- 年終獎金。
- 其他收入。

**支出**
- 固定生活支出。
- 變動生活支出。
- 房租或房貸。
- 保險支出。
- 其他負擔。

**資產**
- 現金與銀行存款。
- 股票。
- ETF。
- 債券。
- 黃金。
- REITs。
- 不動產。
- 其他資產。

**負債**
- 房屋貸款。
- 學貸。
- 信用貸款。
- 信用卡未繳款。
- 其他負債。

### 視覺化設計
1. Net Worth：個人淨資產。
2. Asset Breakdown：資產結構。
3. Liability Breakdown：負債結構。
4. Monthly Cash Flow：每月現金流。
5. Savings Rate：儲蓄率。

使用者完成輸入後，產生一張個人財務概況儀表板。

### 核心計算

- 個人淨資產＝總資產－總負債。
- 每月現金流結餘＝每月收入－每月支出－每月債務還款。
- 儲蓄率＝每月可儲蓄金額／每月收入。

需要在資料模型中明確區分「支出」與「債務本金／利息還款」，避免現金流重複扣除。

## Module 02｜Financial Goals：人生目標規劃

這是產品與一般資產配置工具最大的差異之一。使用者不是單純追求投資報酬，而是根據未來的財務需求安排資產。

### 預設目標類型

| 目標 | 時間範圍 | 主要考量 |
|---|---|---|
| 緊急預備金 | 隨時可動用 | 流動性 |
| 購車基金 | 1–5 年 | 資金穩定性 |
| 留學基金 | 2–5 年 | 時間、匯率 |
| 購屋基金 | 3–10 年 | 資金累積 |
| 子女教育 | 5–20 年 | 長期資金需求 |
| 退休規劃 | 20–40 年 | 長期累積與通膨 |

### 使用者輸入
- 目標名稱。
- 目前已累積的資金。
- 預計需要的金額。
- 預計達成時間。
- 是否有持續投入資金。
- 是否需要分階段提領。

### 互動功能

使用者可以在時間軸上建立不同財務目標。例如：

- 現在：23 歲。
- 27 歲：預計出國留學，需要 100 萬元。
- 30 歲：預計購屋，需要 300 萬元自備款。
- 60 歲：開始退休，需要累積足夠的退休資產。

網站依照使用者設定的條件，動態呈現不同時間點的資金需求。

### 核心視覺化
- Financial Timeline：財務目標時間軸。
- Goal Progress：目標達成進度。
- Funding Gap：目前資金與目標金額的差距。
- Required Monthly Savings：每月需要累積的金額。

## Module 03｜Asset Allocation Builder：資產配置建構器

這是產品最核心的互動介面。使用者可以自由調整不同資產類別的比例，觀察整體配置的變化。

### 預設資產類別

| 資產類別 | 子類別示例 |
|---|---|
| 股票 Equity | 台灣股票、美國股票、全球股票、新興市場 |
| 債券 Bonds | 政府債券、投資級公司債、高收益債 |
| 黃金 Gold | 實體黃金、黃金 ETF |
| 不動產 Real Estate | REITs、不動產 |
| 現金 Cash | 活期存款、定期存款、貨幣市場工具 |

### 操作方式
1. 透過 Slider 調整各資產比例。
2. 直接輸入配置百分比。
3. 增加或刪除資產類別。
4. 儲存不同配置版本。
5. 比較不同配置的差異。

### 動態視覺化

當使用者調整股票比例時，所有相關圖表即時變化。網站同步更新：
- 各類資產投入金額。
- 預估組合報酬假設。
- 組合波動風險。
- 資產集中度。
- 不同情境下的模擬結果。

**資料原則：** 未來報酬及風險數值必須有明確資料來源，或使用者自行設定假設，不應由 AI 隨意生成。

## Module 04｜Simulation Engine：財務情境模擬器

這個模組是整個產品最具特色的地方。使用者不只是看目前的資產配置，而是可以操作不同變數，觀察未來財務狀況如何改變。

### A. Future Wealth Simulator

模擬未來資產累積。

使用者可以調整：
- 初始投資本金。
- 每月投入金額。
- 預期年化報酬假設。
- 投資期間。
- 通膨率。
- 投資成本。

呈現結果：
- 未來資產累積曲線。
- 名目資產與實質購買力。
- 不同報酬假設下的資產差異。

### B. Market Shock Simulator

模擬市場發生劇烈變化時，投資組合的可能影響。

使用者可以選擇或自訂：
- 股票市場下跌 20%。
- 債券價格下跌 10%。
- 黃金價格上漲 15%。
- 通膨率升至 5%。
- 多種市場變化同時發生。

網站依照使用者的資產權重計算衝擊後的組合價值。

**計算示例：**

原始資產 100 萬元，股票占比 60%、債券占比 30%、現金占比 10%。假設股票下跌 30%、債券下跌 5%、現金不變：

- 股票：60 萬 × -30% = -18 萬。
- 債券：30 萬 × -5% = -1.5 萬。
- 現金：10 萬 × 0% = 0。
- 組合總損失：19.5 萬元。

這是情境假設，不代表市場預測。

### C. Life Event Simulator

模擬人生事件對財務狀況的影響，例如：
- 失業六個月。
- 薪資增加 20%。
- 購屋並開始負擔房貸。
- 生育與教育支出。
- 提前退休。
- 突發大型醫療支出。

使用者可以觀察不同事件發生後：
1. 現金流是否足夠。
2. 緊急預備金是否足夠。
3. 是否需要動用投資資產。
4. 原有財務目標是否受到影響。

### D. Inflation Simulator

模擬通膨對未來購買力的影響。例如，現在 100 萬元的購買力，在不同通膨率及期間下會有什麼變化。這能讓使用者理解名目資產增加不等於實質財富增加。

## Module 05｜Portfolio Comparison：配置策略比較

使用者可以儲存多組配置，放在一起比較。

### 比較示例

| 指標 | Strategy A | Strategy B | Strategy C |
|---|---:|---:|---:|
| 股票 | 80% | 60% | 40% |
| 債券 | 10% | 25% | 40% |
| 黃金 | 5% | 10% | 10% |
| 現金 | 5% | 5% | 10% |

### 比較項目
- 預期報酬假設。
- 波動率假設。
- 最大回撤（有歷史資料時）。
- 通膨敏感度。
- 流動性。
- 與人生目標的資金需求匹配程度。

使用者可以切換不同策略，觀察哪一種策略更符合自己設定的財務目標與風險條件。

## Module 06｜Knowledge Assistant：AI 財務知識助理

以現有資產配置 Wiki 作為知識基礎。

使用者可以在操作過程中詢問：
- 為什麼債券價格會受到利率影響？
- 黃金在投資組合中通常扮演什麼角色？
- 如果我將股票比例從 60% 降到 40%，可能產生哪些取捨？

AI 負責：
- 解釋金融概念。
- 說明計算邏輯。
- 解讀模擬結果。
- 引用 Wiki 內容。
- 提供相關知識延伸閱讀。

**核心原則：LLM 負責解釋，程式負責計算。** AI 不應自行捏造歷史報酬、金融數據或預期報酬率。

---

# 三、使用者操作流程（User Journey）

```text
進入網站
   │
   ▼
建立個人財務檔案
   │
   ▼
輸入收入、支出、資產、負債
   │
   ▼
建立人生財務目標
   │
   ▼
系統產生財務概況
   │
   ▼
進入資產配置建構器
   │
   ▼
調整不同資產比例
   │
   ▼
進入情境模擬器
   │
   ├── 未來資產累積
   ├── 市場衝擊
   ├── 人生事件
   └── 通膨影響
   │
   ▼
比較不同配置策略
   │
   ▼
檢視財務目標與資金缺口
   │
   ▼
儲存配置方案
```

---

# 四、UI / UX 設計方向

產品以互動視覺化為主要特色，不應做成傳統金融機構的數據儀表板。希望呈現的感受是：

**Professional、Minimal、Interactive、Data-driven。**

## 4.1 網站主要導覽

| 頁面 | 功能 |
|---|---|
| Dashboard | 個人財務總覽 |
| My Finance | 收入、支出、資產、負債 |
| Goals | 人生財務目標 |
| Allocation Lab | 資產配置建構 |
| Simulation | 情境模擬 |
| Compare | 配置策略比較 |
| Knowledge | 金融知識探索 |

## 4.2 優先開發的互動元件

1. Interactive Donut Chart：資產比例。
2. Cash Flow Sankey：資金流向。
3. Financial Timeline：人生財務目標時間軸。
4. Dynamic Slider：即時調整資產配置。
5. Wealth Projection Chart：未來資產累積。
6. Scenario Comparison：不同情境比較。
7. Asset Composition Treemap：資產結構。
8. Risk-return Visualization：風險與報酬假設。

## 4.3 UI 原則

- 重要資訊應該透過視覺呈現，而非大量文字。
- 調整參數後，圖表應即時更新。
- 使用者應該清楚知道每項數據的來源。
- 不同模擬情境必須有明確標記。
- 避免過多金融專有名詞。
- 提供深入解釋，但不干擾主要操作流程。

---

# 五、技術架構與工程方法

## 5.1 技術建議

| 層級 | 技術 | 目的 |
|---|---|---|
| Frontend | Next.js | 網站框架 |
| Language | TypeScript | 核心程式邏輯 |
| UI | Tailwind CSS | 介面設計 |
| Components | shadcn/ui | UI 元件 |
| Charts | Apache ECharts | 資料視覺化 |
| State Management | Zustand | 管理互動狀態 |
| Database | PostgreSQL | 儲存使用者資料 |
| AI | Claude API | 知識檢索與解說 |
| Workflow | Graph Workflow | 多階段分析流程 |

初期不必急著建立複雜的 Backend 或多 Agent 系統。可以先完成本地端計算與互動介面，待功能穩定後再加入使用者帳號、雲端資料庫及 AI。

## 5.2 Graph Engineering

本專案建議採用 Graph Workflow 作為分析流程管理方式。

```text
User Input
    │
    ▼
Data Validation
    │
    ▼
Financial Profile Analysis
    │
    ├───────────────┐
    ▼               ▼
Cash Flow       Balance Sheet
Analysis        Analysis
    │               │
    └───────┬───────┘
            ▼
      Goal Analysis
            │
            ▼
    Asset Allocation
            │
            ▼
    Scenario Simulation
            │
            ▼
    Results Aggregation
            │
            ▼
     Knowledge Retrieval
            │
            ▼
    User-facing Explanation
```

Graph 負責管理資料流與分析順序。真正的財務計算仍由獨立、可測試的程式模組完成。

---

# 六、現有 Wiki 的擴充計畫

這是正式開發前最重要的工作。目前已知 Wiki 主要涵蓋股票、債券、黃金、REITs 等資產類別知識。這些內容可以支撐 Asset Allocation Builder，但還不足以支撐完整的個人財務規劃。

## 6.1 Priority 0：個人財務規劃基礎

| 知識主題                   | 必須涵蓋的內容      | 用途       |
| ---------------------- | ------------ | -------- |
| Personal Finance       | 個人財務規劃基本架構   | 建立產品核心邏輯 |
| Cash Flow Management   | 收入、支出、現金流    | 財務概況     |
| Personal Balance Sheet | 資產、負債、淨資產    | 建立財務輪廓   |
| Emergency Fund         | 緊急預備金        | 流動性規劃    |
| Savings Rate           | 儲蓄率、儲蓄能力     | 資金累積     |
| Debt Management        | 負債、利息、還款方式   | 負債管理     |
| Financial Goals        | 財務目標、資金需求、時間 | 目標規劃     |
| Time Value of Money    | 貨幣時間價值       | 未來資產計算   |
| Inflation              | 通膨、實質購買力     | 長期財務規劃   |
| Risk Capacity          | 財務上可承受的風險    | 配置情境分析   |

## 6.2 Priority 0：資產配置理論

現有資產類別知識需要搭配資產配置理論。

| 知識主題 | 重要概念 |
|---|---|
| Modern Portfolio Theory | Markowitz、投資組合最佳化 |
| Asset Allocation | 資產配置原則 |
| Diversification | 分散投資 |
| Correlation | 資產相關性 |
| Risk-Return Trade-off | 風險與報酬取捨 |
| Portfolio Volatility | 投資組合波動率 |
| Rebalancing | 資產再平衡 |
| Efficient Frontier | 效率前緣 |
| Risk Tolerance | 主觀風險承受程度 |
| Strategic Asset Allocation | 長期策略性配置 |

## 6.3 Priority 1：人生目標與現金流規劃

| 知識主題 | 必須涵蓋的內容 |
|---|---|
| Goal-based Planning | 以目標為導向的財務規劃 |
| Retirement Planning | 退休資產累積與提領 |
| Education Planning | 教育資金規劃 |
| Housing Planning | 購屋、自備款、房貸 |
| Income Replacement | 收入中斷與替代收入 |
| Emergency Planning | 緊急支出情境 |
| Withdrawal Strategy | 資產提領策略 |
| Sequence of Returns Risk | 報酬順序風險 |

## 6.4 Priority 1：風險與情境分析

建議補充：
- Market Risk：市場風險。
- Interest Rate Risk：利率風險。
- Inflation Risk：通膨風險。
- Currency Risk：匯率風險。
- Liquidity Risk：流動性風險。
- Credit Risk：信用風險。
- Concentration Risk：集中度風險。
- Drawdown：資產回撤。
- Stress Testing：壓力測試。
- Monte Carlo Simulation：蒙地卡羅模擬。

## 6.5 Priority 2：進階投資與財務模型

等第一版產品完成後再補充：
- Capital Market Assumptions。
- Historical Asset Returns。
- Covariance Matrix。
- Risk Parity。
- Black-Litterman Model。
- Monte Carlo Simulation。
- Tax-efficient Investing。
- Asset Location。
- Retirement Withdrawal Models。

這些知識不應該成為 MVP 的開發前置條件。

---

# 七、Wiki 建議採用的知識結構

除了補足主題，更重要的是讓 Wiki 能被 AI 和程式有效使用。

建議每篇知識至少包含以下欄位：

| 欄位 | 說明 |
|---|---|
| Topic | 知識主題 |
| Category | 所屬分類 |
| Definition | 概念定義 |
| Core Principles | 核心原理 |
| Formula | 相關公式 |
| Variables | 公式變數 |
| Example | 實際案例 |
| Application | 實務應用 |
| Limitations | 適用限制 |
| Related Topics | 關聯知識 |
| Sources | 原始資料來源 |
| Last Updated | 最後更新日期 |

例如：

**Topic：** Portfolio Volatility  
**Category：** Portfolio Theory  
**Definition：** 投資組合報酬率的波動程度。  
**Formula：** 投資組合變異數的計算。  
**Variables：** 資產權重、各資產變異數、資產間共變異數。  
**Application：** 用來比較不同配置的歷史波動程度。  
**Limitations：** 歷史波動率不代表未來波動率。  
**Related Topics：** Asset Allocation、Correlation、Diversification、Modern Portfolio Theory。  
**Sources：** 原始學術研究、金融教材或可靠資料來源。

**重要：Wiki 不應該只有知識文章，也要保存可供程式使用的結構化資料與公式定義。**

---

# 八、資料來源與數據需求

這個產品有一個重要區別：金融知識可以從 Wiki 檢索，但實際計算需要數據。因此需要建立兩種資料系統。

## 8.1 Knowledge Data

用於 AI 檢索及知識解釋：
- 資產類別介紹。
- 金融理論。
- 投資策略。
- 學術研究。
- 公式與計算方法。

## 8.2 Financial Data

用於模擬與計算：
- 歷史資產報酬。
- 歷史價格。
- 通膨率。
- 匯率。
- 利率。
- 債券殖利率。
- ETF 歷史價格。

初期可以先採用使用者自行輸入的報酬率、風險及通膨假設。之後再導入經過驗證的歷史資料。這樣可以避免一開始就被資料取得與 API 維護拖慢。

---

# 九、MVP 開發規劃

不建議一開始就完成六大模組。第一版應聚焦在最能呈現產品價值的部分。

## Phase 1：財務輪廓與目標規劃

完成：
- 個人資料輸入。
- 收入與支出。
- 資產與負債。
- 淨資產計算。
- 每月現金流。
- 人生財務目標。

**驗收標準：** 使用者可以建立自己的財務輪廓，並看到目前財務狀況。

## Phase 2：資產配置建構器

完成：
- 資產類別選擇。
- 比例調整。
- 投入金額計算。
- 即時視覺化。
- 多組配置儲存。

**驗收標準：** 使用者能夠自由建立及比較不同資產配置。

## Phase 3：情境模擬器

完成：
- 未來資產累積。
- 通膨影響。
- 市場衝擊。
- 人生事件。
- 不同配置比較。

**驗收標準：** 使用者能透過改變參數，理解財務結果的變化。

## Phase 4：AI Knowledge Assistant

完成：
- Wiki 檢索。
- 金融概念解釋。
- 公式說明。
- 模擬結果解讀。
- 來源引用。

**驗收標準：** AI 的回答能回溯至 Wiki 或其他指定來源，且不自行生成未經驗證的財務數字。

## Phase 5：進階功能

- 歷史資料回測。
- 蒙地卡羅模擬。
- 進階風險分析。
- 再平衡模擬。
- 雲端資料保存。

---

# 十、品質控制與限制

本產品的核心計算必須可驗證，因此需要建立獨立的金融計算測試。

1. 所有資產權重加總必須等於 100%。
2. 資產與負債計算結果必須符合定義。
3. 現金流計算必須正確。
4. 不同報酬假設必須產生符合公式的結果。
5. 通膨調整必須區分名目價值與實質價值。
6. 市場衝擊必須正確反映至組合價值。
7. 使用者修改數值後，相關圖表必須同步更新。

模擬結果必須明確區分：
- 歷史資料。
- 使用者輸入的假設。
- 模型計算結果。
- 示意性情境。

第一版以財務教育及自主管理工具為定位，不進行自動化個人投資建議或金融商品交易。未來若朝商業化投資顧問服務發展，需另行檢視適用法規。

---

# 十一、專案最終目標

Asset Allocation Lab 希望建立的不只是另一個投資組合計算器，而是一個可以讓使用者回答以下問題的互動平台：

1. 我現在的財務狀況如何？
2. 我每個月實際能夠累積多少資金？
3. 我的資產與負債結構是否合理？
4. 我距離人生財務目標還有多遠？
5. 不同資產配置會帶來哪些風險與取捨？
6. 如果未來發生重大變化，我的財務規劃是否還能維持？
7. 我可以透過哪些變數調整自己的財務策略？

**產品最終價值：讓抽象的財務規劃變成可以看見、操作、模擬及比較的互動體驗。**

---

# 十二、開發前的補充判斷與下一步

## 12.1 Wiki 的主要知識缺口

目前的資產類別知識（股票、債券、黃金、REITs 等）可以支撐資產配置建構器，但產品還需要個人財務規劃知識，才能處理使用者的真實需求。

建議將 Wiki 分為三層：

| 層級 | 內容 | 重要性 |
|---|---|---|
| 第一層：資產知識 | 股票、債券、黃金、REITs | 已有基礎 |
| 第二層：財務規劃 | 現金流、負債、財務目標、退休規劃 | 非常高 |
| 第三層：量化模型 | MPT、相關性、Monte Carlo、壓力測試 | 高 |

第二層尤其重要。例如，使用者想在五年後購屋，系統必須知道如何處理：
- 現在有多少可動用資產？
- 每月可以累積多少資金？
- 未來五年預計需要多少購屋資金？
- 是否有其他財務目標會競爭資金？
- 如果收入中斷，目標是否仍可達成？

這些問題不單靠資產類別知識就能回答。

## 12.2 建議優先補充的 15 個 Wiki 主題

| 優先級 | 主題 | 英文關鍵詞 |
|---|---|---|
| P0 | 個人財務規劃 | Personal Financial Planning |
| P0 | 現金流管理 | Cash Flow Management |
| P0 | 個人資產負債表 | Personal Balance Sheet |
| P0 | 緊急預備金 | Emergency Fund |
| P0 | 儲蓄率 | Savings Rate |
| P0 | 財務目標規劃 | Goal-Based Financial Planning |
| P0 | 貨幣時間價值 | Time Value of Money |
| P0 | 通膨與實質報酬 | Inflation and Real Return |
| P0 | 資產配置理論 | Asset Allocation Theory |
| P0 | 資產相關性 | Asset Correlation |
| P1 | 風險承受能力 | Risk Capacity |
| P1 | 投資組合再平衡 | Portfolio Rebalancing |
| P1 | 退休規劃 | Retirement Planning |
| P1 | 蒙地卡羅模擬 | Monte Carlo Simulation |
| P1 | 報酬順序風險 | Sequence of Returns Risk |

這 15 個主題可以先建成 Wiki 的新分類，不需要一次把每個主題都研究到非常深入。

## 12.3 值得放在產品核心的功能：Life Event Simulator

這個功能可能比一般的歷史回測更有產品差異化。

想像使用者在網站上看到自己的財務時間軸：

```text
2026 ───── 2028 ───── 2030 ───── 2040 ───── 2060
  │          │          │          │          │
開始工作   出國留學   購屋       子女教育   退休
```

他可以直接點擊 2028 年的留學事件。假設需要 100 萬元，系統就從現在的財務狀況出發，模擬未來兩年的現金流、儲蓄與資產累積。

接著他可以調整：
- 延後留學一年。
- 每月增加儲蓄 5,000 元。
- 減少非必要支出。
- 改變投資組合假設。

網站即時呈現不同決策對後續財務目標的影響。這讓資產配置不再只是百分比遊戲，而是與真實生活連結。

## 12.4 開發前建議完成的三件事

**第一：盤點現有 Wiki。** 確認目前有哪些資產類別、理論、公式及實證資料。

**第二：補足個人財務規劃知識。** 優先處理現金流、資產負債、財務目標、貨幣時間價值及通膨。

**第三：建立計算模型規格。** 先明確定義公式、輸入欄位、輸出結果、邊界條件與測試案例。

| 功能 | 需要的知識或公式 |
|---|---|
| 淨資產 | Assets - Liabilities |
| 儲蓄率 | Savings / Income |
| 未來資產 | Future Value |
| 實質報酬 | Real Return |
| 投資組合報酬 | Weighted Portfolio Return |
| 投資組合風險 | Portfolio Variance |
| 市場衝擊 | Scenario-based Return |
| 退休資金 | Accumulation & Withdrawal Models |

這樣 Claude Code 才有足夠明確的規格，避免讓 Claude 自己推測金融邏輯。

---

# 附錄：目前產品開發的建議優先順序

1. **先盤點 Wiki：** 建立現有內容清單與知識缺口表。
2. **先做財務模型規格：** 明確定義收入、支出、資產、負債、目標與配置資料結構。
3. **先完成 MVP 主流程：** 財務輪廓 → 人生目標 → 資產配置 → 情境模擬。
4. **以視覺互動建立差異化：** 優先做好時間軸、現金流、動態配置與模擬圖表。
5. **最後再整合 AI：** 讓 AI 讀取 Wiki、解釋計算結果並提供可追溯引用。

