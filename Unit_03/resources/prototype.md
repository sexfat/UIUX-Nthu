# 來源：Figma 官方文件 — Prototype

> 整理自 Figma Help Center 官方文件，僅擷取與課程相關的內容，供 Unit 03 教材撰寫依據。存取日期：2026-08-29。

## Prototype 是什麼

來源：[Guide to prototyping in Figma](https://help.figma.com/hc/en-us/articles/360040314193-Guide-to-prototyping-in-Figma)、[FD4B: Prototyping fundamentals](https://help.figma.com/hc/en-us/articles/31010011820311-FD4B-Prototyping-fundamentals)

Prototype（原型）讓設計者「建立互動流程，模擬使用者可能如何跟設計互動」——在真正開發之前，就能預覽互動、分享想法、蒐集回饋、測試體驗。

- Figma 檔案裡有 **Design** 與 **Prototype** 兩個分頁，可用快捷鍵 `Shift + E` 快速切換：Design 分頁做視覺設計，Prototype 分頁設定互動。
- **Flow（流程）** 指的是「同一個頁面裡，Frame 與連接線組成的網絡」；一個檔案可以有多個 Flow，對應不同的使用者旅程（例如註冊流程、購物車流程、結帳流程各自是一條 Flow）。
- 每條 Flow 需要一個起點：可以手動指定，或者加上第一條連接線時 Figma 會自動建立。

## 端到端流程

1. 在畫面之間建立連接（選一個熱區／物件，拖曳到目標畫面）。
2. 在 Prototype 分頁設定互動（Trigger／Action）與動畫效果。
3. 設定 Prototype 的整體設定（裝置外框、背景色、起始畫面）。
4. 用 Preview 預覽並測試互動流程。
5. 分享整個 Prototype，或分享特定 Flow 的起點連結給他人測試。

## 建立連接（Connect）的步驟

來源：[Connect your prototype](https://help.figma.com/hc/en-us/articles/360040315773-Connect-your-prototype)

1. 切到右側面板的 **Prototype** 分頁。
2. 選取要當作起點的物件（熱區）。
3. 拖曳物件邊緣出現的「＋」到目標 Frame，或在 Interactions 區塊點 **Add**。
4. 在互動細節面板設定 Trigger／Action／Destination。
5. 關掉面板即完成這條連接。

也可以一次選多個物件，把「＋」拖到同一個目標 Frame，批次建立相同的連接。

## Trigger／Action／Destination

- **Trigger（觸發條件）：** 引發互動的事件，例如 On click（點擊）、While hovering（滑鼠停留）、After delay（延遲後）、When video ends（影片播放結束）。同一個物件可以同時有多個 Key/Gamepad、On drag 或 When video hits 類型的觸發條件。
- **Action（動作）：** 觸發後發生的事，例如跳到另一個 Frame、開啟 Overlay（疊加視窗）、播放影片。
- **Destination（目的地）：** 連接線的終點，大多數情況下必須是「最上層的 Frame」。

## 動畫與轉場設定

互動細節面板裡可以設定：

- **動畫類型：** Push（推移）、Slide（滑入）、Dissolve（淡入淡出）等。
- **方向：** 左／右／上／下（依動畫類型而定）。
- **Smart Animate：** 自動對「兩個畫面裡同名的圖層」做轉場動畫（例如按鈕從左邊移到右邊時，會自動產生移動動畫）。
- **Easing／Spring：** 控制轉場的加速曲線。
- **Duration（時長）：** 可設定 1–10,000 毫秒。

設定完成後可以直接在面板裡預覽動畫效果，再決定是否套用。
