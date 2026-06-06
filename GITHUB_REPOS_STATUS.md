# GitHub Repos 當前正確狀態（Grok 版獨立後）

**更新日期**：2026-06（最新：移除 UI GitHub 按鈕 a8d5fb7 + Apple Intelligence 分類修正 d9b1f68）

## 1. 原本小教室專案 Repo（不要動）
- **網址**：https://github.com/snowsepch/workshop-generator
- **main 分支**：已完全回復到 Grok 大改之前的原版（commit d0452d2：「移除兒童(6-12)年齡層；內容改為隨年齡層調整語氣與重點」）
  - 原本的 GitHub 連結（raw、Pages 等）現在應該都指向正確的原版內容。
- **grok 分支**：保留了 Grok 版的備份（可作為參考或緊急備份使用）
- **注意**：這個 repo 的 main 請維持原版，不要再直接 push Grok 內容進去。

## 2. Grok 版（目前這個資料夾）
- **本地位置**：`~/小教室Grok版/`（或你的 iCloud 路徑，例如 `/Users/你的使用者名稱/Library/Mobile Documents/com~apple~CloudDocs/小教室Grok版/`）
- **GitHub Repo**（已上傳完成）：
  - **原始碼**：https://github.com/snowsepch/workshop-generator-grok
  - **線上使用（GitHub Pages）**：https://snowsepch.github.io/workshop-generator-grok/
    - 開啟即用，無需下載 index.html
  - **目前狀態**：
    - 這是一個**全新的獨立 git repo**（已移除舊 .git 歷史）。
    - 只有 Grok 版的內容：
      - index.html（完整最新版，包含所有修正）
      - README.md（詳細說明差異與使用方式）
      - 歷史版本/（舊版 UI 截圖）
      - 各階段版本對照 JPG
      - GITHUB_REPOS_STATUS.md（本狀態紀錄檔）
    - branch：main
    - remote：origin → https://github.com/snowsepch/workshop-generator-grok.git
    - 初始 commit：339768c
    - 上傳 commit：eaa352b（包含本狀態檔）
    - **GitHub Pages 已啟用**（來源：main 分支 + / 根目錄）
- **Repo 名稱選擇**：使用 `workshop-generator-grok`（與原本 `workshop-generator` 平行，易分享且 URL 乾淨）

## 3. 上傳紀錄（已完成）
- 2026-06-06：使用 `gh repo create workshop-generator-grok --public --source . --remote origin --push` 完成首次上傳。
- 隨即啟用 GitHub Pages（`gh api` + `gh repo edit` 設定 homepage 與 topics）。
- 之後的開發：在此資料夾直接 `git add`、`git commit`、`git push` 即可同步到 GitHub 與 Pages（一般檔案OK）。

### 最近開發紀錄（持續更新）
- a8d5fb7：移除 topbar GitHub 按鈕（依使用者要求，GitHub 連結改由本文件 GITHUB_REPOS_STATUS.md 與 README 維護，不在工具 UI 直接顯示按鈕）。
- d9b1f68：修正 Apple Intelligence 未正確歸入 AI 分類問題（為硬編碼主題明確加上 `category: 'AI'`；同步強化 renderTopics() 與快速新增預填的推斷邏輯 — AI 檢查前置、App 檢查嚴謹避免 "apple" 誤中 'app'；更新除錯待辦.md）。
- 2a3aba2：v4 除錯完成同步 + 更新連結（一鍵清除、多選年齡智慧合併、從官網快速新增、分類優化、fixAppleCasing、備課講稿 restructure、除錯待辦.md 紀錄、docs 連結校正）。
- b21e088：docs: add instructions for enabling GitHub Actions Pages deploy（workflow scope limitation noted）。
- 更早：初始上傳 + .nojekyll + 各種 UI/內容修正（詳見 git log）。

**給一般使用者（店員/學員）的唯一連結：**
- 線上直接使用（GitHub Pages）：https://snowsepch.github.io/workshop-generator-grok/
  開啟瀏覽器即可用，無需下載。請只分享這個連結給需要使用工具的人。

**給維護者/內部參考（非公開分享）：**
- 原始碼：https://github.com/snowsepch/workshop-generator-grok
- 本地正本：`~/小教室Grok版/index.html`

**注意**：工具 UI 已完全移除任何 GitHub 按鈕或連結提示。一般使用者只需打開 Pages 連結即可使用所有功能，無需知道原始碼位置。此文件與 README 僅供維護者內部參考。
- **GitHub Pages 部署**：
  - 目前使用 legacy source + .nojekyll 設定（已推）。**注意**：`.github/workflows/deploy-pages.yml` 檔案已在本機小教室Grok版資料夾內準備完成（標準 static pages deploy action）。
  - 推薦改用 GitHub Actions 部署（更穩定）：
    1. 去 https://github.com/snowsepch/workshop-generator-grok 點「Add file」→「Create new file」
    2. 檔名輸入 `.github/workflows/deploy-pages.yml`
    3. 內容從本機資料夾的 `.github/workflows/deploy-pages.yml` 複製貼上（或直接在本機 `git add .github/ && git commit && git push`，但需先用 `gh auth login` 帶 `workflow` scope 刷新 token）。
    4. Commit 後，Actions 會自動部署，完成後即可用 https://snowsepch.github.io/workshop-generator-grok/ 開啟
  - 注意：gh CLI 目前的 token 缺少 `workflow` scope，所以無法直接 push workflow 檔（安全機制）。建議優先用 GitHub 網頁 UI 新增，或本地 re-auth 後再 push。
- 原本 repo 的 main 仍維持原版（Grok 版永遠只在這個新 repo）。

## 4. 資料保護與隱私注意事項（公開 repo 必讀）
- **已採取的保護措施**（2026-06 更新）：
  - GITHUB_REPOS_STATUS.md 內的本地路徑已匿名化（從 `/Users/sep/...` 改為 `~/小教室Grok版/` 通用寫法）。
  - 移除所有 "Lala" 個人提及。
  - 新增 `.gitignore`：排除 .DS_Store、*.log、local-*、暫存檔等，避免個人檔案或 OS 快取意外上傳。
  - Git 作者資訊（snowsepch + 個人 email）已存在於歷史中，無法輕易移除（需 rewrite history，風險高）。未來 commit 請使用隱私 email。
- **未來開發保護規則**：
  - 絕對不要在任何公開檔案中寫真實本地路徑（用 `~` 或「你的 iCloud 路徑」代替）。
  - 門市設定只存 LocalStorage（瀏覽器端），不會進 repo。
  - 截圖（歷史版本/）只保留 UI，注意不要包含真實店名或個人畫面。
  - 每次 commit 前確認 `git status` 沒有敏感檔。
- **Git 隱私建議**（在本機執行一次）：
  ```bash
  git config user.name "你的顯示名稱"
  git config user.email "你的名稱+ID@users.noreply.github.com"  # GitHub 隱私 email
  ```
  並在 GitHub 帳號設定開啟 "Keep my email addresses private"。
- 原本 repo 的 main 仍維持原版（Grok 版永遠只在這個新 repo）。

## 5. 重要提醒（給未來自己）
- 這個資料夾（小教室Grok版）永遠只放 Grok 版。
- 原本 repo 的 main 已經回復，不要混淆。
- 所有內容都已依照使用者要求：台灣用語、25-30分動手實作、情境式融合標題、實際操作課程邏輯等完成。
- 有任何 repo 相關疑問，可參考本檔案 + README.md。

---
此檔案為「正確狀態記憶」，未來對話請以此為準。