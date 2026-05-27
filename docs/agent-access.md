# Agent Access

Agentic Payment Signal is designed to be readable by humans and callable by agents.

The current public layer is intentionally simple: no auth, no private scoring pipeline, and no dependency on one agent framework. Agents can start from the public page, the daily API pattern, and the portable instruction packages in this repo.

## Available Packages

| Package | File | Best for |
|---|---|---|
| Generic Markdown Skill | [`assets/skills/agentic-payment-signal-skill.md`](../assets/skills/agentic-payment-signal-skill.md) | Any agent or workflow tool that can read Markdown instructions |
| Codex Skill | [`assets/skills/codex-agentic-payment-signal/SKILL.md`](../assets/skills/codex-agentic-payment-signal/SKILL.md) | Local Codex skill discovery |
| Claude Instructions | [`assets/skills/claude-agentic-payment-signal.md`](../assets/skills/claude-agentic-payment-signal.md) | Claude Projects, custom instructions, Claude Code context |
| Hermes Agent Spec | [`assets/skills/hermes-agentic-payment-signal.md`](../assets/skills/hermes-agentic-payment-signal.md) | Hermes-style agent routing and workflow specs |

## Canonical Agent Flow

1. Determine the requested date or use today's date in the user's preferred timezone.
2. Fetch the daily digest API for that date.
3. If the date is unavailable, use the archive endpoint or the latest available date on the Daily Signal page.
4. Normalize the result into the public digest schema.
5. Preserve original source links.
6. Include the canonical Stablehunter URL.
7. Keep the output research-oriented, not investment advice.

## Example Agent Questions

```text
What changed in Agentic Payment today?
```

```text
Summarize the past week of stablecoin rail signals for a payment founder.
```

```text
Which recent updates are related to wallet permissions, risk, compliance, or merchant acceptance?
```

```text
Turn today's Agentic Payment Signal into a three-bullet internal research brief.
```

## Boundary

This is a public signal layer. It should not be treated as:

- a trading signal
- investment advice
- legal or compliance advice
- a complete market database
- a replacement for reading primary sources

Agents should preserve source links and make it clear when they are summarizing Stablehunter's curated signal rather than the full original source.
