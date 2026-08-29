# 單元 11：No-Code 實作

> 對應清華大學課程時段：12/2（三）13:20–16:20

## 相關檔案

- `slides.html` — 課堂簡報（19 張）。
- `article.html` — 完整教材（13 節，含 AI 協作提示詞）。
- `exercises.html` — 課堂練習（4 階段，90 分鐘）與回家作業。
- `resources/dev-handoff.md`、`figma-mcp-claude-code.md` — Figma 官方文件與 Claude Code／Gemini CLI 官方說明的中文整理，本單元教材的溯源依據。
- `resources/figma-demo/` — 教材裡引用的示範截圖（一頁式報名頁 Figma 設計稿），取自示範用 Figma 檔案：[Unit03 Figma 基本操作示範](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0)（與 Unit 03／05 共用同一個示範檔）。
- `resources/demo-site/index.html` — 從上述 Figma 設計稿實際生成的靜態網頁，文案與配色跟設計稿一致，供學生對照「設計稿」跟「生出來的網頁」的關係。
- `reference-web-spec/`（舊「Web 設計規範與網頁結構」單元，含 RWD 觀念與雙平台對照）可作為網站雛形產出時的規範參考。

## 單元目標

- 能判斷一份 Figma 檔案是否已經整理到可以交接給工程師的狀態（命名、Component 說明、Ready for dev 標記）。
- 知道 Dev Mode 能提供給開發者哪些資訊，以及怎麼用有脈絡的說明取代傳統紅線標註稿。
- 能設定 Claude Code 或 Gemini CLI 連上 Figma MCP，並用選取式或連結式兩種工作方式把設計轉成網頁。
- 能檢查生成的網頁是否符合響應式（RWD）要求，並對照原設計找出落差、下指令修正。
- 能在「挑剔的工程師」與「預算有限的客戶」兩種立場下，解釋並捍衛自己的設計決策。

## 課程介紹

手上的 Figma 檔案不會自己變成網站。這堂課做兩件銜接的事：先把設計交接好——讓工程師看得懂、接得住；再用 AI 工具把同一份設計直接生成一個能在瀏覽器打開的網頁。兩件事共用同一個邏輯：把設計脈絡講清楚，對方（不管是人還是 AI）才能做出你要的東西。

Unit 11 原本完全沒有來源素材，內容依據改以 Figma 官方文件（Dev Mode、開發者交接指南、Claude Code MCP 設定說明）、Claude Code 與 Gemini CLI 官方 GitHub／文件整理，並用實際建立的 Figma 設計稿與實際生成的靜態網頁作為示範（見 `resources/`）。溝通模擬練習直接沿用 `清華大學課程大綱.md` 的原始設計。

## 課程內容

- 交接前要準備的事：頁面狀態標示、Component 命名與說明、Style／Variable 命名慣例。
- Dev Mode：開啟方式、Ready for dev 狀態、提供給開發者的七類資訊。
- 溝通做法：邀請開發者當 Viewer、用有脈絡的說明取代紅線標註稿、鼓勵早期協作。
- Claude Code 是什麼：agentic 編碼工具，不是聊天介面。
- Figma MCP：讓 Claude Code 讀懂 Figma 設計的結構化脈絡，設定步驟與兩種工作方式（選取式／連結式）。
- Gemini CLI：另一個做同件事的工具，操作邏輯共通。
- 溝通模擬：請 AI 扮演「挑剔的工程師」或「預算有限的客戶」，練習解釋設計決策。

## 課堂練習

**從交接準備到一個能打開的網頁**（90 分鐘，個人，終端機 + Figma）

1. Exercise 01（15 分）— 交接準備：標記 Ready for dev。
2. Exercise 02（30 分）— 設定 Claude Code／Gemini CLI + Figma MCP。
3. Exercise 03（30 分）— 把一個畫面轉成真的網頁。
4. Exercise 04（15 分）— 溝通模擬：跟 AI 練習解釋設計決策。

**上課前準備：** 筆電需事先安裝好 Claude Code 或 Gemini CLI 並完成帳號登入，現場只夠時間裝 Figma 外掛與設定連線，見 `exercises.html` 開頭提醒。

### 三小時時間分配

| 段落 | 時間 | 內容 |
| :--- | :--- | :--- |
| Part 1 | 35 分 | 跟工程師協作：交接、Dev Mode、溝通做法 |
| Part 2 | 35 分 | AI 網頁生成：Claude Code／Gemini CLI + Figma MCP |
| 休息 | 10 分 | |
| Part 3 | 90 分 | 課堂練習四階段 |
| Part 4 | 10 分 | 成果分享 |

講述 70 分 + 實作與分享 100 分 + 休息 10 分 = 180 分。

## 回家作業

**把專題畫面轉成網頁**

1. 挑自己專題的一個核心畫面，整理交接狀態（命名清楚、Component 有說明、標記 Ready for dev）。
2. 用 Claude Code 或 Gemini CLI 把這個畫面轉成網頁，檢查響應式效果與內容一致性。
3. 至少修正一輪，記錄對照落差與修正指令。
4. 完成「挑剔的工程師」與「預算有限的客戶」兩個角色的完整溝通模擬紀錄。

配分：交接準備 20、生成的網頁 40、修正紀錄 15、溝通模擬 25，各項的「通過的樣子」與「不及格的樣子」寫在 `exercises.html#submit`。

## 對應清大日期與時段

- 12/2（三）13:20–16:20

## 本單元產出

- 一個實際能在瀏覽器打開的個人專題網頁（靜態頁面）。
- 一份跟 AI 完成的溝通模擬紀錄（工程師／客戶兩種角色）。

## 參考資料

- [Guide to developer handoff in Figma](https://www.figma.com/best-practices/guide-to-developer-handoff/) — Figma Best Practices。
- [Guide to Dev Mode](https://help.figma.com/hc/en-us/articles/15023124644247-Guide-to-Dev-Mode) — Figma Help Center。
- [Claude Code and Figma: Set up the MCP server](https://help.figma.com/hc/en-us/articles/39888612464151-Claude-Code-and-Figma-Set-up-the-MCP-server) — Figma Help Center。
- [anthropics/claude-code](https://github.com/anthropics/claude-code) — GitHub。
- [Claude Code by Anthropic](https://claude.com/product/claude-code) — 官方產品頁。
- [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) — GitHub。
- [Gemini CLI 官方文件](https://geminicli.com/docs/)。
- `清華大學課程大綱.md`〈第三階段：AI 輔助開發與專題落地〉——「AI 網頁生成」與「溝通模擬」的原始課綱依據。

## 備註

- 這是全課程最後一個新建教材的單元；Unit 06、10、12 是報告／實作／發表課，不需要獨立新教材。
- 內容依用戶指示自主建置，執行方式與 Unit 03／05 一致：Figma 示範素材由 Codex 呼叫 Figma MCP 建置，這邊獨立驗證後才收尾。
