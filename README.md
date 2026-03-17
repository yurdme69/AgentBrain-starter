# AgentBrain — Starter Brain

**Your AI forgets everything every session. Fix that.**

AgentBrain gives your AI agent permanent memory that survives every restart, every compaction, every context wipe.

## Install (2 minutes)

```bash
git clone https://github.com/agentbrain-ai/agentbrain-starter.git
cp agentbrain-starter/templates/* ~/.openclaw/workspace/
```

## First run

1. Edit `SOUL.md` — give your agent a name and personality
2. Edit `USER.md` — tell it who you are and what you're building
3. Tell your agent: **"Read AGENTS.md — you have a new memory system."**

## What to expect

Your agent will:
- Introduce itself by name
- Remember your timezone, goals, and projects across sessions
- Survive context compaction without losing track of what it was doing
- Ask itself 5 questions before every session end to catch knowledge that would otherwise be lost

## What's included

```
templates/
  SOUL.md               — Agent identity and personality
  USER.md               — Who you are (your agent's cheat sheet about you)
  AGENTS.md             — Session startup protocol
  MEMORY.md             — Long-term curated memory
  session-checklist.md  — Write-back checklist (prevents knowledge loss)
docs/
  compaction-recovery.md — How your agent recovers from context resets
```

## What happens after week 3

This starter kit works immediately. But after a few weeks of real use, you'll notice:

- **Daily logs pile up.** 20+ files with no automatic cleanup.
- **MEMORY.md gets bloated.** No structure to separate facts from guesses from decisions.
- **Old context gets buried.** You told your agent something important 2 weeks ago — good luck finding it.
- **No way to track what's proven vs. what's a hunch.** Your agent treats a tested strategy the same as a shower thought.

This is the natural ceiling of flat-file memory. It works, but it doesn't scale.

## AgentBrain Standard ($19) — Memory that doesn't rot

Everything in the starter kit, plus the infrastructure to keep it clean as it grows:

- **Auto-archive** — Daily logs older than 30 days move to cold storage automatically
- **Auto-reindex** — Full-text search across your entire memory vault, updated every 60 seconds
- **Frontmatter validation** — Weekly checks that your structured files have required fields and aren't going stale
- **Hypothesis tracking** — Structured templates with confidence levels, evidence chains, and review dates. Your agent knows the difference between "I think" and "I tested"
- **Strategy log** — Living playbooks with version history. Track what you tried, what worked, and why.
- **Setup wizard** — One script configures everything. Crons, search index, folder structure, validation.

## AgentBrain Pro ($39) — Memory that thinks

Everything in Standard, plus:

- **Interactive knowledge graph** — Browser-based visualization of every concept, decision, and connection in your vault. See how ideas relate across domains.
- **Typed relationship queries** — "What depends on this hypothesis?" "What strategies use this assumption?" Traverse your knowledge like a database.
- **Autonomous goal trees** — Decision trees your agent walks every heartbeat. Green actions happen automatically. Yellow actions happen and notify you. Red actions wait for approval. Your agent works while you sleep.

Coming soon → [link]

---

Built for [OpenClaw](https://github.com/openclaw/openclaw). Works with any agent using file-based memory.

No coding. No setup beyond 2 minutes.

Start here — you'll feel the difference immediately.
