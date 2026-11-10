---
name: git
description: 依照專案的 .claude/GIT.md 原則進行 git commit（conventional commit、繁體中文、簡潔）。當使用者輸入 /git 或要求 commit 時使用。
---

# git commit 技能

## 步驟

1. 讀取 `/Users/jialing/115a_PARA/.claude/GIT.md`，依其中的原則撰寫 commit 訊息。每次都要重新讀取，不要沿用舊記憶。
2. 執行 `git status` 與 `git diff`（含 staged 與 unstaged），確認要提交的變更內容。
3. 只加入與本次變更相關的檔案，避免加入不相關或敏感檔案（如密鑰、`.env`）。若不確定，先問使用者。
4. 撰寫 commit 訊息：
   - 格式：`<type>: <簡潔繁體中文描述>`，type 採 conventional commit（feat、fix、docs、refactor、chore、test、style 等）。
   - 第一行簡潔明瞭；需要時再空一行補充說明。
   - 不加入任何 AI 署名（例如 Co-Authored-By），依 GIT.md 規定。
5. 使用 heredoc 執行 `git commit -F -`，避免引號與換行問題。
6. 執行 `git log --oneline -1` 與 `git status --short`，回報 commit 雜湊值與工作區狀態。

## 注意事項

- 不要 push，除非使用者明確要求。
- 不要使用 `--no-verify`、`--amend` 或 `reset` 等改寫歷史的指令，除非使用者明確要求。
- 若沒有任何變更可提交，直接告知使用者，不要建立空 commit。
- 只提交與本次任務相關的變更；工作區中其他人修改的檔案（例如 GIT.md、CLAUDE.md）若不是本次任務內容，保持未提交並告知使用者。
