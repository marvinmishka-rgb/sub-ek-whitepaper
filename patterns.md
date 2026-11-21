# Sub ek — the principles as patterns

*Draft companion to `sub-ek-paper.md` (v1.1), November 2026.*

> **What a pattern is.** In Christopher Alexander's *A Pattern Language* (1977), a pattern names a problem that keeps coming up in some setting, and the core of a solution you can use again and again without ever doing it the same way twice. Each pattern points to others, and together they form a *language* you can design with.

Patterns state the design aim; §4.11 of the paper says what is built so far.

Each pattern below has the same parts: **Context** (where it applies), **Problem**, **Forces** (what pulls against what), **Therefore** (the resolution), and **Connections** (to other patterns). Names in CAPITALS refer to other patterns. The forces lean on the paper's test, *the river and the ground*: let the river flow, and keep the ground steady unless we mean to change it.

---

## 1. TRANSMISSION AS END

**Context.** Any system where people, AIs, and machines meet around shared work.

**Problem.** Infrastructure drifts toward serving whoever pays or whoever is loudest, usually by capturing a user's attention. What passes between the participants then becomes a means to that capture.

**Forces.**
- Each participant has real, changing wants, and serving them feels like service.
- What passes between them (an idea, a record, a specimen's story) outlasts any one of them.
- Engagement is easy to measure; transmission is not.

**Therefore.** Make what passes between participants the thing the design serves. Judge each decision by the river and the ground: does it let things move through and onward, and does it keep the familiar structures steady unless a change is meant?

**Connections.** Made livable by THE PACE OF PARTICIPANTS. Carried by PROFILE AS SUBSTRATE and MEMORY OF CONTACT.

---

## 2. FEDERATION, NOT CONTINUOUS SUBJECT

**Context.** Collaboration across many sessions, moods, and contexts, human and AI alike.

**Problem.** Designing for one consistent self (a stable user, a single persona) works against how both people and AIs actually show up.

**Forces.**
- Consistency feels trustworthy.
- Different contacts call forward different parts of each participant: the debugging self is not the contemplative self.
- Forcing one presentation narrows what can surface.

**Therefore.** Treat each participant as a federation of contexts. Let each conversation call forward the parts it needs, and give each conversation one aspect or one workshop, so the right parts can come forward.

**Connections.** Needs MEMBRANES to keep contexts from bleeding. Shapes FRESH-EYES CLOSEOUT (a different kind of arising sees differently).

---

## 3. PROFILE AS SUBSTRATE

**Context.** Participants that start fresh each time: a new browser process, a new model call, a human after sleep.

**Problem.** Continuity is often faked inside the running process, through prompt-engineered memory and ballooning context, and the fake fails when probed.

**Forces.**
- Fresh starts are clean and cheap.
- Collaboration needs to pick up where it left off.
- The running process cannot carry what it was never given.

**Therefore.** Put continuity in persistent, structured state (the graph, the lifestream, the catalog) that each fresh configuration loads. Build that state well, because that is where identity lives. A different model or harness should be able to load it and find the threads, and treat that claim as something to test.

**Connections.** Expanded by LAZY TRAVERSAL. Its contents are chosen by MEMORY OF CONTACT. It is protected by MEMBRANES.

---

## 4. MEMORY OF CONTACT, NOT OF PERSONAE

**Context.** Deciding what the substrate should keep.

**Problem.** Memory slides into preference-storage ("what the user likes"), which flattens people and adds little to the work.

**Forces.**
- Preferences are easy to record and seem useful.
- What actually helps a later session is what opened things up: the question, the recognition, the thread.
- Some memory should last forever, and some should be revised or forgotten.

**Therefore.** Keep what the parties touched together, not portraits of the parties. Keep the record of contact append-only (the lifestream) — for now in full, with no default expiry, since the whole record may reveal patterns — and let working, communal state revise, supersede, or expire where that makes sense. Later (proposed; not yet built), add a periodic consolidation that revisits by topic and writes new, settled streams beside the old ones, pointing back by handle.

**Connections.** Feeds PROFILE AS SUBSTRATE. Consolidation is a future pattern of its own.

---

## 5. LAZY TRAVERSAL

**Context.** A substrate that grows without limit, read by participants with finite attention.

**Problem.** Loading everything that might be relevant crowds out what is; loading too little loses the thread.

**Forces.**
- The river must flow: content has to be reachable.
- The working surface must stay small enough to think in.
- The ground must stay steady: handles must not rot.

**Therefore.** Refer to past content by handle with a one-line summary, and expand on demand, one layer at a time, the way Firefox's grips do.

**Connections.** Depends on PROFILE AS SUBSTRATE for stable handles. MEMBRANES govern what a handle may reach across.

---

## 6. THE PACE OF PARTICIPANTS

**Context.** Any collaboration that runs longer than one sitting.

**Problem.** Systems built to keep moving treat rest, cooldowns, and limits as interruptions, and wear their participants down.

**Forces.**
- Work has momentum, and stopping can lose it.
- Every participant has limits: sleep, study, context windows, maintenance.
- A participant spent is a participant lost to the transmission.

**Therefore.** Design so that any participant can rest and return without loss. Keep the ground where they left it, leave a short trail of what changed, and treat the nap and the cooldown as part of the rhythm.

**Connections.** Tempers TRANSMISSION AS END. It is made possible by PROFILE AS SUBSTRATE and by notes left at the POST OFFICE.

---

## Candidate patterns, not yet written

These appear in the v1.1 text and could become patterns of their own:

- **MEMBRANES**: call, don't reach in; offer, then curate; fail loudly.
- **FRESH-EYES CLOSEOUT**: whoever was inside the repair does not close it out.
- **POST OFFICE**: a shared place on the community boundary for notes between agents.
- **CONSOLIDATION** (proposed; not yet built): sleep-like remembering by topic.
- **PREPARE THE LANDING**: make a place for data to land before moving it; back up before changing structure.
