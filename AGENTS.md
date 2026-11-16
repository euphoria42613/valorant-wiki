# AGENTS.md - Valorant 戰術與設定資料庫開發規範

## 1. 專案目的 (Project Overview)
本專案為個人《特戰英豪 (Valorant)》設定與戰術攻略靜態資料庫，部署於 GitHub Pages。
核心目標是建立標準化的攻略模組與視覺元件，讓 AI 未來只需接收零散的遊戲筆記或特務數據，即可自動生成排版完全一致的新攻略頁面並掛載至首頁。

## 2. 技術棧與視覺風格 (Tech Stack & Design System)
- **技術限制**：僅使用原生 HTML5、CSS3 與 Vanilla JavaScript（不依賴任何前端框架或編譯工具）。
- **視覺風格**：Valorant 戰術暗黑電競風（深色底、高對比、利落邊角、經典戰術紅點綴）。
- **共用樣式規範 (`assets/css/style.css`)**：所有頁面必須引入此 CSS，並嚴格使用以下 CSS 變數，禁止使用 inline-style：
  - `--bg-main: #0f1923`（主背景：深戰術藍黑）
  - `--bg-card: #1b2733`（卡片與區塊背景）
  - `--bg-elevated: #243342`（數據框與標籤背景）
  - `--text-primary: #ece8e1`（主文字：米白）
  - `--text-secondary: #9aa5b1`（次要說明文字）
  - `--accent-red: #ff4655`（Valorant 標誌紅）
  - `--accent-teal: #38bdf8`（戰術資訊青）
  - `--border-color: #2c3e50`（邊框線）

## 3. 檔案結構與命名規則 (Directory & Naming)
```text
/
├── index.html                    # 首頁（專案介紹、分類篩選與所有攻略卡片列表）
├── AGENTS.md                     # 本開發規範文件
├── assets/
│   └── css/
│       └── style.css             # 全站共用樣式表
└── pages/                        # 所有攻略子頁面統一放置於此
    ├── 01-sensitivity-setup.html # 命名規則：[兩位數編號]-[英文小寫短橫線連接].html
    └── 02-jett-guide.html