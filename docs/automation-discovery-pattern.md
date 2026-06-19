---
module: module-8-automation
related_skills:
  - skill-discovery
last_updated: 2026-06-19
---

# The Automation Discovery Pattern: Finding What to Automate in Your Own Workflow

## What It Is

You can't discover what should be automated by thinking about it abstractly. You can think about your work for an hour and come up with a few plausible candidates. You'll miss the most valuable ones, because the most valuable automation candidates are the tasks you've stopped noticing — the ones so routine that you execute them on autopilot without registering that you're doing the same thing for the twelfth time.

The **Automation Discovery Pattern** is a methodology for mining your own work history to surface those candidates. It works counter-intuitively: instead of asking "what do I want to automate?", it asks "what did I actually do, and what does the pattern look like?" The distinction matters. The first question is answered by memory and salience — you'll name the tasks that annoyed you recently. The second question is answered by data — what you actually spent time on, with frequency, regardless of whether it annoyed you.

The output of the methodology is not a list of automations to build. It's a scored, prioritized list of candidates, with enough context about each one to make a build/don't-build decision without bias from recency or frustration. Building the wrong automation is worse than building none — it creates maintenance overhead for something that doesn't pay back.

---

## The Three Phases

### Phase 1: History Scan

Retrieve and review 100-200 work sessions from the past 60-90 days. For each session, extract three things: what was the task, what type was the output, and what inputs were used to produce it.

The critical step is clustering by behavioral pattern, not by topic. A team update about project A and a team update about project B are the same cluster. A client report for client X and a client report for client Y are the same cluster. The content differs; the workflow is identical. Clustering by topic would separate them. Clustering by pattern groups them correctly.

Count sessions per cluster. This is the raw frequency signal.

Common cluster types you'll find:

| Cluster type | Example tasks | Signal to look for |
|---|---|---|
| Recurring status reports | Team updates, client summaries, executive briefs | Same output format, same input sources |
| Project initialization | Setup docs, onboarding, project kick-off | Same steps, same template structure |
| Research and synthesis | Competitive analysis, market briefs, topic overviews | Same sources consulted, similar output structure |
| Data pulls and presentations | Weekly metrics, dashboard exports, KPI reports | Same data sources, same visualization format |
| Communication batches | Response sequences, follow-up series | Same tone, same structure, same triggers |

Don't limit yourself to tasks you already feel are repetitive. Include everything, then let the counts surface the pattern.

### Phase 2: Transcript Validation

For the clusters with the highest session counts, go deeper. Read one or two actual session transcripts from that cluster. You're looking for four signals:

**What inputs did the task need?** If the same inputs appear in every transcript, they can be gathered automatically. If inputs vary unpredictably, the task may be less automatable than the frequency suggests.

**What steps were repeated?** Note the specific sequence: did the session always start with a data pull? Did it always end with the same formatting? The more consistent the steps, the stronger the automation candidate.

**What did the output look like?** Compare two transcripts from the same cluster. How similar is the output structure? Near-identical structure with different content is an excellent candidate. Structurally varied output is a weak candidate.

**Was the same setup re-explained?** This is the most important signal. If you find yourself re-explaining the context, the format, or the goal at the start of each session for the same type of task, that explanation should be a permanent setup — not reconstructed from scratch every time. Repeated setup re-explanation is the clearest sign that a task is costing more than it should.

### Phase 3: Scoring and Prioritization

Score each validated candidate across four dimensions.

| Dimension | 3 — Strong | 2 — Moderate | 1 — Weak |
|---|---|---|---|
| **Frequency** | 8+ sessions in period | 4–7 sessions | 2–3 sessions |
| **Recency** | Session in last 14 days | Session in last 30 days | Most recent session 31–90 days ago |
| **Complexity** | Multi-step, multi-input, 20+ min | 2+ inputs, 10–20 min | Single repeated action, under 10 min |
| **Repeatability** | Nearly identical structure each session | Minor structural variations | Significant structural variations each time |

**Score interpretation:**

- **9–12:** High priority. This is a strong candidate. Build this first.
- **5–8:** Medium priority. Worth building, but clarify scope before starting. Some variation may require a decision about what gets automated vs. what stays manual.
- **1–4:** Low priority. Note it for the next review cycle. If frequency increases, reassess.

