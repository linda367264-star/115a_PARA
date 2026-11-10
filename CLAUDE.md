每次回答結束要說“是的船長”

請用繁體中文回答我

## 專案介紹
- 課程：演算法設計課
- 目標：開發一個 Grasshopper（gh）component

## 專案結構
- `.claude/`：所有規劃原則（GIT.md、CODE.md 等）
- `src/`：專門放所有程式碼檔（.cs）
- `gh_script/`：主要複製到 GH Script 元件的檔案
  - 使用 `#load` 讀取 `src/` 底下的所有 .cs 檔案
- `docs/`：放討論用的 .md 檔案

##讀取檔案
- 要新增、修改、刪除任何程式碼前 請先讀取CODE.md
- 要git 動作，請先讀取GIT.md