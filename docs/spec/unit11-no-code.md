# [SPEC] Unit 11 完整教材建置（No-Code 實作）

- **日期**：2026-08-29
- **負責人**：bryant_huang
- **狀態**：done
- **變更紀錄**：[docs/changelog/unit11-no-code.md](../changelog/unit11-no-code.md)

---

## 背景

Unit 11（對應 12/2「No-Code 實作」場次）是全課程最後一個沒有教材的單元。跟 Unit 03、05 一樣，`Unit_11/resources/` 原本是空的（只有 `reference-web-spec/` 這個舊單元的參考資料夾）；`舊版課綱備查.md` 裡也完全沒有對應內容，是唯一一個新舊課綱都沒有素材可循的單元。

## 功能說明

新建 Unit 11 的簡報、講義、課堂練習與作業，主題涵蓋兩件事：① 跟工程師協作的交接流程（Figma Dev Mode、交接前準備、溝通做法）② 用 AI 工具（Claude Code／Gemini CLI）把 Figma 設計轉成實際網頁的 No-Code 實作流程，以及課綱指定的「溝通模擬」練習。內容依據改以 Figma 官方文件與 Claude Code／Gemini CLI 官方說明為來源，並實際建立一組 Figma 設計稿與從中生成的靜態網頁作為示範。

## 實作範圍

- `Unit_11/resources/dev-handoff.md`、`figma-mcp-claude-code.md`：來源整理，逐段標明官方文件出處 URL。
- `Unit_11/resources/figma-demo/`：示範用 Figma 設計稿截圖（一頁式報名頁），取自共用示範檔 `UxS7TVst4TOjqktZUMc4m0` 新增的頁面。
- `Unit_11/resources/demo-site/index.html`：從上述設計稿實際生成的響應式靜態網頁，文案與配色跟設計稿一致。
- `Unit_11/slides.html`（19 張）、`article.html`（13 節）、`exercises.html`（4 階段課堂練習 90 分鐘＋回家作業）、`README.md`：骨架沿用 Unit_08／Unit_03。
- 收尾：`index.html` Unit 11 卡片與頁尾說明（移除「教材尚未建立」，全課程單元教材至此全部建置完成）、根目錄 `README.md` 課程單元表。

## 不在範圍內

- Gemini CLI 的完整安裝與設定教學（僅作為 Claude Code 的替代選項概述，實際操作以現場示範為準）。
- 學生自己專題畫面的 AI 網頁生成成果，屬回家作業產出，不在教材建置範圍內。

## 驗收條件

- [x] `python3 .claude/skills/unit-materials/validate.py Unit_11` 結構檢查全綠。
- [x] 三份檔案的每個觀念都能指回 `resources/` 的來源段落，或直接引用 `清華大學課程大綱.md`。
- [x] 示範用 Figma 設計稿與生成的靜態網頁內容一致（同一組文案、配色）。
