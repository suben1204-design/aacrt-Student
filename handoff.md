# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
招募定位已由「學生志工招募」改為「2027 AACRT 志工招募（含醫學影像相關學系學生志工）」，`index.html` 與 `register.html` 已改版並推上 GitHub Pages。報名表新增「報名身分別」（專業人員／學生志工）切換欄位，Google Sheets 已新增 K 欄「報名身分別」。

## 🚦 目前狀態
- 線上網站：https://suben1204-design.github.io/aacrt-Student/
- 報名資料寫入試算表「2027 AACRT 學生志工招募計劃」（工作表1，A～K 欄）。
- 專業人員：服務單位 → F 欄、職級 → G 欄；學生志工：學校系所 → F 欄、年級 → G 欄；身分別 → K 欄。
- 前端已改為「Apps Script 回傳 `Success` 才顯示成功」，否則顯示失敗彈窗。

## ➡️ 下一步
1. 確認使用者已將新版 Apps Script（新增 `e.parameter.identity`、LockService）以「管理部署作業 → 編輯 → 新版本」部署（網址不變）。
2. 用兩種身分各送一筆測試，檢查試算表 F／G／K 欄是否正確，再決定是否刪除測試資料。

## ⚠️ 注意事項
- GitHub repo 為 **PUBLIC**（GitHub Pages 需要），切勿放入學生個資 Excel/CSV 或任何金鑰。
- 重新部署 Apps Script 時不可按「新增部署作業」（會換網址），必須用「編輯 → 新版本」。
- 讀取試算表時只看標題列與筆數，避免把報名個資帶進對話或筆記。

## 🕐 最後更新
- 時間：2026-11-10 09:52
- 更新者：Antigravity @ FENGYI
- Git push：✅ 已推（main）
