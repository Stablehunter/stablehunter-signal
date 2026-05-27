# Public Endpoints

This document records the public data surface used by the Agentic Payment Signal page and agent instruction packages.

## Daily Signal Page

```text
https://stablehunter.ai/agentic-payment-signal.html#daily-signals
```

Use this as the canonical human-readable entry point.

## Daily Digest API

```text
GET https://cms.stablehunter.com/api/daily-digests/{YYYY-MM-DD}?category=information_signal&locale={locale}
```

Example:

```text
GET https://cms.stablehunter.com/api/daily-digests/2026-05-11?category=information_signal&locale=en
```

Locale values:

```text
en
zh-Hans
```

Authentication:

```text
None required for v1.
```

## Archive API

```text
GET https://cms.stablehunter.com/api/daily-digests/archive?category=information_signal&locale={locale}&page=1&limit=30
```

The public page uses this endpoint to load historical daily digests. If the archive endpoint is unavailable, agents should fall back to the latest available date shown on the Daily Signal page.

## Share Card API

```text
GET https://cms.stablehunter.com/api/public/daily-digests/share-card?date={YYYY-MM-DD}&signal={signal_id}&card=v2
```

Use this when a workflow needs to share a specific signal with a visual card, for example on X, WeChat, or an internal workspace.

If a signal ID is not available, link to the canonical daily page:

```text
https://stablehunter.ai/agentic-payment-signal.html?date={YYYY-MM-DD}#daily-signals
```

## Expected Normalized Shape

Downstream agents should normalize API responses into the schema in [`digest-schema.md`](../digest-schema.md). The minimal routing fields are:

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

## Stability Note

These endpoints are public v1 surfaces. The repo intentionally documents usage patterns without exposing private source notes, internal scoring logic, or bot delivery configuration.
