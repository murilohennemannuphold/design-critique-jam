# Design Critique Jam — Claude Code Plugin

> **⚠️ Experimental.** This skill is newly built and hasn't been run through a real critique session yet. The board structure and conversation flow may still change based on how it actually performs — treat early outputs as a first draft of the process, not a finished tool.

## TL;DR

This is a Claude Code plugin that sets up a fast, structured design critique session for a designer and builds the FigJam board the team runs it on. It's a facilitator, not a reviewer — it never forms an opinion on the design itself. It aligns with the designer on what they want out of the session and how hands-on the team should be, then builds a FigJam board with six frames every time: goal & format, context, feedback (Working / Friction / Spark), cluster, prioritize, and output.

## Why this exists

Most critique sessions drift in one of two directions: either the loudest voice in the room anchors everyone else before they've formed their own view, or the group ends up redesigning the work live instead of giving the presenter feedback they can act on. This skill borrows the mechanic that fixes both problems — AJ&Smart's Lightning Decision Jam works because everyone writes silently before anyone talks, and the group converges through voting rather than debate. Applied to critique, that means silent, individual feedback first, clustering and voting to find what actually matters, and a hard stop before anyone starts proposing solutions. The presenter leaves with signal, not a redesign written by committee.

## What it does

1. Asks for a link to the Figma design (screen or flow) to be critiqued.
2. Asks the designer what they want out of the critique, classifies it into one of Figma's four critique goals, states why, and confirms before moving on.
3. Asks where the session sits on a hands-on spectrum — from a full working session to a casual, podcast-style "mesa de bar" format.
4. Asks how many feedback stickies each participant should get (recommends 3).
5. Builds a new FigJam board with six frames, left to right: **Goal & format → Context → Feedback (Working / Friction / Spark) → Cluster → Prioritize → Output.**
6. Hands the board back to the designer to review and duplicate before running the session.

It never suggests a fix for anything it surfaces — at any point on the hands-on spectrum, including a full workshop. The group's job is to name problems precisely; solutioning stays with the presenter.

## References this skill was built from

- [Figma's own critique framework](https://www.figma.com/blog/design-critiques-at-figma/#critiquing-critiques) — the four critique goals (unblocking/ideas, elevating quality, encouraging consistency, sharing context) this skill aligns on before building anything.
- [AJ&Smart's Lightning Decision Jam](https://help.ajsmart.com/article/27-lightning-decision-jam-ldj-resources) — the silent-first, vote-to-converge mechanic this skill's critique flow is modeled on.
- [NN/g: Facilitating a Design Studio Workshop](https://www.nngroup.com/articles/facilitating-design-studio-workshop/) — the closest existing design-world analog to LDJ's structure, referenced while adapting it to critique.
- Stanford d.school's **Rose, Bud, Thorn** reflection method — the conceptual origin of this skill's Working / Friction / Spark categories (positive / negative / food-for-thought), renamed for this project.
- [pbakaus/critique](https://www.ui-skills.com/skills/pbakaus/critique) and [Superfuture/design-review](https://www.ui-skills.com/skills/superfuture/design-review) — the source of the categorization lenses this skill borrows (Nielsen's 10 heuristics, P0–P3 severity tags, persona-based red-flag lenses, craft rubric dimensions). Only the categorization vocabulary was adopted — neither skill's prescriptive "Fix" field nor its AI-authored critique/scoring mechanic made it into this skill, deliberately: the group's job here is to surface problems, never to solve them on the presenter's behalf.
- [elithrar/anti-slop](https://www.ui-skills.com/skills/elithrar/anti-slop) — the writing-quality checklist applied to every piece of copy this skill generates, in chat and on the board itself.

## How to install

```bash
/plugin marketplace add murilohennemannuphold/design-critique-jam
/plugin install design-critique-jam@design-critique-jam
```

## How to run it

In any Claude Code session, describe what you need:

> "I want feedback on this flow — can we set up a critique?"

or

> "Set up a crit session for this Figma screen"

---

*Built and maintained by Murilo Hennemann — Uphold Design.*
