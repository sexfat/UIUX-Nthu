# [SPEC] Unit 07／Unit 09 補齊課堂練習與回家作業頁面

- **日期**：2026-08-29
- **負責人**：bryant_huang
- **狀態**：done
- **變更紀錄**：[docs/changelog/unit07-unit09-exercises.md](../changelog/unit07-unit09-exercises.md)

---

## 背景

用戶要求「每個課程有設計範例、練習、作業」。盤點全部 12 個單元後，Unit 07（風格發想與建立）與 Unit 09（Design System）是僅有的「已有 slides.html／article.html，但完全沒有 exercises.html」的單元；Unit 07 另外缺少一份文章裡提到、但實際從未建立的「Style Tile 骨架檔」設計範例。Unit 02、04 的課堂練習已存在於各自合併子資料夾（`from-competitor-persona/`、`from-journey-map/`、`from-ia/`、`from-flowchart-wireframe/`）裡，盤點後判斷已足夠，未重建頂層 exercises.html。

## 功能說明

新建 `Unit_07/exercises.html`、`Unit_09/exercises.html`，內容整理自各自 article.html 裡既有的練習／作業段落，不新增未經查證的內容。Unit 07 另建一份真實 Figma Style Tile 骨架範本，供學生複製操作。

## 實作範圍

- `Unit_07/exercises.html`：4 階段課堂練習（80 分鐘，來源 article §12）＋ 作業 6 回家作業（來源 article §12）＋ 評分配分（新設計）。
- `Unit_09/exercises.html`：3 階段課堂練習（45 分鐘，來源 article §12 三步驟）＋ 回家作業兩部分：作業 9 高保真頁面（來源 article §10）、規範文件正式版（來源 article §12，範圍對齊 README 既有的「一個元件」）。
- Figma 頁面「Unit 07 Style Tile 骨架」（`UxS7TVst4TOjqktZUMc4m0`，page `12:2`）：六區骨架，對應 article §10 的定義。
- 收尾：`index.html`、根目錄 `README.md`、兩個單元的 `README.md` 加連結。
- 額外發現並修正：Unit_07 全文殘留改版前的舊單元編號（見 [docs 的姊妹紀錄](../../future/maintain.md)）。

## 不在範圍內

- Unit 02、04 頂層合併頁面的 exercises.html 重建（判斷子資料夾既有練習已足夠）。
- Unit 09 的作業範圍調整為官方定案（目前是把 exercises 與既有 README 對齊到「一個元件」，若之後要擴大範圍需要另外決定）。

## 驗收條件

- [x] `python3 .claude/skills/unit-materials/validate.py Unit_07` 與 `Unit_09` 結構檢查全綠。
- [x] exercises.html 內容均可回指到各自 article.html 的既有段落。
- [x] Figma Style Tile 骨架用 `get_metadata`／`get_screenshot` 獨立驗證，六區結構與文字內容正確。
- [x] Codex 內容審查回報的確定錯誤（Unit_07 樣本數不足以下慣例結論、Unit_09 作業範圍與 README 矛盾）已修正。
