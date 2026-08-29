# [LOG] Unit 05 完整教材建置（產品設計基本元素）

對應規格：[docs/spec/unit05-basic-elements.md](../spec/unit05-basic-elements.md)

---

## 2026-08-29 — 新建 Unit 05 三份教材，來源改用公認設計系統文件

**修改檔案：**
- `Unit_05/resources/color.md`、`typography.md`、`icons.md`、`buttons.md` — 新增，Material Design 3／WCAG／NN/g／Figma／Apple HIG 官方文件中文整理
- `Unit_05/resources/figma-demo/05-color-roles.png`、`06-type-scale.png`、`07-icon-sizes.png`、`08-button-states.png` — 新增，示範用 Figma 檔案截圖
- `Unit_05/slides.html` — 新增，19 張投影片
- `Unit_05/article.html` — 新增，12 節完整教材
- `Unit_05/exercises.html` — 新增，4 階段課堂練習與回家作業
- `Unit_05/README.md` — 補齊單元目標、課程內容、時間分配、練習與作業、參考資料
- `index.html` — Unit 05 卡片換上簡報／講義／練習與作業三個連結；頁尾說明移除 Unit 05
- `README.md` — 課程單元表補 Unit 05 連結

**實作說明：**
跟 Unit 03 一樣，`Unit_05/resources/` 原本是空的。這次改用公認的設計系統官方文件為來源：Material Design 3（色彩角色、選色方案、Type Scale、Icon 設計原則與尺寸）、W3C WAI 與 WebAIM（WCAG 對比度門檻）、NN/g 與 Figma 資源庫（按鈕五狀態、Figma Variants 組織方式）、Apple HIG（按鈕標籤文字寫法）。四份來源整理成 `resources/*.md`，教材每個觀念都標明出處。

示意圖延續 Unit 03 建立的示範用 Figma 檔案（同一個檔案，新增 4 個畫面），用 `use_figma` 做出色彩角色卡（5 個角色配對）、Type Scale 樣本（5 組角色文字比較）、Icon 尺寸對照（20/24/40/48dp）、按鈕 5 狀態 Component Variants，截圖存進 `resources/figma-demo/`。

三份檔案的骨架沿用 Unit_08／Unit_03，色票、JS 行為一致；新增 `.sw-row` 系列樣式參照 Unit_08 但本單元未使用（Codex 審查標記為死樣式，留待下次清理）。

寫完後跑 `python3 .claude/skills/unit-materials/validate.py Unit_05`，結構、連結、錨點、class、編號全部通過；時間對帳：簡報 Agenda 40+40+80+10+休息10=180 分，練習頁 4 階段 20×4=80 分，與簡報 Part 3 相符。

再跑一輪 Codex 內容審查，回報 6 項確定內容錯誤（把 Pressed 縮小 98%／Disabled 透明度 38% 等示例數值寫成硬性規則、Type Scale 被簡化成「字級大小順序」而非四項屬性的完整定義、對比度不足被錯誤歸因成「來源色太飽和」而非配對未實測、Outline 被練習與評分表誤當成需要 On 色配對並測對比度的角色、簡報寫「5 級字級應用」但練習只涵蓋 4 個角色、AI 提示詞問「有沒有角色缺少 Container 版本」過度泛化到 Primary 以外的角色），全部依審查結果修正；另有 1 項教學設計缺口（Exercise 01 要求 20 分鐘內手動推出 5 組色彩角色配對，來源實際做法是用演算法產色，時間上無法穩定完成），補上 `../Unit_09/tools-stark-material.html`（既有的 Material Theme Builder 外掛操作指南）作為產色工具指引。

Codex 另提出 4 項「可刪減」建議，依用戶指示只採用「回家作業刪掉額外製作 2 個 Icon，改把配分（15 分）併入真實畫面套用（25→40 分）」這一項，其餘（第 11 節併入頁尾、簡報作業預告/結尾兩張留一張、AI 提示詞搬到附錄）維持原狀。

收尾階段（`index.html`、根目錄 `README.md` 的修改）依 `CLAUDE.md` 規則，先列出變動清單經用戶確認後才動手。

**已知問題 / 備註：**
- Unit 11（No-Code 實作）教材仍待補齊，`index.html` 頁尾說明已同步更新為僅列 Unit 11。
- `slides.html` 裡的 `.sw-row`／`.sw-item`／`.sw-chip`／`.sw-lbl` 樣式是從 Unit_08 骨架帶過來但本單元未使用的死樣式，Codex 審查標記為可清理項目，這次未處理。

---

## 2026-08-29（後續）— 新增真實課堂範本檔頁面

**修改檔案：**
- Figma 檔案 `UxS7TVst4TOjqktZUMc4m0` — 新增頁面「Unit 05 練習範本」（page `4:2`），含 ① 5 張空白色票卡骨架（`4:4`）② Type Scale 四層文字角色標籤骨架（`4:5`）③ 24dp／40dp Icon 對齊骨架（`4:6`）④ Enabled 按鈕起始 Component（`4:7`），每區都附交件前核取清單
- `Unit_05/exercises.html` — 開頭 callout 加課堂範本檔說明；Exercise 01–04 的 meta 列各加「範本檔 · 區塊 ①–④」連結；foot-nav 加課堂範本檔連結
- `Unit_05/README.md` — 相關檔案清單補課堂範本檔項目

**實作說明：**
跟 Unit 03 同一批處理，做法與理由詳見 [docs/changelog/unit03-figma-basics.md](unit03-figma-basics.md) 的對應段落——這裡只記錄 Unit 05 特有的部分。

Unit 05 的範本檔內容比 Unit 03 更偏向「填空」而非「從零操作」：色彩角色卡是灰色佔位色塊加「背景 #______／On #______」與「［對比度：___］」空格；Type Scale 練習區沿用 Unit 03 卡片的四層文字（Headline/Title/Body/Label），每層旁邊留「［套用角色：___］」空格；Icon 對齊區留兩組空白圖示佔位框與「基準線位移：___px」空格；按鈕狀態區只放一個真正的 Enabled Component（型別驗證為 `COMPONENT`），要求學生自己複製出其餘四個狀態並 Combine as variants，範本檔本身不做五狀態、以免變成讓學生照抄的標準答案。

驗證方式同 Unit 03：用 `get_metadata` 確認結構、`get_screenshot` 重新截圖確認實際渲染文字（metadata 的圖層名稱如「區塊標題」只是通用命名，不代表實際內容），確認四個區塊都對應 `exercises.html` 的四個 Exercise，版面無跑版或重疊。驗證通過後才更新 `exercises.html`／`README.md`；`validate.py Unit_05` 重跑確認結構仍全綠。

**已知問題 / 備註：**
- 範本檔跟 Unit 05 原本的示意截圖共用同一個 Figma 檔案（`UxS7TVst4TOjqktZUMc4m0`），用不同頁面區分。
