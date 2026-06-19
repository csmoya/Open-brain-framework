---
module: module-5-retrieval
related_skills:
  - open-brain-retrieve
  - open-brain-chat
  - open-brain-graph
  - open-brain-remote
last_updated: 2026-06-19
---

# Multi-Modal Retrieval: Four Ways to Access What You Know

## What It Is

Multi-modal retrieval is the practice of using different retrieval methods — each optimized for a distinct type of question and a distinct type of cognitive task — rather than routing all knowledge access through a single search interface.

The central insight is that "I need to access my vault" actually describes several qualitatively different intentions. Finding what you know about a topic is not the same operation as exploring connections across a domain, which is not the same as surfacing contradictions before a decision, which is not the same as collecting material to write with. Collapsing these into one operation — typing keywords into a search box — produces mediocre results for most of them and excellent results for almost none.

Multi-modal retrieval assigns each query intent to the method most appropriate for it. The result is not just faster retrieval — it's qualitatively different access to knowledge. Questions you couldn't answer with keyword search become answerable. Connections you'd never have found by browsing get surfaced automatically. Knowledge you built two years ago becomes as accessible as knowledge you built last week.

---

## Mode 1: Intent-Based Search

### What it is

Before running any query, classify what you're trying to do. The classification determines which entry point to use.

### The six retrieval intents

| Intent | The question you're asking | Optimal entry point |
|---|---|---|
| **Operative** | What do I know about X? | Domain index → keyword refinement |
| **Exploratory** | What is connected to X that I might not have considered? | Domain index → relationship traversal |
| **Critical** | What in my vault argues against my current position? | Graph query for contradictions |
| **Expressive** | What material can I draw on to write about X? | Thematic collection across domain |
| **Serendipitous** | What surprising connection exists between X and something unrelated? | Cross-domain graph query |
| **Contextual** | Given what I'm working on right now, what's most relevant? | Recent context + semantic matching |

### How to use it

Before querying, ask: "What am I trying to do with the result?" If you can't answer, default to Operative intent and be prepared to switch modes when the initial results suggest a different framing is needed.

Intent classification takes 10 seconds and eliminates most search failures caused by using the wrong retrieval method for the actual question.

---

## Mode 2: Conversational Q&A

### What it is

A multi-turn session that maintains context across questions and synthesizes answers as prose rather than returning individual notes. Unlike a single query that produces a list, a conversational session follows a thread — each answer can trigger a follow-up question, and the system maintains awareness of what's already been covered.

### When to use it

- When you're exploring a domain you haven't visited in a while
- When you want to think through a question by testing your knowledge against your vault
- When a single query isn't enough — you need to navigate to an answer through multiple steps
- When you want a synthesized understanding, not a collection of note fragments

### Example session structure

```
Query:     What do I know about decision-making under uncertainty?
Response:  [Synthesized answer from relevant notes]

Follow-up: What contradicts the main framework in that answer?
Response:  [Contradictions and qualifications from other notes]

Follow-up: What real cases from my own experience relate to this?
Response:  [Connected case notes]
```

### What it produces

A conversational session generates a transcript — a record of the questions asked and answers synthesized. This transcript is itself a reusable reference: a curated synthesis of what you know about a topic, produced through a structured exploration, stored for future use.

---

## Mode 3: Graph Traversal

### What it is

A structural query over the typed knowledge graph — the network of relationships between notes, where each connection carries a semantic type (contradicts, extends, exemplifies, validated_by, etc.).

Graph traversal doesn't search for notes that mention a keyword. It searches for notes that stand in a specific relationship to each other or to a given note. This enables queries that are structurally impossible with text search.

### The four core graph queries

| Query type | What it finds | When to use it |
|---|---|---|
| **Contradiction scan** | Pairs of notes that contradict each other within a domain | Before a consequential decision in that domain |
| **Fertile node query** | Notes with the highest number of incoming connections | When you want to identify your most load-bearing ideas |
| **Case-theory query** | Theoretical notes with no connected case examples | To find theories that need grounding in real experience |
| **Cross-domain bridge** | Connections between notes from different domains | When looking for transferable insights or unexpected analogies |

### The compounding effect of myelination

Graph traversal is not just retrieval — it's reinforcement. Every time a path between two notes is traversed, that connection gets stronger. Frequently-used reasoning paths become progressively more prominent in the graph structure, making them easier to surface in future queries.

