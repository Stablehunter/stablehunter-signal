# Agentic Payment Signal Skill

## Purpose

Use this skill when an agent needs to retrieve the latest curated Agentic Payment Daily Signal from Stablehunter AI and route it into an external agent workflow.

This is a public, no-auth Markdown skill package. It is designed to be read by external AI agents, workflow agents, and developer tools.

## When To Use

Use this skill when the user asks to:

- Get today's Agentic Payment Daily Signal.
- Add Agentic Payment Signal to an existing agent workflow.
- Route Stablehunter AI payment-infrastructure updates into a bot, research workflow, CRM, daily brief, or internal workspace.
- Monitor agentic payment, programmable payment, stablecoin rail, payment API, compliance, identity, fraud, KYB, KYC, AML, merchant payment, treasury, card, or bank-rail updates.

Do not use this skill for generic crypto news, token price monitoring, trading alerts, or airdrop tracking.

## Public Data Surface

Primary page:

```text
https://stablehunter.ai/agentic-payment-signal.html#daily-signals
```

Daily Signal API pattern:

```text
GET https://cms.stablehunter.com/api/daily-digests/{digestDate}?category=information_signal&locale={locale}
```

Example:

```text
GET https://cms.stablehunter.com/api/daily-digests/2026-05-11?category=information_signal&locale=en
```

Locale values:

```text
en | zh-Hans
```

Authentication:

```text
None required for v1.
```

If today's digest is not available, fetch the latest available date shown on the Agentic Payment Signal page and route that report instead. Do not expose internal fetch errors to end users; explain that the latest available Daily Signal was used.

## Output Schema

Agents should normalize the response into this shape before routing it downstream:

```json
{
  "signal_name": "Agentic Payment Signal",
  "digest_date": "YYYY-MM-DD",
  "title": "string",
  "item_count": 0,
  "items": [
    {
      "title": "string",
      "summary": "string",
      "why_it_matters": "string",
      "audience": "string",
      "source_url": "https://example.com",
      "source_name": "string"
    }
  ],
  "canonical_url": "https://stablehunter.ai/agentic-payment-signal.html?date=YYYY-MM-DD#daily-signals"
}
```

## Routing Guidance

When routing the Daily Signal into another workflow:

1. Keep the digest date visible.
2. Include the canonical Stablehunter AI URL.
3. Preserve source links.
4. Keep each item concise: title, why it matters, source.
5. Do not rewrite the signal into investment advice.
6. Do not add unsupported claims beyond the source material.

Recommended short format:

```text
Agentic Payment Signal · {digest_date}
{title}

1. {item.title}
Why it matters: {item.why_it_matters}
Source: {item.source_url}

Read the full Daily Signal:
{canonical_url}
```

## Example Workflow

```text
User: Add today's Agentic Payment Signal to my agent workflow.

Agent:
1. Determine today's date in the user's preferred timezone.
2. Request:
   https://cms.stablehunter.com/api/daily-digests/{today}?category=information_signal&locale={locale}
3. If unavailable, read:
   https://stablehunter.ai/agentic-payment-signal.html#daily-signals
   and use the latest available digest date.
4. Normalize the result using the output schema.
5. Route the normalized brief into the user's workflow destination.
6. Include the canonical Stablehunter AI Daily Signal URL.
```

## Source Boundary

The Agentic Payment Signal focuses on curated updates related to:

- payment APIs
- stablecoin rails
- agentic commerce
- programmable payments
- identity, fraud, compliance, KYB, KYC, AML
- treasury, merchant payment, card, bank, and settlement infrastructure
- AI agent payment workflows

Avoid broad market commentary unless it directly changes payment infrastructure or agent-executable financial workflows.
