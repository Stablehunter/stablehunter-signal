# Agentic Payment Signal

> Daily signals for AI-native payments, stablecoin rails, wallets, identity, risk, compliance, and agent-executable commerce.

Agentic Payment Signal is a public signal system by Stablehunter AI.

It is not a crypto news feed, a token watchlist, or a generic AI newsletter. It tracks the middle layer of Agentic Payment: the protocols, payment APIs, stablecoin rails, wallet permissions, merchant trust, identity, risk, compliance, and settlement infrastructure that need to exist before agents can safely initiate and complete payments.

**Live now:** daily web archive, public source list, screening criteria, structured digest schema, contribution templates, signal share cards, and portable instruction packages for agents.

## Start Here

| Use case | Link |
|---|---|
| Read the Daily Signal | [stablehunter.ai/agentic-payment-signal.html#daily-signals](https://stablehunter.ai/agentic-payment-signal.html#daily-signals) |
| Understand the launch | [LAUNCH.md](./LAUNCH.md) |
| See what sources we track | [sources.md](./sources.md) |
| See what counts as a signal | [criteria.md](./criteria.md) |
| Use the digest schema | [digest-schema.md](./digest-schema.md) |
| Add it to an agent workflow | [docs/agent-access.md](./docs/agent-access.md) |
| Fetch the public endpoints | [docs/endpoints.md](./docs/endpoints.md) |
| Suggest a source or signal | [CONTRIBUTING.md](./CONTRIBUTING.md) |

## Why This Exists

The end state of Agentic Payment is easy to describe: agents can subscribe to services, buy API capacity, manage budgets, and complete transactions within user-defined permission boundaries.

The difficult part is the road in between.

From human confirmation to machine execution, the industry needs new layers for identity, authorization, risk, compliance, stablecoin settlement, wallet controls, merchant acceptance, and auditability. This repo tracks whether those layers are actually appearing in the market.

## What Is Live

- **Daily Signal page:** a public, date-based web archive for curated Agentic Payment updates.
- **Archive loading:** the page can browse available daily digests instead of only showing one static report.
- **Signal share cards:** individual signals can be shared with a card URL for X, WeChat, and internal routing.
- **Public source and criteria docs:** the source boundary and screening logic are visible.
- **Structured schema:** signals are normalized so they can be reused in agents, briefs, and dashboards.
- **Agent instruction packages:** generic Markdown, Codex Skill, Claude instructions, and Hermes-style agent spec.
- **GitHub contribution flow:** issue templates for source suggestions, signal candidates, and criteria feedback.

## Use It With Agents

Agentic Payment Signal is also available as portable instructions for agent workflows.

- [Generic Markdown Skill](./assets/skills/agentic-payment-signal-skill.md)
- [Codex Skill](./assets/skills/codex-agentic-payment-signal/SKILL.md)
- [Claude Instructions](./assets/skills/claude-agentic-payment-signal.md)
- [Hermes Agent Spec](./assets/skills/hermes-agentic-payment-signal.md)

Agents can ask questions like:

- What changed in Agentic Payment today?
- Which signals from the past week matter for stablecoin rails?
- What updates are related to wallet permissions, risk, compliance, or merchant acceptance?
- Which signals should a payment founder read first?

For API patterns, archive access, share-card URLs, and fallback behavior, see [docs/endpoints.md](./docs/endpoints.md) and [docs/agent-access.md](./docs/agent-access.md).

## What Counts As A Signal

Every signal should answer four questions:

1. What changed?
2. Why does it matter for Agentic Payment?
3. Who should care?
4. Where is the original source?

Examples:

| Signal type | What it reveals |
|---|---|
| AP2 / UCP | Agent commerce and payment protocol layer |
| Trusted Agent Protocol | Merchant trust and agent identity layer |
| x402 | Crypto-native machine payment rail |
| Stablecoin card or settlement update | Stablecoin rails entering real payment flows |
| Wallet permission update | How agents may hold, spend, approve, or delegate funds |
| Identity / risk / compliance update | Trust and permission boundary for automated payments |

## What We Track

- AI agents initiating, authorizing, executing, or managing payments
- Stablecoin payments, settlement, cards, treasury, on/off-ramp, and merchant flows
- Wallet infrastructure, permissions, custody, account abstraction, and agent access
- Payment APIs and protocol layers for agentic commerce
- Identity, KYB, KYC, AML, fraud, risk, compliance, and auditability
- Infrastructure moves from Stripe, PayPal, Visa, Mastercard, Circle, Coinbase, Bridge, BVNK, Fireblocks, and similar players

## What We Do Not Track

- Token price moves, trading calls, or short-term sentiment
- Generic AI news that does not change payment infrastructure
- Concept-only narratives without product, API, compliance, or commercial evidence
- Airdrops, meme coins, or purely speculative traffic

## Repo Map

```text
.
├── README.md
├── LAUNCH.md
├── CONTRIBUTING.md
├── sources.md
├── criteria.md
├── digest-schema.md
├── roadmap.md
├── assets/skills/
│   ├── agentic-payment-signal-skill.md
│   ├── codex-agentic-payment-signal/SKILL.md
│   ├── claude-agentic-payment-signal.md
│   └── hermes-agentic-payment-signal.md
├── docs/
│   ├── agent-access.md
│   ├── endpoints.md
│   ├── github-operations.md
│   └── share-cards.md
├── examples/
│   └── agent-queries.md
├── samples/
│   └── 2026-05-launch.md
└── release-notes/
    └── v0.1.md
```

## Contribute

The most valuable first contributions are not code. They are high-quality sources, specific signal candidates, and feedback on the screening criteria.

- Suggest a source: [open source suggestion issue](../../issues/new?template=source-suggestion.yml)
- Submit a signal candidate: [open signal candidate issue](../../issues/new?template=signal-candidate.yml)
- Challenge or improve criteria: [open criteria feedback issue](../../issues/new?template=criteria-feedback.yml)

See [CONTRIBUTING.md](./CONTRIBUTING.md).

## Roadmap

The current public surface already includes the daily page, archive, public docs, schema, and agent instruction packages.

Next areas:

- RSS feed
- More structured JSON examples
- OpenAPI-style endpoint description
- Hosted MCP server
- More sample digests by signal type

See [roadmap.md](./roadmap.md).

## Disclaimer

Agentic Payment Signal is for information monitoring and research only. It is not investment, legal, compliance, or business advice. Always verify the original source.

---

# 中文说明

Agentic Payment Signal 是 Stablehunter AI 的每日信号项目，追踪 AI agent、稳定币轨道、钱包、支付 API、风控与合规基础设施如何汇合成机器可执行支付。

这个 repo 的作用不是做一个新闻库，而是公开这套 signal 系统的方法和入口：

- 看哪些 source
- 什么内容算 signal
- 什么内容会被排除
- 每条 signal 应该怎么写
- Daily Signal 页面和 API pattern 怎么读取
- 外部 agent 如何通过 Skill / instructions 使用它

如果你也在看 AI、稳定币、钱包、支付基础设施这些方向，可以先从 Daily Signal 页面开始：

https://stablehunter.ai/agentic-payment-signal.html#daily-signals
