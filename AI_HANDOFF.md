# AI 接手交接手冊

最後更新：2026-09-30

## 這份文件的用途

這份文件是給「之後用另一個 ChatGPT / Codex 帳號接手專案」時使用的交接入口。新的 AI 帳號登入後，請先讀這份文件，再讀 `PROJECT_GUIDE.md` 與 `PROJECT_RECORD.md`。

目標不是讓 AI 猜測專案方向，而是讓它依照既有規則接續工作。

## 新接手者第一步

請新的 ChatGPT / Codex 帳號在專案資料夾中先讀取以下三份文件：

1. `AI_HANDOFF.md`
2. `PROJECT_GUIDE.md`
3. `PROJECT_RECORD.md`

然後請它做一次「接手前盤點」，不要立刻改檔。

建議使用者可以直接貼這段給新帳號：

```text
請先讀取本專案根目錄的 AI_HANDOFF.md、PROJECT_GUIDE.md、PROJECT_RECORD.md。
讀完後請回覆：
1. 你理解的專案目的
2. 目前主要檔案與入口
3. 目前已知待處理事項
4. 你接下來會遵守的維護規則
在我確認前，請不要修改任何檔案。
```

## 專案一句話摘要

這是一個靜態 HTML 前端作品集合，包含房地產分析、股市研究、股癌 EP 內容與早期作品；目前以 `index.html` 作為正式總覽入口。

## 接手時要先確認的狀態

新的 AI 帳號接手時，請先確認：

1. 目前所在資料夾是否為 `testest`。
2. 目前 Git 分支是否為 `main` 或使用者指定的分支。
3. `git status` 是否有未提交變更。
4. `index.html` 內的作品清單是否和實際存在的作品 `.html` 檔一致。
5. `PROJECT_GUIDE.md` 與 `PROJECT_RECORD.md` 是否反映目前狀態。
6. 如果使用者要求推送，確認遠端仍是 `https://github.com/nanglekimo/testest.git`。

## 目前總覽狀態

截至 2026-09-30，`index.html` 已重新盤點並收錄其餘 13 個 HTML 作品，分成四個固定頁籤：

1. 房地產：4 頁
2. 股市與投資：5 頁
3. 股癌專區：2 頁
4. 舊作品集：2 頁

接手者仍應在每次新增或移除 HTML 後，重新比對總覽清單與實際檔案。新增作品必須依用途放入正確頁籤；所有以 `EP` 開頭的頁面都歸入「股癌專區」。

## 不要做的事

除非使用者明確要求，接手者不要做以下事情：

1. 不要把單一作品覆蓋成 `index.html`；它是正式總覽入口。
2. 不要重新建立已刪除的舊公會轉職鑑定頁，除非使用者明確要求。
3. 不要把單檔 HTML 專案強行改成 React、Vue、Vite 或其他框架。
4. 不要刪除舊作品。
5. 不要還原使用者或其他帳號造成的變更。
6. 不要自動推送 GitHub，除非使用者明確要求。
7. 不要把文件寫成「未來想像狀態」；文件必須反映目前實際工作區。

## 每次工作的標準流程

每次接到新任務時，請依序做：

1. 讀取 `AI_HANDOFF.md`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md`。
2. 檢查工作區現況。
3. 判斷任務是否會影響作品清單、總覽頁或專案規則。
4. 執行任務。
5. 若新增、移除、修改作品，更新 `index.html`。
6. 若專案狀態或成果有變，更新 `PROJECT_RECORD.md`。
7. 若使用方式、維護規則或目錄有變，更新 `PROJECT_GUIDE.md`。
8. 在 `PROJECT_GUIDE.md` 的「修改日誌」新增日期紀錄。
9. 最後回報修改了哪些檔案、是否驗證、是否已提交或推送。

## 文件更新判斷表

| 任務類型 | 必須檢查 | 通常需要更新 |
| --- | --- | --- |
| 新增 HTML 作品 | `index.html`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` | 三者都更新 |
| 刪除或移除作品 | `index.html`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` | 三者都更新 |
| 修改作品內容 | `index.html`、`PROJECT_GUIDE.md` | 若描述或分類變更則更新 |
| 新增報告頁 | `index.html`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` | 三者都更新；EP 開頭歸入股癌專區 |
| 修改維護流程 | `AI_HANDOFF.md`、`PROJECT_GUIDE.md`、`PROJECT_RECORD.md` | 三者都更新 |
| 只修 typo | `PROJECT_GUIDE.md` 修改日誌 | 至少登錄一筆簡短紀錄 |
| 推送 GitHub | `PROJECT_RECORD.md`、`PROJECT_GUIDE.md` 修改日誌 | 登錄 commit 或推送摘要 |

## 驗收標準

完成任何一次實質任務後，應至少符合：

1. 沒有不相關檔案被修改。
2. 若總覽頁受影響，`index.html` 中的作品清單已同步。
3. 文件的檔案目錄沒有列出不存在的檔案。
4. `PROJECT_GUIDE.md` 的修改日誌有新增紀錄。
5. 若推送 GitHub，回報分支、commit、遠端與推送結果。

## 建議的接手回覆格式

新的 AI 帳號完成閱讀後，應用這種格式回報：

```text
我已讀取 AI_HANDOFF.md、PROJECT_GUIDE.md、PROJECT_RECORD.md。

我理解此專案是：
...

目前入口頁是：
...

目前需要優先確認：
...

我後續會遵守：
...
```

## 當文件互相矛盾時

若三份文件內容有衝突，依照以下優先順序處理：

1. 目前檔案系統與 Git 狀態
2. 使用者最新明確指示
3. `AI_HANDOFF.md`
4. `PROJECT_GUIDE.md`
5. `PROJECT_RECORD.md`

如果仍不確定，先向使用者確認，不要自行假設。

