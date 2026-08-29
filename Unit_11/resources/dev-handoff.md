# 來源：與工程師協作 — Figma Dev Mode 與交接文件

> 整理自 Figma 官方文件，僅擷取與課程相關的內容，供 Unit 11 教材撰寫依據。存取日期：2026-08-29。

## Dev Mode 是什麼

來源：[Guide to Dev Mode – Figma Learn](https://help.figma.com/hc/en-us/articles/15023124644247-Guide-to-Dev-Mode)

Dev Mode 是「一個以開發者為中心的介面，用來檢視與瀏覽設計」，讓設計師與開發者能順暢協作。提供進階的檢視工具、程式碼產生、版本比較與整合功能，簡化交接流程。

**開啟方式：** 打開一份 Figma Design 檔案，點工具列上的 Dev Mode 切換鈕，或按快捷鍵 **Shift + D**。同樣的快捷鍵可以切回 Design 模式。

**Ready for dev 狀態：** 標示某個 Component、Frame 或 Section 已經準備好交給開發者實作。設計師標記這個狀態後，會出現在 Dev Mode 的導覽面板裡。Organization／Enterprise 方案還多一個「Completed」狀態可以追蹤進度。

**Dev Mode 提供給開發者的資訊：**

| 項目 | 內容 |
| --- | --- |
| 程式碼片段 | 多種語言的程式碼片段，可透過外掛（如 Tailwind、React）自訂輸出格式 |
| 圖層屬性 | 版面、間距、顏色、互動設定 |
| 測量與標註 | 間距與尺寸的視覺化標示 |
| 可下載素材 | 自動偵測的圖示、圖片、影片 |
| 元件中繼資料 | Variant、屬性，可以直接互動測試 |
| 設計變更 | 版本歷史比對 |
| 外部資源連結 | 可連到 GitHub、Jira、Storybook、VS Code |

## 好的交接長什麼樣

來源：[Guide to developer handoff in Figma](https://www.figma.com/best-practices/guide-to-developer-handoff/)

**把開發者當協作夥伴，不是流程最後才收到檔案的人。** Dropbox、Expedia、Cash App 等團隊的做法顯示，及早分享檔案、保持設計過程透明、讓開發者看得到迭代過程（不是只看最終畫面），是建立設計師與工程師互信的關鍵。

**交接前，設計師要準備的事：**

- 用 Emoji 標示頁面狀態（例如 🏗️ 施工中、💭 待討論、🚢 可上線），讓人一眼看出哪些設計還在改、哪些已經定案。
- 幫關鍵 Frame 設定自訂縮圖，在檔案瀏覽時提供視覺線索。
- 把最終設計做成 Component Instance，放在乾淨、整理過的頁面，跟散亂的工作區分開。
- 把 Component 完整記錄：名稱、說明、使用方式、Variant 都要寫清楚。
- 建立跟程式碼庫慣例一致、命名良好的 Style 與 Variable。
- 主元件旁邊附說明 Frame，讓開發者可以直接參考。
- Component 的說明欄位裡加無障礙注意事項與相關連結。
- 確保開發者能存取包含所有主元件的設計系統資料庫。

**跟工程師溝通的做法：**

- **邀請開發者以 Viewer 身分加入檔案**（免費、不需要付費授權），讓他們可以檢視、匯出素材、看程式碼、留言。
- **提供有脈絡的說明文件，而不是傳統的紅線標註稿。** 分享問題定義、研究過程、迭代決策的敘事脈絡；用 Code Panel 顯示 CSS、iOS、Android 的程式碼片段搭配元件細節。
- **鼓勵早期協作。** 讓開發者在設計還在進行時就加入檔案，能持續提問、給回饋，而不是等做完才發現問題，可以減少交接時的意外狀況。
