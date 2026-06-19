# Open Brain — A Knowledge Management Framework

**Open Brain** is an opinionated framework for building and maintaining personal knowledge vaults that stay useful as they scale. It addresses the core problem most PKM systems ignore: **notes don't just need to be captured — they need to be found, connected, kept alive, tested, and turned into output.**

Most knowledge management systems work well at 50 notes. At 500, search gets noisy. At 2,000+, the vault becomes a graveyard of ideas you know you wrote down but can't surface when you need them. And at every scale, without active recall and deliberate output, the knowledge never becomes skill.

Open Brain addresses this with a structured approach across eight modules — from first capture through to published thinking and system automation.

---

## The Eight Modules

### Module 1: Knowledge Enrichment

The foundation. Addresses the three failures that compound as a vault grows: notes becoming unfindable, search terms losing discriminative power, and knowledge connections carrying no semantic meaning.

**Problems:**
- [Retrieval Decay](docs/retrieval-decay.md) — Notes become progressively harder to find as your vocabulary evolves
- [Term Saturation](docs/term-saturation.md) — When a search term accumulates so many notes it loses discriminative power
- [Knowledge Graph Signal vs. Noise](docs/knowledge-graph-signal-noise.md) — Why generic "mentions" links make the graph useless

**Solution:**
- [The Enrichment Pattern](docs/enrichment-pattern.md) — Systematic search term expansion, term decompression, and connection typing

---

### Module 2: Knowledge Extraction

How raw sources — books, articles, PDFs, web content — become atomic, structured notes. The quality of extraction determines the quality of everything downstream. Includes both passive extraction (from sources you read) and active research (filling gaps you identify).

**Problems:**
- [Source Overwhelm](docs/source-overwhelm.md) — The unprocessed inbox: capture without extraction is organized procrastination
- [Atomic Note Decomposition](docs/atomic-note-decomposition.md) — Getting the granularity right when converting a book to notes
- [The Re-reading Trap](docs/re-reading-trap.md) — When your notes fail as references and you keep returning to the original
- [Reactive Knowledge Accumulation](docs/reactive-knowledge-accumulation.md) — When the vault only reflects what you happened to read, not what you need to know
- [The Seven Extraction Layers](docs/seven-extraction-layers.md) — Why single-layer extraction misses most of what a source contains

**Solutions:**
- [The Extraction Pipeline](docs/extraction-pipeline.md) — Ingest → Index → Extract as a 3-phase process
- [The Autonomous Research Loop](docs/autonomous-research-loop.md) — Filling knowledge gaps through targeted multi-round web research

---

### Module 3: Knowledge Maturation

How captured notes become your own ideas. The promotion process that separates storage from understanding.

**Problems:**
- [The Literature Note Graveyard](docs/literature-note-graveyard.md) — 500 notes from 20 books, but no original positions
- [Premature Synthesis](docs/premature-synthesis.md) — Building theses on thin evidence before sufficient convergence
- [Domain Blindness](docs/domain-blindness.md) — Not knowing what you know or what you're missing in a field
- [Convergence Detection](docs/convergence-detection.md) — Why two independent sources confirming an idea beat ten that merely mention it
- [The Endorsement Gap](docs/endorsement-gap.md) — The difference between a note that exists in your vault and one you actually trust

**Solutions:**
- [The Maturation Ladder](docs/maturation-ladder.md) — Literature Note → Analyzed → Convergence → Permanent Note → Domain Synthesis
- [Convergence Promotion](docs/convergence-promotion.md) — The state machine that moves notes from captured to endorsed using convergence signals

---

### Module 4: Active Recall & Practice

How knowledge becomes skill. The practice layer that closes the gap between understanding and doing.

