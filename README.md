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

## Full version

The paid version adds structured knowledge tracking, auto-maintenance, and a visual knowledge graph:

- **$19 Standard** — Memory vault with schemas, auto-reindex, auto-archive, validation scripts, hypothesis + strategy tracking
- **$39 Pro** — Everything standard + interactive knowledge graph, typed relationship queries, autonomous goal trees

Coming soon.

---

Built for OpenClaw. Works best with local agents using file-based memory.

No coding. No setup beyond 2 minutes.

Start here — you'll feel the difference immediately.
