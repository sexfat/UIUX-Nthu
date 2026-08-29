# [LOG] Unit 11 完整教材建置（No-Code 實作）

對應規格：[docs/spec/unit11-no-code.md](../spec/unit11-no-code.md)

---

## 2026-08-29 — 新建 Unit 11 三份教材，含真實 Figma 設計稿與生成網頁示範

**修改檔案：**
- `Unit_11/resources/dev-handoff.md`、`figma-mcp-claude-code.md` — 新增，Figma 官方文件與 Claude Code／Gemini CLI 官方說明的中文整理
- `Unit_11/resources/figma-demo/01-landing-mockup.png` — 新增，示範用 Figma 設計稿截圖
- `Unit_11/resources/demo-site/index.html` — 新增，從設計稿實際生成的靜態網頁
- `Unit_11/slides.html` — 新增，19 張投影片
- `Unit_11/article.html` — 新增，13 節完整教材
- `Unit_11/exercises.html` — 新增，4 階段課堂練習與回家作業
- `Unit_11/README.md` — 補齊單元目標、課程內容、時間分配、練習與作業、參考資料
- `index.html` — Unit 11 卡片換上簡報／講義／練習與作業三個連結；頁尾說明移除「教材尚未建立」
- `README.md` — 課程單元表補 Unit 11 連結

**實作說明：**
Unit 11 是全課程最後一個沒有教材的單元，跟 Unit 03、05 一樣 `resources/` 原本是空的，而且連 `舊版課綱備查.md` 都沒有對應內容——改以 Figma 官方文件（[Guide to Dev Mode](https://help.figma.com/hc/en-us/articles/15023124644247-Guide-to-Dev-Mode)、[Guide to developer handoff in Figma](https://www.figma.com/best-practices/guide-to-developer-handoff/)、[Claude Code and Figma: Set up the MCP server](https://help.figma.com/hc/en-us/articles/39888612464151-Claude-Code-and-Figma-Set-up-the-MCP-server)）與 Claude Code／Gemini CLI 官方 GitHub／文件為來源，整理成 `resources/*.md`。「AI 網頁生成」與「溝通模擬」兩節直接引用 `清華大學課程大綱.md` 第三階段（12/2 & 12/9）的原始文字，不是另外杜撰的教學設計。

**示範素材的建置方式**：用戶指示這部分「呼叫 Codex 執行，你負責核對」，延續前一輪 Unit 03／05 範本檔建置時確認過的做法——這個環境的 Codex CLI 設定了 `mcp_servers.figma`（`https://mcp.figma.com/mcp`），對同一個 Figma 帳號開放完整的 `use_figma`／`get_screenshot` 等工具，因此請 `codex exec --approve-for-me` 在共用示範檔 `UxS7TVst4TOjqktZUMc4m0` 裡：① 新增頁面「Unit 11 示範：Figma 轉網頁」（page `7:2`），做出一個 1440×1024 的「學習角」線上課程報名頁 Frame（`7:3`，含導覽列、Hero、三張特色卡片、Footer，Auto Layout 排版）；② 不透過任何自動轉檔工具，直接依照這個設計稿手寫一個內嵌 CSS、無外部依賴、響應式的靜態網頁，存到 `Unit_11/resources/demo-site/index.html`，文案與配色跟設計稿一致。

驗證方式：**不採信 Codex 自己的完成報告**，由這邊獨立用 `get_metadata`（確認 `7:2`／`7:3` 節點結構跟需求一致）與 `get_screenshot`（重新截圖，跟 Codex 回報的內容比對）驗證 Figma 設計稿；直接讀取並檢視 `demo-site/index.html` 原始碼，確認文案、色票（`--primary: #1d4ed8` 等）、RWD 中斷點（700px）、無障礙屬性（aria-label、focus-visible）都存在且合理。截圖與程式碼比對後兩者內容完全一致（同一組文案：學習角／30 天學會 UI/UX 設計基礎／業界講師／實作練習／作品集產出／立即報名／© 2026 學習角）。

寫完後跑 `python3 .claude/skills/unit-materials/validate.py Unit_11`，結構、連結、錨點、class、編號全部通過；時間對帳：簡報 Agenda 35+35+90+10+休息10=180 分，練習頁 4 階段 15+30+30+15=90 分，與簡報 Part 3 相符。

再跑一輪 Codex 內容審查，回報 4 項確定內容錯誤（把「響應式」窄化成「手機一定要直向堆疊」而非課綱原意的「具備響應式」；把「重新啟動 Claude Code」的官方步驟誤寫成「重開終端機」；用來源沒提到的「列出最近開啟的 Figma 檔案」當連線驗證方式，來源只支援選取式／連結式操作；簡報宣稱做出「能點的網頁」，但作業與評分只驗證靜態頁面的開啟與響應式，用詞超出實際範圍）與 4 項用詞過度斷言（「不用工程師畫」混淆了工程師的角色是實作不是畫設計；「顏色間距全部從真的檔案讀出來」過度保證完整性；「命名越清楚生成結果越準」宣稱了來源沒證明的因果關係；「Desktop 版本 Enterprise 專用」原本沒有來源根據），全部依審查結果修正，其中 Desktop 版本的說法改為補上出處到 `resources/figma-mcp-claude-code.md`（原始 WebFetch 內容裡本來就有，只是先前整理來源檔案時漏收）。

另有 2 項確定的教學設計缺口：Exercise 03 原本要學生「打開範例設計稿」卻沒有給任何連結，而教材裡的示範圖只是一張 PNG，學生無法在圖片上選取 Frame 或複製連結——這是會讓練習完全做不下去的阻塞，已補上真正的 Figma Frame 連結（`https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0?node-id=7-3`），並把「連結式」調整為主要工作方式（選取式改成「時間夠再試」），同時補上工作資料夾的建議（先建空白資料夾再啟動 Claude Code）；回家作業的評分表原本只有「通過／不及格」兩極、且「交接準備」一項沒有要求任何可檢查的佐證，已改成三級（通過／部分達成／不及格）並要求附 Figma 連結或截圖，同時把「客戶」溝通模擬角色從必做改為加分項（+10），避免溝通模擬佔用太多本該花在網站修正上的時間。

Codex 另外指出 Gemini CLI 免費額度（來源已列出：個人帳號每分鐘 60 次、每天 1,000 次）完全沒進教材，屬於「有價值但不確定時效性」的補充，已加進講義第 10 節並註明「依 Google 官方公告為準」；其餘可刪減建議（Gemini CLI 簡報頁併入 Claude Code 頁、Exercise 01 課堂版元件數量從 3 個減為 1 個等）評估後判斷影響有限，這次未採用。

收尾階段（`index.html`、根目錄 `README.md` 的修改）依用戶授權自主執行完成，不再逐項確認。

**已知問題 / 備註：**
- 這是全課程最後一個新建教材的單元；至此 12 個單元全部有教材（Unit 06、10、12 為報告／實作／發表課，依課程設計本就不需要獨立簡報）。
- Exercise 02 標題提到 Gemini CLI，但步驟只詳細列出 Claude Code 的安裝流程（來源沒有 Gemini CLI 的對應官方設定步驟可引用）；使用 Gemini CLI 的學生需依賴現場口頭示範，教材裡已加註明。
