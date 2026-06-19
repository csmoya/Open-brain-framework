---
module: module-1-enrichment
related_skills:
  - open-brain-enrich
  - open-brain-autolink
last_updated: 2026-06-19
---

# Knowledge Graph Signal vs. Noise

## The Problem

Your vault has a knowledge graph. Every wikilink creates an edge. After a few hundred notes, the graph looks impressive — a dense web of interconnected ideas. You open the graph view and see... everything connected to everything.

The graph is telling you nothing.

This is the **signal-to-noise problem** in knowledge graphs: when every connection is a generic "mentions" relationship, the graph has volume but no meaning. It can tell you that Note A links to Note B, but not *why*. Does A contradict B? Extend it? Depend on it? Provide evidence for it? The graph can't say, because all edges are the same.

A knowledge graph without typed relationships is a road map where every road is the same color and width. It shows you that cities are connected, but not whether the connection is a highway, a dirt trail, or a one-way street.

---

## Why It Happens

### The wikilink contract

Most linked-note tools (Obsidian, Logseq, Roam) treat every `[[wikilink]]` as an equal, untyped connection. The tool sees `[[Feedback Loops]]` in a note and creates an edge. It doesn't know — or care — whether the note *uses* feedback loops, *critiques* feedback loops, or *contradicts* the standard model of feedback loops.

This is by design. Wikilinks are frictionless. Typed links would require you to classify every connection at write time, which would slow capture to a crawl. The speed-accuracy tradeoff favors speed.

### Context after the link

In practice, many authors write context *after* the wikilink: `[[Feedback Loops]] — this model breaks down in contexts with delayed signals`. The human reader understands the relationship from the sentence. But the graph engine only sees the link and ignores the context. The meaning is there in the text; it's just invisible to the graph.

### Exponential noise growth

In a vault of *n* notes with an average of *k* links each, the graph has approximately *n × k* edges. At 1,000 notes with 5 links each, that's 5,000 edges — all untyped. The noise doesn't grow linearly with vault size; it grows with the number of connections, which grows faster than the number of notes.

---

## What You Lose

An untyped graph can answer: "What notes are connected to X?"

A typed graph can answer:

- **"What contradicts X?"** — Find notes that challenge an assumption, enabling intellectual honesty
- **"What extends X?"** — Find notes that build on a concept, enabling synthesis
- **"What depends on X?"** — Find notes that would need revision if X turns out to be wrong
- **"What provides evidence for X?"** — Find notes with empirical backing for a claim
- **"What applies X to a different domain?"** — Find cross-domain transfers, the most valuable kind of connection

These are the queries that turn a vault from a storage system into a thinking tool. Without them, the graph is decoration.

---

## The Solution: Typed Connections

Typed connections classify the relationship between two notes using a controlled vocabulary of relationship types. Instead of a generic edge, each connection carries a verb that describes how the source relates to the target.

### A practical type system

The following types cover the most common and useful relationships in a knowledge vault, ordered from strongest to weakest semantic signal:

| Type | Meaning | Example |
|---|---|---|
| `refutes` | Provides counter-evidence or counter-argument | "This study refutes the 10,000-hour rule" |
| `contradicts` | States the opposite position | "Fixed mindset contradicts growth-oriented feedback" |
| `refines` | Narrows or adds precision to | "Adds a boundary condition to the general principle" |
| `extends` | Builds on, adds a new dimension | "Extends the model to multi-agent settings" |
| `depends_on` | Cannot hold without the target being true | "This strategy assumes the user has a mental model of X" |
| `exemplifies` | Provides a concrete instance of | "This case study exemplifies the theory" |
| `validated_by` | Has empirical support from | "The principle is validated by this experiment" |
| `applies_to` | Operationalizes in a specific context | "Applies spaced repetition to product onboarding" |
| `feeds` | Provides input that strengthens | "This observation feeds the emerging pattern" |
| `operationalizes` | Turns an abstract concept into a concrete process | "Operationalizes the framework into a checklist" |
| `synthesizes_from` | Combines multiple sources into a new insight | "Synthesizes from three domain-specific observations" |
| `cross_domain` | Transfers a concept to a different field | "Transfers the biological concept to organizational design" |

### What to skip

Not every connection deserves a type. The filter: **if the relationship isn't more specific than "mentions," skip it.** Generic connections like "is related to" or "touches on" add noise, not signal. It's better to have 6 well-typed connections than 20 vague ones.

---

## Implementation

### The sentence-first pattern

The most practical way to type connections is to write a sentence where the relationship verb comes *before* the link:

```
Refines [[Progressive Disclosure]] by adding a time-decay condition to the disclosure trigger.
```

This pattern has two advantages: it's human-readable (the sentence makes sense as prose), and it's machine-parseable (a script can extract the verb + target to build the typed graph).

Compare with the typical wikilink style:

```
[[Progressive Disclosure]] — adding a time-decay condition
```

Same information, but the relationship is implicit. The verb comes after the link (or is missing entirely), so the graph engine can't extract it.

### Typed connections as a separate section

Rather than rewriting all existing wikilinks, a practical approach is to add a dedicated section at the end of mature notes:

```markdown
## Typed Connections

- Refines [[Progressive Disclosure]] by adding a time-decay condition.
- Contradicts [[Information Overload Hypothesis]] in contexts with expert users.
- Extends [[Cognitive Load Theory]] to sequential multi-step interfaces.
```

This keeps the original note body untouched (preserving the natural writing flow) while adding a structured layer that the graph engine can process with higher confidence.

### Priority: which notes to type first

Not all notes benefit equally from typed connections. Prioritize:

1. **Permanent Notes** (mature, synthesized insights) — These are the nodes where relationship quality matters most
2. **Notes with 5+ outgoing links** — They have enough connections that typing would add meaningful discrimination
3. **Cross-domain notes** — The most valuable connections are often cross-domain, and they're also the hardest to discover without typing

---

## Measuring Improvement

### Signal-to-noise ratio

Before typed connections: % of edges that are "mentions" (typically 90%+). After: % of edges with a specific type. A well-typed vault should have 40–60% of its connections carrying a type stronger than "mentions."

### Query precision

Test with specific questions: "What contradicts my assumption about X?" In an untyped graph, you'd need to manually scan all connected notes. In a typed graph, you filter by `contradicts` and get a precise answer. Measure the ratio of useful results to total results.

### Graph navigability

Can you trace a meaningful path through the graph? In an untyped graph, every path is equally meaningless. In a typed graph, you can follow chains: "A depends on B, which is validated by C, which contradicts D." These chains are the thinking paths that make a vault genuinely useful for intellectual work.

---

## Related

- [Retrieval Decay](retrieval-decay.md) — Typed connections are a second layer of enrichment beyond search terms
- [Term Saturation](term-saturation.md) — Typed connections help disambiguate notes that share the same search term
- [The Enrichment Pattern](enrichment-pattern.md) — Connection typing as the third layer of the enrichment process
