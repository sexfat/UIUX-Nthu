# [LOG] Unit 07／Unit 09 補齊課堂練習與回家作業頁面

對應規格：[docs/spec/unit07-unit09-exercises.md](../spec/unit07-unit09-exercises.md)

---

## 2026-08-29 — 新建兩個單元的 exercises.html，Unit 07 另補真實 Figma 範本

**修改檔案：**
- `Unit_07/exercises.html` — 新增，4 階段課堂練習（80 分）＋ 作業 6 回家作業＋配分
- `Unit_07/README.md`、`article.html`、`slides.html` — 加課堂練習／回家作業／Style Tile 骨架檔連結；README 標題數字修正（見下方「殘留舊編號」段落）
- `Unit_09/exercises.html` — 新增，3 階段課堂練習（45 分）＋ 回家作業兩部分（作業 9、規範文件正式版）＋配分
- `Unit_09/README.md`、`article.html`、`slides.html` — 加課堂練習／回家作業連結；README「本單元產出」改寫為 Part A／Part B
- Figma 檔案 `UxS7TVst4TOjqktZUMc4m0` — 新增頁面「Unit 07 Style Tile 骨架」（page `12:2`，主 Frame `12:4`）
- `index.html`、根目錄 `README.md` — 兩個單元卡片／表格加練習與作業連結；順便把 Unit 08 也一起補進根目錄 README 表格（Unit 08 本來就有 exercises.html，只是表格一直沒收錄）

**實作說明：**
用戶要求「每個課程有設計範例、練習、作業」，盤點後 Unit 07、09 是僅有的「有簡報＋講義、完全沒有練習頁」的單元。兩個單元的 exercises.html 都**不含新研究內容**——內容整理自各自 article.html 早就寫好的段落：Unit 07 是 §12（課堂練習與回家作業）與 §13（AI 提示詞）；Unit 09 是 §10（作業 9：Figma APP 介面頁面）與 §12（用 AI 撰寫規範文件的三步驟：草稿→找漏洞→轉檢核表）。

Unit 07 的 article.html 第 10 節定義了「Style Tile 骨架」該有的六個區塊（風格故事、色票、字體、介面元素、質感規格、圖像方向，每區都要有一句理由說明），練習裡也提到學生課前要準備「一份空白的 Style Tile 骨架檔」，但這個檔案從來沒有真的存在過——延續 Unit 03／05／11 已經確認可行的做法，交給 `codex exec --approve-for-me` 在共用示範檔 `UxS7TVst4TOjqktZUMc4m0` 新增一個頁面，做出六區骨架（半成品＋空白待填欄位＋理由說明提示，不是完成品範例）。這邊不採信 Codex 的完成報告，另外用 `get_metadata` 讀取新頁面結構（確認六區、命名、Auto Layout 都跟指定的一致）與 `get_screenshot` 重新截圖（確認實際渲染文字——虛線框的待填提示、色票的色碼空格、按鈕/輸入框/標籤/卡片的視覺占位都正確），驗證通過才把連結接進 `exercises.html`、`article.html`、`slides.html`、`README.md` 四個地方。

寫 Unit 07 exercises.html 時，順手核對了 article.html 全文的單元編號引用，發現自我指稱整份寫成「Unit 08」（改版前的舊編號），跨單元引用也停留在舊編號（Wireframe 講成「Unit 07」應為 Unit 04、Persona/競品分析講成「Unit 03/04」應為合併後的 Unit 02、多斷點版面講成「Unit 09」應為 Unit 11），還有一個死連結指向已經清空的 `Unit_06/`。這是獨立於練習頁的既有 bug，修正過程與佐證記在 [future/maintain.md](../../future/maintain.md) 2026-08-29 第 10 筆，這裡不重複。

寫完後跑 `validate.py`，Unit_07、Unit_09 皆全綠；時間對帳：Unit_07 簡報 Agenda「講述70+課堂練習80+成果分享15+休息15=180」與 exercises.html 四階段 20+15+20+25=80 一致；Unit_09 沒有既有的 Agenda 可對，exercises.html 自訂的三階段 15+15+15=45 分鐘是這次新設計的練習時間，不影響其他檔案的既有數字。

再跑一輪 Codex 內容審查，回報 2 項確定錯誤：① Unit_07 Exercise 01 只給 2 個競品的樣本，卻要學生標出「類別慣例」——article 原文其實是用 3 個競品才稱為慣例（樣本數不足以下這個結論），改成「兩家共通的候選模式」的講法，並在交件說明裡加註「樣本只有 2 個，先當候選，不要下結論說是整個類別的慣例」；② Unit_09 的 exercises.html 自行把回家作業擴大成「至少 2 個元件、10 項檢核表、獨立 70 分」，這是實質新增的規格，跟 `Unit_09/README.md` 原本寫的「一個元件的規範文件草稿」互相矛盾，造成 article／README／exercises 三份文件對本單元產出有三種不同定義——已把 exercises.html 的 Part B 縮回符合 README 的範圍（1 個元件、至少 4 條規則、至少 6 項檢核），並把 README 的「本單元產出」改寫成明確列出 Part A（作業 9）與 Part B（規範文件）兩部分，讓三份文件對齊同一個範圍。另有兩項小型可刪減建議（Unit_09 exercises 裡未使用的 `.prompt` CSS、部分重複的說明文字）一併處理。

**已知問題 / 備註：**
- Unit_09 exercises.html 自訂的 45 分鐘課堂練習時間，Codex 審查認為「數學正確但執行偏緊」（45 分鐘內要完成 3 條規則＋5 個邊界情況＋5 項檢核＋三輪 AI 對話），屬於建議層級，這次未調整，留給授課者依實際班級狀況微調。
- Unit_02、04 頂層未重建練習頁（子資料夾內容已足夠），但檢查 `index.html` 時發現兩個單元的子資料夾 exercises.html（`from-competitor-persona`、`from-journey-map`、`from-ia`、`from-flowchart-wireframe`，檔案本來就存在）完全沒有從課程總覽連過去，等於學生找不到——順手在 `index.html` 補上四個「練習：⋯」連結，都確認檔案存在才加。