**Problems:**
- [The Collector's Fallacy](docs/collectors-fallacy.md) — When saving notes feels like learning but produces no retention
- [Skill Stagnation](docs/skill-stagnation.md) — The gap between understanding a concept and actually doing it well
- [Invisible Progress](docs/invisible-progress.md) — Learning without a feedback loop: you don't know if you're improving
- [Course Gate Design](docs/course-gate-design.md) — Why linear reading produces recognition but not generation or transfer
- [Context-Absent Output](docs/context-absent-output.md) — When AI generates answers without grounding in your actual knowledge
- [The Judgment Gap](docs/judgment-gap.md) — The distance between knowing about X and having developed judgment on X
- [Empty Prompting](docs/empty-prompting.md) — Using AI as a content dispenser without building judgment: outputs accumulate, capability stays flat

**Solutions:**
- [The AI-Driven Creation Loop](docs/practice-loop.md) — Delegate Draft → Elevate Output → Challenge Log → Learning Signals → back to vault
- [The Specificity Delta](docs/specificity-delta.md) — Measuring the gap between Phase 1 and Phase 2 output as an objective score of how much your knowledge contributes

---

### Module 5: Knowledge Retrieval

How to access what you know — in multiple modes, for different purposes, from any context.

**Problems:**
- [The Search Box Bottleneck](docs/search-box-bottleneck.md) — Why text search degrades as the primary retrieval method for complex knowledge
- [Isolated Retrieval](docs/isolated-retrieval.md) — Finding individual notes without following the reasoning thread connecting them
- [Knowledge Portability](docs/knowledge-portability.md) — When your vault is stranded on your laptop and inaccessible everywhere else

**Solution:**
- [Multi-Modal Retrieval](docs/multi-modal-retrieval.md) — Intent-based search, conversational Q&A, graph traversal, and remote access

---

### Module 6: Vault Health & Maintenance

How to keep a large vault reliable. The immune system that prevents structural decay.

**Problems:**
- [Structural Debt](docs/structural-debt.md) — The compounding pathologies of orphan notes, broken links, and maturity inflation
- [The Unmeasured Vault](docs/unmeasured-vault.md) — Running blind: no metrics, no signal of health or decay
- [The Manual Maintenance Ceiling](docs/manual-maintenance-ceiling.md) — Why one-by-one review stops scaling at 500+ notes
- [The Flat Graph Problem](docs/uniform-graph-traversal.md) — Why all-equal edge weights make graph retrieval less useful as the vault grows

**Solutions:**
- [The Vault Immune System](docs/immune-system-pattern.md) — Automated detection, eval scorecard, continuous graph maintenance, periodic review
- [Graph Myelination](docs/myelination-pattern.md) — Traversal-reinforced edge weights that make the graph self-organize around how you actually think

---

### Module 7: Knowledge Output

How a full vault becomes published thinking. The output layer that closes the loop.

**Problems:**
- [The Blank Page Problem with a Full Vault](docs/blank-page-full-vault.md) — 1,000 notes and still can't write a paragraph
- [Writing Without Evidence](docs/writing-without-evidence.md) — Opinions disconnected from the knowledge you actually built
- [Single-Perspective Blindness](docs/single-perspective-blindness.md) — The structural limit of evaluating your own work

**Solution:**
- [Knowledge-Grounded Output](docs/knowledge-grounded-output.md) — Claim-first writing, vault-grounded evidence, conversational draft, multi-perspective review

---

### Module 8: System Automation

How to discover and eliminate manual repetition in your own workflow. The meta-layer that makes the system improve itself over time.

**Problems:**
- [Manual Repetition Overhead](docs/manual-repetition-overhead.md) — The cost of doing the same multi-step tasks repeatedly without recognizing the pattern
- [Automation Opportunity Blindness](docs/manual-repetition-overhead.md) — You can't see your own patterns from inside them

**Solution:**
- [The Automation Discovery Pattern](docs/automation-discovery-pattern.md) — Mining your own session history to surface what should be automated

---

### Framework Context

How Open Brain relates to the traditions it draws from — and where it diverges.

- [Where Open Brain Fits in the PKM Landscape](docs/pkm-genealogy.md) — What it takes from Forte (CODE/PARA), Zettelkasten, and Deliberate Practice — and the four things none of them have

---

## Design Principles

**Content is sacred; metadata is the lever.** Enrichment and maintenance operations never modify the core insight in a note. They improve the metadata, connections, and structure that make notes findable and usable.

**Additive only.** The framework adds search terms, connections, and structure. It never silently removes or rewrites existing content.

**Human in the loop.** The framework proposes changes; the author approves them. No automated edits without consent.

**Diagnosis before treatment.** Every maintenance operation starts with a scan. Fix what the data says is broken, not what you assume.

**Active recall over passive review.** Reading notes is not learning. Testing recall, producing answers, and applying knowledge to new cases is learning.

**Output closes the loop.** Knowledge that never becomes output — writing, decisions, conversations — hasn't been integrated. The vault exists to make you better at thinking, not to make you better at storing.

---

## Who This Is For

Open Brain is built for knowledge workers who:

- Use Obsidian, Logseq, or any linked-note tool and have outgrown basic tagging
- Have 500+ notes and notice that search is getting worse, not better
- Want their vault to function as a retrieval system, not just a storage system
- Care about the *structure* of knowledge, not just the *volume*
- Want to close the loop from reading → notes → synthesis → skill → output

---

## Repository Structure

```
docs/
├── retrieval-decay.md                  # Module 1: Why notes become unfindable
├── term-saturation.md                  # Module 1: When search terms lose power
├── knowledge-graph-signal-noise.md     # Module 1: Why generic links degrade graph value
├── enrichment-pattern.md               # Module 1: The systematic solution (solution doc)
│
├── source-overwhelm.md                 # Module 2: The unprocessed inbox problem
├── atomic-note-decomposition.md        # Module 2: Getting granularity right
├── re-reading-trap.md                  # Module 2: When notes fail as references
├── reactive-knowledge-accumulation.md  # Module 2: Vault mirrors reading history, not knowledge gaps
├── seven-extraction-layers.md          # Module 2: Why single-layer extraction misses most of a source
├── extraction-pipeline.md              # Module 2: Ingest → Index → Extract (solution doc)
├── autonomous-research-loop.md         # Module 2: Filling gaps via targeted multi-round research (solution doc)
│
├── literature-note-graveyard.md        # Module 3: Notes that never become ideas
├── premature-synthesis.md              # Module 3: Building on thin evidence
├── domain-blindness.md                 # Module 3: Not knowing what you know
├── convergence-detection.md            # Module 3: Why two confirming sources beat ten mentioning ones
├── endorsement-gap.md                  # Module 3: Notes that exist vs. notes you trust
├── maturation-ladder.md                # Module 3: From captured to owned (solution doc)
├── convergence-promotion.md            # Module 3: State machine for convergence-based promotion (solution doc)
│
├── collectors-fallacy.md               # Module 4: Saving ≠ learning
├── skill-stagnation.md                 # Module 4: Understanding ≠ doing
├── invisible-progress.md               # Module 4: Learning without feedback
├── course-gate-design.md               # Module 4: Why linear study produces recognition, not transfer
├── context-absent-output.md            # Module 4: AI output without your knowledge context
├── judgment-gap.md                     # Module 4: Knowing about X vs. having judgment on X
├── empty-prompting.md                  # Module 4: Using AI without building judgment — outputs accumulate, capability stays flat
├── practice-loop.md                    # Module 4: Delegate Draft → Elevate Output → Challenge Log → Learning Signals (solution doc)
├── specificity-delta.md                # Module 4: Measuring how much your vault elevates Phase 2 output (solution doc)
├── learning-science-of-courses.md      # Module 4+: Learning science foundations for course design
├── three-gate-progression.md           # Module 4+: Vocabulary → Production → Transfer gate model
│
├── search-box-bottleneck.md            # Module 5: Why text search degrades
├── isolated-retrieval.md               # Module 5: Notes without their context
├── knowledge-portability.md            # Module 5: Vault stranded on one device
├── multi-modal-retrieval.md            # Module 5: Four retrieval modes (solution doc)
│
├── structural-debt.md                  # Module 6: Compounding vault pathologies
├── unmeasured-vault.md                 # Module 6: No metrics, no signal
├── manual-maintenance-ceiling.md       # Module 6: Manual review doesn't scale
├── uniform-graph-traversal.md          # Module 6: Why all-equal edge weights flatten the graph
├── immune-system-pattern.md            # Module 6: Automated health, human judgment (solution doc)
├── myelination-pattern.md              # Module 6: Traversal-reinforced graph self-organization (solution doc)
│
├── blank-page-full-vault.md            # Module 7: Full vault, blank page
├── writing-without-evidence.md         # Module 7: Opinions without vault evidence
├── single-perspective-blindness.md     # Module 7: The limit of self-review
├── knowledge-grounded-output.md        # Module 7: Claim → Evidence → Draft → Review (solution doc)
│
├── manual-repetition-overhead.md       # Module 8: Cost of tasks without recognized patterns
├── automation-discovery-pattern.md     # Module 8: Mining session history for automation candidates (solution doc)
│
└── pkm-genealogy.md                    # Framework Context: How Open Brain extends Forte, Zettelkasten, and Deliberate Practice
```

---

## Further Reading

- Ahrens, S. (2017). *How to Take Smart Notes.* — The Zettelkasten foundation that Open Brain extends.
- Matuschak, A. *Evergreen Notes.* — The concept of notes that develop over time, which enrichment operationalizes.
- Bush, V. (1945). *As We May Think.* — The original vision of associative trails that typed connections implement.
- Roediger, H.L. & Karpicke, J.D. (2006). *Test-Enhanced Learning.* — The science behind active recall over passive review.
- Wozniak, P. (1990). *Optimization of Learning.* — The spaced repetition foundation for SM-2 scheduling.

---

## License

MIT — Use it, adapt it, extend it. If it helps you think better, that's the point.
