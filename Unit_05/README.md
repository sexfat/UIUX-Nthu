# 單元 5：產品設計基本元素

> 對應清華大學課程時段：10/14（三）13:20–16:20

## 相關檔案

- `slides.html` — 課堂簡報（19 張）。
- `article.html` — 完整教材（12 節，含 AI 協作提示詞）。
- `exercises.html` — 課堂練習（4 階段，80 分鐘）與回家作業。
- `resources/color.md`、`typography.md`、`icons.md`、`buttons.md` — Material Design 3、WCAG、NN/g、Figma、Apple HIG 官方文件的中文整理，本單元教材的溯源依據。
- `resources/figma-demo/` — 教材裡引用的 4 張示範截圖（色彩角色、Type Scale、Icon 尺寸對照、按鈕狀態），取自示範用 Figma 檔案：[Unit03 Figma 基本操作示範](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0)（與 Unit 03 共用同一個示範檔）。
- 課堂範本檔：[Unit 05 練習範本（Figma）](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0?node-id=4-2)（同一份檔案的另一個頁面）——① 5 張空白色票卡 ② Type Scale 角色標籤骨架 ③ Icon 對齊骨架 ④ Enabled 按鈕起始 Component，各對應課堂練習一個階段；學生複製區塊到自己的檔案操作。
- `../Unit_09/tools-stark-material.html` — Material Theme Builder 外掛操作指南，Exercise 01 產生色階時使用。

## 單元目標

- 能用色彩角色系統（Primary、Secondary、Surface、Error 等）決定畫面用色，而不是隨手挑顏色。
- 能用線上工具實測文字對比度，達到 WCAG AA 最低門檻（一般文字 4.5:1）。
- 能用 Type Scale 的五組角色管理畫面上的字級層級。
- 能做出符合尺寸與對齊準則的 Icon，並判斷裝飾用與資訊用 Icon 的差異。
- 能設計按鈕的五個核心狀態（Enabled、Hover、Pressed、Focus、Disabled），並用 Figma Variants 組織。

## 課程介紹

Unit 03 學會了怎麼在 Figma 裡操作，這堂課換內容：顏色、文字、Icon、按鈕這四樣東西，要怎麼決定規則，而不是每次畫畫面都重新選一次。色彩角色系統讓「這個顏色用在哪裡」有明確答案；Type Scale 讓字級不用每頁重新猜；Icon 有尺寸與對齊的準則；按鈕要設計的不只一個樣子，是五種狀態。這四件事定好之後，會變成整個專題重複使用的規範，Unit 06 開始畫真的介面時直接套用。

Unit 05 原本完全沒有來源素材，內容依據改以 Material Design 3、WCAG、NN/g、Figma、Apple HIG 等公認的官方設計系統文件整理（見 `resources/`），並用實際建立的 Figma 示範檔截圖取代手繪示意圖。

## 課程內容

- 色彩角色系統：Primary／Secondary／Tertiary／Surface／Error 等角色與 On 色配對慣例。
- 怎麼選色彩方案：來源色（seed color）與自動產色。
- WCAG 對比度門檻：4.5:1／3:1／7:1 三個等級。
- Type Scale：Display／Headline／Title／Body／Label 五組角色，字級／行高／字重／字距四項屬性。
- Icon 設計原則、標準尺寸（20/24/40/48dp）與跟文字搭配的基準線位移。
- 按鈕五個狀態：Enabled、Hover、Pressed、Focus、Disabled，以及標籤文字寫法。
- 在 Figma 裡怎麼組織：Component Variants + Prototype Trigger + Smart Animate。

## 課堂練習

**四個規範疊上去，做出一份風格小卡**（80 分鐘，個人，Figma，延續 Unit 03 的檔案）

1. Exercise 01（20 分）— 色彩角色卡：用 Material Theme Builder 產色階，推出 5 組角色配對並實測對比度。
2. Exercise 02（20 分）— Type Scale：把卡片的標題、副標換成套用正確角色的版本。
3. Exercise 03（20 分）— Icon 對齊：兩組 Icon＋文字做基準線位移。
4. Exercise 04（20 分）— 按鈕 5 狀態：擴充 Unit 03 的按鈕成 5 個 State 的 Component Set。

### 三小時時間分配

| 段落 | 時間 | 內容 |
| :--- | :--- | :--- |
| Part 1 | 40 分 | 顏色與文字概念與示範 |
| Part 2 | 40 分 | Icon 與按鈕概念與示範 |
| 休息 | 10 分 | |
| Part 3 | 80 分 | 課堂練習四階段 |
| Part 4 | 10 分 | 成果分享 |

講述 80 分 + 實作與分享 90 分 + 休息 10 分 = 180 分。

## 回家作業

**擴充成一頁風格指南**

1. 把 5 組「背景／On」色彩角色配對擴充到 7 組以上，加上 Outline 一項功能角色。
2. 補上 Display 角色，整理成完整的 Type Scale 對照表（含字級／行高／字重／字距）。
3. 把風格指南套用在一個真實畫面上，全部文字與顏色都要能指回今天定義的角色。

配分：色彩角色 25、Type Scale 20、真實畫面套用 40、按鈕 Component 15，各項的「通過的樣子」與「不及格的樣子」寫在 `exercises.html#submit`。

## 對應清大日期與時段

- 10/14（三）13:20–16:20

## 本單元產出

- 一份含色彩角色、Type Scale、Icon、按鈕 5 狀態規範，並套用在真實畫面上的 Figma 風格指南。

## 參考資料

- [Color roles](https://m3.material.io/styles/color/roles) — Material Design 3。
- [Choosing a color scheme](https://m3.material.io/styles/color/choosing-a-scheme) — Material Design 3。
- [Understanding Success Criterion 1.4.3: Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum) — W3C WAI。
- [WebAIM: Contrast and Color Accessibility](https://webaim.org/articles/contrast/) — WebAIM。
- [Typography · Type scale tokens](https://m3.material.io/styles/typography/type-scale-tokens) — Material Design 3。
- [Designing icons](https://m3.material.io/styles/icons/designing-icons) — Material Design 3。
- [Button States: Communicate Interaction](https://www.nngroup.com/articles/button-states-communicate-interaction/) — NN/g。
- [Understanding Button States in UI Design](https://www.figma.com/resource-library/button-states/) — Figma。
- [Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons) — Apple Human Interface Guidelines。
- 舊版課綱備查〈介面視覺基礎：版面、排版、色彩與一致性〉，見 `../舊版課綱備查.md`——主題方向參考，非教材內容來源。

## 備註

- 內容經 Codex 內容審查一輪，修正 6 項確定錯誤（把示例數值當成硬性規則、Type Scale 被簡化成單一字級排序、對比度不足的錯誤歸因、Outline 被誤當成需要 On 色配對的角色、簡報與練習交件數量不一致、AI 提示詞問題過度泛化）與 1 項教學設計缺口（Exercise 01 缺少可執行的產色方法，補上 Material Theme Builder 指引）。
