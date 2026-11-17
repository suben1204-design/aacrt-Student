# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
完成報名表單精簡與工作服功能升級，並同步更新首頁、Google Sheets 與 Apps Script（第 6 版），已推送至 GitHub Pages 上線：
1. **移除敏感個資**：刪除 `register.html` 的「身分證字號」與「出生年月日」，並刪除試算表原 C、D 欄，第 1 列改為 `姓名｜電話`。
2. **新增「AACRT 志工工作人員服」**：加入點選式按鈕（`黑色`/`白色` × `S`～`XXXL`），並內嵌尺寸表圖片 `assets/images/shirt-size-chart.jpg`（點擊可開啟放大燈箱），試算表新增 J、K 欄接收。
3. **更新排班方案**：`index.html` 與 `register.html` 同步改為五種排班時段選項（含 4/24 晚宴協助選項），並加入 4/24 07:00–08:00 志工教育訓練及 4/25 晚上慶功宴提醒。

## 🚦 目前狀態
- **GitHub Pages 線上網站已部署更新**：https://suben1204-design.github.io/aacrt-Student/
- **Google Apps Script 第 6 版已部署**（端點 ID 未變），試算表 A～K 欄與前端完全對齊。

## ➡️ 下一步
1. 至線上網址 `register.html` 實測送出一筆報名（含選擇工作服與五種排班方案之一），確認試算表 A～K 欄寫入無誤後即可清除測試列。
2. 檢視本地未追蹤目錄 `rdq/` 是否需留存或移出 Git 工作目錄（目前暫未納入 commit）。

## ⚠️ 注意事項
- GitHub repo 為 **PUBLIC**，切勿將含真實志工個資的 Excel/CSV 或敏感金鑰放入 repo。
- 更新 Apps Script 時必須使用「管理部署作業 → 編輯 → 新版本」，不可按「新增部署作業」。

## 🕐 最後更新
- 時間：2026-11-17 17:11
- 更新者：Antigravity @ FENGYI
- Git push：✅ 已推（main）
