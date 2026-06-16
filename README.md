# AI 二創影片導演 Skill

可發佈的 Agent Skill repo，用來把 AI 二創影片想法整理成完整製作包：需求確認、素材盤點、劇本、分鏡、素材生成提示詞與逐鏡影片提示詞。

## 支援的 Agent

這個 Skill 採用標準 Agent Skills 結構：

```text
skills/ai-fan-video-director/SKILL.md
```

已知可透過 `npx skills` 安裝到：

- Codex
- Claude Code
- Cursor
- OpenCode
- 其他支援 Agent Skills 標準或 `npx skills` 的 Agent

## 安裝方式

發佈到 GitHub 後，請把 `yourname` 換成你的 GitHub 帳號或組織名稱：

```bash
npx skills@latest add yourname/ai-fan-video-skill --skill ai-fan-video-director
```

指定安裝到常見 Agent：

```bash
npx skills@latest add yourname/ai-fan-video-skill --skill ai-fan-video-director -a codex
npx skills@latest add yourname/ai-fan-video-skill --skill ai-fan-video-director -a claude-code
npx skills@latest add yourname/ai-fan-video-skill --skill ai-fan-video-director -a cursor
npx skills@latest add yourname/ai-fan-video-skill --skill ai-fan-video-director -a opencode
```

本機測試：

```bash
npx skills@latest add ./ai-fan-video-skill --skill ai-fan-video-director
```

Codex 也可以透過內建 `$skill-installer` 安裝：

```text
$skill-installer install https://github.com/yourname/ai-fan-video-skill/tree/main/skills/ai-fan-video-director
```

## Skill 內容

- `ai-fan-video-director`: 引導 AI 二創影片規劃，預設支援 Updream/Seedance-style 工作流，但會先確認目前模型限制與素材狀態。

這個 Skill 會協助產出：

- 專案簡介
- 已確認的模型限制
- 素材清單與缺口
- 角色、道具、場景補素材提示詞
- 故事劇本
- 分鏡表
- 逐鏡影片生成提示詞
- 鏡頭銜接與重抽建議
- 合規改編建議

## 發佈到 GitHub

初始化後可用：

```bash
git remote add origin https://github.com/yourname/ai-fan-video-skill.git
git push -u origin main
git push origin v1.0.0
```

如果要用 GitHub CLI 建立 repo：

```bash
gh repo create yourname/ai-fan-video-skill --public --source . --remote origin --push
git push origin v1.0.0
```

## 備註

- Skill 內容使用繁體中文。
- 影片生成提示詞跟隨使用者輸入語言。
- 不內建 scripts，這是純文字引導與提示詞製作型 Skill。
- 發佈前請把 README 裡的 `yourname` 換成你的 GitHub 帳號或組織名稱。
