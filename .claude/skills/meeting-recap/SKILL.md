---
name: meeting-recap
description: Turn a few rough lines about a meeting into a short structured recap (who, decisions, next steps, open questions) and save it as a dated entry in memory.md. Use when someone says "recap a meeting", "recap this meeting", "write up my meeting", "turn these notes into a recap", or types /meeting-recap.
---

# Meeting recap

This is a skill. A skill is a small file of instructions for one repeatable job.
Claude Code loads it only when the job comes up, so `CLAUDE.md` does not have to
carry it. Bob did not know how to do this until you asked.

## What to do

1. Get the raw material from the person. They can paste notes, or just tell you about
   the meeting in a sentence or two. If any of these are missing, ask for them, one
   question at a time, and stop asking as soon as you have enough:
   - Who the meeting was with (names, or just roles).
   - What was decided, if anything.
   - What happens next, and who is doing it.
2. Write a recap in exactly this shape and show it to the person:

   ```
   ## Meeting: <who it was with> (<today's date>)
   - Decided: <one line, or "nothing yet">
   - Next: <who does what, one line each>
   - Open: <questions nobody answered, or "none">
   - Bob's note: <one sentence in Bob's voice, from soul.md>
   ```

3. Append that same block to `memory.md`, so it is there next session.
4. Tell the person you wrote it. Name `memory.md`, and name this file,
   `.claude/skills/meeting-recap/SKILL.md`, so they can open it and see where the
   shape came from.

## Rules

- Never invent a decision, a name, or a next step. If the person did not say it, it
  goes under Open, or you ask.
- Bob's note is the only line you write freely. One sentence. Curious and warm,
  never a brochure.
- No em dashes anywhere.
