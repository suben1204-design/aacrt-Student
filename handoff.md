# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
完成宣傳首頁後勤福利橫幅更新與導覽列錨點遮擋修復，並已推送至 GitHub Pages 上線：
1. **後勤福利橫幅（`index.html`）**：移除「活動平安險」字樣，改為「🎁 專屬生活與後勤福利」，納入「專屬 AACRT 志工工作人員服」與「預計於 4/25 晚間舉辦志工慶功宴」，與報名表單口徑完全一致。
2. **導覽列錨點修復（`index.html`）**：於 `<html>` 加入 `scroll-pt-16`（64px），避免點擊導覽列錨點跳轉時區塊標題被固定導覽列遮住。

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
- 時間：2026-11-18 10:03
- 更新者：Antigravity @ FENGYI
- Git push：✅ 已推（main）
