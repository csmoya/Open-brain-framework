---
module: module-1-enrichment
related_skills:
  - open-brain-enrich
  - open-brain-retrieve
last_updated: 2026-06-19
---

# Retrieval Decay in Knowledge Vaults

## The Problem

You wrote a note six months ago about a concept you understood well. Today, you need that note — but your search comes up empty. The note still exists. Your search query is reasonable. Yet the vault fails to surface it.

This is **retrieval decay**: the progressive loss of findability that affects knowledge vaults as they grow. It's not a storage problem — it's a discoverability problem.

Retrieval decay is the silent failure mode of every personal knowledge management system. It doesn't announce itself. You don't notice the notes you're not finding. You just gradually stop trusting the vault and start Googling things you already know you wrote down.

---

## Why It Happens

Retrieval decay has three root causes, and they compound each other:

### 1. Vocabulary drift

The way you think about a concept changes over time. Six months ago you wrote about "feedback loops in onboarding." Today you search for "activation flywheel." Same concept, different framing. The note was indexed with the old vocabulary; your search uses the new one.

This is especially common in fast-moving domains like product management, AI, or design — where terminology shifts quarterly.

### 2. Single-angle indexing

Most notes are indexed by what they're *about* — the topic, the concept name. But when you search, you often come from a *problem* angle ("how do I reduce churn?") or an *inverse* angle ("what kills retention?"). If the note only has the concept name as its search term, it misses these lateral approaches.

A note titled "Cohort-Based Retention Analysis" might be exactly what you need when you search for "why are users leaving after week 2" — but without problem-angle search terms, it won't surface.

### 3. Metadata stagnation

Search terms are typically set when the note is created and never updated. But the vault around the note changes: new domains emerge, new connections form, the note's role in your thinking evolves. The metadata becomes a snapshot of how you thought about the note on day one — not how you'd search for it today.

---

## How to Detect It

Retrieval decay is measurable. The diagnostic signals are:

**Search term count per note.** Notes with fewer than 4 search terms are statistically harder to find. A healthy note has 4–8 well-chosen terms covering the concept name, the problem it addresses, and at least one lateral angle.

**Retrieval frequency distribution.** If 80% of your retrievals hit the same 20% of notes, the rest of your vault is decaying. The "long tail" notes — often the most valuable because they hold non-obvious insights — are being buried.

**Query-to-zero-result ratio.** Track how often a search returns no results or irrelevant results. A rising ratio over time is the clearest signal of retrieval decay.

---

## How to Fix It

The fix is **search term enrichment** — a systematic process of adding alternative entry points to existing notes.

### Enrichment strategies

**Problem-angle terms.** For every note, ask: "What problem would someone be trying to solve when they need this note?" A note about "Jobs-to-be-Done Framework" should also be findable via "understanding what customers actually want" or "why feature requests are misleading."

**Inverse-angle terms.** What's the opposite or the thing to avoid? A note about "Progressive Disclosure in UI" should surface when searching for "information overload in onboarding" or "cognitive load in complex interfaces."

**Domain-crossing terms.** Some notes are relevant to domains beyond the one they were created in. A note about "Spaced Repetition" lives in learning theory but is equally relevant to product onboarding, habit formation, and content strategy. Adding cross-domain terms prevents siloing.

**Synonym consolidation.** If your vault uses both "churn" and "attrition" for the same concept, pick a canonical term and add aliases. Enrichment adds the alias — it doesn't rename the original.

### The process

1. **Diagnose** — Scan for notes below threshold (<4 terms), audit for broken links and orphan domains
2. **Propose** — Generate candidate terms using the strategies above
3. **Approve** — Human review before any metadata changes
4. **Apply** — Write approved changes and timestamp the enrichment

This is a maintenance operation, not a one-time fix. A healthy vault runs enrichment periodically — monthly or after a significant batch of new notes.

---

## The Compounding Effect

Retrieval decay compounds. Every unfound note is a missed connection — a link that should have been made, an insight that should have informed a decision. Over time, the vault splits into two populations: the "popular" notes that get found and linked frequently, and the "buried" notes that accumulate dust.

Enrichment reverses this. Each added search term is a new pathway into the note. Over time, enriched notes get found more often, which leads to more connections, which increases their visibility further. The compounding works in your favor — but only if you invest in the maintenance.

---

## Related

- [Term Saturation](term-saturation.md) — The inverse problem: when a search term is *too* findable
- [The Enrichment Pattern](enrichment-pattern.md) — The systematic process for solving retrieval decay
- [Knowledge Graph Signal vs. Noise](knowledge-graph-signal-noise.md) — How typed connections extend enrichment beyond search terms
