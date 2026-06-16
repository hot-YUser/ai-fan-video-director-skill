# AI 二創影片導演 Skill

把 AI 二創影片想法整理成完整製作包：需求確認、素材盤點、劇本、分鏡、素材生成提示詞與逐鏡影片提示詞。

## 快速安裝

安裝到目前偵測到的 Agent：

```bash
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director
```

指定 Agent：

```bash
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director -a codex
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director -a claude-code
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director -a cursor
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director -a opencode
```

安裝到全部支援的 Agent：

```bash
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director --agent '*'
```

全域安裝：

```bash
npx skills@latest add hot-YUser/ai-fan-video-director-skill --skill ai-fan-video-director --global
```

本機測試：

```bash
npx skills@latest add ./ai-fan-video-skill --skill ai-fan-video-director
```

Codex 內建安裝器：

```text
$skill-installer install https://github.com/hot-YUser/ai-fan-video-director-skill/tree/main/skills/ai-fan-video-director
```

## Skill 內容

- `ai-fan-video-director`：引導 AI 二創影片規劃，預設支援 Updream/Seedance-style 工作流，但會先確認目前模型限制與素材狀態。

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

## 支援的 Agent

本 repo 採用標準 Agent Skills 結構：

```text
skills/ai-fan-video-director/SKILL.md
```

