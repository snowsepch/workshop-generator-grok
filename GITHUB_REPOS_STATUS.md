# GitHub Repos 當前正確狀態（Grok 版獨立後）

**更新日期**：2026 年最新狀態

## 1. 原本小教室專案 Repo（不要動）
- **網址**：https://github.com/snowsepch/workshop-generator
- **main 分支**：已完全回復到 Grok 大改之前的原版（commit d0452d2：「移除兒童(6-12)年齡層；內容改為隨年齡層調整語氣與重點」）
  - 原本的 GitHub 連結（raw、Pages 等）現在應該都指向正確的原版內容。
- **grok 分支**：保留了 Grok 版的備份（可作為參考或緊急備份使用）
- **注意**：這個 repo 的 main 請維持原版，不要再直接 push Grok 內容進去。

## 2. Grok 版（目前這個資料夾）
- **本地位置**：`/Users/sep/Library/Mobile Documents/com~apple~CloudDocs/小教室Grok版/`
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
- **GitHub Pages 部署**：
  - 目前使用 legacy source + .nojekyll 設定（已推）。
  - 推薦改用 GitHub Actions 部署（更穩定）：
    1. 去 https://github.com/snowsepch/workshop-generator-grok 點「Add file」→「Create new file」
    2. 檔名輸入 `.github/workflows/deploy-pages.yml`
    3. 內容從本機資料夾的 `.github/workflows/deploy-pages.yml` 複製貼上（或見下方程式碼）
    4. Commit 後，Actions 會自動部署，完成後即可用 https://snowsepch.github.io/workshop-generator-grok/ 開啟
  - 注意：gh CLI 目前的 token 缺少 `workflow` scope，所以無法直接 push workflow 檔（安全機制），需用網頁或重新 `gh auth login` 時勾選 workflow 權限。
- 原本 repo 的 main 仍維持原版（Grok 版永遠只在這個新 repo）。

## 4. 重要提醒（給未來自己）
- 這個資料夾（小教室Grok版）永遠只放 Grok 版。
- 原本 repo 的 main 已經回復，不要混淆。
- 所有內容都已依照 Lala 的要求：台灣用語、25-30分動手實作、情境式融合標題、實際操作課程邏輯等完成。
- 有任何 repo 相關疑問，可參考本檔案 + README.md。

---
此檔案為「正確狀態記憶」，未來對話請以此為準。