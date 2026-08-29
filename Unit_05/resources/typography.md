# 來源：文字系統 — Material Design 3 Type Scale

> 整理自 Material Design 3 官方文件，僅擷取與課程相關的內容，供 Unit 05 教材撰寫依據。存取日期：2026-08-29。

## Type Scale 是什麼

來源：[Typography – Material Design 3](https://m3.material.io/styles/typography/type-scale-tokens)

Type Scale（字級量表）是一組可以在整個產品裡重複使用的字體樣式，提供足夠的風格彈性去對應不同的用途，同時維持一致、容易辨識的風格。Material Design 3 把 Type Scale 組織成 **5 組角色**，每組再分 **Large／Medium／Small** 三個級別：

| 角色組 | 用途 |
| --- | --- |
| Display | 畫面上最大的文字，保留給簡短、重要的文字或數字使用 |
| Headline | 中等大小，用在區塊標題、次標題，建立在 Display 之下的視覺層級 |
| Title | 比 Headline 小，常用在 Card、對話框裡的內容標題，提供次級結構 |
| Body | 標準內文字級，用在較長的段落與主要內容，確保段落閱讀的可讀性 |
| Label | 最小的角色，用在圖片標註，以及按鈕、分頁標籤這類重要介面元素上的文字 |

## 每個 Token 記錄的四個屬性

每一個 Type Scale 的 Token（例如 Body Large、Label Small）都同時記錄四項屬性：

- **Font size（字級）**：文字的視覺大小。
- **Line height（行高）**：確保可讀性的垂直間距。
- **Font weight（字重）**：文字的粗細與強調程度（Regular、Medium 等）。
- **Letter spacing / Tracking（字距）**：調整字元密度的水平間距。

一套 Type Scale 訂好之後，設計時只要從 15 個 Token 裡挑對應角色使用，不用每個畫面各自決定字級——這是維持整個產品文字風格一致的關鍵做法。
