# AACRT-志工招募暨培訓(含學生)（專案藍圖）

> 本檔為跨 Agent 通用的專案藍圖（AGENTS.md 開放標準）。任何 Agent 的每個 session 都應先讀本檔＋`handoff.md`。

## 專案簡介
2027年第26屆亞澳區醫事放射師學術國際會議（The 26th AACRT）與中華民國醫事放射學會第60次年會（TWSRT 60th Annual Meeting）之「志工招募計畫（含醫學影像相關學系學生志工）」官方宣傳網站與線上報名系統。透過 GitHub Pages 發佈前端頁面，並串接 Google Apps Script 將報名表單資料直接寫入 Google Sheets「2027 AACRT 學生志工招募計劃」。

- **線上網址（GitHub Pages）**：https://suben1204-design.github.io/aacrt-Student/
- **GitHub 儲存庫**：https://github.com/suben1204-design/aacrt-Student

## 關鍵時程
- **大會日期**：2027 年 4 月 24 日（六）至 4 月 25 日（日）
- **大會地點**：台北南港展覽館 2 館（TaiNEX 2）
- **排班方案**：
  - 方案一【兩日完整體驗】：4/24 (六) 及 4/25 (日) 全程參與（外縣市夥伴／同學自行衡量交通與住宿）
  - 方案二【單日彈性服務】：僅 4/24 (一天) 或 僅 4/25 (一天)，另一天享免費入場觀摩學習

## 目標與路線圖
- [x] 階段一：完成學生志工招募宣傳首頁（`index.html`）與線上報名表（`register.html`）初版並部署至 GitHub Pages
- [x] 階段二：串接 Google Apps Script Web App 與 Google Sheets 自動收集報名資料
- [x] 階段三：建立 Antigravity 三層級專案架構（L1 本地雲端硬碟 + L2 GitHub `aacrt-Student` + L3 Obsidian）並完成風格格式與技術分析
- [x] 階段四：全面改版為「志工招募（含醫學影像相關學系學生志工）」，完成首頁文案升級、手機版漢堡選單、身分別（專業人員/學生志工）雙向切換、格式防呆、結果彈窗與 Google Sheets 實地驗證測試
- [ ] 階段五：依後續大會籌備進度，擴充行前培訓專區、SOP 線上檢視或報名統計儀表板

## 視覺風格與前端技術規範（Style & Format Guide）
- **技術框架**：純靜態 HTML5 + **Tailwind CSS (CDN)** + 原生 JavaScript（Fetch API），零建置依賴，直接推上 GitHub `main` 分支即透過 GitHub Pages 生效。
- **核心色彩系統（皇家海軍藍 × 榮耀琥珀金，Royal Navy & Prestige Gold）**：
  - **主色（深邃海軍藍漸層）**：`linear-gradient(135deg, #0f172a 0%, #1e3a8a 100%)`（`slate-900` 至 `blue-900`），營造國際學術會議的專業與莊重感。
  - **強調色（榮耀琥珀金漸層）**：文字與按鈕採用 `#fbbf24` → `#f59e0b` → `#d97706`（`amber-400` 至 `amber-600`），象徵第 60 次年會與國際盛會的榮耀感，並作為高對比行動呼籲（CTA）。
  - **背景與卡片色**：頁面底色 `bg-slate-50`（`#f8fafc`），內容區塊交錯使用純白卡片 `bg-white` 搭配細邊框 `border-slate-100`/`border-slate-200` 與柔和陰影 `shadow-lg`/`shadow-xl`，玻璃擬態採用 `bg-white/10 backdrop-blur-md`。
- **排版與版面結構**：
  - 導覽列：`sticky top-0 z-50 bg-white/90 backdrop-blur-md` 固定頂部毛玻璃導覽列（含手機版下拉收合選單）。
  - 首頁（`index.html`）五段式 Landing Page：
    1. `#hero` 首頁主視覺區（大會中英文全銜、志工招募雙軌主副標、時間地點玻璃卡片、主 CTA 按鈕）
    2. `#benefits` 四大專屬福利（實質經歷加分、學術技術接軌、商展產業交流區跨世代交流、專屬會費減免 + 底部海軍藍生活保障橫幅）
    3. `#roles` 團隊任務與協同作業模式（前輩領航團隊共進安心提示框 + 3 欄組別卡片）
    4. `#schedule` 排班方案與大會焦點時程（左欄方案卡片 + 右欄垂直時間軸 Timeline）
    5. `#register` 報名資訊與聯絡方式（雙軌招募對象、報名 4 步驟、官方聯絡資訊與底部 CTA）
  - 報名頁（`register.html`）：頂部大會識別橫幅 + 金色裝飾線（`h-2 accent-bar`）+ 置中單欄白卡表單（含專業人員/學生志工身分別動態切換、身分證手機即時驗證防呆、客製化互動結果彈窗）。

## 後端資料串接架構（Google Sheets + Apps Script）
- **綁定試算表**：Google Drive 檔案「`2027 AACRT 學生志工招募計劃`」（ID：`1TX93rZnOeMkLc7L3YB91vULRyNonicFiZHs08ruz168`，工作表1）
- **Apps Script 端點**：`https://script.google.com/macros/s/AKfycbxPlSm1CDxxmjx1to0lKJ37szr0XncLojfx1DoG0Pa2bGKSZtB4d1UmgcPNQz-eTOcX5w/exec`
- **資料欄位對應（A～K 欄）**：
  1. A 報名時間（自動戳記）
  2. B 姓名 (`name`)
  3. C 身分證字號 (`id_number`)
  4. D 出生年月日 (`birthday`)
  5. E 電話 (`phone`，已自動補連字號 `09xx-xxxxxx`)
  6. F 學校系所／服務單位 (`school`)
  7. G 年級／職級 (`grade`)
  8. H Email (`email`)
  9. I 飲食習慣 (`diet`)
  10. J 排班方案 (`plan`)
  11. K 報名身分別 (`identity`，`專業人員` / `學生志工`)

## 資料夾結構
```text
AACRT-志工招募暨培訓(含學生)/
├── AGENTS.md        # 跨 Agent 靜態專案藍圖與風格規範
├── handoff.md       # 跨電腦／跨 Agent 當下交接檔
├── .gitignore       # Git 忽略規則
├── README.md        # GitHub Repo 說明檔
├── index.html       # 志工招募宣傳首頁（Landing Page，已支援手機版選單與新文案）
└── register.html    # 志工線上報名表單頁（支援專業人員/學生雙軌切換、格式驗證與彈窗）
```

## 同步層級（本專案初始化至第 3 層級）

| 層級 | 平台 | 位置 | 讀取時機 |
|------|------|------|---------|
| L1 | 本地（雲端硬碟資料夾） | `AGENTS.md`＋`handoff.md` | 每個 session |
| L2 | GitHub | `suben1204-design/aacrt-Student`（GitHub Pages 公開部署） | 指定時 |
| L3 | Obsidian | `AACRT-志工招募暨培訓(含學生)/專案工作流程.md` | 有需要時 |

## 工作約定
- 任何 Agent、任何電腦：**開工先讀 `handoff.md`，收工必更新 `handoff.md`**
- 修改共用檔案前先讀最新內容，避免覆蓋其他 Agent 的變更
- 所有回應與文件使用繁體中文
- 修改前先確認計畫，優先保留原有資料結構

## 安全與隱私（不可違反）
- **不把 API key、密碼、憑證寫進 repo**，也不要貼進 `AGENTS.md`／`handoff.md`；一律放 `.env` 並列入 `.gitignore`
- 要公開分享前，先確認檔案裡沒有上述敏感憑證內容
