# 來源：按鈕設計 — 狀態、標籤與 Figma 元件規範

> 整理自 NN/g、Figma 官方資源庫與 Apple Human Interface Guidelines，僅擷取與課程相關的內容，供 Unit 05 教材撰寫依據。存取日期：2026-08-29。

## 五個核心按鈕狀態

來源：[Button States: Communicate Interaction – NN/g](https://www.nngroup.com/articles/button-states-communicate-interaction/)、[Understanding Button States in UI Design – Figma](https://www.figma.com/resource-library/button-states/)

| 狀態 | 代表意思 | 視覺處理 |
| --- | --- | --- |
| Enabled（預設） | 按鈕已準備好被點擊 | 高對比、清楚的標籤文字，一眼看出可以互動 |
| Hover | 游標移到按鈕上，確認可以點擊 | 顏色些微加深，或加陰影浮起效果 |
| Pressed / Active | 使用者正在點擊、按住的瞬間 | 顏色些微變化，常搭配輕微縮小（例如縮到 0.98 倍）模擬實體按壓的回饋 |
| Focus | 使用者用鍵盤（Tab）導覽到這個按鈕 | 需要清楚可見的外框（stroke），不能只靠顏色變化，這是無障礙的硬性要求 |
| Disabled | 這個動作目前不可用 | 降低飽和度與對比，但文字仍要維持可讀，不能整個消失 |

**回饋時機：**按下（pressed）狀態的視覺回饋要在 **100–150 毫秒**內出現，避免使用者因為看不到反應而重複點擊。

**Focus 樣式的無障礙要求：**要用外框式的焦點提示（不是只靠顏色），才能符合 WCAG 對「使用者要看得出目前選到哪個元件」的要求。

## 延伸狀態

除了上述五個核心狀態，複雜流程還會用到：

- **Loading**：顯示轉圈動畫或進度條，通常搭配降低透明度。
- **Selected / Toggled**：用在切換型按鈕（如篩選標籤），維持一種持續存在的樣式（填色或反轉配色），跟按下瞬間的 Pressed 狀態不同。

## 在 Figma 裡怎麼組織

來源：[Understanding Button States in UI Design – Figma](https://www.figma.com/resource-library/button-states/)

- 用 **Component Variants** 把同一顆按鈕的所有狀態收進同一個 Component Set，每個狀態是一個 Variant。
- 在 **Prototype 分頁**用 Trigger（例如 While hovering、Mouse down）把各個 Variant 連接起來，模擬狀態切換。
- 轉場動畫建議用 Smart Animate，時長約 150 毫秒，讓狀態切換感覺跟得上使用者的操作節奏。

## 按鈕標籤文字的寫法

來源：[Buttons – Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/buttons)

- **標籤用動詞。**具體的動作型標籤能讓使用者一眼看出這是可以互動的按鈕，也知道點下去會發生什麼事。
- **用標題大小寫（Title Case）**：除了四個字母以下的冠詞、對等連接詞、介系詞之外，每個字首都大寫。
- **標籤要簡短。**過長的文字會讓介面顯得擁擠，在較小的螢幕上還可能被截斷。
- **邊框與背景只在必要時才加。**系統按鈕預設沒有邊框或背景；某些內容區塊裡需要邊框或背景才能表達「這是可以互動的」時才加上去。
