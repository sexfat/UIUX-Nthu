# [SPEC] Unit 03 完整教材建置（Figma 基本操作）

- **日期**：2026-08-29
- **負責人**：bryant_huang
- **狀態**：done
- **變更紀錄**：[docs/changelog/unit03-figma-basics.md](../changelog/unit03-figma-basics.md)

---

## 背景

`index.html` 是課程狀態的唯一依據，Unit 03（對應 9/30「Figma 基本操作」場次）在改版前標示「教材準備中」，`Unit_03/` 底下只有一份 README，`resources/` 完全是空的。9/30 是清華大學課程開課後第三場，是所有缺口單元中最迫近上課日的一個，優先處理。

## 功能說明

新建 Unit 03 的簡報、講義、課堂練習與作業，主題涵蓋 Figma 的四個基本操作：形狀與圖層、Auto Layout、Component 與 Variants、Prototype。因為單元本身沒有既有課程素材可溯源，改以 Figma 官方 Help Center 文件作為內容依據，並用實際建立的 Figma 示範檔截圖取代文字示意圖。

## 實作範圍

- `Unit_03/resources/*.md`：4 份來源整理（形狀圖層、Auto Layout、Component 與 Variants、Prototype），逐段標明 Figma Help Center 出處 URL。
- `Unit_03/resources/figma-demo/`：4 張示範截圖，取自實際建立的 Figma 檔案（[Unit03 Figma 基本操作示範](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0)）。
- `Unit_03/slides.html`（20 張）、`article.html`（11 節）、`exercises.html`（4 階段課堂練習 70 分鐘＋回家作業）、`README.md`：骨架沿用 Unit_08 的三份檔案。
- Codex 內容審查一輪：修正 4 項確定內容錯誤、3 項教學設計缺口，並依建議精簡投影片核心內容與回家作業規模。
- 收尾：`index.html` Unit 03 卡片與頁尾說明、根目錄 `README.md` 課程單元表與修改紀錄、`教學排程整合草稿.md` 封存標記。

## 不在範圍內

- Unit 05（產品設計基本元素）、Unit 11（No-Code 實作）教材，仍待後續處理。
- Figma 示範檔僅用於截圖教學圖示，未整理成學生可複製使用的範本檔（Unit 03 練習是學生自建檔案，不依賴共用範本）。

## 驗收條件

- [x] `python3 .claude/skills/unit-materials/validate.py Unit_03` 結構檢查全綠。
- [x] 三份檔案的每個觀念都能指回 `resources/` 的來源段落。
- [x] Codex 內容審查回報的確定錯誤已全部修正。
- [x] `index.html`、根目錄 `README.md`、`教學排程整合草稿.md` 的收尾更新，皆先列變動清單經用戶確認後才執行。
