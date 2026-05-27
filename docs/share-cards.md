# Signal Share Cards

Agentic Payment Signal supports signal-specific share cards for social and internal distribution.

The goal is to make each signal shareable without turning the repo into a generic newsletter archive. A share card should communicate:

- the signal title
- why it matters
- report date
- source name
- Stablehunter branding

## URL Pattern

```text
https://cms.stablehunter.com/api/public/daily-digests/share-card?date={YYYY-MM-DD}&signal={signal_id}&card=v2
```

Example:

```text
https://cms.stablehunter.com/api/public/daily-digests/share-card?date=2026-05-11&signal={signal_id}&card=v2
```

## When To Use

Use share cards for:

- X posts
- WeChat article embeds
- Lark / Feishu internal posts
- launch notes
- source follow-up threads

Do not use cards to imply endorsement, investment recommendations, or claims not supported by the signal and original source.

## Suggested Social Format

```text
New Agentic Payment Signal:
{signal_title}

Why it matters:
{one_sentence_judgment}

Source:
{source_url}

Daily Signal:
https://stablehunter.ai/agentic-payment-signal.html?date={YYYY-MM-DD}#daily-signals
```
