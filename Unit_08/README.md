# 單元 8：介面組件介紹

> 對應清華大學課程時段：11/4（三）13:20–16:20

## 本單元教材現況（請先讀這段）

原訂主題是「介面組件介紹：按鈕組件／card 設計／登入設計／表單設計／顏色設計」。目前教材是舊「Wireframe 實作延伸」單元改編，狀態如下：

- **可直接使用**：第 2–6 節（空狀態、錯誤訊息、表單錯誤回報十條、載入狀態、指示器與通知的分工）。這些內容本身就是介面組件層級的規則（表單組件、通知組件、載入指示器組件），有 NN/g 原文可溯源，直接沿用。
- **保留但非本單元主軸**：第 7–11 節（把畫面接成 Wireflow、標註、設計說明、同儕檢核、修正紀錄）是舊單元的流程收尾內容，跟「介面組件介紹」關聯較低，這次沒有刪除，但不建議當本單元的教學重點。
- **完全沒有教材，需要補充**：按鈕組件、Card 設計、登入設計、顏色系統——舊版課綱備查（`../舊版課綱備查.md` 單元 8〈元件、樣式與設計系統概念〉、練習 7〈基礎元件庫與樣式〉）只有一行主題與一句練習描述，沒有可用的教學內容，這次沒有杜撰內容頂上。

## 相關檔案

