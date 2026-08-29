# 來源：AI 網頁生成 — Figma MCP 與 Claude Code

> 整理自 Figma 官方文件、Claude Code 官方 GitHub 說明，僅擷取與課程相關的內容，供 Unit 11 教材撰寫依據。存取日期：2026-08-29。

## Claude Code 是什麼

來源：[anthropics/claude-code – GitHub](https://github.com/anthropics/claude-code)、[Claude Code by Anthropic](https://claude.com/product/claude-code)

Claude Code 是「一個活在終端機裡的 agentic 編碼工具，能理解你的程式碼庫，透過執行例行任務、解釋複雜程式碼、處理 git 工作流程，幫你更快寫程式——全部用自然語言下指令」。

它不是一個「生成程式碼的聊天介面」，而是一個會**規劃工作、讀你的程式碼庫、跨多個目錄編輯檔案、跑測試、建立 Pull Request** 的 Agent。安裝完成後，在任何專案資料夾執行 `claude` 就能開始互動式工作階段，它會偵測專案內容並在第一次執行時要求登入驗證。

CLI 版本是功能最完整的介面——新功能最先出現在這裡，支援完整的參數集合，可以在任何終端機環境原生執行。VS Code 擴充套件、JetBrains 外掛、桌面應用程式與網頁介面都共用同一套底層引擎，所以在 CLI 裡設定的 CLAUDE.md 檔案、設定值與 MCP 伺服器，在其他介面也通用。

## Figma MCP Server：讓 Claude Code 讀懂 Figma 設計

來源：[Claude Code and Figma: Set up the MCP server – Figma Learn](https://help.figma.com/hc/en-us/articles/39888612464151-Claude-Code-and-Figma-Set-up-the-MCP-server)、[Figma MCP + Claude Code](https://www.builder.io/blog/claude-code-figma-mcp-server)

Figma MCP Server 讓 Claude Code「讀取結構化的設計脈絡——包含 Component、Variable、版面資料、FigJam 內容——並且能從選取的 Frame 產生程式碼，透過 Code Connect 讓產生的程式碼跟真正的元件保持一致」。連上之後，Claude Code 能讀到 Figma 檔案裡實際的顏色、間距、Component Variant，不需要人工把設計規格再轉譯一次成文字。

**設定步驟（Remote 版本，官方建議大多數人使用）：**

1. 在終端機執行 `claude plugin install figma@claude-plugins-official`。
2. 按 Enter，重新啟動 Claude Code。
3. 輸入 `/plugin`，切到 Installed 分頁。
4. 選取 figma 伺服器，按 Enter 進行授權登入。
5. 在跳出的外部授權頁面點「Allow access」。
6. 回到終端機再執行一次 `/plugin`，確認 figma 伺服器顯示為已連線。

**兩種主要工作方式：**

| 方式 | 做法 |
| --- | --- |
| 選取式（Selection-based） | 在 Figma 裡選取一個 Frame 或 Component，跟 Claude 說「幫這張卡片加一個按鈕」 |
| 連結式（Link-based） | 直接貼 Figma 連結，跟 Claude 說「把這個註冊卡片設計轉成程式碼：[figma 連結]」 |

**Desktop 版本（Enterprise 專用）：** 除了上面的 Remote 版本，官方文件也提到可以透過 Figma App 的 Dev Mode 啟用桌面版 MCP Server，再用 `claude mcp add` 指令，搭配本機伺服器位址設定連線——這是針對特定組織需求的選項，Remote 版本是官方建議大多數人使用的預設做法，桌面版功能更完整但僅限 Enterprise 方案。

## Gemini CLI：另一個可以做同件事的工具

來源：[google-gemini/gemini-cli – GitHub](https://github.com/google-gemini/gemini-cli)、[Gemini CLI 官方文件](https://geminicli.com/docs/)

Gemini CLI 是 Google 的開源 AI 終端機助手，把 Gemini 模型整合進命令列工作流程，讓開發者能在終端機裡自動化除錯、重構程式碼、產生測試、寫文件。以互動式的 REPL（Read-Eval-Print Loop）環境運作，內建 Google 搜尋、檔案操作、Shell 指令、網頁擷取等工具，並支援 MCP，可以用類似的方式接上其他資料來源（包含 Figma）。個人 Google 帳號的免費額度是每分鐘 60 次、每天 1,000 次請求。

清華大學課程大綱把 Claude Code 與 Gemini CLI 並列為「介紹用的 AI 網頁生成工具」——兩者的核心能力類似：讀懂脈絡（程式碼庫或設計檔案）、用自然語言下指令、直接修改檔案。上課示範用哪一個，看現場環境跟帳號能不能用決定，操作邏輯是共通的。
