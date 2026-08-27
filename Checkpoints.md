# 📍 Checkpoint 歷史紀錄 (Checkpoints.md)

本檔案自動記錄專案的所有 Checkpoint 快照與異動摘要。

---

## 📌 [v1.06] - 2026-08-27 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.06`
- **記錄日期**：2026-08-27
- **狀態**：[一般快照]
- **異動摘要**：
  - **收錄數學科錯題 12**：新增「錯題 12：相似三角形紙卡翻面與比例線段計算（中點重疊與翻面線段比轉換）」。
  - **同步雙軌檔案**：
    - 於 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md) 加入完整題目、選項、四步驟詳細推導、思考盲點與 CSS 原地放大圖片標籤。
    - 於 [math.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.html) 同步更新題庫資料陣列 `questionsData` 與 `🔥 最新收錄` 標記。
  - **圖片裁切與存檔**：
    - 儲存原始題目截圖 `images/math_12_source.png`。
    - 裁切幾何圖形區域為 `images/math_12.png` 以供清晰對照。
- **廢棄/提純規則**：無

---

## 📌 [v1.05] - 2026-08-23 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.05`
- **記錄日期**：2026-08-23
- **狀態**：[一般快照]
- **異動摘要**：
  - **錯題重複加入與二刷標記**：偵測到使用者再次加入「平行線截比例線段與相似三角形性質（母子相似與沙漏形相似綜合題）」，判定為重複題目。
  - **更新錯題 11 刷題狀態**：
    - 於 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md) 將標題升級為 `## 📌 錯題 11 [二刷]`，並新增記錄 `- **二刷日期**：2026-08-23`。
    - 於 [math.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.html) 標註 `[二刷]` 徽章並同步更新二刷日期。
- **廢棄/提純規則**：無

---

## 📌 [v1.04] - 2026-08-22 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.04`
- **記錄日期**：2026-08-22
- **狀態**：[一般快照]
- **異動摘要**：
  - **新增理化科錯題本**：建立 [science.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/science.md) 並收錄「錯題 1：凸透鏡成像實驗與焦距判斷（物距與像距數據分析與不等式逼近法）」。
  - **建立理化科互動網頁系統**：建立 [science.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/science.html)，提供大字縮放、護眼模式、測驗模式，並在 [math.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.html) 與 `science.html` 頂部加入跨學科即時切換標籤。
  - **圖片裁切與存檔**：儲存並裁切題目數據表 `science_1.png` 與原始完整截圖 `science_1_source.png`。
- **廢棄/提純規則**：無

---

## 📌 [v1.03] - 2026-08-22 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.03`
- **記錄日期**：2026-08-22
- **狀態**：[一般快照]
- **異動摘要**：
  - **選項排版自適應優化**：重構 [math.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.html) 答案選項區，改採自然文字長度緊湊排版，短答案不硬拉撐 100% 畫面寬度，長答案流暢自動折行。
  - **全載具手機響應式 (RWD) 升級**：支援手機與平板垂直單欄排版、滑出式抽屜篩選欄（Off-canvas Drawer）與半透明背景遮罩。
  - **GitHub Pages 自動發布工作流程**：建立 `.github/workflows/deploy.yml`，實現每次 push 自動部署至 GitHub Pages 靜態網站。
  - **規則提純與閉環規範**：於 `.agents/AGENTS.md` 新增「網頁版同步與自動 Checkpoint 發布規則」。
- **廢棄/提純規則**：無

---

## 📌 [v1.02] - 2026-08-22 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.02`
- **記錄日期**：2026-08-22
- **狀態**：[一般快照]
- **異動摘要**：
  - 新增「錯題 10：坐標平面正方形頂點移動與規律相遇（等速率相遇問題與餘數週期規律）」至 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md)。
  - 新增「錯題 11：平行線截比例線段與相似三角形性質（母子相似與沙漏形相似綜合題）」至 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md)。
  - 升級 [math.html](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.html) 互動複習系統（UI/UX 專家協同規劃）：
    - 側邊欄一鍵內縮/展開，並新增**左側垂直中間常駐懸浮 `>` 展開按鈕**（滾動頁面時始終固定在左側中央，一鍵外放）。
    - 超大字級動態縮放系統（支援 60% ~ 300%+ 無上限級距、提供 100%~250% 快捷檔位，文字與 KaTeX 公式自適應折行，100% 消除水平捲軸）。
    - 護眼模式（Light / Dark / Sepia 暖色羊皮紙模式）。
  - 儲存並裁剪題目幾何圖 `math_10.png`、`math_11.png` 與原始截圖 `math_10_source.png`、`math_11_source.png`。
- **廢棄/提純規則**：無

---

## 📌 [v1.01] - 2026-08-16 增量快照 (Incremental Checkpoint)

- **版本號**：`v1.01`
- **記錄日期**：2026-08-16
- **狀態**：[一般快照]
- **異動摘要**：
  - 新增「錯題 8：平行線截比例線段與連比計算（三角形中點與平行截線）」至 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md)。
  - 擷取與裁剪題目圖 `math_8.png` 並保存原始截圖 `math_8_source.png`。
- **廢棄/提純規則**：無

---

## 📌 [v1.00] - 2026-08-16 初始快照 (Initial Checkpoint)

- **版本號**：`v1.00`
- **記錄日期**：2026-08-16
- **狀態**：[穩定版 Stable]
- **異動摘要**：
  - 初始化 Git 儲存庫與 `.agents/config.json` 設定。
  - 導入 `checkpoint_master` 快照管理制度。
  - 歸檔現有錯題本內容（包含 `math.md`, `chinese.md`, `rules_log.md`, `README.md`, `.agents/AGENTS.md` 及相關圖片）。
- **廢棄/提純規則**：無
