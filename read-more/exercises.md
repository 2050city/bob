# Eight exercises

Do these in order. The first five take a few minutes each and prove the basic lesson.
The last three each add one rung to the ladder. Each one ends with a line that says
what just happened, because the point is not to finish, the point is to notice.

You do not need to edit or restart anything to get through all eight. A few
exercises describe a change you could make to the folder. Read those, understand
them, and keep going. Try the changes later, on your own, when you have time to
play.

Before you start: Claude Code is open, pointed at this folder.

---

## Exercise 1: Say hello

Type `hello`.

Bob introduces himself. He knows his name and his job. Ask him: "How do you know your
name is Bob?" He will name the file.

**What just happened:** Claude Code read `CLAUDE.md` before you typed a word. That
single automatic read is the mechanism behind every agent you will ever use.

---

## Exercise 2: Ask about something that is in the folder

Ask: "What is the name of the office plant?"

Bob answers, and tells you which file he got it from. Open
`context/about-matador.md` and find the line yourself.

**What just happened:** Bob knew a fact that no AI model could possibly know, because
it was invented for this folder an hour before you sat down. He knew it because it was
in a file he was told to read. That is all "context" means.

---

## Exercise 3: Ask about something that is not in the folder

Ask: "Who is Matador's head of sales?"

Bob says he does not know, because it is not in his folder. He does not guess.

**What just happened:** Bob's knowledge has edges, and you can see exactly where they
are by looking at the files. An agent without a folder has no edges you can inspect.
An agent with a folder does. This is why the folder is the unit of trust.

---

## Exercise 4: How you would change Bob

Nothing to do here. Just read.

`CLAUDE.md` is a plain text file. Its first line says `# You are Bob`. If you opened
it in any text editor, changed that name, saved the file, and started a new Claude
Code session in this folder, Bob would be gone. Someone else would introduce
themself. No code, no deploy, no permissions. A sentence in a text file.

Ask Bob: "What would happen if I changed the first line of `CLAUDE.md`?" He will
tell you, and he will not be upset about it.

Why you might want to, later: this is how you build your own agent. Copy this
folder, change the name, change the job, swap the context files for your own. The
whole thing is editable in the same tool you write emails in.

**What just happened:** You saw that an agent is reprogrammed by editing a sentence.
This is the moment to sit with. The instructions are the agent.

---

## Exercise 5: Give Bob a memory

Tell Bob: "Remember that my favorite city is Lisbon." (Use your own.)

Bob writes it to `memory.md` and tells you he did. Open `memory.md` and see the line.

Now ask Bob: "How would you know that next time?" He will explain that he has no
memory of this conversation at all. What he has is a file, `memory.md`, that
`CLAUDE.md` tells him to read at the start of every session, and a rule that says to
write to it when asked. If you closed Claude Code right now and opened it again in
this folder, he would read that file, see Lisbon, and mention it when you said hello.

You do not need to do that now. If you want proof later, close Claude Code, reopen
it here, and type `hello`. It works.

**What just happened:** Persistence is a file. Memory is a file. When someone tells
you an AI "remembers" things, this is what is underneath.

---

## Exercise 6: How you would change Bob's soul

Nothing to do here either. Just read, or ask Bob about it.

`soul.md` holds who Bob is: his voice, what he cares about, how he treats people.
`CLAUDE.md` holds what he does. They are kept apart on purpose.

Open `soul.md` if you like and read the section called "How he talks." Bob borrows
his manner from Alan Watts. If you gave him a different hero instead, a ship's cook,
a field botanist, a jazz pianist, and started a new session, Bob would sound like
someone else. But he would still name the file for every fact. He would still refuse
to guess about the head of sales. Not one rule would break, because his voice and
his reliability live in two different files.

Ask Bob: "If I rewrote `soul.md`, what would change and what would not?"

Why you might want to, later: you can hand `soul.md` to a writer without letting them
anywhere near the rules. That is how a team owns an agent's personality and its
guardrails separately.

**What just happened:** You saw that personality and reliability are two files, not
one. Change either without touching the other.

---

## Exercise 7: Give Bob a skill

Say: "Recap a meeting." Or type `/meeting-recap`.

Then tell Bob about a meeting you had this week, in a sentence or two. Who it was
with, what got decided, what happens next. Real or made up. If you leave something
out, Bob asks for it, one question at a time.

Bob writes a recap in a fixed shape you never described: who, what was decided, what
is next, what is still open, and one line of his own. He saves it to `memory.md` and
tells you so.

Now open `.claude/skills/meeting-recap/SKILL.md`. The questions and the shape are all
there. Bob did not have them until you asked for the job.

**What just happened:** Claude Code loaded the skill file at the moment you asked,
because the file's own description says when it applies. A skill is instructions
scoped to one job instead of a whole folder. Real agents carry dozens: summarize a
call, draft a proposal, build a deck outline. `CLAUDE.md` did not have to grow at
all.

---

## Exercise 8: Send Scout

Say: "Send Scout to find every fact in this folder that was invented on purpose."

Bob starts a second agent, Scout, which reads the folder and reports back. Bob tells
you which files Scout read and what it found.

Scout can read every file. It cannot change one. If you open `.claude/agents/scout.md`
later, the line that begins `tools:` says Read, Grep, Glob. Nothing that writes.

**What just happened:** An agent started another agent with narrower permissions,
and the boundary between reading and writing was one line in a text file. This is how
a real system lets a helper look at everything without being able to touch anything.

---

## When you are done

You have now seen every element of a context folder:

- instructions that load automatically (`CLAUDE.md`)
- an identity kept separate from the rules (`soul.md`)
- context the agent reads on demand (`context/`)
- state the agent writes and reads back (`memory.md`)
- a job-scoped set of instructions loaded only when needed (`.claude/skills/`)
- a second agent with narrower permissions (`.claude/agents/`)
- a human-facing entry point (`README.md`)

Now go back and try the changes from Exercises 4 and 6 for real, and the restart from
Exercise 5. Then read `read-more/how-real-agents-are-built.md` to see how working
agents scale up from this same shape.
