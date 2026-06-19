---
module: module-6-health
related_skills:
  - open-brain-eval
  - open-brain-health
last_updated: 2026-06-19
---

# The Unmeasured Vault: Running Blind on Your Own Knowledge

## The Problem

Most knowledge vaults have no metrics. You don't know how many notes you have, how many have been synthesized into durable principles, what percentage are well-connected, how often notes are actually retrieved during real work, or whether the vault has improved or degraded over the past three months.

Without measurement, you can't distinguish a healthy vault from a sick one. You have an intuition — "feels pretty good," or "getting a bit cluttered" — but intuition about complex systems is unreliable. It's biased toward recent activity (you just added a great set of notes, so the vault feels alive) and toward visible content (the notes you wrote about things you find interesting, not the ones that have silently become orphans).

The result is that most PKM practitioners spend months or years building a knowledge system without knowing whether it's working. They can't answer basic questions: Is the vault more connected than it was six months ago? Has the inbox backlog grown or shrunk? Are notes being retrieved in practice, or just captured and forgotten? These questions have answers — but only if someone is tracking them.

Without measurement, you also can't improve deliberately. Improvement requires a baseline. If you don't know where you started, you can't know whether you've moved.

---

## Why It Happens

### Obsidian and similar tools are file systems, not knowledge databases

The standard PKM tools — Obsidian, Logseq, Notion — are designed around file management and editing. They're excellent at storing and displaying content. They are not designed to compute aggregate metrics across a collection of files.

There's no built-in dashboard that tells you your orphan rate, your average inbound link count, your synthesis funnel conversion, or your inbox backlog size. Getting those numbers requires either manual counting (impractical at scale) or scripts that process the files and compute the metrics. Since the tools don't offer this natively, most users never set it up — and the vault remains unmeasured.

### No baseline was established

Measurement requires a starting point. If you never recorded what your vault looked like at 100 notes — orphan rate, graph density, backlog size, note count by maturity level — then you have nothing to compare against at 500 notes. You can compute current state, but you can't track change over time.

Most practitioners don't establish a baseline because measurement doesn't feel like the point. The vault is for thinking and learning, not for tracking. This is a reasonable intuition that leads to a significant blind spot: you can't tell whether the habits you're building are making the vault better or just keeping it busy.

### Measurement feels like overhead

There's a common perception that measuring a knowledge vault is bureaucratic overhead — the kind of thing corporations do to feel like they're managing things, not what a practitioner does to actually use their knowledge. This perception conflates two different things: measuring for compliance (pointless overhead) and measuring to detect problems early (the only way to maintain a complex system).

A vault with 2,000 notes is a complex system. Complex systems degrade in ways that aren't visible without instrumentation. The measurement overhead is not the cost of bureaucracy — it's the cost of actually knowing whether your system works.

---

## How to Detect It

Without looking anything up, answer these questions about your vault right now:

| Metric | Can you answer? |
|---|---|
| Total note count | Yes / No / Approximately |
| Broken link count | Yes / No |
| Orphan rate (% of notes with no inbound links) | Yes / No |
| Average inbound links per note | Yes / No |
| Inbox backlog (unprocessed sources) | Yes / No |
| Notes added in the last 30 days | Yes / No |
| Notes that have been retrieved at least once in real work | Yes / No |

If you can't answer most of these, the vault is unmeasured. The inability to answer isn't a problem with your memory — it's evidence that the metrics aren't being tracked.

---

## How to Fix It

**Step 1: Establish a baseline**

Run a one-time analysis that records:

- Total note count
- Notes by maturity level
- Orphan rate
- Broken link count
- Inbox backlog size
- Average inbound links per note (proxy for graph connectedness)

Record this as a snapshot with a date. This is your starting point. Without it, future measurements are absolute values with no context.

**Step 2: Run regular evaluations**

Compute the same metrics on a schedule — monthly is reasonable for most vaults; weekly if the vault is actively growing. Compare against the baseline and the previous period.

What you're looking for: trends, not perfection. An orphan rate that's declining month over month is a healthy vault even if the absolute number is still high. An orphan rate that's climbing month over month is a structural problem even if the number seems small.

**Step 3: Use a scorecard with 6 dimensions**

A single metric will mislead you. A vault can have high note count (looks healthy) but low graph connectedness (structurally weak). Use a multi-dimensional scorecard:

| Dimension | What it measures | Key metric |
|---|---|---|
| Integrity | Structural soundness | Orphan rate, broken links, maturity accuracy |
| Graph quality | Connectedness and link semantics | Average inbound links, typed link ratio |
| Pipeline health | Capture-to-synthesis flow | Inbox backlog, synthesis conversion rate |
| Practice activity | Whether knowledge is being used | Sessions in last 30 days, retrieval events |
| Funnel conversion | Notes advancing through maturity stages | % advancing per period |
| Output production | Knowledge becoming external artifacts | Posts, docs, decisions in last 30 days |

Each dimension gets a status (healthy, watch, critical) based on its metrics. The scorecard gives you a systemic view in one pass.

---

## Related

- [Structural Debt](structural-debt.md) — what the metrics will reveal when you first measure a vault that's never been audited
- [The Manual Maintenance Ceiling](manual-maintenance-ceiling.md) — why manual measurement doesn't scale and automation is required
- [The Vault Immune System](immune-system-pattern.md) — the complete maintenance system that includes measurement as a core layer
