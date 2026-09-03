# [LOG] Unit 01「UX 5層架構」層級詳情彈窗

對應規格：[docs/spec/unit01-layer-modal.md](../spec/unit01-layer-modal.md)

---

## 2026-09-02 — 新增 UX 5 層架構的層級詳情彈窗，並修正課程大綱第 3 小時內容

**修改檔案：**
- `Unit_01/slides.html` — 新增 `.layer-detail-btn`／`.layer-modal-overlay`／`.layer-modal` CSS；Slide 4 金字塔列改為帶 `data-layer` 的 `<button>`；Slide 5–9 各加一個「查看目標文件與範例」按鈕；新增共用彈窗 HTML 容器；新增 `layerData` 資料物件與開關彈窗的 JS。另外同一次調整也把 Slide 3 課程大綱「第 3 小時」卡片文字，從過時的「課後作業練習 (Homework)」改成「設計思考 / Design Thinking」（詳見 `future/maintain.md` 2026-09-02 第 1 筆，這裡不重複記述細節）。

**實作說明：**
用戶要求「ux 的五層架構，每一個層，可以說明一下，產出的目標文件會有哪些，以及要給我範例，可以用彈窗 modal 的方式詳細說明」。彈窗架構參考 `Unit_09/article.html` 既有的 `.term-modal-overlay`／`.term-modal`（單一硬編碼彈窗，只給「Dynamic Type」一個名詞用），這次把它改寫成資料驅動的共用彈窗：一份 `layerData`（key 1–5）搭配一個彈窗 DOM，依點擊來源的 `data-layer` 動態填入標題、副標、說明、目標文件清單、範例，兩個觸發點（金字塔列、單層說明頁按鈕）共用同一個彈窗與同一份資料，不重複硬編碼五次。

5 層的「目標文件」與「範例」依 Jesse James Garrett 的 Elements of UX 五層模型撰寫，範例刻意全部取自這門課程自己已經做出來的真實產出，不用外部案例，讓學生看得到「這一層的文件，我們後面哪個單元真的會交」：策略層對應 Unit 02 的 Persona／訪談洞察，範圍層／結構層／骨架層對應 Unit 04 的 Functional Map／資訊架構圖／Flowchart／Wireframe，表現層對應 Unit 05 的色彩字體規範與 Unit 09 的 Design System 元件規範文件。

因為 Unit 01 的簡報用的是它自己一套獨立的 CSS／JS 架構（跟 Unit 03/05/07/09/11 已經標準化的版型不同，例如色票變數、`.pyr-row`、`.blist` 等 class 都是 Unit 01 專屬），這次沒有把整份簡報改成標準化版型，只在既有架構內新增彈窗功能，並比照既有的 `.slide.dark` 規則補了深色頁的按鈕樣式，避免深色投影片上出現看不見的文字。也在既有的方向鍵／空白鍵翻頁 keydown handler 裡加了一個判斷式：彈窗開啟時忽略這些按鍵，避免使用者在看彈窗內容時不小心把簡報切頁。

寫完後起了本機 `python3 -m http.server`，用 Chrome 自動化實際操作：翻到 Slide 4 點擊金字塔第 1 列，確認彈窗正確顯示策略層的說明／文件／範例；按 Escape 確認彈窗關閉且沒有連動切頁；翻到 Slide 5（深色頁）點擊「查看目標文件與範例」按鈕，確認深色頁的按鈕樣式清楚可見、彈窗內容與金字塔點出來的完全一致；也截圖確認 Slide 3 的「第 3 小時」卡片與下方 `design-thinking.html` 連結內容一致。

使用者事後追加要求，策略層的範例再補一個「用麥當勞點餐服務」的具體情境。因為原本彈窗的範例區塊是單一 `<p>`，只能放一段文字，這次把容器改成 `<div id="layerModalExample">`，內容統一改成用 `<p>` 分段（其他 4 層維持單段，策略層變成兩段），並補上 `.layer-modal-example p` 的段落間距 CSS。新增的段落用「麥當勞要推出手機點餐、到店取餐服務」這個情境說明策略層要先回答「為什麼做」「做給誰用」兩題，貼近 `unit-materials` skill 對範例要「舉學生生活裡的例子」的要求。改完重新用 Chrome 自動化截圖確認策略層彈窗同時顯示 Unit 02 與麥當勞兩段範例、段落間距正常，其餘 4 層彈窗內容未受影響。

**已知問題 / 備註：**
- Unit_01 目前仍是全課程唯一還沒對標標準化版型（Unit 03/05/07/09/11 共用架構）的單元，`<title>` 與頁尾 `course-label` 也還留著改版前的舊文案（「UI 設計實作：Figma 與 UX 流程 × AI 設計整合」）。這不在本次調整範圍內，若之後要做，建議另開一個獨立的 Unit 01 版型對標任務，而不是跟著彈窗功能一起改。
- Unit_01 沒有 `validate.py` 支援（該腳本假設標準化版型的結構），這次只能用手動截圖檢查，沒有跑自動化結構驗收。
