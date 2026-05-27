# Roadmap

Agentic Payment Signal 的路线分两条线：让人更容易读，让 agent 更容易调用。

## Phase 1: Public Signal Layer

状态：已开放

- Daily Signal 页面
- 日期归档和 Load more
- 公开 source list
- 公开 screening criteria
- 公开 digest schema
- Launch sample digest
- Source / signal / criteria feedback issue templates

目标：

让读者理解这个项目追踪什么、不追踪什么，以及为什么这些 signal 对 payment builder 有价值。

## Phase 2: Distribution Layer

状态：部分可用

- Telegram updates
- Feishu bot / workspace setup
- WeChat launch article
- Signal-specific share cards

下一步：

- RSS feed
- 更稳定的 X / WeChat share workflow
- Weekly founder-facing recap

目标：

让读者不需要每天主动打开页面，也能在自己的工作流里接收高质量 signal。

## Phase 3: Developer Access

状态：v1 API pattern 已公开

- Public Daily Digest API pattern
- Archive API pattern
- Share card API pattern
- Structured output schema
- Query by date

下一步：

- OpenAPI-style endpoint description
- More JSON examples
- Query by tag
- Query by source
- Better error / fallback guidance

目标：

让开发者和研究工作流可以直接读取 Agentic Payment Signal，而不是手动复制页面内容。

## Phase 4: Agent / Skill Access

状态：instruction packages 已开放

- Generic Markdown Skill
- Codex Skill
- Claude Instructions
- Hermes Agent Spec
- Agent query examples

下一步：

- Hosted MCP server
- More framework-specific adapters
- Daily briefing workflow examples
- Integration examples for Lark / Feishu / Telegram / CRM

目标：

让外部 agent 可以直接调用这个 signal：查询今天的变化、总结某个标签、查找过去一周和 stablecoin rails 有关的更新。

## Not Doing Yet

- Trading signals
- Investment advice
- A comprehensive news database
- Automatic aggregation from unverified sources
- Opening the internal scoring pipeline too early

---

# Roadmap

The roadmap has two goals: make the signal easier for humans to read, and easier for agents to call.

## Phase 1: Public Signal Layer

Status: open

- Daily Signal page
- Date archive and Load more
- Public source list
- Public screening criteria
- Public digest schema
- Launch sample digest
- Source / signal / criteria feedback issue templates

Goal:

Help readers understand what this project tracks, what it does not track, and why these signals matter for payment builders.

## Phase 2: Distribution Layer

Status: partially available

- Telegram updates
- Feishu bot / workspace setup
- WeChat launch article
- Signal-specific share cards

Next:

- RSS feed
- More stable X / WeChat share workflow
- Weekly founder-facing recap

Goal:

Let readers receive high-quality signals inside their existing workflows without opening the page every day.

## Phase 3: Developer Access

Status: v1 API pattern is public

- Public Daily Digest API pattern
- Archive API pattern
- Share card API pattern
- Structured output schema
- Query by date

Next:

- OpenAPI-style endpoint description
- More JSON examples
- Query by tag
- Query by source
- Better error and fallback guidance

Goal:

Let developers and research workflows read Agentic Payment Signal directly instead of copying content from the page.

## Phase 4: Agent / Skill Access

Status: instruction packages are open

- Generic Markdown Skill
- Codex Skill
- Claude Instructions
- Hermes Agent Spec
- Agent query examples

Next:

- Hosted MCP server
- More framework-specific adapters
- Daily briefing workflow examples
- Integration examples for Lark / Feishu / Telegram / CRM

Goal:

Let external agents call this signal directly: query today's changes, summarize a tag, or find the past week's updates related to stablecoin rails.

## Not Doing Yet

- Trading signals
- Investment advice
- A comprehensive news database
- Automatic aggregation from unverified sources
- Opening the internal scoring pipeline too early
