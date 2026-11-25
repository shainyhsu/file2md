# 01_CURRENT_STATE.md（SSSM 語義狀態空間快照）

- 最後更新：2026-11-25 09:09（台灣時間）

## 1. 逐字任務目標（Verbatim Objective & Done Criteria）

- 當前唯一原子任務：MWG 修正。Shainy 2026-11-25 08:04 逐字：「開始修正，在不改變或降低安全、ui、計算、效能的前提下（可變好，不可變差）。」
- 完成驗收條件：畫面與結果不變（main 與分支逐字、逐像素比對）；外部腳本雜湊與 npm 原檔一致；一個分支、一個 PR，Shainy 說合併才合併。

## 2. 已驗證事實（Verified Facts）

- 版本：main 為 V18（2026-11-25 09:01）；本分支 V19。〔程式碼核對〕
- 轉換函式庫（cdn.jsdelivr.net，皆鎖版本）：mammoth 1.8.0、xlsx 0.18.5、jszip 3.10.1、turndown 7.2.0、tesseract.js 5.1.1；V18 起五者加 SRI，sha384 與 npm 套件原檔一致。〔雜湊比對〕
- pdf.js（pdfjs-dist 4.4.168）在 L334 的 `<script type="module">` 以 ES module import 載入，worker 同版本；ES module import 加 SRI 需 import map integrity（未達 Widely available），未加。〔程式碼核對〕
- 狀態存 localStorage：forest-md-lang、theme；檔案只在瀏覽器內轉換。〔程式碼核對〕

## 3. 未驗證想法與待確認假設（Unverified，不得當作已實作）

- 待 Shainy 指定。

## 4. 已套用變更與下一步唯一動作（Applied Changes & Immediate Next Action）

- 已修改檔案（2026-11-25，09:01 合併上線）：index.html（五個函式庫加 integrity＋crossorigin＋referrerpolicy；renderList() 內 innerHTML = '' 改 replaceChildren()）、README.md、CHANGELOG.md（V18）、AGENTS.md（Popover 說明、改指向 .ai/）、新建 .ai/00–02。
- 已修改檔案（2026-11-25，分支 theme-meta，PR 待合併）：index.html（開頁腳本與切換鈕同步 `<meta name="color-scheme">`）、README.md、CHANGELOG.md（V19）。
- 下一步唯一動作：待 Shainy 指定。
