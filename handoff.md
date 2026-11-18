# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
完成宣傳首頁 7 大任務編組改版與報名表飲食選項精簡，並已推送至 GitHub Pages 上線：
1. **宣傳首頁（`index.html`）**：將「團隊任務與協同作業模式」由 3 組擴充為 7 組（議事組、報到／接待組、國際外賓接待組、展場與海報組、節目典禮組、講者試片組、機動組），採 6 格網格＋1 全寬機動組排版，並為每組設計駐點標籤與排班重點說明。
2. **報名表單（`register.html`）**：「飲食習慣」移除「是否素食」與「是／否」，改為純淨的 `葷食`／`素食` 選項（後端 Apps Script 與 Google Sheets G 欄直接相容）。

## 🚦 目前狀態
- **GitHub Pages 線上網站已更新**：https://suben1204-design.github.io/aacrt-Student/
- **Google Apps Script 第 6 版運行中**，試算表 A～K 欄與前端完全對齊。

## ➡️ 下一步
1. 至線上網址 `register.html` 實測送出一筆報名，確認試算表 A～K 欄寫入無誤後即可清除測試列。
2. 檢視本地未追蹤目錄 `rdq/` 是否需留存或移出 Git 工作目錄（目前暫未納入 commit）。

## ⚠️ 注意事項
- GitHub repo 為 **PUBLIC**，切勿將含真實志工個資的 Excel/CSV 或敏感金鑰放入 repo。
- 更新 Apps Script 時必須使用「管理部署作業 → 編輯 → 新版本」，不可按「新增部署作業」。

## 🕐 最後更新
- 時間：2026-11-18 09:19
- 更新者：Antigravity @ FENGYI
- Git push：✅ 已推（main）
