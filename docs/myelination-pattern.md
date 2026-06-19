---
module: module-6-health
related_skills:
  - open-brain-autolink
last_updated: 2026-06-19
---

# Graph Myelination

A knowledge graph that never updates its edge weights doesn't get more useful with use — it just gets bigger. The myelination pattern fixes this by treating traversal events as data: connections you follow repeatedly get stronger; connections you never follow gradually weaken. The graph structure that emerges over months reflects how you actually think, not how you expected to think when you first linked two notes.

---

## What It Is

Graph myelination is an edge-weighting mechanism for knowledge vaults. Every connection between notes starts with a neutral weight. As you use the vault — running retrievals, following reasoning threads, working through a problem — traversal events are logged. A periodic myelination cycle processes those logs: traversed edges are reinforced, and all edges receive a small decay. Over time, the graph develops topology.

The name comes from neuroscience. Myelin is the substance that wraps around frequently-used neural axons, making signal transmission faster and more reliable. Neural pathways that are used more become faster; unused pathways atrophy. The brain doesn't maintain all connections equally — it invests in the paths that matter.

Graph myelination applies the same principle to a knowledge vault.

---

## The Biological Analogy

In the nervous system, myelination isn't a deliberate decision — it's an emergent property of use. The axons you fire repeatedly get wrapped in myelin. The axons you don't use gradually lose it. The structure of your neural connectivity is, in part, a record of what you've thought about.

The analogy to a knowledge graph is direct. When you follow a connection during retrieval — moving from a note about "feedback mechanisms" to a connected note about "activation thresholds" because that path is part of how you reason about this domain — that traversal is equivalent to firing a neural pathway. The myelination cycle reinforces it. The connection that proves productive over hundreds of sessions becomes a strong edge in the graph.

The connections you added speculatively — "these two might relate" — but never followed are the unmyelinated axons. The system doesn't delete them. But it stops prioritizing them. They recede.

---

## How the Myelination Cycle Works

The cycle runs on a schedule (weekly by default) and processes accumulated traversal logs.

**Step 1: Traversal logging.** Every time a graph edge is followed during a retrieval operation — when the system walks from a note to a connected note as part of finding related knowledge — the traversal is logged. The log entry contains the edge identifier, the direction of traversal, and a timestamp.

**Step 2: Reinforcement.** During the myelination cycle, the system processes all traversals since the last cycle. For each edge that was traversed, its weight is multiplied by the reinforce factor. An edge traversed five times in a week receives five separate reinforcement multiplications.

**Step 3: Decay.** After reinforcement, every edge in the graph — including newly reinforced ones — is multiplied by the decay factor. This is applied universally: no edge is exempt. The effect is that even heavily myelinated edges lose a small amount of weight each cycle if they aren't traversed. The graph doesn't permanently memorize old usage patterns; it reflects current ones.

**Step 4: Threshold classification.** After weights are updated, edges are classified:

- Edges above the strong threshold are marked as myelinated. They're prioritized in graph walks.
- Edges below the weak threshold are flagged as decay candidates. They're still present in the graph but are deprioritized in retrieval and eligible for pruning review.

---

## Reinforcement and Decay

| Parameter | Default | Effect |
|---|---|---|
| Reinforce factor | 1.05 per traversal | Each traversal adds 5% weight |
| Decay factor | 0.98 per cycle | All edges lose 2% per cycle |
| Strong threshold | 1.5 | "Myelinated" — prioritized in graph walks |
| Weak threshold | 0.3 | Decay candidate — pruning eligible |

These defaults are calibrated for a weekly cycle on an active vault. The math: an edge that isn't traversed at all will lose roughly 65% of its weight over a year (0.98^52 ≈ 0.35). An edge traversed once per week will reach an equilibrium around weight 2.6 (the point at which weekly +5% and weekly -2% balance). An edge traversed five times per week will push significantly higher.

The parameters can be adjusted. A vault with heavier daily use might lower the reinforce factor to avoid runaway weight concentration on a small number of edges. A longer cycle (monthly) would require recalibrating decay to prevent too-rapid attenuation.

---

## What You Can Observe (The Report)

The myelination report surfaces three things after each cycle runs.

**Myelinated edges by connection type.** Which relationship types appear most frequently among your strongest edges? Open Brain uses typed connections — "extends," "contradicts," "applies to," "cross-domain." The types that appear most in myelinated edges reveal how you reason. If "contradicts" dominates, your thinking is comparative and critical. If "applies to" dominates, you're application-focused — you follow ideas into their practical consequences. If "cross-domain" leads, your most productive paths cross subject-matter boundaries.

**Top myelinated pairs.** The specific note pairs with the strongest connections. These are your intellectual highways — the specific concept adjacencies your thinking returns to most often. They often surface non-obvious structure: two notes you'd never consciously have identified as central to your thinking, but which the traversal history reveals as a core link in how you navigate a domain.

**Decay candidates.** Edges that have fallen below the weak threshold. These are connections that were added — sometimes speculatively — and never followed. They warrant a brief audit: was the connection real? If you review a decay candidate and it still seems meaningful, you can manually reinforce it. If it looks like a historical artifact, pruning it cleans the graph.

---

## The Effect on Retrieval

When graph traversal is used as a retrieval mode — walking outward from a note to find related knowledge — the walk follows myelinated edges preferentially. This changes what gets surfaced.

In a flat graph, the walk is essentially random with respect to quality: connected notes are returned in whatever order the graph enumerates them. In a myelinated graph, the walk follows your intellectual history. Notes that have proven connected to the retrieved concept in your actual usage come first. Notes you've never navigated to from this starting point come later, if at all.

The practical effect: when you retrieve knowledge on a topic you work in daily, you get the notes your thinking most depends on. When you retrieve knowledge on a topic you haven't touched in a year, the walk returns more tentative results — the myelination hasn't been reinforced, so the structure is less settled. This is accurate. Your knowledge in a dormant domain has genuinely atrophied relative to an active one.

---

## Cadence

The default myelination cycle runs weekly. This is a balance between responsiveness (daily would work but adds overhead) and stability (monthly would allow too much drift before the graph updates).

The traversal log accumulates continuously between cycles. Nothing is lost if the cycle runs late. When it does run, it processes all accumulated traversals and updates weights in a single pass.

Myelinated edges don't need to be re-myelinated from scratch after a vault migration or schema change. The weights are stored as edge metadata and persist across cycles.

---

## Related

- [The Flat Graph Problem](uniform-graph-traversal.md) — Why all-equal edge weights make graph retrieval progressively less useful at scale
- [Knowledge Graph Signal vs. Noise](knowledge-graph-signal-noise.md) — The prerequisite: typed connections give myelination something meaningful to reinforce
- [The Enrichment Pattern](enrichment-pattern.md) — How connections are typed and created, which is the input that myelination operates on
- [The Vault Immune System](immune-system-pattern.md) — The broader maintenance system that myelination plugs into, alongside structural debt detection and health scoring
- [Multi-Modal Retrieval](multi-modal-retrieval.md) — How myelinated graph traversal fits into the four retrieval modes and when to use it
