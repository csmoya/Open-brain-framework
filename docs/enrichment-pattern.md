---
module: module-1-enrichment
related_skills:
  - open-brain-enrich
last_updated: 2026-06-19
---

# The Enrichment Pattern

## What It Is

The Enrichment Pattern is a systematic maintenance process for knowledge vaults. It treats findability and connectedness as ongoing operations — not something you set up once and forget.

The pattern addresses three failures that compound as a vault grows:

1. **[Retrieval decay](retrieval-decay.md)** — Notes become unfindable because their search metadata hasn't kept pace with how your thinking evolves
2. **[Term saturation](term-saturation.md)** — Search terms lose discriminative power as too many notes accumulate under the same tag
3. **[Knowledge graph noise](knowledge-graph-signal-noise.md)** — Connections between notes are all generic "mentions," making the graph structurally rich but semantically empty

The Enrichment Pattern solves all three with a single, repeatable process that operates on three layers.

---

## The Three Layers

### Layer 1: Search Term Expansion

**Goal:** Every note should be findable from at least 4 distinct angles.

Most notes are created with a title and maybe a tag or two. This captures what the note *is about*, but not how you'd *search for it* later. Search term expansion closes this gap by adding entry points that match future search intent.

**The four angles:**

| Angle | Question it answers | Example for a note on "Spaced Repetition" |
|---|---|---|
| Concept name | What is this about? | `spaced repetition`, `SRS` |
| Problem angle | What problem does this solve? | `forgetting what I learned`, `knowledge retention` |
| Inverse angle | What's the failure mode it prevents? | `cramming doesn't work`, `memory decay` |
| Domain crossing | Where else does this apply? | `product onboarding intervals`, `habit formation timing` |

**Quality test:** For each proposed search term, ask: *"If I searched for this term and found this note, would I think 'this is exactly what I needed'?"* If the answer is no, the term is too broad or too tangential.

**What to avoid:**
- Adding a synonym for every possible phrasing (use aliases for true synonyms instead)
- Adding terms that are technically accurate but nobody would search for
- Adding domain-crossing terms that are speculative rather than demonstrated in the note's content

### Layer 2: Term Decompression

**Goal:** No search term should return more than 10 notes.

When a term accumulates too many notes, it needs to be decomposed into sub-terms. This is not re-tagging — the parent term stays. Sub-terms are added to notes that warrant the more specific framing.

**Splitting axes:**

```
Parent term: [[Feedback Loops]]