**Coverage classification:**

Before finalizing the priority list, classify each candidate against existing automations you already have:

- **NEW:** No existing automation touches this workflow — it's a pure gap
- **PARTIAL:** An existing automation covers a subset of this task — building this would extend it
- **OVERLAP:** An existing automation already covers this, but it may not be triggering or surfacing correctly — the fix is configuration, not a new build

PARTIAL candidates are often faster to build than NEW ones because the infrastructure exists. OVERLAP candidates don't need a build at all — they need diagnosis.

---

## The Full Process

1. **Set the review window:** Choose the last 60-90 days of work sessions. Too short produces false negatives (one-off tasks look like patterns). Too long includes outdated workflows that no longer apply.

2. **Run the history scan:** Cluster all sessions by behavioral pattern, count sessions per cluster, sort by frequency.

3. **Validate top clusters:** For any cluster with 4+ sessions, read 1-2 actual session transcripts. Fill in the four validation signals: inputs, steps, output structure, setup re-explanation.

4. **Score and rank:** Apply the four-dimension scoring table to all validated candidates. Sort by total score.

5. **Classify coverage:** Mark each candidate as NEW, PARTIAL, or OVERLAP against existing automations.

6. **Present findings and confirm scope:** Review the ranked list. For candidates scoring 9–12, confirm: what exactly gets automated, what stays manual (judgment calls, approvals, customization), and what the success signal is. Don't build anything before this conversation.

7. **Build in priority order:** Start with the highest-scoring NEW or PARTIAL candidate. Build a minimal version first, use it for 2-4 weeks, then evaluate before building the next.

---

## Cadence

Run the full discovery pattern monthly for active users — those with 50+ work sessions in the period. Run quarterly for occasional users.

Frequency of review matters for one reason: patterns strengthen over time. A task that appeared twice last month and three times this month is a stronger signal than a task that appeared five times in a single week six months ago. The monthly cadence catches emerging patterns before they become invisible through habituation.

Between formal reviews, note any task where you catch yourself thinking "I've done this before" or "I wish I didn't have to explain this again." These are candidate flags to add to the next review cycle, not immediate triggers for automation.

---

## What It Is Not

**Not automatic automation.** The discovery pattern identifies candidates. Building automations requires a separate decision: does the efficiency gain justify the build time? Will the automation actually be used? What happens when the task changes? These are judgment calls that the scoring surface but doesn't resolve.

**Not about eliminating judgment.** High-judgment, high-variation tasks should not be automated even if they're frequent. A task that requires you to weigh competing priorities, read organizational context, or make nuanced decisions is valuable because of that judgment. Automating the shell of such a task while preserving the judgment is often possible; automating the judgment is not the goal.

**Not a substitute for intentional workflow design.** Sometimes the right response to a high-frequency, high-overhead task is to redesign the workflow itself — to ask whether the task should exist, whether it should be delegated, or whether the output format should change. Automation applied to a poorly-designed task produces fast, reliable bad outputs. Redesign first; automate the redesigned version.

**Not a one-time audit.** Workflows change. New tasks emerge, old ones become irrelevant, frequencies shift with project cycles. The automation discovery pattern is a cadenced practice, not a project with a completion date.

---

## Measuring Impact

Track these metrics before and after implementing automations discovered through this process:

| Metric | What it measures | Target direction |
|---|---|---|
| Hours per week on previously manual tasks | Raw time savings | Declining |
| Coverage rate | % of high-frequency tasks (4+ sessions) with an automation | Increasing |
| False positive rate | Automations built but used fewer than 3 times in 90 days | Near zero |
| Setup re-explanation rate | Sessions that start by re-explaining context for a repeating task type | Near zero |
| Output consistency | Variation in structure across instances of the same task type | Declining |

The clearest success signal: after implementing automations from a discovery cycle, the next review cycle surfaces fewer high-scoring candidates in the same clusters. The high-priority gaps have been filled, and new patterns have emerged to replace them.

---

## Related

- [Manual Repetition Overhead](manual-repetition-overhead.md) — the problem this pattern systematically addresses
- [Invisible Progress](invisible-progress.md) — how to measure effort reduction that doesn't announce itself
- [The Vault Immune System](immune-system-pattern.md) — a complementary pattern for maintenance work that follows a similar detect-score-act structure
