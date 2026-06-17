# An accumulative "second brain" on top of Claude Code

> Presentation (EN) · Русский: [PRESENTATION.md](PRESENTATION.md) · Text version: [README.en.md](README.en.md)


Full presentation. Dated snapshot, 17 June 2026. A personal system built between roughly 11 April and 17 June 2026 (about 2.2 months). Applied projects, their domains, servers and clients are not disclosed.

Terms: a hook is a script Claude Code runs by itself at a set moment; a skill is a command of the form `/name`; launchd is the macOS scheduler; an embedding is a numeric "fingerprint of meaning" for search; a K-note is a knowledge atom; a lesson is a "symptom, cause, fix" record; a MOC is a map of content.

---

## Slide 1. The problem

A normal AI chat starts every conversation from zero. It forgets context. It repeats the same mistakes. It makes up facts when it does not know. This system fixes exactly those three problems and turns a one-off chat into an accumulative, self-improving layer.

---

## Slide 2. In one paragraph

Every session adds knowledge to long-term memory. Every mistake becomes a lesson. Every rule is enforced by machine, not by human memory. Nightly timers tidy up without the human. External research and external repositories are studied automatically and reduced to their essence. The difference from a folder of notes is that the system rests on verifiable principles from knowledge theory and engineering practice, implemented as executable code.

---

## Slide 3. Scale (17.06.2026)

| What | How much |
|---|---|
| Commands (skills) | 40 |
| Interceptor hooks | 357 files (274 Python + 83 shell), 288 registered |
| Background timers (launchd) | 76 plists, 75 loaded |
| Lessons | 140 |
| Knowledge atoms (K-notes) | 437 |
| Session files | about 867 |
| Behavior rules | 73 contracts |
| Maps of Content | 27 |
| Procedures | 22 |
| Link graph | 1434 nodes, 12073 edges |
| Lines of code (Python + shell) | about 74,800 |
| External repositories in registry | 69 (114 cards) |
| Total memory | 2242 files, 264k lines, about 1.95M words |

Numbers depend on the counting method: part of the system's culture is that a number without its method is unreliable.

---

## Slide 4. Architecture: four loops

1. Memory: what we know (6 tiers).
2. Learning: how knowledge is born, checked, decays and is revived (8 phases).
3. Execution and protection: rules and hooks keep work on protocol and block mistakes in real time.
4. Observation: timers, audits and a dashboard watch that the first three loops stay alive.

Cross-cutting principles sit on top. They are the core.

---

## Slide 5. Principle 1: Zettelkasten

Luhmann's idea: knowledge is stored as atoms (one note equals one thought) linked by references; structure comes from maps of content, not folders.

Implemented: one file equals one note, a linter catches short notes and duplicates. 2789 wiki-links across 437 notes (6.38 per note), zero notes without outgoing links. 27 maps are assembled by a script. A bidirectional index is rebuilt daily. Difference from Luhmann: most links and all maps are machine-generated. Stronger in coverage, weaker in organic feel.

---

## Slide 6. Principle 2: Knowledge graph

Links form a directed graph. 1434 nodes, 12073 edges, average degree about 8.4, a power-law distribution with hubs. The top hub, a meta-security rule, has 413 citations. A separate code-dependency graph is built by parsing syntax, with decay protection: a new graph under 10% of the old one rolls back.

---

## Slide 7. Principle 3: Accumulative self-evolution (Karpathy)

The system evolves on its own. Executable artifacts with metrics were found:

- A nightly fitness loop: one change up to 50 lines, a metric measurement (search precision plus canary plus drift), rollback via git on regression.
- Four-tier memory: semantic, procedural, episodic, working.
- Hybrid search by keywords and by meaning.
- Reflection after each session (a "session voice" field in 359 files).

Sign of maturity: part of the approach was deliberately rejected as premature. What works is taken; the form is not copied.

---

## Slide 8. Principle 4: Cross-project memory

A lesson from one project protects the others. Lesson search is three-tier: the project's own lessons, related projects' lessons, a random by-meaning pick. A single base of 140 lessons and 73 rules applies to all projects.

---

## Slide 9. Principle 5: Portable storage

Memory is code. Several git repositories, one-way sync after each edit, auto-commit and auto-push on a timer. A hook blocks hardcoded absolute paths so moving to another machine does not break the system.

---

## Slide 10. External repositories: collect, analyze, choose

The system continuously collects, analyzes and standardizes external GitHub repositories, and takes only what is needed.

- Auto-collect: a hook catches every GitHub link from four sources.
- Analyze: stars, license, freshness, releases, dependencies. A separate tool checks "am I reinventing something that exists".
- Standardize: a uniform card and a status (use as is, adopt the idea, watch, reject).
- Selective integration: a part is taken, often rewritten for the local stack. A license with no usage rights or a paid SaaS means rejection.

Registry: 69 repositories (114 cards): catalog 21, adopt pattern 24, installed 11, watch 5, rejected 4.

---

## Slide 11. Self-development

The principle running through it all: anything that can be automated, studied quickly and reduced to its essence without spending the human's time is done by itself. The human gets a finished conclusion, not raw material.

- Research via NotebookLM runs by itself, the answer is distilled into a knowledge atom.
- Repositories are reduced to a card with a verdict.
- Mistakes become lessons by themselves, lessons surface by themselves, contradictions are caught.
- Nightly timers repair, index, back up and check.
- A fitness loop tries edits and rolls back whatever worsened a metric.

