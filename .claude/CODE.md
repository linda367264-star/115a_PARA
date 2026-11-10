#程式碼的撰寫原則

*程式碼依照 SOLID DRY OOP 習慣原則

#命名與結構（待確認）
- 類別、方法使用 PascalCase；區域變數、參數使用 camelCase
- 一個 .cs 檔案只放一個主要類別，檔名與類別名稱相同
- 可重用的演算法邏輯放在 `src/`；GH 介面與輸入輸出綁定放在 `gh_script/`
- `gh_script/` 內的 `#load` 路徑統一由一個變數指定 `src/` 位置，避免硬寫路徑