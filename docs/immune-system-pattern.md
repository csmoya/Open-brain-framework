---
module: module-6-health
related_skills:
  - open-brain-health
  - open-brain-eval
last_updated: 2026-06-19
---

# The Vault Immune System: Automated Health, Human Judgment

## What It Is

The Vault Immune System is a layered approach to knowledge vault maintenance. It separates automated detection from human judgment, and continuous monitoring from periodic review — so the vault can maintain structural health at scale without requiring a proportionally growing maintenance effort.

The name comes from the analogy: a healthy immune system doesn't wait for you to feel sick and then do a manual inspection of every organ. It runs continuously, detects anomalies automatically, and escalates to conscious attention only when something requires a decision. The vault equivalent does the same: automated checks run without human attention, flag problems with severity signals, and surface only what requires a human decision.

The system has four layers. Each layer addresses a different class of problem. Together, they cover everything from broken links (mechanical) to whether your vault is improving over time (strategic).

---

## The Four Layers

### Layer 1: Automated Detection

Deterministic checks that run over the vault without requiring human attention. No AI, no judgment — pattern matching over structured data.

| Check | What it finds | Why it matters |
|---|---|---|
| Orphan scan | Notes with zero inbound links | Orphans are invisible to navigation and search |
| Broken link scan | References to notes that no longer exist | Broken links silently corrupt retrieval paths |
| Crowding scan | Search terms associated with too many notes | Crowded terms lose discriminative power |
| Maturity audit | Notes claiming high maturity without supporting evidence | Inflated confidence markers mislead retrieval priority |
| Stale-use scan | Notes that are heavily retrieved but not updated recently | High-use stale notes may be confidently spreading outdated thinking |
| Count drift | Significant changes in note count across domains | Unexpected changes signal processing failures or deletions |
| Structural consistency | Labels, tags, or schema used inconsistently | Inconsistency fragments search and navigation |

Output: a prioritized list of flagged notes with the specific problem, severity, and suggested action. The human reads the list, not the vault.

### Layer 2: Eval Scorecard

Periodic measurement of six vault dimensions, each producing a trend-tracked status. This layer answers the question the automated checks can't: "Is the vault getting better or worse over time?"

| Dimension | What it measures | Status signal |
|---|---|---|
| Integrity | Orphan rate, broken links, maturity accuracy | Improving / Stable / Degrading |
| Graph quality | Average inbound links, typed link ratio, graph density | Improving / Stable / Degrading |
| Pipeline health | Inbox backlog, synthesis conversion rate | Improving / Stable / Degrading |
| Practice activity | Sessions in last 30 days, retrieval frequency | Improving / Stable / Degrading |
| Funnel conversion | Notes advancing through maturity stages per period | Improving / Stable / Degrading |
| Output production | Posts, documents, decisions produced in last 30 days | Improving / Stable / Degrading |

The scorecard is computed on a schedule (monthly for stable vaults, weekly during active growth periods) and compared against prior periods. A single bad month is noise. Three consecutive months of declining graph quality is a structural pattern that requires a decision.

### Layer 3: Continuous Graph Maintenance

Every time a significant batch of notes is added to the vault, the knowledge graph is updated. New connections between notes are classified by semantic type — not just "this note mentions that note," but "this note *contradicts* / *extends* / *refines* / *provides evidence for* that note."

This layer runs after note-creation operations, not on a separate schedule. It keeps the graph current without requiring a dedicated maintenance session.

The practical effect: when you retrieve a note and explore its connections, the connection types are accurate and current. You can navigate from "this principle" to "the cases that support it" to "the principles that contradict it" — rather than following generic links that all look the same.

This is deterministic. It reads the verbs and phrases around each link to classify the relationship. No LLM required; no human attention required.

### Layer 4: Periodic Review

Once per week, a review of actual vault activity — what was practiced, what sessions occurred, what ideas surfaced during daily work that weren't formally captured.

This layer catches what automated detection misses: signal buried in the noise of daily activity. A note that keeps appearing in different contexts might be a cornerstone idea that deserves promotion to a higher maturity level. A pattern of failed retrievals on a topic suggests a gap in coverage. An idea that appeared in three separate sessions but was never written as a note is a synthesis opportunity.

The review produces a brief: what actually happened this week vs. what you thought happened. The gap between perceived activity and real activity is often significant.

---

## The Process

**After each significant batch of new notes (10+):**

1. Run Layer 1 automated detection on the new notes and their affected domains
2. Run Layer 3 graph update on the new notes
3. Review the flagged items list (typically 5-15 minutes)
4. Fix critical issues immediately; add maintenance tasks to queue

**Weekly:**

1. Run Layer 4 review
2. Check the maintenance task queue; address high-priority items
3. Note any ideas surfaced in the review that should be captured as notes

**Monthly:**

1. Run Layer 2 eval scorecard
2. Compare against prior month
3. If any dimension is degrading for 2+ consecutive months, diagnose root cause and adjust process

---

## Cadence

| Trigger | Layer | Time required |
|---|---|---|
| After significant note addition | Layer 1 (detection) + Layer 3 (graph) | Automated; 5-15 min human review |
| Weekly | Layer 4 (activity review) | 15-20 min |
| Monthly | Layer 2 (eval scorecard) | Automated; 10 min human interpretation |
| Quarterly | Full structural review of flagged queue | 60-90 min |

Total human time per month: approximately 2-3 hours. This compares to 8-12 hours for a manual equivalent at 1,000+ notes.

---

## What It Is Not

**Not a reorganization system.** The Vault Immune System maintains structure; it doesn't redesign it. If your vault's fundamental organization is wrong, this system will keep it consistently wrong, not fix it. Structural redesign is a separate, deliberate project.

**Not content editing.** Automated checks can flag a note as potentially stale or thin. They can't determine whether the content is good. Content quality — the accuracy and depth of what's written — requires human judgment and is out of scope for this system.

**Not about having a "perfect" vault.** The goal is not zero orphans or zero structural issues. The goal is to know about problems early, prioritize the ones that matter, and address them incrementally. A vault under active development will always have some structural roughness. The immune system keeps that roughness from compounding into debt.

**Not a one-time setup.** The system works through cadence. Running the checks once tells you the current state. Running them monthly for a year tells you whether you're building a better knowledge system or just a bigger one.

---

## Measuring Impact

Track these metrics before and after implementing the system:

| Metric | Baseline | Target direction |
|---|---|---|
| Orphan rate | Establish at start | Declining |
| Broken link count | Establish at start | Zero or near-zero |
| Time spent on manual maintenance | Estimate current | Declining |
| Scorecard trend (3-month) | Establish at month 3 | Stable or improving across all 6 dimensions |
| Retrieval success rate | Self-reported | Improving |

The clearest signal that the system is working: you stop thinking about vault maintenance as a large periodic project, and it becomes background infrastructure you barely notice.

---

## Related

- [Structural Debt](structural-debt.md) — the problem this system prevents from accumulating
- [The Unmeasured Vault](unmeasured-vault.md) — Layer 2 directly addresses this failure mode
- [The Manual Maintenance Ceiling](manual-maintenance-ceiling.md) — Layer 1 and Layer 3 directly address this failure mode
- [The Enrichment Pattern](enrichment-pattern.md) — a complementary maintenance pattern focused on findability
