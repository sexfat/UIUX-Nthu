# [SPEC] Unit 01「UX 5層架構」層級詳情彈窗

- **日期**：2026-09-02
- **負責人**：bryant_huang
- **狀態**：done
- **變更紀錄**：[docs/changelog/unit01-layer-modal.md](../changelog/unit01-layer-modal.md)

---

## 背景

Unit 01 簡報的 UX 5 層架構（Jesse James Garrett 的 Elements of UX 五層模型）只用金字塔圖與每張單層說明頁列出關鍵字（例如「商業目標」「使用者需求」），沒有說明每一層實際要產出什麼文件、產出的文件長什麼樣子。使用者希望補上這段說明，並用彈窗（modal）呈現，避免把簡報塞得更長。

## 功能說明

- Slide 4 的 UX 5 層金字塔，每一列都可以點擊，點下去會開啟彈窗，顯示該層的說明、目標產出文件、範例。
- Slide 5～9（策略層～表現層各自的單層說明頁）各新增一個「查看目標文件與範例」按鈕，功能與內容跟金字塔列的彈窗完全相同（同一層對應同一份內容）。
- 彈窗內容分四段：層級標籤（Layer N · 英文名）、標題與副標、一段說明文字、「目標文件」清單、「範例」段落。
- 範例主要對應課程本身既有的真實產出，不舉外部案例：
  - 策略層 → Unit 02（訪談洞察筆記、Persona），另補一段生活化情境（麥當勞推出手機點餐、到店取餐服務）幫助理解「為什麼做、做給誰」兩個問題
  - 範圍層 / 結構層 / 骨架層 → Unit 04（Functional Map、資訊架構圖、Flowchart、Wireframe）
  - 表現層 → Unit 05（色彩字體規範）、Unit 09（Design System 元件規範文件）
- 彈窗可用右上角 ✕、點擊背景遮罩、或按 Escape 關閉；彈窗開啟時，方向鍵／空白鍵不會誤觸簡報翻頁。
- 淺色與深色（`.slide.dark`）投影片上的觸發按鈕都有對應樣式，彈窗本身固定使用淺色卡片（跟 Unit_09 既有彈窗一致），確保內文在任何背景下都易讀。

## 實作範圍

- `.layer-detail-btn`、`.layer-modal-overlay`、`.layer-modal` 系列 CSS（含 hover、深色頁變體、手機版 `max-height` 調整）。
- Slide 4 金字塔列從 `<div class="pyr-row">` 改為 `<button type="button" class="pyr-row" data-layer="N">`。
- Slide 5–9 各新增一個 `<button class="layer-detail-btn" data-layer="N">查看目標文件與範例</button>`。
- 共用彈窗 HTML 容器（`#layerModalOverlay`）。
- JS：`layerData`（1–5 層的標題／副標／說明／文件清單／範例）、`openLayerModal`／`closeLayerModal`、觸發點事件綁定、Escape 監聽、既有翻頁 keydown handler 加上彈窗開啟時的判斷式。

## 不在範圍內

- 未把 Unit_01 整份簡報改成標準化版型（Unit 03/05/07/09/11 使用的通用 CSS/JS 架構）——這份簡報沿用它原本就有的獨立架構，只在既有架構內新增彈窗功能。
- 未修改 Slide 3 之外的課程大綱敘述、未調整第 1／2 小時的內容分配。

## 驗收條件

- [x] Slide 4 金字塔每一列點擊都能開啟對應層級的彈窗，內容正確且不重複。
- [x] Slide 5–9 各自的「查看目標文件與範例」按鈕開啟的彈窗內容，跟金字塔對應列一致。
- [x] 深色投影片（Slide 5、7、9）上的觸發按鈕清楚可見、可點擊。
- [x] 彈窗可用 ✕、點擊背景、Escape 三種方式關閉；彈窗開啟時方向鍵／空白鍵不會切換投影片。
- [x] 手機寬度（`max-width: 768px`）下彈窗高度與內距有對應調整，不會被截斷。
