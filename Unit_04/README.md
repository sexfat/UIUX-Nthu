# 單元 4：產品設計流程

> 對應清華大學課程時段：10/7（三）13:20–16:20
> 課程名稱與教材狀態以 `../index.html` 為準。
>
> **本單元為合併單元**，已把兩個舊單元的簡報／講義整合成一份連貫教材：
> - `slides.html`（43 張）／`article.html`（24 節）依序涵蓋「資訊架構、功能清單、卡片分類法、IA 圖」（原「產品結構與資訊架構」單元）→「Flowchart、例外路徑、Wireframe、Auto Layout」（原「Flowchart 到 Wireframe」單元）。
> - 原始兩份教材保留在 `from-ia/` 與 `from-flowchart-wireframe/`（連同各自的練習作業 `exercises.html`），作為備查與練習素材來源，未刪除。
>
> ⚠️ **First draft 備註**：這次做了結構性合併（兩份簡報接成一份、兩份講義接成一份、CSS／JS／連結修過、`validate.py` 全綠），課堂練習與回家作業也重寫成單一場次的版本。但原本兩堂課各自有 80–95 分鐘的課堂實作，合併後壓縮成 40 分鐘做完「卡片分類 → Flow → Wireframe」全套流程，步調偏緊——這是第一版時間安排草案，需要你依班級狀況細修。
>
> 已跑過兩輪 Codex 內容複審並修正確定錯誤（Sitemap 與多重層級的用詞矛盾、卡片分類結果過度推論「直接採用」、高保真成本的假二分、樹狀測試直接率的誤判）。以下是複審抓出、但沒有自動處理的部分：
> - **教學設計判斷**：課堂實作是個人自己分類（10 分鐘），嚴格說不算真正的卡片分類研究（需要獨立於設計師的參與者）；作業要求「六類例外路徑一律必交」對某些流程可能不適用，會逼學生硬掰不存在的分支；兩份舊 `exercises.html`（`from-ia/`、`from-flowchart-wireframe/`）仍各自寫著 80 分鐘，跟新的 40 分鐘沒有同步，只有摘要頁更新過。
> - **來源涵蓋落差（建議補充）**：一般可用性測試與定量研究其實也能揭露 IA 問題，目前教材只強調卡片分類與樹狀測試；導覽項目的排序原則、hover 選單在觸控裝置上的風險，來源有提但教材沒寫進去。
> - **可刪減候選（要你決定）**：`slides.html` 第 1325–1527 張（保真度／Figma 操作）偏多，可考慮壓成 4 張左右，細節移到講義；`article.html` 第 1482–1603 行的 7 組 AI 提示詞份量偏重，可考慮改成附錄。

## 單元目標

- 能把研究洞察（訪談、旅程地圖）轉成有證據支持的功能清單，並區分核心路徑、次要功能與邊緣案例。
- 理解資訊架構（IA）與導覽、Sitemap 的差異，能用卡片分類法找出使用者的心智模型，畫出一張標注核心路徑與例外狀態的 IA 圖。
- 能把 IA 圖上的核心路徑，拆解成 Flowchart：標出判斷點、路徑條件，並補齊六種常被漏掉的例外路徑。
- 能畫出低保真 Wireframe，只放結構不放視覺，並用六題檢查清單自我驗收。
- 能用 Figma Auto Layout 建立會隨內容自動反應的版面骨架，理解 Hug／Fill／Fixed 與 Constraints 的分工。

## 課程介紹

前面幾個單元累積的訪談洞察、競品分析、Persona 與旅程地圖，如果沒有轉成結構，就無法進入介面設計。這個單元是研究與設計之間的橋：先把洞察整理成功能清單，用資訊架構決定內容怎麼分組、命名與導覽，再用卡片分類法驗證分類邏輯，產出 IA 圖；接著把 IA 圖上的核心路徑畫成 Flowchart，補齊使用者一定會遇到的例外狀況，最後畫出第一批低保真 Wireframe，並用 Auto Layout 建立不會一改就垮的版面骨架。

