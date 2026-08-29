# 來源：Figma 官方文件 — 形狀與圖層

> 整理自 Figma Help Center 官方文件，僅擷取與課程相關的內容，供 Unit 03 教材撰寫依據。存取日期：2026-08-29。

## 形狀工具（Shape tools）

來源：[Shape tools – Figma Learn](https://help.figma.com/hc/en-us/articles/360040450133-Shape-tools)、[Layers 101: Explore layer types](https://help.figma.com/hc/en-us/articles/26620239826199-Layers-101-Explore-layer-types)

Figma 提供六種基本形狀工具，是大多數畫面裡「非文字」圖層的來源：

| 工具 | 快捷鍵 | 說明 |
| --- | --- | --- |
| Rectangle（矩形） | `R` | 畫矩形或正方形 |
| Line（線段） | `L` | 畫任意方向的直線 |
| Arrow（箭頭） | `Shift + L` | 畫單向或雙向箭頭 |
| Ellipse（橢圓） | `O` | 畫橢圓或正圓 |
| Polygon（多邊形） | — | 預設三角形，可調整邊數 |
| Star（星形） | — | 預設五角星，可調整角數 |

操作方式一致：從工具列選工具 → 在畫布上點擊拖曳 → 拖曳時畫面會即時顯示尺寸。

**修飾鍵：**
- 拖曳時按住 `Shift`：畫出正方形、正圓、正多邊形（等比例）。
- 拖曳時按住 `Option/Alt`：從中心點開始畫圖形／縮放。
- 兩者可以同時按住。

**編輯形狀屬性：**
- 矩形有專屬的圓角控制點，可直接在畫布上拖曳調整圓角（corner radius）。
- 線段與箭頭可在右側面板調整描邊（stroke）顏色、粗細、樣式，也可以設定虛線的長度與間距。
- 所有形狀都能在右側面板調整 Fill（填色）與 Stroke（描邊）。
- 多邊形／星形的邊數／角數，在右側 Appearance 區塊的 Count 欄位調整。

**Image／影像：** 圖片、GIF、影片不是獨立的圖層類型，而是「填色（fill）」的一種——只要圖層支援 fill 屬性，就能用拖放或貼上的方式把影像加進去。

## 圖層（Layers）基礎

來源：[Layers 101: Get started with layers](https://help.figma.com/hc/en-us/articles/26584819173271-Layers-101-Get-started-with-layers)、[Layers 101: Explore layer types](https://help.figma.com/hc/en-us/articles/26620239826199-Layers-101-Explore-layer-types)

- 一份設計通常是形狀、文字與其他圖層的組合，這些圖層可以在畫布上互相堆疊，同時仍然可以被個別編輯。
- **圖層順序（layer order）決定畫布上的堆疊關係**：圖層面板裡「排在上面」的圖層，在畫布上會蓋在「排在下面」的圖層上方。
- 每個圖層都有對應屬性：位置（X/Y 座標）、尺寸（寬高），以及外觀相關的顏色、描邊、效果（如陰影、模糊）。這些屬性顯示在右側面板，內容依圖層類型而不同。

**主要圖層類型：**

| 類型 | 說明 |
| --- | --- |
| Frame（框架） | 最基礎的容器，用來組織物件與畫面；有明確的寬高與屬性，是 Component、Auto Layout、Prototype 這些功能的基礎。內建裝置尺寸預設（如 iPhone、Apple Watch）與常用素材尺寸。 |
| Text（文字） | 用 Text 工具建立，可在 Typography 區塊調整字體樣式，內建數百款免費 Google 字體，也可加自訂字體。 |
| Shape（形狀） | 矩形、橢圓、多邊形等；Pen 工具可畫線條與自訂插畫。 |
| Image（影像） | 以 fill（填色）的形式存在，不是獨立圖層類型。 |

> 官方文件提到圖層類型「還有更多可以探索」（如 Group、Component、Instance），但這篇入門文章沒有展開說明；Group 與 Frame 的差異、Component／Instance 的細節見本資料夾其他來源檔案（`components-variants.md`）與 Figma 產品內的實際操作。
