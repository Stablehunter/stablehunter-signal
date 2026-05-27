# 日报字段结构

Agentic Payment Daily Signal 的每条内容应该尽量保持结构一致，方便人读，也方便后续接入 RSS、API、MCP 或 Skill。

## Digest

| 字段 | 类型 | 说明 |
|---|---|---|
| `digestDate` | string | 日期，格式 `YYYY-MM-DD` |
| `categorySlug` | string | 默认 `agentic_payment_signal` |
| `title` | string | 当日标题 |
| `summary` | string | 当日总览 |
| `itemCount` | number | signal 数量 |
| `items` | array | 当日 signal 列表 |

## Signal Item

| 字段 | 类型 | 说明 |
|---|---|---|
| `title` | string | signal 标题 |
| `url` | string | 原始来源链接 |
| `sourceName` | string | 来源名称 |
| `sourceType` | string | `official` / `media` / `research` / `regulatory` / `community` |
| `summary` | string | 发生了什么 |
| `why` | string | 为什么重要 |
| `audience` | string | 适合谁看 |
| `tags` | array | 标签，如 `stablecoin rails`、`wallet`、`compliance` |
| `confidence` | string | `high` / `medium` / `low` |
| `evidenceLevel` | string | `L1 official` / `L2 third-party` / `L3 inference` |
| `watchNext` | string | 后续观察点 |

## 示例 JSON

```json
{
  "digestDate": "2026-05-17",
  "categorySlug": "agentic_payment_signal",
  "title": "Agentic Payment Daily Signal · 2026-05-17",
  "summary": "Today's signals focus on stablecoin card rails, programmable wallet authorization, and payment risk infrastructure.",
  "itemCount": 3,
  "items": [
    {
      "title": "Example payment network expands stablecoin settlement support",
      "url": "https://example.com/news",
      "sourceName": "Example Newsroom",
      "sourceType": "official",
      "summary": "A payment network added stablecoin settlement support for selected merchant flows.",
      "why": "This matters because stablecoin settlement is moving from crypto-native apps into payment network infrastructure.",
      "audience": "payment founders, stablecoin operators, wallet builders",
      "tags": ["stablecoin rails", "merchant settlement", "payment network"],
      "confidence": "medium",
      "evidenceLevel": "L1 official",
      "watchNext": "Watch whether this expands from pilot programs into developer-accessible APIs."
    }
  ]
}
```

## 写作约束

- `summary` 写事实，不夹太多判断。
- `why` 写判断，但要标清楚推断边界。
- `audience` 要具体，不要只写“Web3 users”。
- `confidence` 不等于喜欢程度，而是证据强度。
- 如果来源是媒体报道而非官方消息，`evidenceLevel` 不要写成 `L1 official`。

---

# Daily Digest Schema

Each Agentic Payment Daily Signal item should keep a consistent structure so it is easy to read and later expose through RSS, API, MCP, or a Skill.

## Digest

| Field | Type | Description |
|---|---|---|
| `digestDate` | string | Date in `YYYY-MM-DD` format |
| `categorySlug` | string | Default: `agentic_payment_signal` |
| `title` | string | Daily digest title |
| `summary` | string | Daily overview |
| `itemCount` | number | Number of signals |
| `items` | array | List of signal items |

## Signal Item

| Field | Type | Description |
|---|---|---|
| `title` | string | Signal title |
| `url` | string | Original source URL |
| `sourceName` | string | Source name |
| `sourceType` | string | `official` / `media` / `research` / `regulatory` / `community` |
| `summary` | string | What changed |
| `why` | string | Why it matters |
| `audience` | string | Who should care |
| `tags` | array | Tags such as `stablecoin rails`, `wallet`, `compliance` |
| `confidence` | string | `high` / `medium` / `low` |
| `evidenceLevel` | string | `L1 official` / `L2 third-party` / `L3 inference` |
| `watchNext` | string | What to watch next |

## Example JSON

```json
{
  "digestDate": "2026-05-17",
  "categorySlug": "agentic_payment_signal",
  "title": "Agentic Payment Daily Signal · 2026-05-17",
  "summary": "Today's signals focus on stablecoin card rails, programmable wallet authorization, and payment risk infrastructure.",
  "itemCount": 3,
  "items": [
    {
      "title": "Example payment network expands stablecoin settlement support",
      "url": "https://example.com/news",
      "sourceName": "Example Newsroom",
      "sourceType": "official",
      "summary": "A payment network added stablecoin settlement support for selected merchant flows.",
      "why": "This matters because stablecoin settlement is moving from crypto-native apps into payment network infrastructure.",
      "audience": "payment founders, stablecoin operators, wallet builders",
      "tags": ["stablecoin rails", "merchant settlement", "payment network"],
      "confidence": "medium",
      "evidenceLevel": "L1 official",
      "watchNext": "Watch whether this expands from pilot programs into developer-accessible APIs."
    }
  ]
}
```

## Writing Rules

- `summary` should describe facts, not overpack interpretation.
- `why` should contain judgment, while making inference boundaries clear.
- `audience` should be specific, not generic "Web3 users."
- `confidence` means evidence strength, not enthusiasm.
- If the source is media coverage rather than an official announcement, do not mark it as `L1 official`.
