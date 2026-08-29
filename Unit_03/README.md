# 單元 3：Figma 基本操作

> 對應清華大學課程時段：9/30（三）13:20–16:20

## 相關檔案

- `slides.html` — 課堂簡報（20 張）。
- `article.html` — 完整教材（11 節，含 AI 協作提示詞）。
- `exercises.html` — 課堂練習（4 階段，70 分鐘）與回家作業。
- `resources/shapes-layers.md`、`auto-layout.md`、`components-variants.md`、`prototype.md` — Figma 官方文件的中文整理，本單元教材的溯源依據。
- `resources/figma-demo/` — 教材裡引用的 4 張示範截圖（形狀與圖層、Auto Layout 前後對照、Component 與 Variants、Prototype 連接示意），取自示範用 Figma 檔案：[Unit03 Figma 基本操作示範](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0)。
- 課堂範本檔：[Unit 03 練習範本（Figma）](https://www.figma.com/design/UxS7TVst4TOjqktZUMc4m0?node-id=4-8)（同一份檔案的另一個頁面）——① 形狀與圖層起始畫布 ② Auto Layout 手動排版錯誤示範 ③ 尚未 Component 化的按鈕 ④ 列表頁／詳細頁空白手機畫面，各對應課堂練習一個階段；學生複製區塊到自己的檔案操作。

## 單元目標

- 能用六種形狀工具畫出基本圖層，並理解圖層堆疊順序如何決定畫面的遮擋關係。
- 能幫版面加上 Auto Layout，並正確設定 Padding、Gap、Alignment、Resizing 四個屬性。
- 能把重複使用的元素做成 Component，並用 Combine as variants 建立命名清楚的 Variant。
- 能用 Prototype 把兩個以上的畫面接成可以點擊測試的原型，說得出 Trigger／Action／Destination 的差異。

## 課程介紹

Unit 01–02 把使用者、問題、旅程想清楚了，這堂課換工具：把想法變成一份能在 Figma 裡打開、點得動的檔案。四件事疊起來講——形狀與圖層是最基本的畫面素材，Auto Layout 讓版面跟著內容自動調整，Component 與 Variants 讓重複的元素只需要維護一份，Prototype 把靜態畫面接成可以點擊測試的原型。這四件事是 Unit 04 開始畫 Wireframe、建立設計元件、做互動原型的地基。

內容全部依據 Figma 官方 Help Center 文件整理（見 `resources/`），並用實際建立的 Figma 示範檔截圖取代手繪示意圖。

## 課程內容

- 形狀工具（矩形／線段／箭頭／橢圓／多邊形／星形）與圖層堆疊順序。
- Frame：Auto Layout、Component、Prototype 三個功能的地基。
- Auto Layout：加上的三種方式、四個關鍵屬性（Padding、Gap、Alignment、Resizing）。
- Component 與 Instance：可以改與不能改的部分。
- Variants 與 Component Set：合併步驟、屬性命名慣例。
- Prototype：Flow、Design／Prototype 分頁切換、建立連接的步驟。
- 連接的三要件：Trigger、Action、Destination，以及動畫與轉場設定。

## 課堂練習

**四個功能疊上去，做出一張真的卡片**（70 分鐘，個人，Figma）

1. Exercise 01（15 分）— 形狀與圖層：畫出一張卡片（照片、頭像、標題、副標 4 個圖層）。
2. Exercise 02（15 分）— Auto Layout：幫卡片加上一排會自動撐開、換行的標籤。
3. Exercise 03（20 分）— Component：把按鈕做成 Component，合併出 2 個命名清楚的 Variant。
4. Exercise 04（20 分）— Prototype：把列表頁與詳細頁接成一次可以點的互動。

### 三小時時間分配

| 段落 | 時間 | 內容 |
| :--- | :--- | :--- |
| Part 1 | 45 分 | 形狀、圖層與 Auto Layout 概念與示範 |
| Part 2 | 45 分 | Component、Variants 與 Prototype 概念與示範 |
| 休息 | 10 分 | |
| Part 3 | 70 分 | 課堂練習四階段 |
| Part 4 | 10 分 | 成果分享 |

講述 90 分 + 實作與分享 80 分 + 休息 10 分 = 180 分。

## 回家作業

**擴充成小型元件庫**

1. 再做 1 個 Component，跟課堂的按鈕湊成 2 個，至少 1 個要有 2 個以上的 Variant。
2. 用 Auto Layout 重排整張卡片，同時用 Ignore auto layout 保留頭像疊在照片上的效果。
3. 串成至少 3 個畫面的 Prototype Flow，含返回連接。
4. （加分，非必要）至少 1 個轉場改用 Smart Animate。

配分：Component 與 Variants 35、Auto Layout 35、Prototype 30，Smart Animate 加分 +5，各項的「通過的樣子」與「不及格的樣子」寫在 `exercises.html#submit`。

## 對應清大日期與時段

- 9/30（三）13:20–16:20

## 本單元產出

- 一張含 Component、Variants、Auto Layout 與 Prototype 連接的 Figma 檔案。

## 參考資料

- [Shape tools](https://help.figma.com/hc/en-us/articles/360040450133-Shape-tools) — Figma Help Center。
- [Layers 101: Get started with layers](https://help.figma.com/hc/en-us/articles/26584819173271-Layers-101-Get-started-with-layers) — Figma Help Center。
- [Layers 101: Explore layer types](https://help.figma.com/hc/en-us/articles/26620239826199-Layers-101-Explore-layer-types) — Figma Help Center。
- [Guide to auto layout](https://help.figma.com/hc/en-us/articles/360040451373-Guide-to-auto-layout) — Figma Help Center。
- [Toggle on auto layout in designs](https://help.figma.com/hc/en-us/articles/5731482952599-Toggle-on-auto-layout-in-designs) — Figma Help Center。
- [Components collection: Overview](https://help.figma.com/hc/en-us/articles/39719619313047-Components-collection-Overview) — Figma Help Center。
- [Apply changes to instances](https://help.figma.com/hc/en-us/articles/360039150733-Apply-changes-to-instances) — Figma Help Center。
- [Create and use variants](https://help.figma.com/hc/en-us/articles/360056440594-Create-and-use-variants) — Figma Help Center。
- [Guide to prototyping in Figma](https://help.figma.com/hc/en-us/articles/360040314193-Guide-to-prototyping-in-Figma) — Figma Help Center。
- [Connect your prototype](https://help.figma.com/hc/en-us/articles/360040315773-Connect-your-prototype) — Figma Help Center。
- 舊版課綱備查〈Figma 基礎操作與討論〉、〈Auto Layout、Constraints 與彈性版面〉，見 `../舊版課綱備查.md`——主題方向參考，非教材內容來源。

## 備註

- 內容經 Codex 內容審查一輪，修正 4 項確定錯誤（快捷鍵誤寫、過度絕對的敘述、無來源依據的除錯歸因）與 3 項教學設計缺口（Auto Layout 巢狀結構、Instance 建立步驟、頭像疊圖與 Auto Layout 衝突），並依審查建議精簡了投影片核心內容與回家作業規模。
