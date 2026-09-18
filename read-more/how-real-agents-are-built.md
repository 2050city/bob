# How real agents are built

Bob is a context folder with a handful of files and one lesson. Real working agents
have the same shape with more of everything. Here is the ladder, one rung at a time.
Bob now stands on the first rung of most of them, so each section names the file where
you can see it.

## More context files

Bob has two context files, `context/about-matador.md` and `context/about-guidegeek.md`,
and a table in `CLAUDE.md` that says which one to read for which kind of question. A
working agent might have twenty: one per client, one per project, a glossary, a style
guide, a list of open commitments. The table gets longer. Nothing else changes.

## Instructions that stack

Claude Code reads a `CLAUDE.md` in the folder you open. It also reads one from your
home directory that applies everywhere, and one from any parent folder above you.
They layer. House rules at the top, project rules in the middle, task rules closest
to the work. Greg's machine does this today: his global file knows who he is, and each
client folder knows that client.

## Skills

A skill is a small file of instructions for one repeatable job: summarize a call
transcript, draft a proposal in house style, build a deck outline. The agent loads it
only when the job comes up. Same idea as `CLAUDE.md`, scoped to a task instead of a
folder. Bob has one, at `.claude/skills/meeting-recap/SKILL.md`. Exercise 7 uses it.

## Subagents

An agent can start another agent with its own instructions to go do one thing and
report back. A read-only researcher, for example, that can look at everything but
write nothing. Each subagent is, again, a set of instructions in a file. Bob has one,
called Scout, at `.claude/agents/scout.md`. Exercise 8 sends it out.

## Tools and connectors

Bob can read and write files in his folder. A working agent can also read email, check
a calendar, search a CRM, post to Slack. Each of those is a connection granted to the
agent, and the instructions file says when to use it and when to ask first. Bob has
none of these. That is the one rung this folder does not climb, because it needs
accounts and permissions that do not belong in a training folder.

## Rules about when to stop

The most important lines in a real agent's instructions are not about what it can do.
They are about what it must ask before doing. Send this? Draft this? Delete this? The
folder holds those rules too, in plain text, where a human can read and change them.
Bob's version is the short list at the bottom of `CLAUDE.md`, and the `tools` line at
the top of `.claude/agents/scout.md`.

## The thing to carry with you

Every rung on this ladder is still text in a folder. When someone shows you an
"AI agent," ask to see the folder. If they cannot show you one, ask what the
instructions are and where they live. The answer tells you everything about how much
to trust it.

## Bob's soul

Some agent folders split the instructions into two files. One says who the agent is:
its voice, its values, how it treats people, what it cares about. The other says what
it does: the file table, the rules, the tools, when to ask before acting. Bob does
this. The first file is `soul.md`. Claude Code does not know that name. It only matters
because `CLAUDE.md` says, in its second line, "Read `soul.md` first and be that." Same
mechanism as everything else in this folder. A file the agent reads because the
instructions point to it.

The reason to split them is that identity and operations change at different speeds
and belong to different people. The rules in `CLAUDE.md` change whenever you add a
file or a tool. Who Bob is should change almost never, and when it does, the person
changing it is more likely to be a writer than an engineer. Keeping the soul in its
own file means someone can rewrite Bob's voice with confidence and never risk breaking
the rule that tells him where the exercises are.

Exercise 6 is the proof. Give a trainee `soul.md` and tell them to change Bob's hero,
or make him formal, or make him answer only in questions. Start a new session. Bob's
personality changes and every rule still holds: he still knows where his files are,
still refuses to guess, still writes to `memory.md`. That separation, the voice moving
while the behavior stays put, is the clearest way to see that an agent's personality
and an agent's reliability are two different things, and that you can hand one of them
to almost anyone.
