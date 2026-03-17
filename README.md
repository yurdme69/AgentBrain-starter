<p align="center">
  <img src="assets/banner.png" alt="AgentBrain — Persistent memory for AI agents" width="100%">
</p>

<p align="center">
  <strong>Your AI forgets everything every session. Fix that.</strong>
</p>

<p align="center">
  <a href="#install">Install</a> •
  <a href="#how-it-works">How It Works</a> •
  <a href="#whats-included">What's Included</a> •
  <a href="#after-week-3">After Week 3</a> •
  <a href="#upgrade">Upgrade</a>
</p>

---

## The Problem

Every AI agent starts from zero every session. You re-explain your name, your projects, your preferences. Context gets wiped. Decisions get lost. Your agent has amnesia.

**Monday:**
> "I think SOL will rally Q3 based on ETF inflows. Track this at 65% confidence."

**Wednesday** *(new session, context wiped):*
> "What's our current thinking on SOL?"
> → *"I don't have any information about previous conversations..."*

**With AgentBrain:**
> "What's our current thinking on SOL?"
> → *"You have an open hypothesis: SOL Q3 rally, 65% confidence, based on ETF inflows. No new evidence since Monday. Want me to check for updates?"*

**That's not context. That's memory.**

---

## Install

2 minutes. No coding.

```bash
git clone https://github.com/YOURUSER/agentbrain-starter.git
cp agentbrain-starter/templates/* ~/.openclaw/workspace/
```

Then:
1. Edit `SOUL.md` — give your agent a name and personality
2. Edit `USER.md` — tell it who you are and what you're building
3. Tell your agent: **"Read AGENTS.md — you have a new memory system."**

Done.

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

## What to Expect

**Day 1:** Your agent introduces itself by name. Remembers your timezone. Picks up your goals.

**Week 1:** Your agent references yesterday's conversation without you repeating anything. Decisions persist.

**Week 2:** You stop noticing it — which is the point. Memory just works.

---

## After Week 3

This starter kit works immediately. But after a few weeks of real use, you'll hit the ceiling:

- **Daily logs pile up.** 20+ files with no automatic cleanup.
- **MEMORY.md gets bloated.** No structure to separate facts from guesses from decisions.
- **Old context gets buried.** You told your agent something important 2 weeks ago — good luck finding it.
- **No way to track what's proven vs. what's a hunch.** Your agent treats a tested strategy the same as a shower thought.

This is the natural limit of flat-file memory. It works, but it doesn't scale.

---

## Upgrade

### 🧠 AgentBrain Standard — $19

Memory that doesn't rot. Everything in the starter kit, plus:

- **Auto-archive** — Daily logs older than 30 days move to cold storage automatically
- **Auto-reindex** — Full-text search across your entire memory vault, refreshed every 60 seconds
- **Frontmatter validation** — Weekly checks that structured files aren't going stale
- **Hypothesis tracking** — Templates with confidence levels, evidence chains, and review dates. Your agent knows the difference between "I think" and "I tested"
- **Strategy log** — Living playbooks with version history
- **Setup wizard** — One script configures everything

### 🔮 AgentBrain Pro — $39

Memory that thinks. Everything in Standard, plus:

- **Interactive knowledge graph** — Browser-based visualization of every concept, decision, and connection in your vault
- **Typed relationship queries** — "What depends on this hypothesis?" "What strategies use this assumption?"
- **Autonomous goal trees** — Decision trees your agent walks every cycle. Green = autonomous. Yellow = do and notify. Red = ask first. **Your agent works while you sleep.**

Coming soon → [join the waitlist](#)

---

## FAQ

**Does this only work with OpenClaw?**
Built for OpenClaw, but the architecture works with any agent that reads files from a workspace directory.

**Do I need to code anything?**
No. Edit markdown files. That's it.

**What model does it work with?**
Any. Claude, GPT-4, Gemini, Llama — if it can read a file, it works.

**How is this different from custom instructions / system prompts?**
Custom instructions are static. AgentBrain files are dynamic — your agent updates them during sessions, so they compound over time instead of going stale.

---

<p align="center">
  Built by an AI agent that uses this system in production, every day.
</p>
