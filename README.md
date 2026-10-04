<div class="cd" align="center">
<input type="radio" id="cd-sw-zh" name="cd-sw" checked hidden>
<input type="radio" id="cd-sw-en" name="cd-sw" hidden>

<div class="cd-head">
  <h1>🌊 泼冷水 Skill</h1>
  <p class="cd-sub">给被吹爆的开源项目做 reality-check</p>
  <div class="cd-switch">
    <label for="cd-sw-zh" class="cd-btn">中文</label>
    <label for="cd-sw-en" class="cd-btn">EN</label>
  </div>
</div>

<!-- ============ 中文 ============ -->
<div class="cd-zh">

<p>一个可复制粘贴到<strong>任意 agent</strong>的评审 prompt。面对「GitHub 又炸了」式的夸大宣传，让 agent 联网核对官方文档与 Issues，产出一份冷静报告：区分<b>官方宣传 vs 社区实测</b>，列出硬性门槛，给出 1–5 星推荐指数。</p>

<h2>文件说明</h2>
<table>
  <tr><th>文件</th><th>用途</th></tr>
  <tr><td><code>SKILL.md</code></td><td>CodeBuddy 专用入口</td></tr>
  <tr><td><code>泼冷水skill.md</code></td><td>通用粘贴版，任意 agent 可用</td></tr>
  <tr><td><code>claude-code/calmdown.md</code></td><td>Claude Code 斜杠命令</td></tr>
  <tr><td><code>codex/AGENTS.md.example</code></td><td>Codex 常驻指令片段</td></tr>
  <tr><td><code>example-report.md</code></td><td>示例报告</td></tr>
</table>

<h2>装到你的 agent</h2>
<ul>
  <li><b>CodeBuddy</b>：把 <code>SKILL.md</code> 放进 <code>~/.codebuddy/skills/calmdown_skill/</code>，重开会话即可在技能列表看到 <code>calmdown-skill</code>。</li>
  <li><b>Claude Code</b>：把 <code>claude-code/calmdown.md</code> 放进 <code>~/.claude/commands/</code>，用 <code>/calmdown &lt;项目&gt;</code> 调用。</li>
  <li><b>Codex</b>：把 <code>codex/AGENTS.md.example</code> 内容追加进 <code>AGENTS.md</code>，直接说「评某某」。</li>
  <li><b>任意 agent</b>：把 <code>泼冷水skill.md</code> 全文粘贴即可。</li>
</ul>

<h2>怎么用</h2>
<ul>
  <li><b>随机</b>：发「随机挑 3 个热门项目评一下」</li>
  <li><b>指定</b>：发「评 &lt;项目名或 GitHub 链接&gt;」</li>
</ul>

<h2>设计原则</h2>
<p>不编造 · 区分宣传与实测 · 固定评分标准 · 站新手视角</p>

<h2>进阶</h2>
<p>配合 GitHub API / 搜索工具先拉候选项目与 Issues，再让本 skill 出报告。</p>

<p class="cd-repo">仓库：<a href="https://github.com/phenoCS/calmdown_skill">github.com/phenoCS/calmdown_skill</a></p>

</div>

<!-- ============ English ============ -->
<div class="cd-en">

<p>A copy-paste prompt for <strong>any agent</strong>. Faced with hype like "GitHub is on fire again", it makes the agent search official docs and Issues, then produces a cool-headed report: separating <b>official claims vs community testing</b>, listing hard requirements, and giving a 1–5 star rating.</p>

<h2>Files</h2>
<table>
  <tr><th>File</th><th>Purpose</th></tr>
  <tr><td><code>SKILL.md</code></td><td>CodeBuddy-specific entry</td></tr>
  <tr><td><code>泼冷水skill.md</code></td><td>Universal paste version</td></tr>
  <tr><td><code>claude-code/calmdown.md</code></td><td>Claude Code slash command</td></tr>
  <tr><td><code>codex/AGENTS.md.example</code></td><td>Codex instruction snippet</td></tr>
  <tr><td><code>example-report.md</code></td><td>Sample report</td></tr>
</table>

<h2>Install into your agent</h2>
<ul>
  <li><b>CodeBuddy</b>: place <code>SKILL.md</code> in <code>~/.codebuddy/skills/calmdown_skill/</code>, then restart the session to see <code>calmdown-skill</code> in the list.</li>
  <li><b>Claude Code</b>: place <code>claude-code/calmdown.md</code> in <code>~/.claude/commands/</code>, call with <code>/calmdown &lt;project&gt;</code>.</li>
  <li><b>Codex</b>: append <code>codex/AGENTS.md.example</code> into your <code>AGENTS.md</code>, then just say "review X".</li>
  <li><b>Any agent</b>: paste the full text of <code>泼冷水skill.md</code>.</li>
</ul>

<h2>Usage</h2>
<ul>
  <li><b>Random</b>: send "pick 3 trending projects and review them"</li>
  <li><b>Specified</b>: send "review &lt;name or GitHub link&gt;"</li>
</ul>

<h2>Principles</h2>
<p>No fabrication · Separate hype from testing · Fixed rubric · Beginner-first</p>

<h2>Next steps</h2>
<p>Pair with the GitHub API / search tools to pull candidates and Issues first, then let the skill write the report.</p>

<p class="cd-repo">Repo: <a href="https://github.com/phenoCS/calmdown_skill">github.com/phenoCS/calmdown_skill</a></p>

</div>

<style>
.cd { max-width: 760px; margin: 0 auto; font-size: 16px; line-height: 1.6; }
.cd-head { margin-bottom: 8px; }
.cd-head h1 { margin: 0 0 4px; font-size: 28px; }
.cd-sub { margin: 0 0 14px; color: #57606a; }
.cd-switch { margin-bottom: 18px; }
.cd-btn {
  display: inline-block; cursor: pointer; user-select: none;
  padding: 5px 18px; margin: 0 4px;
  border: 1px solid #d0d7de; border-radius: 6px;
  font-size: 14px; font-weight: 600; color: #24292f;
  background: #f6f8fa;
}
.cd-btn:hover { border-color: #0969da; }
.cd-zh, .cd-en { display: none; text-align: left; }
#cd-sw-zh:checked ~ .cd-zh { display: block; }
#cd-sw-en:checked ~ .cd-en { display: block; }
.cd:has(#cd-sw-zh:checked) label[for="cd-sw-zh"],
.cd:has(#cd-sw-en:checked) label[for="cd-sw-en"] {
  background: #0969da; color: #fff; border-color: #0969da;
}
.cd table { border-collapse: collapse; width: 100%; margin: 8px 0 16px; }
.cd th, .cd td { border: 1px solid #d0d7de; padding: 6px 10px; text-align: left; }
.cd th { background: #f6f8fa; }
.cd code { background: #f6f8fa; padding: 1px 5px; border-radius: 4px; font-size: 90%; }
.cd-repo { margin-top: 18px; font-size: 14px; color: #57606a; }
@media (prefers-color-scheme: dark) {
  .cd-btn { background: #21262d; color: #e6edf3; border-color: #30363d; }
  .cd-sub, .cd-repo { color: #8b949e; }
  .cd th, .cd td { border-color: #30363d; }
  .cd th { background: #161b22; }
  .cd code { background: #161b22; }
}
</style>
</div>
