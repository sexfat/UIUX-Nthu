# [LOG] Unit 03 完整教材建置（Figma 基本操作）

對應規格：[docs/spec/unit03-figma-basics.md](../spec/unit03-figma-basics.md)

---

## 2026-08-29 — 新建 Unit 03 三份教材，來源改用 Figma 官方文件

**修改檔案：**
- `Unit_03/resources/shapes-layers.md`、`auto-layout.md`、`components-variants.md`、`prototype.md` — 新增，Figma Help Center 文件中文整理
- `Unit_03/resources/figma-demo/01-shapes-layers.png`、`02-auto-layout.png`、`03-component-variants.png`、`04-prototype-connection.png` — 新增，示範用 Figma 檔案截圖
- `Unit_03/slides.html` — 新增，20 張投影片
- `Unit_03/article.html` — 新增，11 節完整教材
- `Unit_03/exercises.html` — 新增，4 階段課堂練習與回家作業
- `Unit_03/README.md` — 補齊單元目標、課程內容、時間分配、練習與作業、參考資料
- `index.html` — Unit 03 卡片換上簡報／講義／練習與作業三個連結；頁尾說明移除 Unit 03
- `README.md` — 課程單元表補 Unit 03 連結；「修改紀錄」段落更新為現況
- `教學排程整合草稿.md` — 標記為已封存

**實作說明：**
`Unit_03/resources/` 原本是空的，沒有既有課程素材可溯源。用 WebSearch／WebFetch 蒐集 Figma Help Center 官方文件（Shape tools、Layers 101、Guide to auto layout、Components collection、Create and use variants、Guide to prototyping、Connect your prototype 等），整理成 4 份來源檔案，教材每個觀念都標明出處。

示意圖沒有用文字/ASCII 拼流程圖，改成直接呼叫 Figma MCP（`create_new_file` + `use_figma` + `get_screenshot`）建立一個示範用 Figma 檔案，做出形狀圖層卡片、Auto Layout 前後對照的標籤列、Button Component 的 4 個 Variant、Prototype 連接的兩張手機畫面，截圖存進 `resources/figma-demo/`，教材直接引用並附 `figcaption`。

三份檔案的 CSS／JS 骨架沿用 Unit_08（目前唯一具備 slides／article／exercises 三檔齊全的單元），只新增 `.img-cap`（投影片圖說）與 `.fig`（講義圖片區塊）兩個內容型 class，深色頁樣式一併補齊。

寫完後跑 `python3 .claude/skills/unit-materials/validate.py Unit_03`，結構、連結、錨點、class、編號全部通過；時間對帳：簡報 Agenda 45+45+70+10+休息10=180 分，練習頁 4 階段 15+15+20+20=70 分，與簡報 Part 3 相符。

再跑一輪 `codex exec` 內容審查（依 `references/content-traps.md` 的審查提示詞骨架），回報 4 項確定內容錯誤（Auto Layout 批次快捷鍵 Mac/Windows 寫反、「大多數圖層」漏講「非文字」、Frame 的「基礎」被寫成 Component/Prototype 的絕對必要條件、Shift+A 沒反應被錯誤歸因成 Group）與 3 項教學設計缺口（Exercise 02 只對外層標籤列設定 Auto Layout，個別標籤本身仍是固定寬度，文字變長會在標籤內溢出而非撐開標籤；Exercise 04 要求用 Instance 卻沒有講怎麼從 Assets 面板拖出來；回家作業要求把整張卡片包進一個 Auto Layout Frame，會讓原本疊在照片上的頭像被排開，需改用巢狀結構＋頭像走 Ignore auto layout），全部依審查結果修正。另有 4 項「可刪減」建議（AI 提示詞維持在講義最後一節、Push overrides 移出投影片核心改留講義查、進階快捷鍵集中成講義查詢內容、回家作業規模從 3–5 個 Component 降為 2 個並把 Smart Animate 改為加分項），經用戶確認後全部採用。