The human spends time only on what needs a human decision.

---

## Slide 12. Memory loop: six tiers

| Tier | What it stores | Count |
|---|---|---|
| Lessons | symptom, cause, fix | 140 |
| Knowledge (K-notes) | knowledge atoms | 437 |
| Sessions | log of each session | ~867 |
| Procedures | recipes "on X, steps 1..N" | 22 |
| Maps of Content | navigation | 27 |
| Indexes | summary indexes | ~10 |

Any fact is found three ways: by index, by meaning, by graph.

---

## Slide 13. Learning loop: eight phases

Capture, review, promotion, indexing, decay, supersession, recall, linking. Each phase is run by its own hook or timer. Known weak spot: the capture queue stalls, the review phase lags.

---

## Slide 14. Protection loop: rules and hooks

A rule you "have to remember" gets forgotten. So critical rules are turned into blocking hooks. Protection is three-layered: before the action, after the action, before the answer.

What gets blocked in practice:

| Moment | What it blocks |
|---|---|
| Before a command | destructive ops (rm -rf, force-push, writing to keys) |
| Before the answer | the words "done, fixed, correct" without command output |
| Before an agent | an agent without a narrow scope and a testable hypothesis |
| Before an edit | an unread cross-model review |
| Before an edit | hardcoded absolute paths in new code |
| End of a turn | finishing with unclosed checks |

73 rules with priorities and conflict resolution. Every rule with a state dependency must have an enforcing hook, otherwise it counts as an orphan and is caught by an audit.

---

## Slide 15. Observation and quality control

- Dashboard (21 sections, a single state file). Over a month the assistant cost under $2, the main research is free.
- Cross-model control: a second model (Codex/GPT) reviews code changes.
- Free research via NotebookLM, answers pulled into memory.
- Three-model debates for assessments and brainstorms: a guard against shared hallucinations of a single model.
- External inputs: notes and photos from the phone via a messenger bridge with text recognition.

---

## Slide 16. Cross-model control (Codex), June numbers

- 5 auto-hooks: review after edits (a $5 per day cap), review injection into the prompt, a blocker on an unread review, a verdict tracker, an auto-call for help after three stalls.
- June volume: 324 reviews, 1336 findings (689 valid, 366 stylistic, 278 false).
- Live false-positive rate about 21% (measured by fact, not hardcoded).
- Cost about $0.05 per call.

Purpose: a second model catches bugs the primary model missed, before deploy.

---

## Slide 17. Maturity by domain

CMMI scale (1 ad-hoc, 5 optimizing), 10 domains, average about 2.9.

- Level 4 (Managed, measured): Rules, Lessons.
- Level 3 (Defined): Hooks, Commands, Dashboard, Plans, Memory index, Graph.
- Level 2 (Repeatable, code-behavior gap): Capture, Verdicts, NotebookLM.
- Level 5: none yet.

Rule coverage by enforcers: of 73 rules, 22 fit a hard blocker, the other 51 by nature require judgment (style, assessments) and are checked by a judge model. Of the 22, blockers cover 12. The main limiter of the whole system is the gap "code works, behavior lags", treated by turning reminders into blockers.

---

## Slide 18. How it grew (four phases)

- Foundation (before 11 April 2026): rules as text files, no enforcement.
- Skeleton (11 April): the main backbone of memory, hooks and commands in a single day.
- Saturation (April and May): growth in lessons and rules, a shift from reminders to hard blockers.
- Hardening (June): a kill switch, a circuit breaker, cross-model control, a rule-coverage audit.

More than half of all commits were made in the last month. The pace is rising.

---

## Slide 19. Production reality

The system was built alongside the applied projects, not at their expense. The portfolio is 14 projects of varying complexity (3 complex, 4 medium, 7 simple). The complex flagships are in production and working: verified by a live network ping rather than by cards, every checked endpoint responds, certificates are valid. The flagship has automated deployment with linters, a health check, smoke tests and a cross-model check. Project domains and purpose are not disclosed. The author is not a professional programmer; the system was built for personal use.

---

## Slide 20. Time and volume

- Start: about 11-14 April 2026.
- Duration: about 67 days (roughly 9.5 weeks) to 17 June.
- Volume: about 867 sessions, about 1464 commits, about 74,800 lines of code.
- Person-hours are deliberately not invented: objective metrics, not an eyeball estimate.

---

## Slide 21. Honest limitations

- Over-engineering risk: 357 hooks maintained by one person, some long dormant. The system counts firings, not the benefit of each.
- Meta-work competes with the product: a large part of two months went into the tool itself.
- Metrics are self-referential: the system rates itself, with no external A/B comparison "with versus without".
- Bus factor of one: everything depends on one person and one Mac.
- A machine Zettelkasten loses the serendipity of hand-made links.
- Even a self-documenting system drifts: while preparing the reports a gap was found between documentation and code.

---

## Slide 22. Bottom line

In about 2.2 months an accumulative, self-improving layer on top of Claude Code was built: about 2242 memory files, about 74,800 lines of code, 357 hooks, 76 nightly timers, 73 rules serving a portfolio of 14 projects. It rests on verifiable principles: Zettelkasten, knowledge graph, accumulative self-evolution, cross-project transfer, portable storage. It studies incoming material on its own, drops the excess, keeps the essence and builds itself out. Maturity about 2.9 of 5. The main front is closing the gap "code works, behavior lags" with enforcement instead of reminders. The pace is not slowing.
