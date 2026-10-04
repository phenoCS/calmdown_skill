# 泼冷水报告（示例 · 模式 B 指定：FreeToken 类"消费级显卡跑大模型"项目）／ Cold-Water Report (Sample · Mode B specified: FreeToken-style "run big models on consumer GPU" project)

> 下面是一份**格式示范**，不是对某真实项目的定论。真实结论需 agent 联网搜 Issues / 文档后填写。
> The following is a **format demo**, not a verdict on any real project. Real conclusions require the agent to search Issues / docs online.

## 1. 项目名（https://github.com/示例/example-token）／ Project name (https://github.com/example/example-token)
号称让你在消费级 5060 显卡上部署大参数模型。／ Claims to let you deploy large-parameter models on a consumer 5060 GPU.

### 口碑 ／ Reputation
- 官方/宣传说的是：消费级显卡也能跑大模型，穷人福音，一键部署。
  Official says: consumer GPUs can run LLMs too, a blessing for the poor, one-click deploy.
- 社区实测/差评是：
  - Issue #123：「实测 5060 8G 显存，跑 7B 都爆显存，所谓大参数要靠量化到没法用」（来源：项目 Issues）
    Issue #123: "tested 5060 8G VRAM, even 7B OOMs, the 'large' params need quantization to uselessness" (source: project Issues)
  - 论坛帖：「宣传的'大参数'实际是 1.5B 量化版，和宣传视频里的效果差很远」（来源：搜索）
    Forum post: "the 'large params' are actually a 1.5B quantized version, far from the promo video" (source: search)

### 使用限制（硬门槛）／ Limitations (hard barriers)
- 硬件：显存 ≥ 12G 才勉强；5060 8G 基本跑不动原宣传效果。
  Hardware: ≥12G VRAM勉强; 5060 8G basically can't run the promoted effect.
- 环境：需 CUDA 12.x、特定驱动；Windows 用户踩坑多。
  Environment: needs CUDA 12.x, specific drivers; many Windows pitfalls.
- 不满足会：要么跑不起来，要么只能跑严重量化、质量很差的版本，体验与宣传不符。
  If unmet: either won't run, or only a heavily quantized, low-quality version runs — not matching the promo.
- 用不了的人：8G 显存及以下显卡用户、不想折腾驱动的人。
  Who can't use: ≤8G VRAM GPU users, those unwilling to tinker with drivers.

### 推荐指数：⭐⭐（宣传夸大，硬门槛卡住大部分消费级用户）／ Rating: ⭐⭐ (exaggerated, hard barrier blocks most consumer users)
- 适合：有 12G+ 显存、愿意折腾量化的玩家。／ Good for: 12G+ VRAM users who enjoy quant tinkering.
- 不适合：拿 5060 想"直接跑大模型"的小白——和宣传对不上。／ Not for: newbies with a 5060 expecting "just run big models" — mismatches the promo.

---

（模式 A 时，上面结构再重复 2 次，共 3 个项目）／ (In Mode A, repeat the above structure 2 more times for 3 projects total)
