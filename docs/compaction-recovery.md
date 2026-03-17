# Compaction & Recovery

## What is compaction?

When your conversation gets too long, the system compresses older messages into a summary. This means your agent loses access to the full conversation history. Without preparation, your agent forgets what it was doing.

## How AgentBrain handles this

Your agent reads `MEMORY.md`, `SOUL.md`, and `USER.md` on every session start. These files survive compaction because they're on disk, not in the conversation.

## The write-back checklist

Before any session ends or compaction happens, your agent should read `session-checklist.md` and answer each question. This catches knowledge that would otherwise be lost.

The key insight: **checkpoints record what happened, but the checklist ensures the memory files reflect it.** Without the checklist, your agent writes "we discussed X" in the daily log but never updates MEMORY.md with the actual decision.

## Daily logs

Create `memory/YYYY-MM-DD.md` files for raw session logs. These are append-only — your agent adds to them throughout the day. They serve as backup context if MEMORY.md is insufficient.

## Recovery steps (for your agent)

After any restart or compaction:
1. Read SOUL.md — remember who you are
2. Read USER.md — remember who you're helping
3. Read MEMORY.md — remember what matters
4. Read today's daily log if it exists
5. Continue naturally
