# [SPEC] Unit 05 完整教材建置（產品設計基本元素）

- **日期**：2026-08-29
- **負責人**：bryant_huang
- **狀態**：done
- **變更紀錄**：[docs/changelog/unit05-basic-elements.md](../changelog/unit05-basic-elements.md)

---

## 背景

Unit 05（對應 10/14「產品設計基本元素」場次）在 Unit 03 完成後，是課程時程上第二迫近的教材缺口。跟 Unit 03 一樣，`Unit_05/resources/` 原本完全是空的，沒有既有課程素材可溯源。

## 功能說明

新建 Unit 05 的簡報、講義、課堂練習與作業，主題涵蓋顏色、文字、Icon、按鈕四個產品設計基本元素。因為單元本身沒有既有課程素材可溯源，改以公認的設計系統官方文件（Material Design 3、W3C WAI／WebAIM、NN/g、Figma、Apple HIG）作為內容依據，並延續 Unit 03 建立的示範用 Figma 檔案新增截圖。

## 實作範圍

- `Unit_05/resources/*.md`：4 份來源整理（色彩、文字、Icon、按鈕），逐段標明官方文件出處 URL。
- `Unit_05/resources/figma-demo/`：4 張示範截圖，取自 Unit 03 的示範用 Figma 檔案新增的 4 個畫面。
- `Unit_05/slides.html`（19 張）、`article.html`（12 節）、`exercises.html`（4 階段課堂練習 80 分鐘＋回家作業）、`README.md`：骨架沿用 Unit_08／Unit_03。
- Codex 內容審查一輪：修正 6 項確定內容錯誤、1 項教學設計缺口，並依用戶指示只採用「刪減回家作業額外 Icon 製作」一項可刪減建議。
- 收尾：`index.html` Unit 05 卡片與頁尾說明、根目錄 `README.md` 課程單元表。

## 不在範圍內

- Unit 11（No-Code 實作）教材，仍待後續處理。
- 「用色彩生成工具產生色階」這一步驟指向 `Unit_09/tools-stark-material.html` 既有的 Material Theme Builder 操作指南，未另外重寫一份。

## 驗收條件

- [x] `python3 .claude/skills/unit-materials/validate.py Unit_05` 結構檢查全綠。
- [x] 三份檔案的每個觀念都能指回 `resources/` 的來源段落。
- [x] Codex 內容審查回報的確定錯誤已全部修正。
- [x] `index.html`、根目錄 `README.md` 的收尾更新，皆先列變動清單經用戶確認後才執行。
