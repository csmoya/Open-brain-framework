---
module: module-1-enrichment
related_skills:
  - open-brain-enrich
last_updated: 2026-06-19
---

# Term Saturation in Knowledge Vaults

## The Problem

You search for "product strategy" in your vault. 37 results come back. Technically, all of them are relevant. Practically, none of them are useful — because the term has lost its ability to discriminate between notes.

This is **term saturation**: the point where a search term or tag accumulates so many linked notes that it stops being a useful retrieval signal. The term becomes a category, not a search key.

Term saturation is the opposite of [retrieval decay](retrieval-decay.md). Decay means a note has too few entry points and can't be found. Saturation means an entry point has too many notes and can't filter. Both produce the same result: the vault fails to surface the note you need.

---

## Why It Happens

### Natural gravity

Some concepts are hubs in your thinking. "Mental models," "feedback loops," "cognitive load" — these terms are genuinely relevant to dozens of notes because they're foundational concepts. The saturation isn't an error in tagging; it's a reflection of how interconnected these ideas are.

The problem isn't that you tagged too many notes with "mental models." The problem is that the term needs to be decomposed now that your vault has enough notes to warrant sub-categories.

### Lazy indexing

When you're capturing a note quickly, it's tempting to tag it with the broadest applicable term. "AI" instead of "retrieval-augmented generation." "Design" instead of "progressive disclosure in multi-step forms." Each lazy tag adds noise to the broad term and deprives the narrow term of a note.

### Missing vocabulary

Sometimes a concept doesn't have a name yet in your vault. You have 12 notes that are all about the same sub-pattern of "product-led growth," but you haven't coined a search term for that specific angle. So they all live under the parent term, crowding it.

---

## How to Detect It

### Crowding analysis

A crowding report counts how many notes point to each search term and flags terms above a threshold. In practice:

| Notes per term | Status |
|---|---|
| 1–5 | Healthy |
| 6–10 | Watch — may need splitting |
| 11–20 | Saturated — splitting recommended |
| 20+ | Critical — the term is functionally useless as a search key |

### The "would you scroll?" test

Search for the term. If the results list is long enough that you'd need to scroll and scan to find the specific note you want, the term is saturated. A useful search term should return a short enough list that you can identify the right note in under 3 seconds.

### Domain concentration

A saturated term that spans multiple domains is harder to split than one concentrated in a single domain. Checking domain distribution helps you decide the right splitting axis.

---

## How to Fix It

The fix is **term decompression** — splitting a saturated term into sub-terms that preserve specificity while keeping the parent term intact.

### Splitting strategies

**By sub-theme.** `[[Agent Memory]]` → `[[Agent Episodic Memory]]`, `[[Agent Semantic Memory]]`, `[[Agent Working Memory]]`. Each sub-term captures a distinct aspect of the parent concept.

**By domain.** `[[Feedback Loops]]` → `[[Feedback Loops in Product]]`, `[[Feedback Loops in Learning]]`, `[[Feedback Loops in Systems Thinking]]`. The mechanism is the same, but the application context differs.

**By specificity level.** `[[Onboarding]]` → `[[Onboarding First-Run Experience]]`, `[[Onboarding Activation Metrics]]`, `[[Onboarding Content Sequencing]]`. This splits by how granular the note's focus is.

**By problem vs. solution.** `[[Retention]]` → `[[Why Users Churn]]` (problem angle) + `[[Retention Mechanisms]]` (solution angle). This is especially useful for terms that mix diagnostic and prescriptive notes.

### Rules for splitting

**Keep the parent.** The original term stays as a category-level concept. Notes that are genuinely about the broad concept (e.g., a synthesis note on "Mental Models" as a discipline) keep it. Notes about specific sub-patterns get the more precise sub-term.

**Don't over-split.** If a sub-term would only have 1–2 notes, it's not worth creating. The goal is to reduce noise, not to create a taxonomy so granular that every note has a unique tag.

**Name sub-terms for findability.** The sub-term should be something you'd plausibly search for. `[[Agent Episodic Memory]]` works because someone would search that. `[[Agent Memory Type 2]]` does not.

**Add, don't replace.** Splitting adds a sub-term to qualified notes. It doesn't remove the parent term — the parent remains as a broader entry point for notes that genuinely warrant it.

---

## Saturation vs. Legitimate Hubs

Not every high-count term needs splitting. Some terms are legitimate hubs — concepts so foundational that many notes should link to them. The distinction:

**Saturated term:** The notes under it are heterogeneous. They cover different sub-aspects, different domains, different levels of specificity. Searching the term doesn't narrow your focus.

**Legitimate hub:** The notes under it are homogeneous in their relationship to the concept. They all contribute to the same conversation. Searching the term gives you a coherent reading list, not a grab bag.

A domain index note (e.g., "Product Strategy — Domain Map") is a hub, not a saturated term. Thirty notes under `[[Cognitive Bias]]` where half are about UX, a quarter about negotiation, and a quarter about decision-making — that's saturation.

---

## The Maintenance Cycle

Term saturation is a natural consequence of vault growth. A term that was perfectly discriminative at 200 notes may be saturated at 800. This means decompression is a recurring operation, not a one-time cleanup.

A practical cadence: run a crowding analysis monthly, or after adding 50+ notes. Flag terms above threshold, propose splits, approve, apply.

---

## Related

- [Retrieval Decay](retrieval-decay.md) — The inverse problem: notes with too few entry points
- [The Enrichment Pattern](enrichment-pattern.md) — The systematic process that includes term decompression
- [Knowledge Graph Signal vs. Noise](knowledge-graph-signal-noise.md) — How typed connections complement search term management
