# 來源：色彩系統 — Material Design 3 與 WCAG 對比度

> 整理自 Material Design 3 官方文件與 WCAG／WebAIM 官方文件，僅擷取與課程相關的內容，供 Unit 05 教材撰寫依據。存取日期：2026-08-29。

## 色彩角色（Color Roles）

來源：[Color roles – Material Design 3](https://m3.material.io/styles/color/roles)

Material Design 3 用「色彩角色」取代「固定色票」——每個角色有明確的用途，不是單純的一組顏色。核心角色（約佔介面 90% 用色）：

| 角色 | 用途 |
| --- | --- |
| Primary / On Primary | 主品牌色與其對比色。Primary 用在關鍵動作與高強調元素；On Primary 是疊在 Primary 上的文字／圖示顏色，確保可讀對比 |
| Primary Container | Primary 的淺色（深色模式下較暗）版本，用在強調程度較低的元件，例如填色按鈕（filled tonal button）、被選取的狀態 |
| Secondary / Tertiary | 輔助色與第三強調色。Secondary 用在次要動作、Chip 等較不顯眼的元件；Tertiary 提供第三種強調色，用來做視覺平衡與對比重點 |
| Surface / On Surface | Surface 是卡片、Sheet、選單等元件的背景色；On Surface 是疊在 Surface 上的文字與圖示 |
| Surface Variant / On Surface Variant | Surface 的替代版本，用於需要輕微區隔但仍屬同一層級的區塊；On Surface Variant 是強調程度較低的文字 |
| Outline | 用在邊框與分隔線 |
| Error / On Error | 錯誤狀態的顏色與其對比色 |

**「On-」命名慣例：**角色名稱前綴 On 的顏色，代表疊在對應角色顏色「上面」的內容色（文字、圖示），例如 On Primary 就是疊在 Primary 背景上的文字顏色——這個配對關係本身就是為了確保對比度足夠、內容看得清楚。

## 怎麼選色彩方案

來源：[Choosing a color scheme – Material Design 3](https://m3.material.io/styles/color/choosing-a-scheme)

一個色彩方案（color scheme）描述一個產品在亮／暗兩種主題下的所有顏色、色彩角色與彼此的關係。

- Material 3 的作法是從**單一來源色（source color／seed color，通常是品牌色）**，用演算法自動生成一整套跟色彩角色一一對應的完整色階（primary、secondary、tertiary、neutral、error 各自的色階），不用逐一手動挑幾十種顏色深淺。
- 來源色的選擇建議「不要太飽和，也不要太灰」——Material 3 的演算法在中等飽和度的顏色上效果最好。
- 來源色可以直接用官方基準色，也可以自訂品牌色，或依使用者產生的內容／情境動態決定。

## WCAG 對比度門檻

來源：[Understanding Success Criterion 1.4.3: Contrast (Minimum) – W3C WAI](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum)、[WebAIM: Contrast and Color Accessibility](https://webaim.org/articles/contrast/)

- **一般文字（18pt 以下，或 14pt 以下的粗體）**：對比度至少 **4.5:1**。
- **大字級文字（18pt 以上，或 14pt 以上的粗體）**：對比度至少 **3:1**。
- 更高標準的 WCAG AAA 等級：一般文字要達 7:1，大字級要達 4.5:1。
- 這個門檻不是隨便訂的：研究顯示視力約 20/40（常見的視力障礙門檻）的使用者，大約需要這個對比度才能舒適閱讀文字。
- 例外：純裝飾用、不會顯示給任何人看的文字、圖片裡含大量其他視覺內容的文字，以及品牌 Logo／商標文字，不受這個門檻限制。
