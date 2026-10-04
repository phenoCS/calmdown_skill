# 泼冷水 Skill ／ Calm-Down Skill（开源项目 reality-check）

一个**可复制粘贴到任意 agent** 的评审 prompt。面对"GitHub 又炸了 / 开源圈又炸了"之类的夸大宣传时，
让 agent 自动搜 GitHub 热门项目（或你指定的项目），产出一份"泼冷水"报告，帮新手快速看清项目到底适不适合自己。
A copy-paste prompt for any agent. When faced with hype like "GitHub is on fire again / the open-source world is exploding",
it makes the agent search GitHub trending projects (or a project you name) and produce a "cold-water" report,
so beginners can quickly see whether a project actually fits them.

GitHub 仓库 ／ Repo: https://github.com/phenoCS/calmdown_skill

## 文件说明 ／ Files
- `SKILL.md` —— **CodeBuddy 专用入口**。放进 CodeBuddy 的 skills 目录即可被技能列表识别（见下方"方式一"）。
  CodeBuddy-specific entry. Place it in CodeBuddy's skills dir to appear in the skill list (see Method 1).
- `泼冷水skill.md` —— **通用粘贴版**。任何 agent（Claude Code / Codex / ChatGPT / 网页 agent）都能直接粘贴使用。
  Universal paste version. Any agent can use it by pasting directly.
- `claude-code/calmdown.md` —— 给 **Claude Code** 的斜杠命令文件（已带 frontmatter），丢进 `.claude/commands/` 即可。
  Ready-to-use slash-command file for Claude Code (frontmatter included).
- `codex/AGENTS.md.example` —— 给 **Codex** 的指令片段，追加进你的 `AGENTS.md` 即可常驻生效。
  Ready-to-use instruction snippet for Codex; append into your AGENTS.md.
- `example-report.md` —— 一份示例报告，看产出长什么样。A sample report.

## 怎么装到你的 agent ／ Install into your agent

### 方式一：CodeBuddy（最省事，原生技能）
1. 把 `SKILL.md` 放进你的用户技能目录（目录名随意，文件必须叫 `SKILL.md`）：
   - Windows：`C:\Users\<你>\.codebuddy\skills\calmdown_skill\SKILL.md`
   - macOS / Linux：`~/.codebuddy/skills/calmdown_skill/SKILL.md`
2. **重开 / 刷新 CodeBuddy 会话**（技能是加载时扫描的，不会热更新）。
3. 对话里调用技能 `calmdown-skill`（或输入 `/` 选技能），然后说「随机评 3 个」或「评 <项目名/链接>」。

> ⚠️ 关键：目录里**必须有 `SKILL.md`（带 `name`/`description` 头）**，CodeBuddy 才认。
> 光有 `泼冷水skill.md` 不会显示在技能列表里——这就是早期版本"装了却看不到"的原因。
> Key: the dir MUST contain `SKILL.md` with `name`/`description` frontmatter, or CodeBuddy ignores it.

### 方式二：Claude Code（斜杠命令）
1. 把仓库里的 `claude-code/calmdown.md` 复制到：
   - 用户级：`~/.claude/commands/calmdown.md`
   - 或项目级：`<你的项目>/.claude/commands/calmdown.md`
2. 对话里输入 `/calmdown` 走随机模式，或 `/calmdown <项目名或URL>` 评指定项目。
   （文件顶部已有 `description` frontmatter，Claude Code 会自动识别为命令；`<项目名>` 会作为 `$ARGUMENTS` 传入。）

### 方式三：Codex（常驻指令）
1. 把 `codex/AGENTS.md.example` 的内容**追加**进你的 `AGENTS.md`：
   - 全局：`~/.codex/AGENTS.md`
   - 或项目根：`AGENTS.md`
2. Codex 每次执行前会读取 `AGENTS.md`，之后直接说「随机评 3 个开源项目」或「评 <项目名/链接>」即可。

### 方式四：任意网页 / 聊天 agent（ChatGPT、元宝、网页版 Claude 等）
直接把 `泼冷水skill.md` 全文粘贴到对话，再发「随机评 3 个」或「评 <项目名>」。

## 怎么用（两种模式）／ How to use (two modes)
1. **随机模式 ／ Random**：发送「随机挑 3 个热门项目评一下」→ 出 3 份报告。
   Send "pick 3 trending projects and review them" → 3 reports.
2. **指定模式 ／ Specified**：发送「评一下这个项目：<项目名或 GitHub 链接>」→ 出 1 份报告。
   Send "review this project: <name or GitHub link>" → 1 report.
两种模式最终都输出同一格式的 Markdown 报告（口碑 / 使用限制 / 推荐指数 1–5 星）。
Both modes output a Markdown report in the same format (reputation / limitations / rating 1–5 stars).

## 设计原则（已写进 skill）／ Design principles (baked into the skill)
- 不编造：只写真搜到的内容并附链接，搜不到就写"未找到明确反馈"。
  No fabrication: only write what was actually found, with links; if nothing found, say "no clear feedback found".
- 区分"官方宣传"与"社区实测"。
  Separate "official claims" from "community testing".
- 评分固定 rubric，避免 agent 乱打分。
  Fixed scoring rubric, so the agent can't score randomly.
- 用户视角：新手下载后能否轻松用，才是高分标准。
  User perspective: whether a beginner can use it easily is the only high-score criterion.

## 可选进阶 ／ Optional next steps
- 想更自动：可在 agent 里配合 GitHub API / 搜索工具先拉候选项目和 Issues，再让本 skill 出报告。
  For more automation: pair with GitHub API / search tools to pull candidates and Issues first.
- 想常驻：按上面"方式二/三"把 prompt 注册为 Claude Code 命令或 Codex 指令即可，不用每次粘贴。
  To make it permanent: register as a Claude Code command or Codex instruction per Method 2/3.
