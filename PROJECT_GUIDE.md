# 專案使用說明書

最後更新：2026-09-30

## 目錄

1. [專案用途](#專案用途)
2. [AI 接手閱讀順序](#ai-接手閱讀順序)
3. [檔案目錄與簡述](#檔案目錄與簡述)
4. [如何檢視作品](#如何檢視作品)
5. [如何新增作品](#如何新增作品)
6. [如何修改既有作品](#如何修改既有作品)
7. [文件維護規則](#文件維護規則)
8. [Git 與推送流程](#git-與推送流程)
9. [修改日誌](#修改日誌)

## 專案用途

這個專案是前端作業、互動原型與視覺化報告的集中收藏。它目前不是單一產品網站，而是一個作品集合。

核心使用方式：

- 用 `index.html` 快速檢視所有作品。
- 保留每個 HTML 檔作為獨立作品。
- 新增作品時同步更新總覽頁與本說明文件。
- 每次進度更新都在修改日誌中留下紀錄。

## AI 接手閱讀順序

若後續由公司同事使用另一個 ChatGPT / Codex 帳號接手，請先要求該帳號閱讀：

1. `AI_HANDOFF.md`
2. `PROJECT_GUIDE.md`
3. `PROJECT_RECORD.md`

接手帳號讀完後，應先回報它理解的專案目的、目前入口、主要檔案、已知待處理事項與後續維護規則。使用者確認前，不應直接修改檔案。

建議第一句提示：

```text
請先讀取本專案根目錄的 AI_HANDOFF.md、PROJECT_GUIDE.md、PROJECT_RECORD.md。
讀完後請回覆你理解的專案目的、目前主要檔案、已知待處理事項，以及你後續會遵守的維護規則。
在我確認前，請不要修改任何檔案。
```

## 檔案目錄與簡述

目前工作區主要內容如下：

| 路徑 | 用途 | 簡述 |
| --- | --- | --- |
| `index.html` | 總覽入口 | 網站正式首頁，收錄 13 個作品，以「房地產」、「股市與投資」、「股癌專區」、「舊作品集」四個頁籤分區，包含搜尋、簡述、預覽與開啟連結。 |
| `login.html` | 互動原型 | 數位財金公會認證中心，登入/註冊 UI。Firebase 為模擬描述。 |
| `investment_cash_manager.html` | 股市與投資 | 投資現金水位管理，含市場評分、配置比例、本機儲存。 |
| `LoanCalculator.html` | 房地產 | 貸款月付金試算器，含 CSV 下載。 |
| `resume.html` | 展示頁 | LinkedIn 風格履歷與互動小工具。 |
| `nanfeng-150-2-3f.html` | 房地產 | 桃園區南豐街住宅售價評估與銷售策略。 |
| `project20260912001.html` | 房地產 | 清豐路透天物件價格與風險評估。 |
| `property-tracker.html` | 房地產 | 房產標的與狀態追蹤清單。 |
| `IBKR_KRW_interest_visual_report_20260804.html` | 股市與投資 | IBKR/KRW 借款利息驗證報告。 |
| `SKhynix_Q2_2026_claude.html` | 股市與投資 | SK hynix Q2 2026 財報查證與市場分析版本。 |
| `SK_hynix_Q2_2026_chatgpt.html` | 股市與投資 | SK hynix Q2 2026 完整財報與預測版本。 |
| `TSLA_SPCX_Optimus_投資框架_查證版.html` | 股市與投資 | Tesla、SpaceX 與 Optimus 投資框架查證版。 |
| `EP700.html` | 股癌專區 | 個股與 AI 產業鏈互動式簡報。 |
| `EP701.html` | 股癌專區 | 個股、AI 產業鏈與多重市場敘事簡報。 |
| `img/` | 圖片素材 | 既有作品使用的圖片資料夾。 |
| `PROJECT_RECORD.md` | 專案紀錄 | 整理目前討論、已完成成果與重要決策。 |
| `PROJECT_GUIDE.md` | 使用說明書 | 本文件。規範後續維護方式、目錄與修改日誌。 |
| `AI_HANDOFF.md` | AI 接手手冊 | 給其他 ChatGPT / Codex 帳號接手時使用的閱讀入口與操作規範。 |

## 如何檢視作品

最推薦的檢視入口：

```text
index.html
```

可用方式：

1. 直接用瀏覽器打開 `index.html`。
2. 或在本機資料夾啟動簡單伺服器後瀏覽。

若直接用 `file://` 打開時，部分瀏覽器可能限制內嵌預覽或外部資源；若預覽不完整，可改用本機伺服器方式。

## 如何新增作品

新增一個 HTML 作品時，請依序做以下事情：

1. 把新的 `.html` 檔放在專案根目錄，或放在清楚命名的子資料夾。
2. 確認新檔案可以獨立開啟。
3. 更新 `index.html` 內的 `projects` 清單：
   - `title`：作品名稱
   - `file`：檔案路徑
   - `group`：頁籤分類代碼；以 `EP` 開頭的頁面使用 `episode`
   - `type`：卡片顯示的內容類型
   - `description`：一到兩句簡述
   - `notes`：幾個短標籤
4. 更新本文件的「檔案目錄與簡述」。
5. 更新 `PROJECT_RECORD.md` 的「目前實際存在的主要檔案」或新增成果紀錄。
6. 在本文件「修改日誌」新增一筆日期紀錄。
7. 檢查 Git 狀態並提交。

## 如何修改既有作品

修改既有 HTML 頁面時：

1. 先確認這個檔案是否被 `index.html` 收錄。
2. 若作品名稱、用途、分類或描述有改，更新 `index.html`。
3. 若修改影響專案定位、維護方式或使用方式，更新本文件。
4. 若修改是重大成果或方向變更，更新 `PROJECT_RECORD.md`。
5. 在「修改日誌」新增一筆紀錄。

## 文件維護規則

後續每次進度都要檢查這兩份文件是否需要更新：

- `AI_HANDOFF.md`
- `PROJECT_RECORD.md`
- `PROJECT_GUIDE.md`

判斷方式：

| 情境 | 要更新的文件 |
| --- | --- |
| 新增作品 | `index.html`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` |
| 移除作品 | `index.html`、`PROJECT_GUIDE.md`、必要時 `PROJECT_RECORD.md` |
| 修改作品說明或分類 | `index.html`、`PROJECT_GUIDE.md` |
| 改變專案方向 | `PROJECT_RECORD.md`、`PROJECT_GUIDE.md` |
| 改變 AI 接手流程 | `AI_HANDOFF.md`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` |
| 推送或完成一個里程碑 | `PROJECT_RECORD.md`，並在本文件修改日誌登錄 |
| 只修小錯字或微調樣式 | 至少在本文件修改日誌簡短登錄 |

原則：

- 文件要反映目前實際工作區狀態。
- 不要把已刪除或不存在的檔案寫成仍在使用。
- 若有不確定狀態，標記為「待確認」，不要硬寫成既定事實。
- `index.html` 是正式總覽入口；不要把單一作品覆蓋到此檔案。

## Git 與推送流程

建議流程：

1. 檢查目前狀態。
2. 確認本次修改只包含相關檔案。
3. 提交前快速檢查總覽頁是否仍能開啟。
4. 建立清楚的 commit message。
5. 推送到 GitHub。
6. 在 `PROJECT_RECORD.md` 或本文件修改日誌補上重要推送紀錄。

已知遠端：

```text
origin https://github.com/nanglekimo/testest.git
```

主要分支：

```text
main
```

## 修改日誌

### 2026-09-30

- 重新盤點專案內全部 HTML 頁面，確認總覽頁以外共有 14 個可檢視頁面。
- 重做 `overview.html`，移除已不存在的舊頁面，補入目前所有房地產與投資研究頁面。
- 將總覽改為「房地產」、「股市與投資」、「舊作品集」三個獨立頁籤，避免不同用途的內容混在一起。
- 各頁籤保留搜尋、簡短說明、標籤、即時預覽與完整頁面連結；預覽只載入目前頁籤內容以降低負擔。
- 同步更新 `PROJECT_GUIDE.md`、`PROJECT_RECORD.md` 與 `AI_HANDOFF.md`。
- 依使用者指示刪除原 `index.html` 公會轉職鑑定系統，將重做後的總覽頁改為新的 `index.html` 正式首頁；目前收錄 13 個作品。
- 新增「股癌專區」第四個頁籤，將 `EP700.html`、`EP701.html` 及後續所有 EP 開頭頁面與一般股市研究分開管理。

### 2026-08-10

- 新增 `AI_HANDOFF.md`，作為其他 ChatGPT / Codex 帳號接手專案時的第一份閱讀文件。
- 補充 AI 接手閱讀順序、第一句提示、不可做事項、標準流程、文件更新判斷表與驗收標準。
- 更新本說明書，明確指出後續接手帳號需先讀 `AI_HANDOFF.md`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md`。

### 2026-08-09

- 新增 `PROJECT_RECORD.md`，整理目前討論、成果、重要決策與目前實際檔案狀態。
- 新增 `PROJECT_GUIDE.md`，建立後續維護規則、目錄、使用方式與修改日誌格式。
- 明確規定後續每次進度應檢查並必要更新 `PROJECT_RECORD.md` 與 `PROJECT_GUIDE.md`。

### 2026-05-25

- 新增 `overview.html` 作為前端作業總覽頁。
- 總覽頁包含搜尋、分類、簡短說明、作品標籤與內嵌預覽。
- 已提交並推送到 GitHub `main` 分支。