收尾階段（`index.html`、根目錄 `README.md`、`教學排程整合草稿.md` 的修改）依 `CLAUDE.md` 規則，先列出變動清單經用戶確認後才動手。

**已知問題 / 備註：**
- Unit 05（產品設計基本元素）、Unit 11（No-Code 實作）教材仍待補齊，`index.html` 頁尾說明已同步更新為僅列這兩個單元。
- 示範用 Figma 檔案（[Unit03 Figma 基本操作示範](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0)）建立在使用者的 Figma 帳號 drafts 底下，僅供截圖來源，未整理成學生共用範本檔。（後續更新：已於下方 2026-08-29 補上真實範本檔頁面）

---

## 2026-08-29（後續）— 新增真實課堂範本檔頁面

**修改檔案：**
- Figma 檔案 `UxS7TVst4TOjqktZUMc4m0` — 新增頁面「Unit 03 練習範本」（page `4:8`），含 ① 形狀與圖層起始畫布（`4:11`）② Auto Layout 手動排版錯誤示範＋重做區（`4:12`）③ 尚未 Component 化的按鈕起始狀態（`4:13`）④ 列表頁／詳細頁空白 iPhone 尺寸畫面（`4:14`），每區都附交件前核取清單
- `Unit_03/exercises.html` — 開頭 callout 加課堂範本檔說明；Exercise 01–04 的 meta 列各加「範本檔 · 區塊 ①–④」連結；foot-nav 加課堂範本檔連結
- `Unit_03/README.md` — 相關檔案清單補課堂範本檔項目

**實作說明：**
用戶要求 Unit 03／05 比照 Unit 08、09 已有的模式，提供真實 Figma 範本檔而不只是教材裡的示意截圖，並指定由 Codex 執行、這邊負責核對。原先假設 Codex CLI 在 headless 模式下無法操作 Figma（`figma-use` skill 的一般性說明），但實測發現這個環境的 `~/.codex/config.toml` 設定了 `mcp_servers.figma`（`https://mcp.figma.com/mcp`），對同一個帳號開放完整的 `use_figma`／`get_screenshot` 等工具（`codex exec` 呼叫 `whoami` 回傳的帳號跟這邊一致）——因此把實際建置工作交給 `codex exec --approve-for-me`，而不是自己動手。

給 Codex 的提示詞要求先讀 `Unit_03/exercises.html` 掌握四個 Exercise 的確切內容（時間、步驟、常卡住提示、交件標準），不可自行編造規則；並參照 Unit 08 既有範本檔（`X0nEWewUts2YSRElqN6dE3`）的資訊架構做法：使用說明 Frame + 每個 Exercise 一個大 Frame（標題、摘要、起始狀態半成品、核取清單）。Unit 03 與 Unit 05 兩個 Codex 執行工作以背景平行進行，各自建自己的新頁面，未互相干擾。

Codex 完成後，**由這邊獨立驗證**，不採信 Codex 自己的完成報告：用 `get_metadata` 讀取新頁面結構，發現節點名稱（如「區塊標題」「練習說明」）只是通用圖層命名，因此另外用 `get_screenshot` 重新截圖確認實際渲染文字——確認四個區塊的標題、說明、起始狀態、核取清單內容都正確對應 `exercises.html`，版面沒有跑版或文字重疊，起始按鈕確實還是一般 Frame（不是 Component，符合練習要學生自己動手做的設計）。

驗證通過後才動手更新 `exercises.html` 與 `README.md` 加連結，寫法對齊 Unit 08 既有的「範本檔 · 區塊 N」模式；`validate.py Unit_03` 重跑確認結構仍全綠。

**已知問題 / 備註：**
- 範本檔跟 Unit 03 原本的示意截圖共用同一個 Figma 檔案（`UxS7TVst4TOjqktZUMc4m0`），用不同頁面區分，避免管理兩份檔案。
