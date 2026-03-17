<p align="center">
  <img src="assets/banner.png" alt="AgentBrain" width="100%">
</p>

<h3 align="center">Your AI forgets everything. Fix that.</h3>

<p align="center">
  Give your AI agent permanent memory that compounds across every session.
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> •
  <a href="#how-it-works">How It Works</a> •
  <a href="#whats-included">What's Included</a> •
  <a href="#upgrade">Upgrade</a>
</p>

---

<p align="center">
  <img src="assets/proof-moment.png" alt="Agent recalling a hypothesis from a previous session" width="680">
</p>

<p align="center"><em>Session 47. The agent remembers a hypothesis from Monday — confidence level, evidence, next review date. No re-explaining needed.</em></p>

---

## Quick Start

**2 minutes. No coding.**

```bash
git clone https://github.com/yurdme69/AgentBrain-starter.git
cp AgentBrain-starter/templates/* ~/.openclaw/workspace/
```

1. Edit `SOUL.md` — give your agent a name and personality
2. Edit `USER.md` — tell it who you are and what you're building
3. Tell your agent: **"Read AGENTS.md — you have a new memory system."**

**Your agent now remembers across sessions.** It knows who it is, who you are, and what you were working on — every time it starts up.

Over time, memory compounds. Decisions persist. Context builds. Your agent gets sharper the longer you use it.

---

## How It Works

```
┌─────────────────────────────────────────────────────┐
│                   SESSION START                      │
│                                                     │
│   Agent reads: SOUL.md → USER.md → MEMORY.md        │
│   "I know who I am, who you are, and what we        │
│    were working on."                                 │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────┐
│                  DURING SESSION                      │
│                                                     │
│   Agent works normally. Learns new things.           │
│   Makes decisions. Gets new information.             │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────┐
│                   SESSION END                        │
│                                                     │
│   Write-back checklist triggers:                     │
│   ✓ Did any belief change? → Update file             │
│   ✓ Was a decision made? → Log to MEMORY.md          │
│   ✓ New fact about the human? → Update USER.md       │
│   ✓ Mistake made? → Record the lesson                │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
          ┌────────────────────────┐
          │  Files updated on disk  │
          │  ↩ Next session reads   │
          │    them on startup      │
          └────────────────────────┘
```

The key insight: **most agents lose knowledge not because they can't store it, but because nothing tells them to write it down before the session ends.** The write-back checklist fixes that.

---

## What's Included

```
templates/
  SOUL.md               — Agent identity and personality
  USER.md               — Who you are (agent's cheat sheet about you)
  AGENTS.md             — Session startup protocol
  MEMORY.md             — Long-term curated memory (grows over time)
  session-checklist.md  — Write-back checklist (prevents knowledge loss)
docs/
  compaction-recovery.md — How your agent recovers from context resets
```

Every file has fill-in-the-bracket prompts. Edit, save, done.

---

## What Happens After Week 3

This starter kit works immediately. But after a few weeks, you'll hit the natural ceiling of flat-file memory:

- Daily logs pile up with no automatic cleanup
- MEMORY.md gets bloated — no structure to separate facts from guesses
- Old context gets buried and hard to find
- No way to track what's been tested vs. what's still a hunch

When you hit that wall, **AgentBrain Standard** ($19) adds auto-archive, full-text search, frontmatter validation, and structured hypothesis tracking — everything you need to keep memory clean as it grows.

**AgentBrain Pro** ($39) adds an interactive knowledge graph, typed relationship queries, and autonomous goal trees — your agent works while you sleep.

Coming soon.

---

## FAQ

**Does this only work with OpenClaw?**
Built for OpenClaw, but works with any agent that reads files from a workspace directory.

**Do I need to code anything?**
No. Edit markdown files. That's it.

**What model does it work with?**
Any. Claude, GPT-4, Gemini, Llama — if it can read a file, it works.

**How is this different from custom instructions?**
Custom instructions are static. AgentBrain files are dynamic — your agent updates them during sessions, so memory compounds instead of going stale.

---

<p align="center">
  Built from the same memory system our AI agent relies on daily.
</p>
