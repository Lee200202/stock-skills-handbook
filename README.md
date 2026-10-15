# 盤勢有據｜工作規格與技能手冊

線上閱讀：**[開啟互動手冊](https://lee200202.github.io/stock-skills-handbook/)**

這是盤勢有據專案的公開工作規格索引，整理 2026/10/03–10/15 討論中確認的網站視覺、內容分類、公開文字、規則調整、行情計算、自動化續跑、發布驗收、網站 AI 助理與協作授權經驗。讀者可以搜尋規格、操作十站流程圖與分類圖卡、展開完整內容，以及複製 19 組常用請求。

## 內容

- `index.html`：自足的互動手冊，支援手機、深淺色、鍵盤及減少動態；沒有 JavaScript 仍可閱讀。
- `常用工作規格與指令.md`：角色、共用規格、請求範本和常見錯誤。
- `skills/`：九個 Stock skills 的入口與詳細參考文件（2026/10/15 新增 `stock-public-writing`、`stock-rule-tuning`、`stock-assistant`、`stock-collaboration`，其餘五個併入新規則）。
- `驗收紀錄.md`：手冊建立當時的本機驗收範圍。
- `scripts/build_stock_skill_handbook.py`：由 Markdown 重建 HTML。

這個靜態網站不會呼叫模型、讀取正式股票資料或發送通知。分類及計價是原專案的產品規則，不是投資報酬保證。文中的本機路徑與指令以原專案為情境；其他專案使用時需要調整。

## 維護

資料來源為 [Lee200202/Stock 的 stock-skills 目錄](https://github.com/Lee200202/Stock/tree/main/docs/stock-skills)，初始內容對應提交 `2c3fcea`，九個技能版本對應 `73952a3`。本儲存庫提供獨立的公開閱讀網址，首次發布的 HTML 與來源檔一致。

在本儲存庫修改 Markdown 後，可執行：

```sh
python -m pip install -r requirements.txt
python scripts/build_stock_skill_handbook.py
```

不帶參數只重建 HTML，不安裝技能。只有明確需要更新本機 Codex 的九個 Stock skills 時才使用 `--install`；可用 `--check-installed` 比對副本。此操作不會更改其他技能。

本儲存庫以 GitHub Pages 的 `main` 分支根目錄發布；`.nojekyll` 讓手冊、中文 Markdown 與技能來源保留原路徑。修改並推送後，仍須確認 Pages 建置與線上內容。