- `slides.html` — 課堂簡報（25 張，沿用舊架構）。
- `article.html` — 完整教材（13 節，含 AI 協作提示詞）。
- `exercises.html` — 課堂練習（四階段）與回家作業。
- `resources/guide.md` — NN/g 五組來源的中文整理，本單元教材的溯源依據。
- 課堂範本檔：[狀態設計與 Wireflow 練習範本](https://www.figma.com/design/X0nEWewUts2YSRElqN6dE3)（① 狀態盤點表 ② 三種狀態範本 ③ 標註格式 ④ 修正紀錄表，各對應課堂練習一個階段；學生複製區塊到自己的檔案填寫）。
- 作業題目卡：同檔案的[「作業題目」分頁](https://www.figma.com/design/X0nEWewUts2YSRElqN6dE3?node-id=6-2)，三題各含情境、Persona、必須畫出的狀態、容易踩的坑、交件清單與五個空白畫框。
- Flowchart→Wireframe 的來源整理在 `../Unit_04/from-flowchart-wireframe/resources/guide.md`，本單元第 7 節沿用。
- 線框元件庫：[Wireframe Web UI Kit](https://www.figma.com/design/XKrTQ38VaU4PZeuwT0uocp/Wireframe_Web_UI_Kit-%E5%88%87%E7%89%88%E7%9A%84100%E7%A8%AE%E7%B7%B4%E7%BF%92?node-id=0-1)，補畫狀態畫面時可直接取用現成區塊。

## 單元目標

- 能分辨空狀態、錯誤狀態、載入狀態三種畫面，並依準則各畫出一張。
- 能寫出同時做到明確、看得懂、有禮貌、精準、給下一步的錯誤訊息。
- 能依等待時間（1 秒／2–10 秒／10 秒以上）選對進度指示的型別。
- 能分辨指示器、驗證、通知三種溝通方式，不互相誤用。
- （待補充）能認識按鈕、Card、登入頁三類組件的基本設計原則，並建立一套簡單的顏色使用規範。

## 課程介紹

介面不是一次畫好的整張圖，是一組可以重複使用的小零件拼出來的：表單、通知、載入指示器、空狀態……每一種都有自己該遵守的規則，用錯了使用者會卡住或誤解。

這堂課先從最容易出錯、最常被忽略的幾種組件講起：空狀態要放什麼而不是留白、錯誤訊息要同時做到哪五件事、表單出錯的十條準則、要等待時該顯示什麼、指示器與通知怎麼分工不誤用。這些規則本身就是「組件」層級的內容，不是流程層級的內容。

按鈕、Card、登入頁與顏色系統這幾種原訂要教的組件，目前沒有現成教材，需要授課者補充。

## 課程內容

- 表單組件：錯誤回報十條準則（五條該做、五條不要做）。
- 空狀態組件三條準則：講清楚系統狀態、教功能怎麼用、給一條直達關鍵任務的路；以及「還沒有」與「找不到」的文案差別。
- 錯誤訊息的五要件：明確、看得懂、有禮貌、精準、給下一步。
- 載入指示器組件：回應時間三門檻（0.1 秒／1 秒／10 秒）與進度指示的三種型別。
- 通知組件：指示器、驗證、通知的分工與誤用代價。
- （待補充）按鈕組件：狀態（default／hover／active／disabled）與尺寸規範。
- （待補充）Card 設計：版面結構與使用情境。
- （待補充）登入設計：欄位、驗證與錯誤處理的組合應用。
- （待補充）顏色系統：主色、輔色、語意色（錯誤／警告／成功）的規範方式。
- 附錄（非本單元主軸，保留舊教材）：Wireflow 合成、標註、設計說明、同儕檢核、修正紀錄。

## 課堂練習

**把 Wireframe 補成能被檢核的一份**（85 分鐘，個人＋跨組配對，Figma）

開始前先挑一條流程：用自己專題的流程，或用三個指定題目其中一題（會員註冊與登入／結帳付款出錯／中途離開與返回）。題目之間沒有分數差別。

1. 狀態盤點（15 分）— 用五欄檢查表逐頁盤，把 Flowchart 攤在旁邊對，至少標出 3 個「缺」。
2. 補畫三種狀態（25 分）— 空狀態 10 分、錯誤狀態 10 分、載入狀態 5 分，每張畫完逐條過檢查清單。
3. 接成 Wireflow 並標註（20 分）— 接線 12 分、標註 8 分。箭頭從可點元件出發，課堂上每張畫面先寫 1 條關鍵標註，回家補到 3 條。
4. 兩人互相檢核（25 分）— 各 10 分鐘互換，最後 5 分鐘各自整理修正清單。要跟不同專題的人配對。

之後另有 15 分鐘成果分享與作業說明（抽點 3–4 位，講被問倒的那一題與打算怎麼改）。

產出：3 張新狀態畫面 + 1 張接起來的 Wireflow + 標註 + 修正清單至少 5 則。

### 三小時時間分配

| 段落 | 時間 | 內容 |
| :--- | :--- | :--- |
| Part 1 | 45 分 | 表單、空狀態、錯誤訊息、載入指示器、通知等組件規則 |
| 休息 | 10 分 | |
| Part 2 | 25 分 | Wireflow 合成、標註、設計說明、設計檢核的規則與回饋改寫（附錄內容） |
| Part 3 | 85 分 | 課堂練習四階段 |
| Part 4 | 15 分 | 成果分享與作業說明 |

講述 70 分 + 實作與分享 100 分 + 休息 10 分 = 180 分。

## 回家作業

**狀態補齊與修正紀錄**

1. 核心畫面補到 3–5 張（狀態版本不另計數），整組畫面裡空狀態、錯誤狀態、載入狀態至少各出現一次。
2. 接成一張完整的 Wireflow，每一條例外路徑都要找得到對應畫面，不能有斷掉的箭頭。
3. 每張畫面至少 3 條標註，整份至少一條「刻意不做的事」。
4. 修正紀錄至少 5 則，每則四欄（原話、決定、理由、下一步）填滿，決定「不改」的也要寫。
5. 一段設計說明，挑三個版面決策各寫一句「因為研究裡的 ______，所以 ______」。
6. （加分，非必要）把其中一條流程做成 Figma 可點原型。

配分：流程完整性 25、狀態設計 25、標註品質 20、修正紀錄 20、設計說明 10，各項的「通過的樣子」與「不及格的樣子」寫在 `exercises.html#submit`。

## 對應清大日期與時段

- 11/4（三）13:20–16:20

## 本單元產出

- 對應 `清華大學課程大綱.md`：本單元尚未列正式交件。

## 參考資料

- [Designing Empty States in Complex Applications: 3 Guidelines](https://www.nngroup.com/articles/empty-state-interface-design/) — NN/g，空狀態三條準則。
- [Error-Message Guidelines](https://www.nngroup.com/articles/error-message-guidelines/) — NN/g，錯誤訊息五要件。
- [10 Design Guidelines for Reporting Errors in Forms](https://www.nngroup.com/articles/errors-forms-design-guidelines/) — NN/g，表單錯誤回報十條。
- [Response Times: The 3 Important Limits](https://www.nngroup.com/articles/response-times-3-important-limits/) — NN/g，0.1／1／10 秒三門檻。
- [Progress Indicators Make a Slow System Less Insufferable](https://www.nngroup.com/articles/progress-indicators/) — NN/g，進度指示三型別。
- [Indicators, Validations, and Notifications](https://www.nngroup.com/articles/indicators-validations-notifications/) — NN/g，三種溝通方式的分工。
- [Wireflows: A UX Deliverable for Workflows and Apps](https://www.nngroup.com/articles/wireflows/) — NN/g，Wireflow 定義與實作準則（附錄）。
- [Design Critiques: Encourage a Positive Culture to Improve Products](https://www.nngroup.com/articles/design-critiques/) — NN/g，角色、三個前提與回饋改寫（附錄）。
- [Closing the Loop: What to Do After a Design Critique Ends](https://www.nngroup.com/articles/after-design-critique/) — NN/g，檢核之後的四步範本（附錄）。
- 舊版課綱備查〈元件、樣式與設計系統概念〉、練習 7〈基礎元件庫與樣式〉，見 `../舊版課綱備查.md`——主題方向參考，非教材內容來源。

## 備註

- 本單元原內容為舊「Wireframe 實作延伸」單元（第 12 版課表 Unit 07），因清大課綱重編改配到「介面組件介紹」的位置。第 2–6 節可直接沿用，第 7–11 節保留為非主軸附錄，按鈕／Card／登入／顏色四項教材需要授課者補充。
- 文中對前置單元的引用已配合清大新編號更新（例如 Flowchart／Wireframe 前置內容現在是 `Unit_04/from-flowchart-wireframe/`）；仍有部分練習題文字引用舊編號的 Unit 03／04／05 前置產出（Persona、旅程地圖、IA），尚未逐一核對更新，屬於全課程重編號後留下的已知缺口，非本次改版範圍。
