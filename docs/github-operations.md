# GitHub Operations

This document defines how to operate the Stablehunter Signal GitHub repo after launch.

## Role of the Repo

The repo is public proof and participation infrastructure.

It should make three things clear:

1. The signal system has a method.
2. The source and criteria are transparent.
3. Readers can contribute without writing code.
4. Agents can discover a stable public data surface.

The repo is not the main traffic destination. The main destinations are:

- Daily Signal page
- WeChat article
- X posts
- Telegram / Feishu / RSS later
- Agent instruction packages and public endpoint docs

## Weekly Operating Rhythm

Recommended cadence:

- 2-3 times per week: review new source suggestions and signal candidates.
- Weekly: update source list or criteria if needed.
- Weekly: add or refine one sample digest when useful.
- Weekly: check that public endpoints and skill instructions still match the live Daily Signal page.
- Monthly: publish a short release note if the public surface changes.

## Issue Triage

Labels to use:

- `source`
- `signal-candidate`
- `criteria`
- `needs-verification`
- `accepted`
- `declined`
- `roadmap`

Triage rules:

- Accept sources that are official, primary, or consistently high-signal.
- Ask for original links when a signal is second-hand.
- Decline price-only, airdrop, meme, or low-depth market sentiment items.
- Keep reasoning public and concise.

## Release Notes

Use `release-notes/` for meaningful public changes:

- New public surface
- New schema
- New access path
- Significant source policy change
- New sample digest format

Avoid release notes for small typo fixes.

## README Rule

The README first screen should always answer:

1. What is this?
2. Who is it for?
3. What is live now?
4. Where do I start?
5. How can I contribute or use it from an agent?

Do not let README drift into a long research memo.

## GitHub Launch Pattern

The repo should borrow the strongest pattern from high-signal open-source information products:

- Put the working surface above the fold: page, endpoints, skills, contribution path.
- Keep sources and criteria visible, not buried in private notes.
- Make non-code contribution easy through issue templates.
- Keep agent access practical: clear API pattern, fallback behavior, output shape, and guardrails.
- Avoid over-claiming automation that is not yet public.