以下支援矩陣來自 [`vercel-labs/skills`](https://github.com/vercel-labs/skills#supported-agents) 的 Supported Agents 表，於 2026-06-17 查核。Antigravity 2.0 使用表中的 `Antigravity` / `antigravity` 目標。

| Agent | `npx skills --agent` | 專案內原生路徑 | 全域原生路徑 |
|---|---|---|---|
| AiderDesk | `aider-desk` | `.aider-desk/skills/` | `~/.aider-desk/skills/` |
| Amp, Replit, Universal | `amp`, `replit`, `universal` | `.agents/skills/` | `~/.config/agents/skills/` |
| Antigravity | `antigravity` | `.agents/skills/` | `~/.gemini/antigravity/skills/` |
| Antigravity CLI | `antigravity-cli` | `.agents/skills/` | `~/.gemini/antigravity-cli/skills/` |
| AstrBot | `astrbot` | `data/skills/` | `~/.astrbot/data/skills/` |
| Autohand Code CLI | `autohand-code` | `.autohand/skills/` | `~/.autohand/skills/` |
| Augment | `augment` | `.augment/skills/` | `~/.augment/skills/` |
| IBM Bob | `bob` | `.bob/skills/` | `~/.bob/skills/` |
| Claude Code | `claude-code` | `.claude/skills/` | `~/.claude/skills/` |
| OpenClaw | `openclaw` | `skills/` | `~/.openclaw/skills/` |
| Cline, Dexto, Kimi Code CLI, Loaf, Warp, Zed | `cline`, `dexto`, `kimi-code-cli`, `loaf`, `warp`, `zed` | `.agents/skills/` | `~/.agents/skills/` |
| CodeArts Agent | `codearts-agent` | `.codeartsdoer/skills/` | `~/.codeartsdoer/skills/` |
| CodeBuddy | `codebuddy` | `.codebuddy/skills/` | `~/.codebuddy/skills/` |
| Codemaker | `codemaker` | `.codemaker/skills/` | `~/.codemaker/skills/` |
| Code Studio | `codestudio` | `.codestudio/skills/` | `~/.codestudio/skills/` |
| Codex | `codex` | `.agents/skills/` | `~/.codex/skills/` |
| Command Code | `command-code` | `.commandcode/skills/` | `~/.commandcode/skills/` |
| Continue | `continue` | `.continue/skills/` | `~/.continue/skills/` |
| Cortex Code | `cortex` | `.cortex/skills/` | `~/.snowflake/cortex/skills/` |
| Crush | `crush` | `.crush/skills/` | `~/.config/crush/skills/` |
| Cursor | `cursor` | `.agents/skills/` | `~/.cursor/skills/` |
| Deep Agents | `deepagents` | `.agents/skills/` | `~/.deepagents/agent/skills/` |
| Devin for Terminal | `devin` | `.devin/skills/` | `~/.config/devin/skills/` |
| Droid | `droid` | `.factory/skills/` | `~/.factory/skills/` |
| Firebender | `firebender` | `.agents/skills/` | `~/.firebender/skills/` |
| ForgeCode | `forgecode` | `.forge/skills/` | `~/.forge/skills/` |
| Gemini CLI | `gemini-cli` | `.agents/skills/` | `~/.gemini/skills/` |
| GitHub Copilot | `github-copilot` | `.agents/skills/` | `~/.copilot/skills/` |
| Goose | `goose` | `.goose/skills/` | `~/.config/goose/skills/` |
| Hermes Agent | `hermes-agent` | `.hermes/skills/` | `~/.hermes/skills/` |
| inference.sh | `inference-sh` | `.inferencesh/skills/` | `~/.inferencesh/skills/` |
| Jazz | `jazz` | `.jazz/skills/` | `~/.jazz/skills/` |
| Junie | `junie` | `.junie/skills/` | `~/.junie/skills/` |
| iFlow CLI | `iflow-cli` | `.iflow/skills/` | `~/.iflow/skills/` |
| Kilo Code | `kilo` | `.kilocode/skills/` | `~/.kilocode/skills/` |
| Kiro CLI | `kiro-cli` | `.kiro/skills/` | `~/.kiro/skills/` |
| Kode | `kode` | `.kode/skills/` | `~/.kode/skills/` |
| Lingma | `lingma` | `.lingma/skills/` | `~/.lingma/skills/` |
| MCPJam | `mcpjam` | `.mcpjam/skills/` | `~/.mcpjam/skills/` |
| Mistral Vibe | `mistral-vibe` | `.vibe/skills/` | `~/.vibe/skills/` |
| Moxby | `moxby` | `.moxby/skills/` | `~/.moxby/skills/` |
| Mux | `mux` | `.mux/skills/` | `~/.mux/skills/` |
| OpenCode | `opencode` | `.agents/skills/` | `~/.config/opencode/skills/` |
| OpenHands | `openhands` | `.openhands/skills/` | `~/.openhands/skills/` |
| Ona | `ona` | `.ona/skills/` | `~/.ona/skills/` |
| Pi | `pi` | `.pi/skills/` | `~/.pi/agent/skills/` |
| Qoder | `qoder` | `.qoder/skills/` | `~/.qoder/skills/` |
| Qoder CN | `qoder-cn` | `.qoder/skills/` | `~/.qoder-cn/skills/` |
| Qwen Code | `qwen-code` | `.qwen/skills/` | `~/.qwen/skills/` |
| Reasonix | `reasonix` | `.reasonix/skills/` | `~/.reasonix/skills/` |
| Rovo Dev | `rovodev` | `.rovodev/skills/` | `~/.rovodev/skills/` |
| Roo Code | `roo` | `.roo/skills/` | `~/.roo/skills/` |
| Tabnine CLI | `tabnine-cli` | `.tabnine/agent/skills/` | `~/.tabnine/agent/skills/` |
| Terramind | `terramind` | `.terramind/skills/` | `~/.terramind/skills/` |
| Tinycloud | `tinycloud` | `.tinycloud/skills/` | `~/.tinycloud/skills/` |
| Trae | `trae` | `.trae/skills/` | `~/.trae/skills/` |
| Trae CN | `trae-cn` | `.trae/skills/` | `~/.trae-cn/skills/` |
| Windsurf | `windsurf` | `.windsurf/skills/` | `~/.codeium/windsurf/skills/` |
| Zencoder, Zenflow | `zencoder`, `zenflow` | `.zencoder/skills/` | `~/.zencoder/skills/` |
| Neovate | `neovate` | `.neovate/skills/` | `~/.neovate/skills/` |
| Pochi | `pochi` | `.pochi/skills/` | `~/.pochi/skills/` |
| PromptScript | `promptscript` | `.agents/skills/` | N/A（僅支援專案內安裝） |
| AdaL | `adal` | `.adal/skills/` | `~/.adal/skills/` |

## 發佈資訊

目前 GitHub repo：

```text
https://github.com/hot-YUser/ai-fan-video-director-skill
```

驗證 Skill：

```bash
python C:/Users/YUser/.codex/skills/.system/skill-creator/scripts/quick_validate.py skills/ai-fan-video-director
```

列出可安裝 Skill：

```bash
npx skills@latest add hot-YUser/ai-fan-video-director-skill --list
```

發佈新版本：

```bash
git tag -a vX.Y.Z -m "vX.Y.Z"
git push origin main
git push origin vX.Y.Z
```

## 備註

- Skill 內容使用繁體中文。
- 影片生成提示詞跟隨使用者輸入語言。
- 不內建 scripts，這是純文字引導與提示詞製作型 Skill。
- 支援矩陣的路徑由 `npx skills` 生態提供；各 Agent 若改版，請以 `vercel-labs/skills` 最新 README 為準。
