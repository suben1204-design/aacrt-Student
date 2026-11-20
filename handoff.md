# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
完成宣傳首頁細節優化與每日總表備份排程設定，並已推送至 GitHub Pages 上線：
1. **宣傳首頁（`index.html`）**：Hero 活動日期補註「（4/23 為會前論壇與理事會議）」、統一時程表 Day 1～Day 3 標題格式、移除外部紋理圖檔依賴（改為純 CSS 漸層以提升穩定性）。
2. **Google Apps Script（第 7 版＋每日總表備份）**：新增 `sendDailyBackup()` 函式並設定每日時間驅動觸發條件，每日自動寄送含 UTF-8 BOM 的完整報名總表 CSV 至管理員與副本信箱。

## 🚦 目前狀態
- **GitHub Pages 線上網站已更新**：https://suben1204-design.github.io/aacrt-Student/
- **Google Apps Script 第 7 版＋每日排程備份已就緒**，試算表 A～K 欄與雙向寄信正常運作。

## ➡️ 下一步
1. 至線上網址 `register.html` 實測送出一筆報名，確認試算表寫入與兩封通知信／確認信正常後清除測試列。
2. 檢視本地未追蹤目錄 `rdq/` 是否需留存或移出 Git 工作目錄（目前暫未納入 commit）。

## ⚠️ 注意事項
- GitHub repo 為 **PUBLIC**，切勿將含真實志工個資的 Excel/CSV 或敏感金鑰放入 repo。
- 更新 Apps Script 時必須使用「管理部署作業 → 編輯 → 新版本」，不可按「新增部署作業」。

## 🕐 最後更新
- 時間：2026-11-20 20:32
- 更新者：Antigravity @ FENGYI
- Git push：✅ 已推（main）
