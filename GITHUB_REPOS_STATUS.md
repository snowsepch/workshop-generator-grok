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
- **目前狀態**：
  - 這是一個**全新的獨立 git repo**（已移除舊 .git 歷史）。
  - 只有 Grok 版的內容：
    - index.html（完整最新版，包含所有修正）
    - README.md（詳細說明差異與使用方式）
    - 歷史版本/（舊版 UI 截圖）
    - 各階段版本對照 JPG
  - 目前 branch：main
  - 初始 commit：339768c "Initial commit: Apple Shop 小教室專案 Grok 版"
  - **尚未設定任何 remote**（準備好推到全新的獨立 GitHub repo）
- **建議新 repo 名稱**（建立時使用）：
  - `小教室Grok版`
  - 或 `apple-shop-xiao-jiao-shi-grok`
  - 或 `workshop-generator-grok`

## 3. 未來上傳方式
1. 在 GitHub 建立全新空白 repo（不要自動產生 README）。
2. 複製新 repo 的 HTTPS 或 SSH 網址。
3. 在本資料夾執行：
   ```bash
   git remote add origin <新repo網址>
   git branch -M main
   git push -u origin main
   ```
4. 以後所有 Grok 版的開發與上傳，都在這個新 repo 進行。

## 4. 重要提醒（給未來自己）
- 這個資料夾（小教室Grok版）永遠只放 Grok 版。
- 原本 repo 的 main 已經回復，不要混淆。
- 所有內容都已依照 Lala 的要求：台灣用語、25-30分動手實作、情境式融合標題、實際操作課程邏輯等完成。
- 有任何 repo 相關疑問，可參考本檔案 + README.md。

---
此檔案為「正確狀態記憶」，未來對話請以此為準。