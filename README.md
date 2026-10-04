# 泼冷水 Skill ／ Calm-Down Skill（开源项目 reality-check）

一个**可复制粘贴到任意 agent** 的评审 prompt。面对"GitHub 又炸了 / 开源圈又炸了"之类的夸大宣传时，
让 agent 自动搜 GitHub 热门项目（或你指定的项目），产出一份"泼冷水"报告，帮新手快速看清项目到底适不适合自己。
A copy-paste prompt for any agent. When faced with hype like "GitHub is on fire again / the open-source world is exploding",
it makes the agent search GitHub trending projects (or a project you name) and produce a "cold-water" report,
so beginners can quickly see whether a project actually fits them.

GitHub 仓库 ／ Repo: https://github.com/phenoCS/calmdown_skill

## 它解决什么 ／ What it solves
- 开源项目多、跟风下载多，但很多项目**实测并不好用 / 有隐藏硬件门槛**。
  Many open-source projects get downloaded on hype, yet plenty **don't work well in practice / hide hardware requirements**.
- 短视频博主常用 AI 配文夸大事实（"AI 圈又炸了"），新手容易点赞收藏后真用才发现没用。
  Short-video creators exaggerate with AI-written captions ("the AI world is exploding"), so newbies like & save, then find it useless.
- 本 skill 把「宣传」和「真实门槛」拆开摆，报告三项：①用户口碑 ②使用限制 ③推荐指数(1–5星)。
  This skill separates **marketing** from **real barriers**, reporting three things: ① reputation ② limitations ③ rating (1–5 stars).

## 怎么用（两种模式）／ How to use (two modes)
1. **随机模式 ／ Random**：打开任意支持联网的 agent，把 `泼冷水skill.md` 全文粘贴进去，发送「随机挑 3 个热门项目评一下」。
   Open any internet-capable agent, paste the full `泼冷水skill.md`, and send "pick 3 trending projects and review them".
2. **指定模式 ／ Specified**：粘贴 skill 后，发送「评一下这个项目：<项目名或 GitHub 链接>」。
   After pasting, send "review this project: <name or GitHub link>".

两种模式最终都输出同一格式的 Markdown 报告。
Both modes output a Markdown report in the same format.

## 文件说明 ／ Files
- `泼冷水skill.md` —— **核心**，复制它粘贴给 agent 即可。／ **Core file** — copy and paste it to the agent.
- `example-report.md` —— 一份示例报告，看产出长什么样。／ A sample report showing the output shape.
- `README.md` —— 本文件。／ This file.

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
  For more automation: pair with GitHub API / search tools to pull candidates and Issues first, then let the skill report.
- 想常驻：部分 agent 支持把本 prompt 注册为"skill/指令"，按平台说明导入即可。
  To make it permanent: some agents let you register this prompt as a "skill/command" — import per platform docs.
- 想要英文版 skill：可把 `泼冷水skill.md` 也做成双语或纯英文版，方便只说英文的用户。
  Want an English skill: make `泼冷水skill.md` bilingual or English-only for English-only users.
