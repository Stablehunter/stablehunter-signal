# Hermes Agent Spec: Agentic Payment Signal

This is a portable agent spec for Hermes-style agent workflows. It describes the capability, trigger conditions, public data surface, output contract, and routing behavior for Stablehunter AI's Agentic Payment Signal.

## Capability

Retrieve the latest available Stablehunter AI Agentic Payment Daily Signal and route it into a downstream agent workflow, bot, research brief, CRM note, workspace, or operating dashboard.

## Trigger Conditions

Invoke this capability when the task mentions:

- Agentic Payment Signal
- agentic payments
- programmable payments
- stablecoin payment rails
- payment APIs
- AI agent commerce
- compliance, identity, fraud, KYC, KYB, AML, merchant payment, treasury, card, bank, or settlement infrastructure

Do not invoke it for generic token news, price monitoring, trading decisions, or airdrop discovery.

## Public Inputs

```yaml
signal_name: Agentic Payment Signal
date: YYYY-MM-DD | latest
category: information_signal
auth: none
```

## Public Data Surface

```yaml
primary_page: https://stablehunter.ai/agentic-payment-signal.html#daily-signals
daily_signal_api: https://cms.stablehunter.com/api/daily-digests/{digestDate}?category=information_signal&locale={locale}
locale_values:
  - en
  - zh-Hans
canonical_url: https://stablehunter.ai/agentic-payment-signal.html?date={digestDate}#daily-signals
```

If the requested date is unavailable, fall back to the latest available Daily Signal date shown on the primary page.

## Output Contract

```yaml
signal_name: Agentic Payment Signal
digest_date: YYYY-MM-DD
title: string
item_count: number
items:
  - title: string
    summary: string
    why_it_matters: string
    audience: string
    source_url: string
    source_name: string
canonical_url: string
```

## Routing Contract

When routing downstream:

- keep the digest date visible
- include the canonical Stablehunter AI URL
- preserve original source links
- keep every item concise
- do not add unsupported market claims
- do not rewrite the signal into investment advice

## Minimal Brief Template

```text
Agentic Payment Signal · {digest_date}
{title}

{index}. {item.title}
Why it matters: {item.why_it_matters}
Source: {item.source_url}

Full report: {canonical_url}
```
