# 來源：Figma 官方文件 — Auto Layout

> 整理自 Figma Help Center 官方文件，僅擷取與課程相關的內容，供 Unit 03 教材撰寫依據。存取日期：2026-08-29。

## 什麼是 Auto Layout、為什麼要用

來源：[Guide to auto layout](https://help.figma.com/hc/en-us/articles/360040451373-Guide-to-auto-layout)

Auto Layout 讓 Frame 裡的元素「根據方向、間距、留白、對齊等屬性自動排列」——內容一旦變動，版面會自動跟著調整，不用手動重新排位置。

**適合使用的情境：** 文字長度會變的按鈕、項目數量會增減的清單、儀表板，以及要支援多種螢幕尺寸的網頁。

## 關鍵屬性

| 屬性 | 說明 |
| --- | --- |
| **Flow 方向** | Vertical（沿 y 軸排列）／Horizontal（沿 x 軸排列，可選是否換行）／Grid（用欄與列排成網格） |
| **Padding（留白）** | Frame 邊界與內容之間的空白 |
| **Gap（間距）** | 物件與物件之間的距離，可以是固定值，也可以用 Between／Around／Evenly 等自動間距模式 |
| **Alignment（對齊）** | 決定物件在 Frame 裡的對齊方式 |
| **Resizing（縮放行為）** | Hug contents（依內容縮到最小）／Fill container（撐滿父層可用空間）／Fixed（固定尺寸不變）／可設定 min/max 限制範圍 |

還可以針對個別物件開啟「Ignore auto layout」，讓它跳出自動排列邏輯、改用絕對定位（例如浮動的角標）。

## 怎麼加上 Auto Layout

來源：[Toggle on auto layout in designs](https://help.figma.com/hc/en-us/articles/5731482952599-Toggle-on-auto-layout-in-designs)

1. 選取一個或多個圖層。
2. 三種方式都可以觸發：按快捷鍵 `Shift + A`／點右側面板 Auto Layout 旁的加號／右鍵選單選 Add auto layout。
3. Auto Layout **只作用在 Frame 上**——如果選取的是一般圖層（不是 Frame），Figma 會自動在外面包一層 Auto Layout Frame。
4. 如果選取的是 Frame 或 Main Component，可以直接選擇 Flow 類型：Vertical／Horizontal／Grid。
5. 加上後，右側面板會顯示可調整的排版屬性與對齊設定。

**批次判斷：** 面對複雜版面，可以用 `Control + Shift + A`（Mac）或 `Control + Alt + Shift + A`（Windows）讓 Figma 自動判斷合適的 Auto Layout 結構，之後再手動微調。

**移除 Auto Layout：** 點選 Freeform，或按 `Option + Shift + A`（Mac）／`Alt + Shift + A`（Windows），會還原成一般 Frame。

## 跟手動排版的差別

手動排版時，內容一變動就要重新調整每個元素的位置；Auto Layout 設定好方向、間距、留白、縮放行為後，內容變動時所有元素會依照這些規則自動同步調整位置，省下大量重新對齊的時間，也是讓設計稿更接近「可用元件」的第一步。
