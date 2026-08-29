# 來源：Figma 官方文件 — Component 與 Variants

> 整理自 Figma Help Center 官方文件，僅擷取與課程相關的內容，供 Unit 03 教材撰寫依據。存取日期：2026-08-29。

## Main Component 與 Instance

來源：[Components collection: Overview](https://help.figma.com/hc/en-us/articles/39719619313047-Components-collection-Overview)、[Apply changes to instances](https://help.figma.com/hc/en-us/articles/360039150733-Apply-changes-to-instances)

- **Main Component（主元件）** 定義這個元素的所有屬性；**Instance（實體）** 是主元件的副本，可以在設計裡重複使用。
- 修改 Instance 時可以調整文字、填色、描邊、效果等屬性，讓它符合當下的使用情境，或用來嘗試不同的設計變化。
- **不能**修改 Instance 的底層結構——不能覆寫元件內圖層的堆疊順序（z-index），也不能移動元件內圖層的位置。
- **Push overrides to main component**：可以把對 Instance 做的修改「推回」主元件，這樣同一個主元件底下的其他 Instance 也會一併更新。但這個功能只在主元件與 Instance 位於同一個檔案時才能使用。

## Variants 與 Component Set

來源：[Create and use variants](https://help.figma.com/hc/en-us/articles/360056440594-Create-and-use-variants)

- **Variant（變體）** 是同一個元件的不同版本，彼此之間有可預期的差異（例如按鈕的大小、狀態）。
- 多個 Variant 會被收進一個 **Component Set（元件集）** 容器，方便管理與尋找。
- Variant 用「屬性（Property）」與「數值（Value）」定義差異：屬性代表可變動的面向（例如 Size、State），數值是每個屬性底下的具體選項。每個 Variant 必須是屬性數值的唯一組合。

**把多個 Component 合併成 Variants：**
1. 選取多個 Component。
2. 在右側面板點 **Combine as variants**。
3. Figma 會把它們整合進同一個 Component Set。
4. Figma 預設會把屬性命名成 Variant、Property 2、Property 3 等通用名稱，**要自己重新命名成有意義的名稱**（例如 Type、Size、State）。

**命名慣例範例（按鈕元件）：** `Button/Primary/Large/Default/False`，代表 Component Set 名稱是 Button，底下有 Type（Primary）、Size（Large）、State（Default）、Icon（False）等屬性。這種命名法讓團隊可以透過同一個資產、切換不同屬性組合，取得需要的按鈕版本。

**設計原則：** 建議用「獨立、命名清楚的屬性」控制單一面向的差異，而不是用一個「Style」屬性同時控制多個變化（例如不要用一個屬性值「Primary Large」，而是拆成 Type=Primary、Size=Large 兩個獨立屬性），這樣使用者才能自由混搭組合。
