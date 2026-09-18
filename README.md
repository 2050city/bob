# Start here

This folder is an agent. His name is Bob.

That sentence is the whole lesson. Everything else in this folder exists to make you
believe it.

## What you are looking at

There is no app, no database, no code. There are ten short text files and one Word
doc. One of them, `CLAUDE.md`, is read automatically by Claude Code the moment you
open this folder. That file tells Claude what it does and which other files to read.
The first file it points to, `soul.md`, tells Claude who it is. The rest are read only
when `CLAUDE.md` says to or when you ask.

Open `CLAUDE.md` now and read it. It takes two minutes. Then open `soul.md`. You will
understand Bob better than Bob does.

Notice the shape of the folder. Three files sit at the root of every context folder
you will ever open, here or anywhere: `CLAUDE.md`, `README.md`, and `memory.md`. This
folder adds a fourth, `soul.md`, which is a choice, not a rule. The two visible
subfolders, `context/` and `read-more/`, are just how this folder chose to organize
the rest. There is also a hidden folder, `.claude/`, holding one skill and one
subagent. In Finder, press Command, Shift and the period key to see it. Learn the
root files and you can read any agent.

## How to meet Bob

1. Open Claude Code.
2. Point it at this folder. In the desktop app, choose this folder as the working
   directory. In a terminal, `cd` into this folder and run `claude`.
3. Type `hello`.

Bob will introduce himself. He knows his name because you just opened a folder that
contains a file that says "You are Bob." He sounds the way he sounds because that file
told him to read `soul.md`. No other reason.

One thing to expect: the first time Bob tries to write to `memory.md`, or to send
Scout, Claude Code will stop and ask your permission. Nothing is broken. Say yes.
Bob cannot change a file or start a helper without a human agreeing to it, and that
is part of the lesson.

## Then what

Open `read-more/exercises.md` and do the eight exercises in order. The first five take
a few minutes each and prove the basic lesson. The last three each add one rung: a
soul, a skill, and a subagent. Or just ask Bob to walk you through them. He has read
the file.

## The formula

If you want the idea in one line before you meet Bob, open `read-more/The Formula.docx`.
It says: Agent = Assistant (Claude) + Tools + Instructions. Bob is that formula with
small numbers plugged in.

## Read in this order

1. `README.md`, this file.
2. `CLAUDE.md`, then `soul.md`. What Bob does, then who Bob is.
3. `read-more/exercises.md`, then do the exercises with Bob.
4. `read-more/The Formula.docx`, the one-line version of what you just saw.
5. `read-more/how-real-agents-are-built.md`, how the same shape scales up to working
   agents. Bob now has a small version of most rungs on that ladder.

## Why this matters

Every serious AI agent you will hear about, at Matador or anywhere else, is a more
elaborate version of this folder. More files, more rules, more tools plugged in. The
shape is the same: a place on disk, a set of instructions that load automatically,
and a pile of context the agent can read. Once you can see that shape here, you can
see it everywhere, and you stop being impressed by the wrong things.

## A note if Greg is demoing this on his machine

Greg's Mac has a second instructions file that loads in every folder, not just this
one. So when he runs Bob, Bob also carries a few of Greg's house rules. That is not a
bug. It is the next lesson: instructions stack, and the folder closest to the work
usually wins. On your own machine, Bob will have only what is in this folder.