This mirrors the neurological process of myelination — the insulation of frequently-fired neural pathways that makes them faster and more reliable. In a knowledge vault, myelination means that the reasoning structures you actually use compound over time: the more you traverse a connection, the more visible and accessible it becomes in subsequent retrievals.

The practical implication: a vault that has been actively used for retrieval over years is qualitatively more valuable than a vault that has only been used for authoring. The retrieval history is structural knowledge that makes future retrieval better.

---

## Mode 4: Remote Access

### What it is

Retrieval via a queryable endpoint rather than the local application — enabling vault access from mobile devices, different computers, AI assistant conversations, and any other context where the primary authoring application isn't available.

### When to use it

- Mobile: You're away from your desk and need to retrieve or reference vault knowledge
- AI integration: You want an AI assistant to have access to your specific knowledge during a conversation
- Cross-tool: You're working in a different application and need vault access without switching contexts
- Collaboration: You want to share or discuss specific vault content with someone else

### The architecture

Remote access requires the vault to expose a lightweight API — four to six operations that cover the retrieval use cases without requiring the full application:

| Operation | What it does |
|---|---|
| `search` | Natural language query → relevant notes with context |
| `read` | Note identifier → full note content |
| `ask` | Question → synthesized prose answer |
| `graph` | Structural query → connection data |
| `related` | Note identifier → connected notes by relationship type |

Once this API exists, the vault travels with you. An AI assistant can call `search` to find relevant notes during a conversation. A mobile browser can call `ask` to answer a question. A team tool can call `read` to display a specific note.

---

## When to Use Which Mode

| Situation | Recommended mode |
|---|---|
| Quick factual lookup | Intent-based search (Operative) |
| Pre-decision research | Graph traversal (contradiction scan) + Conversational Q&A |
| Writing preparation | Intent-based search (Expressive) + Conversational Q&A |
| Domain review after time away | Conversational Q&A |
| Finding structural patterns in knowledge | Graph traversal (fertile nodes, cross-domain bridges) |
| Access from mobile or AI context | Remote access |
| Deep exploration of a new connection | Conversational Q&A starting from a graph finding |

There is no hierarchy among the modes — they are complementary, not competing. A single retrieval session often uses multiple modes in sequence: a conversational session might begin with an intent-based query, follow a contradiction found via graph traversal, and access a specific note via remote API.

---

## What It Is Not

**Not full-text search.** Multi-modal retrieval builds on top of search but is not reducible to it. Keyword search is the input to Operative retrieval. The other modes don't use keyword search at all — they use graph structure, session context, and API queries.

**Not folder browsing.** Organizing notes into folders is an authoring concern. Retrieval should not depend on having organized correctly at the time of capture. Multi-modal retrieval is index-based and graph-based, not folder-based.

**Not just keyword matching.** The most important queries a knowledge worker needs to answer — "what contradicts my current view?", "what's connected across domains?", "what do I know that's relevant to this decision?" — are not answerable by matching words. They require semantic understanding of note relationships.

**Not a one-time configuration.** The graph traversal and myelination modes become more powerful the more the vault is used for retrieval. The value compounds over time with use — which means delaying adoption has a genuine cost.

---

## Measuring Impact

| Metric | Baseline (search-only) | With multi-modal retrieval |
|---|---|---|
| Query success rate | ~30–50% (varies with vault age) | Track improvement over 60 days |
| Time to useful answer | Multiple attempts + phrasing variants | Single intent-classified query |
| Contradictions surfaced before decisions | Near zero | Systematic (graph query) |
| Cross-domain connections discovered | Accidental | Queryable |
| Vault access frequency | Limited to desk + app | Any device, any context |

Track query success rate explicitly: after each vault session, record whether you found what you were looking for. If success rate is below 70%, the retrieval system has significant room for improvement.

---

## Related

- [The Search Box Bottleneck: Why Text Search Fails Knowledge Vaults](search-box-bottleneck.md)
- [Isolated Retrieval: Finding Notes Without Following the Thread](isolated-retrieval.md)
- [Knowledge Portability: When Your Vault Is Stranded on Your Laptop](knowledge-portability.md)
- [The Practice Loop: From Passive Notes to Active Skills](practice-loop.md)
