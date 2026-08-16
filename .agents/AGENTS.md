# Agent Rules for Miley 錯題本

## Cache and Preview Troubleshooting
- **Cache Refresh / Preview Update Issues**:
  If the user mentions that Markdown previews, images, or files are not updating due to cache issues, remind the user of this solution:
  1. Press `Ctrl + Shift + P` (Command Palette) in VS Code.
  2. Search for and select `Developer: Reload Window` (開發人員: 重新載入視窗) to clear the IDE cache and reload the workspace.

## 🔁 錯題重複加入處理規則 (Duplicate Question Handling Rules)
當使用者要求「新增」或「整理」錯題時，你必須先讀取現有的錯題本（如 [math.md](file:///p:/bennychen/0AI_共用資料夾/Miley錯題本/math.md) 或是其他學科的 `.md` 檔案），並執行以下檢查與標記邏輯：

1. **重複性檢查標準**：
   - 檢查新題目的**核心內容、文字描述、題目圖片檔名**是否與已有的錯題相似或相同。
   - 若相同或高度相似，判定為「重複加入的題目」。

2. **處理與標示邏輯 (不要重複搜集，但標示刷題次數)**：
   - **不新增新的錯題區塊**，而是直接在**原有的錯題標題**上進行修改。
   - **更新標題標籤**：
     - 若為第二次加入，在標題的 `## 📌 錯題 N` 後方加上 `[二刷]`（例如：`## 📌 錯題 2 [二刷]：題目名稱...`）。
     - 若為第三次加入，則將 `[二刷]` 升級為 `[三刷]`，依此類推（例如：`## 📌 錯題 2 [三刷]：...`）。
   - **更新日期紀錄**：
     - 在原題目區塊的 `📅 記錄日期` 下方，新增一行再次加入的日期（例如：`- **二刷日期**：2026-07-27`）。
   - **提示使用者**：
     - 修改完成後，主動告知使用者：「*偵測到該題目已存在於錯題本中（錯題 N），已為您更新為 `[二刷/三刷...]` 並記錄今日日期。*」

3. **使用者手動要求複習/標示重錯邏輯**：
   - 當使用者在複習時，表示「某一題又錯了一次」、「這題解不出來，需要再複習此題」等類似要求時，你必須找出該題目，同樣套用「更新標題標籤」與「更新日期紀錄」的規則，將刷數往上累加（如 `[二刷]` 變 `[三刷]`），並記錄當天日期。

## 🖼️ 附圖放大對照與雙視窗檢視規則 (In-Page Image Zoom & Cross-Reference Rules)
當錯題本中含有附圖（包含題目幾何圖、解答推導圖、原始截圖等）時，必須確保使用者**在閱讀解析的同時能對照大圖**，遵循以下設計：

1. **原地展開/放大與收合/縮小語法 (In-Page Toggle Zoom & CSS Checkbox Hack)**：
   在 Markdown 頂部置入一次 CSS 樣式定義：
   ```html
   <style>
     .zoom-toggle {
       display: none !important;
     }
     .zoom-label img {
       cursor: zoom-in !important;
       transition: max-width 0.25s ease-in-out !important;
     }
     .zoom-toggle:checked + .zoom-label img {
       max-width: 100% !important;
       cursor: zoom-out !important;
     }
   </style>
   ```
   圖片使用 HTML `<details open>`、`<input type="checkbox">` 與 `<label>` 包裹（其中 `id` 與 `for` 需設為本題唯一識別碼，如 `zoom-m1-src`）：
   ```html
   <details open>
   <summary>🔍 <b>[圖片說明]（點擊可展開/收合整個區塊，點擊下方圖片可原地放大/縮小）</b></summary>
   <input type="checkbox" id="zoom-唯一識別碼" class="zoom-toggle">
   <label for="zoom-唯一識別碼" class="zoom-label">
     <img src="images/圖檔名稱.png" alt="圖片說明" style="width: 100%; max-width: 450px; margin-top: 8px; border-radius: 6px; border: 1px solid #ddd;">
   </label>
   </details>
   ```
   - **原地對照**：預設以縮圖尺寸（`max-width: 450px`）顯示於解析中，不干擾主線閱讀。
   - **原地放大**：點擊圖片本身，即會就地平滑放大至 100% 寬度（填滿預覽視窗寬度，可達 900px+ 方便看清細節）；再次點擊即可恢復預覽尺寸。
   - **收合整個區塊**：點擊 `<summary>` 可收合整個圖片區塊以節省空間。

2. **側邊獨立視窗對照模式 (Side-by-Side Split View)**：
   對於原始完整截圖或大圖連結，統一採用：
   `[🖼️ 查看原始完整截圖（💡 提示：點擊連結開啟圖片後，可將分頁拖曳至右側或按 Ctrl + \ 分割視窗對照）](images/科目_題號_source.png)`
   引導使用者藉由 VS Code 的分頁拖曳或分割視窗功能（快速鍵 `Ctrl + \`）進行左右雙視窗對照。