## 課程內容

**資訊架構部分**
- IA 是什麼、與導覽／Sitemap 的差異、三個關鍵模型（底層結構、分類法、導覽）。
- 可尋性 vs. 可發現性、資訊氣味、扁平 vs. 深層層級的取捨。
- 從研究洞察到功能清單，Functional Map：核心路徑、次要功能、邊緣案例。
- 卡片分類法：開放式／封閉式、四步驟、常見錯誤、結果分析。
- 樹狀測試、內容模型、命名的 4 個 S、IA 圖製作。

**Flowchart 與 Wireframe 部分**
- 先把 User Journey、User Flow、Flowchart、Wireflow 四個詞分開，什麼時候用哪一種。
- Flowchart 的四個符號、一條流程要交代的三件事、六種容易漏掉的例外路徑。
- 從 IA 圖轉成 Flow 的四步驟。
- Wireframe 在回答什麼問題、保真度的三個維度、該放什麼不該放什麼、六題檢查清單。
- Figma Auto Layout：三種排列方向、Padding／Gap、Hug／Fill／Fixed、Constraints 與 Auto Layout 的分工。

## 課堂練習

**從卡片分類到第一張 Wireframe**（40 分鐘，個人作業，用自己的專題）

1. 快速卡片分類（10 分）— 用功能清單做一輪開放式分類，整理出第一版 IA。
2. 畫 Flowchart（10 分）— 從 IA 挑一條核心路徑，補上判斷點與至少 2 種例外路徑。
3. 畫 Wireframe（15 分）— 用 Auto Layout 畫 1–2 張低保真 Wireframe，涵蓋流程的頭與尾。
4. 自我檢查（5 分）— 對照六題檢查清單，寫下答不出來的那一題。

結束後另有 15 分鐘各組成果分享與作業說明。詳細步驟仍可參考舊教材：`from-ia/exercises.html`、`from-flowchart-wireframe/exercises.html`。

## 回家作業

整條「產品設計流程」的完整交件，涵蓋功能清單、資訊架構、Flowchart 與 Wireframe：

1. 看完 [Information Architecture — 3 Key Models](https://www.youtube.com/watch?v=v39z0JPeIc8)（NN/g）。
2. 選一個網站逆向拆解 Sitemap（至少 3 層、20 個節點），用三個模型標注並找出 3 個 IA 問題。
3. 回到自己的專題，把功能清單與 IA 圖修正完整。
4. 把課堂上的 Flowchart 補完整：六種例外路徑一條都不能少。
5. Wireframe 補到 3–5 個畫面，至少涵蓋一個關鍵例外狀態，每張旁邊寫下六題檢查清單的答案。
6. 主要容器與重複元件用 Auto Layout 做，交件前拉寬拉窄各一次檢查是否爆版。

繳交：Figma 連結一份，含 Sitemap 分析、功能清單、IA 圖、1 張 Flow、3–5 個 Wireframe。

## 對應清大日期與時段

- 10/7（三）13:20–16:20

## 本單元產出

- 對應 `清華大學課程大綱.md`：產品設計流程（Functional Map／Flow Chart／Wireframe）。
- 課堂與作業產出：功能清單、IA 圖、Flowchart、3–5 個低保真 Wireframe。

## 參考資料

- [Information Architecture: Study Guide](https://www.nngroup.com/articles/ia-study-guide/) — NN/g，資訊架構部分教材主要來源。
- [Wireflows: A UX Deliverable for Workflows and Apps](https://www.nngroup.com/articles/wireflows/) — NN/g，Wireflow 定義與圖例。
- [Guide to auto layout](https://help.figma.com/hc/en-us/articles/360040451373-Guide-to-auto-layout) — Figma 官方文件。
- 完整參考資料清單見 `article.html` 頁尾「參考資料」區塊。
- 舊教材原始檔：`from-ia/`（產品結構與資訊架構）、`from-flowchart-wireframe/`（Flowchart 到 Wireframe）。