By sub-theme:    [[Positive Feedback Loops]], [[Negative Feedback Loops]], [[Delayed Feedback]]
By domain:       [[Feedback Loops in Product]], [[Feedback Loops in Learning]], [[Feedback Loops in Teams]]
By specificity:  [[Feedback Loop Design]], [[Feedback Loop Measurement]], [[Feedback Loop Failure Modes]]
By problem/sol:  [[When Feedback Loops Break]], [[Building Effective Feedback Loops]]
```

**Decision criteria for which axis to use:**

- If the notes under the term cover different sub-topics → split by sub-theme
- If the notes apply the same concept to different fields → split by domain
- If the notes range from abstract to concrete → split by specificity
- If the notes mix diagnosis and prescription → split by problem/solution

**Rule:** Only create a sub-term if it would have at least 3 notes. Below that threshold, the split adds taxonomy overhead without retrieval benefit.

### Layer 3: Connection Typing

**Goal:** At least 40% of graph edges should carry a semantic type stronger than "mentions."

This layer classifies the relationships between notes using a controlled vocabulary: `refutes`, `contradicts`, `refines`, `extends`, `depends_on`, `exemplifies`, `validated_by`, `applies_to`, `feeds`, `operationalizes`, `synthesizes_from`, `cross_domain`.

Connection typing is the most labor-intensive layer and delivers the most long-term value. It turns the knowledge graph from a visual novelty into a queryable reasoning structure.

**The sentence-first pattern:**

```markdown
## Typed Connections
- Extends [[Cognitive Load Theory]] to sequential decision-making under time pressure.
- Contradicts [[Information Abundance Hypothesis]] in expert-domain contexts.
- Validated by [[Sweller 1988 Experiment]] across three task complexity levels.
```

The relationship verb comes *before* the wikilink. This makes the connection human-readable and machine-parseable simultaneously.

**Priority for typing:**

1. Permanent Notes (synthesized insights) — highest value per connection typed
2. Notes with 5+ outgoing links — most noise to clean up
3. Cross-domain connections — hardest to discover, most valuable when typed

---

## The Process

Enrichment follows a four-phase cycle:

### Phase 1: Diagnose

Run a diagnostic scan across the vault. The scan produces:

- **Distribution of search terms per note** — Identify notes below threshold (< 4 terms)
- **Crowding report** — Terms with too many notes, ranked by severity
- **Domain registry** — Active domains and orphan domains (domains referenced in notes but not in the registry)
- **Connection coverage** — % of edges with types, untyped edges between high-value notes

The diagnosis tells you where to focus. Don't enrich everything at once — start with the most impactful gaps.

### Phase 2: Propose

Generate candidate changes for each identified gap:

- New search terms for under-indexed notes (Layer 1)
- Sub-term splits for saturated terms (Layer 2)
- Relationship types for untyped connections between Permanent Notes (Layer 3)

Every proposal includes a rationale: why this term, why this split, why this relationship type.

### Phase 3: Approve

Human review of all proposals before any changes are written. This is non-negotiable. Automated enrichment without review leads to metadata drift — terms that are technically plausible but don't match how the author actually thinks.

What to check during review:

- Does the search term match how I'd actually search? (Not how someone else might search)
- Does the split create sub-terms I'd recognize? (Not academic categories I'd never use)
- Does the relationship type feel right? (Not the most technically precise, but the most *useful*)

### Phase 4: Apply

Write approved changes to note metadata:

- Add search terms to frontmatter
- Add domain assignments
- Add typed connections section
- Timestamp the enrichment (`enriched: 2024-11-15`)
- Generate a report of all changes for audit trail

---

## Cadence

Enrichment is maintenance, not a one-time operation. Recommended cadence:

| Vault size | Cadence | Focus |
|---|---|---|
| < 200 notes | Quarterly | Layer 1 only (search terms) |
| 200–500 notes | Monthly | Layers 1–2 (terms + decompression) |
| 500–1,000 notes | Biweekly | All three layers |
| 1,000+ notes | Weekly | Rotating focus by domain |

The cadence should increase after large ingestion events (processing a new book, batch-importing notes from a course, migrating from another tool).

---

## What Enrichment Is Not

**It's not reorganization.** Enrichment doesn't move notes, change titles, merge duplicates, or restructure folders. Those are separate operations with different risk profiles.

**It's not content editing.** The core insight, evidence, and argument in a note are never touched. Enrichment operates exclusively on metadata and connection layers.

**It's not automated tagging.** AI can propose terms, but the quality test requires human judgment about how the author actually searches. Fully automated enrichment tends toward plausible but unused terms.

**It's not a substitute for good capture.** If notes are captured with poor structure or unclear insights, enrichment can make them more findable — but it can't make them more useful. Quality at capture is a prerequisite.

---

## Measuring Impact

**Retrieval success rate:** After enrichment, search queries that previously returned zero or irrelevant results should improve. Track before/after for a sample of "hard" queries.

**Search term distribution:** The distribution should shift from bimodal (many notes with 1–2 terms, few with 6+) to roughly normal (most notes with 4–6 terms).

**Crowding reduction:** Saturated terms should drop below threshold after splitting. Track the number of terms above 10 notes.

**Graph signal ratio:** The percentage of typed connections should increase over time. A vault that starts at 5% typed and reaches 40% after six months has materially improved its reasoning infrastructure.

---

## Related

- [Retrieval Decay](retrieval-decay.md) — The core problem that Layer 1 solves
- [Term Saturation](term-saturation.md) — The core problem that Layer 2 solves
- [Knowledge Graph Signal vs. Noise](knowledge-graph-signal-noise.md) — The core problem that Layer 3 solves
