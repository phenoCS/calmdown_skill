<h1 align="center">🌊 泼冷水 Skill · Calm-Down Skill</h1>

<p align="center">
给被吹爆的开源项目做 reality-check ／ A reality-check for over-hyped open-source projects
</p>

<details open>
<summary><b>🇨🇳 中文</b>（点击展开／收起）</summary>
<br>

一个可复制粘贴到<b>任意 agent</b> 的评审 prompt。面对「GitHub 又炸了」式的夸大宣传，让 agent 联网核对官方文档与 Issues，产出一份冷静报告：区分<b>官方宣传 vs 社区实测</b>，列出硬性门槛，给出 1–5 星推荐指数。

## 文件说明

| 文件 | 用途 |
| --- | --- |
| `SKILL.md` | CodeBuddy 专用入口 |
| `泼冷水skill.md` | 通用粘贴版，任意 agent 可用 |
| `claude-code/calmdown.md` | Claude Code 斜杠命令 |
| `codex/AGENTS.md.example` | Codex 常驻指令片段 |
| `example-report.md` | 示例报告 |

## 装到你的 agent

- **CodeBuddy**：把 `SKILL.md` 放进 `~/.codebuddy/skills/calmdown_skill/`，重开会话即可在技能列表看到 `calmdown-skill`。
- **Claude Code**：把 `claude-code/calmdown.md` 放进 `~/.claude/commands/`，用 `/calmdown <项目>` 调用。
- **Codex**：把 `codex/AGENTS.md.example` 内容追加进 `AGENTS.md`，直接说「评某某」。
- **任意 agent**：把 `泼冷水skill.md` 全文粘贴即可。

## 怎么用

- **随机**：发「随机挑 3 个热门项目评一下」→ 3 份报告
- **指定**：发「评 <项目名或 GitHub 链接>」→ 1 份报告

## 设计原则

不编造 · 区分宣传与实测 · 固定评分标准 · 站新手视角

## 进阶

配合 GitHub API / 搜索工具先拉候选项目与 Issues，再让本 skill 出报告。

</details>

<details>
<summary><b>🇬🇧 English</b> (click to expand / collapse)</summary>
<br>

A copy-paste prompt for <b>any agent</b>. Faced with hype like "GitHub is on fire again", it makes the agent search official docs and Issues, then produces a cool-headed report: separating <b>official claims vs community testing</b>, listing hard requirements, and giving a 1–5 star rating.

## Files

| File | Purpose |
| --- | --- |
| `SKILL.md` | CodeBuddy-specific entry |
| `泼冷水skill.md` | Universal paste version |
| `claude-code/calmdown.md` | Claude Code slash command |
| `codex/AGENTS.md.example` | Codex instruction snippet |
| `example-report.md` | Sample report |

## Install into your agent

- **CodeBuddy**: place `SKILL.md` in `~/.codebuddy/skills/calmdown_skill/`, then restart the session to see `calmdown-skill` in the list.
- **Claude Code**: place `claude-code/calmdown.md` in `~/.claude/commands/`, call with `/calmdown <project>`.
- **Codex**: append `codex/AGENTS.md.example` into your `AGENTS.md`, then just say "review X".
- **Any agent**: paste the full text of `泼冷水skill.md`.

## Usage

- **Random**: send "pick 3 trending projects and review them" → 3 reports
- **Specified**: send "review <name or GitHub link>" → 1 report

## Principles

No fabrication · Separate hype from testing · Fixed rubric · Beginner-first

## Next steps

Pair with the GitHub API / search tools to pull candidates and Issues first, then let the skill write the report.

</details>

---

<p align="center">
仓库 ／ Repo：<a href="https://github.com/phenoCS/calmdown_skill">github.com/phenoCS/calmdown_skill</a>
</p>
