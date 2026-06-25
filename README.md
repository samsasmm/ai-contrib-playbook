# The AI-Contribution Playbook

**How real open-source projects are handling the flood of AI-generated
contributions — and ready-to-copy templates so yours can too.**

*中文见下方 ↓*

---

## Why this exists

2026 broke something in open source. AI made it trivial to generate pull
requests, issues, and "security reports" — and maintainers, mostly volunteers,
are buried. This isn't a vibe; it's documented:

- **curl** ended its public bug-bounty program after roughly a fifth of
  submissions turned into AI "slop." ([InfoQ][infoq])
- **AI agents are flooding maintainers** with low-quality, sometimes bogus
  security reports. ([Axios][axios])
- **GitHub is exploring restrictions on pull requests** to slow the deluge.
  ([InfoWorld][infoworld])
- A wave of projects has written explicit **AI-contribution rules** in
  response. ([The New Stack][tns])

Most projects are figuring out their policy alone, in a panic. This repo
collects what others decided, so you don't start from a blank page.

> **Note:** policies change. Every claim below links to its source — click
> through and verify before you rely on it. A weekly link-check keeps these
> references from rotting.

## Part 1 — What projects are doing (a map)

| Stance | What it looks like | Good fit for |
|---|---|---|
| **Welcome, with rules** | AI is fine if a human read it, ran it, and discloses use | Most projects |
| **Require proof** | No PR/issue without a reproducible test or repro steps | Bug-heavy projects |
| **Restrict external PRs** | Auto-close or gate drive-by external PRs | Tiny maintainer teams |
| **Ban AI contributions** | AI-generated code/reports not accepted | Safety-critical / low-trust inflow |

For sourced, project-by-project examples and how each framed its policy, see
[The New Stack's overview][tns] and the [link collection](#sources) below.

## Part 2 — Pick your stance in 5 minutes

1. **How much inflow do you get?** Low → "welcome with rules." High/abusive →
   "require proof" or "restrict external PRs."
2. **How risky is a bad merge?** High (security, infra) → stricter; lean toward
   required tests and human sign-off.
3. **Write it down once.** Drop a policy file in your repo so you can link it
   instead of re-arguing it every time.

## Part 3 — Copy these templates

Ready to adapt, in these template files:

- **[`AI-CONTRIBUTING.md`](TEMPLATE_AI-CONTRIBUTING.md)** — a balanced
  "welcome, with rules" policy.
- **[`PULL_REQUEST_TEMPLATE.md`](TEMPLATE_pull_request.md)** — a PR
  checklist that asks the right questions (read it? ran it? AI used?).
- **[`bug_report.md`](TEMPLATE_issue_bug_report.md)** — an
  issue form that asks for a real, self-confirmed reproduction.

Drop them into your repo's root / `.github/` folder and edit to taste.

> Pair this with **[prcheck](https://github.com/samsasmm/prcheck)** — a local, no-API tool that
> lets *contributors* self-check a PR before they open it. (Update the link to
> your prcheck repo.)

## Contributing

Seen a good (or instructive) AI-contribution policy in the wild? Open a PR
adding it to the map — with a link to the source. Bilingual entries welcome.

## Sources

- [The New Stack — the AI-generated-code crisis in open source][tns]
- [InfoQ — AI submissions push projects to close programs (curl)][infoq]
- [Axios — AI agents spam the volunteers securing open source][axios]
- [InfoWorld — GitHub eyes restrictions on pull requests][infoworld]

[tns]: https://thenewstack.io/ai-generated-code-crisis/
[infoq]: https://www.infoq.com/news/2026/02/ai-floods-close-projects/
[axios]: https://www.axios.com/2026/03/10/ai-agents-spam-the-volunteers-securing-open-source-software
[infoworld]: https://www.infoworld.com/article/4127156/github-eyes-restrictions-on-pull-requests-to-rein-in-ai-based-code-deluge-on-maintainers.html

---

# AI 贡献政策手册（中文）

**真实开源项目是怎么应对"AI 生成贡献"洪水的——附可直接复制的政策模板。**

## 为什么做它

2026 年，开源世界被冲垮了一角。AI 让"生成 PR、issue、安全报告"变得极其廉价，
而维护者大多是志愿者，被彻底淹没。这不是情绪，是有据可查的：

- **curl** 因约五分之一提交沦为 AI"垃圾"，关停了公开漏洞赏金计划。（[InfoQ][infoq]）
- **AI agent 正用低质、甚至虚假的安全报告淹没维护者。**（[Axios][axios]）
- **GitHub 正在考虑限制 PR** 来缓解洪流。（[InfoWorld][infoworld]）
- 一批项目因此写下了明确的 **AI 贡献规则**。（[The New Stack][tns]）

大多数项目都在孤军奋战、临时拍脑袋定政策。这个仓库把别人已经做出的选择收集起来，
让你不必从一张白纸开始。

> **注意：** 政策会变。下面每条都附了来源链接——用之前请点进去核实。
> 仓库每周自动跑一次链接检查，避免引用失效。

## 三步选定你的立场

1. **你的贡献流入量多大？** 少 →"欢迎，但有规矩"；多/被滥用 →"要求可复现证明"或"限制外部 PR"。
2. **一次错误合并的风险多高？** 高（安全、基础设施）→ 更严，倾向强制测试 + 人工签字。
3. **写下来一次。** 在仓库里放一个政策文件，以后直接甩链接，不用每次重新吵。

## 直接复制模板

下面的模板文件，均可改：AI 贡献政策、PR 自检清单、要求真实复现的 issue 模板。

> 建议搭配 **prcheck**（本地、零 API 的贡献者端 PR 自检工具）一起用。

欢迎提 PR 补充你见过的 AI 贡献政策（附来源链接，支持中英双语）。

MIT License · 模板可自由复制。
