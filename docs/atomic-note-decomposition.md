---
module: module-2-extraction
related_skills:
  - open-brain-extract
last_updated: 2026-06-19
---

# Atomic Note Decomposition: Getting the Granularity Right

## The Problem

You've finished a book and you're extracting notes. You create a note called "Chapter 4: Feedback Loops." It's 600 words. It covers the concept, an example, a counterexample, and a practical application. You feel like you've captured something.

Six months later, you search for "feedback loops" and find this note. You read it again. It still makes sense. But when you try to connect it to something else in your vault — a concept from a different book about the same mechanism — you can't. The notes don't link cleanly. They're the right size for reading, but the wrong size for thinking.

This is the **granularity problem**: extracting notes at the wrong unit of analysis. Too broad, and notes become chapter summaries that can't be connected, cited, or reused as discrete building blocks. Too granular, and you're transcribing rather than thinking, and the vault fills with decontextualized fragments. Getting granularity right is the hardest skill in knowledge extraction — and the one with the highest downstream impact, because every other operation (linking, synthesis, retrieval) depends on the quality of the atoms.

---

## Why It Happens

### Mirroring source structure

Books are organized into chapters. Articles have sections. The natural tendency when extracting is to follow that structure: one note per chapter, one note per section heading. This produces notes that are useful for remembering the book, but useless for building knowledge across books. The source's organizational logic — which serves the author's argument, not your thinking — gets baked into your notes. You end up with a replica of the book instead of a set of ideas you own.

### Conflating facts and insights

A fact is a data point: "Studies show the average attention span for online video is 8 minutes." An insight is a claim with explanatory power: "Attention is a function of perceived relevance, not content length." Both feel worth capturing. But they serve completely different functions in a knowledge system. Mixing them in the same note — or treating them at the same granularity — produces notes that are neither good references nor good building blocks for synthesis.

### No layer model

Without a framework for what kinds of ideas to extract, extraction becomes a judgment call made under uncertainty on every note. Some people over-extract (capturing every interesting sentence), others under-extract (only noting things that feel immediately useful). Without categories, there's no systematic way to decide what granularity is appropriate for what type of content.

---

## How to Detect It

Run these three tests on a sample of 10 notes from your vault:

**The single-claim test**: Can you state the core claim of each note in one sentence? If a note requires three sentences to summarize, it likely contains multiple distinct ideas that should be separate notes.

**The title test**: Are your notes titled after chapter names, source names, or section headings ("Chapter 4: Systems Thinking," "Atomic Habits — Key Ideas")? Source-mirroring titles are a reliable signal that notes follow the book's structure, not an atomic claim structure.

**The connection test**: Pick any two notes from different sources on a related topic. Can you link them as "Note A supports Note B" or "Note A contradicts Note B"? If the notes are too broad, this kind of precise linking is impossible — you can only say "both are about the same general topic."

---

## How to Fix It

**The core principle: one note, one falsifiable claim**

An atomic note has exactly one core idea, expressed as a claim that can be true or false. Not a topic, not a theme, not a chapter — a claim. "Feedback loops amplify small initial differences" is a claim. "Chapter 4: Feedback Loops" is a container. Only claims can be linked, challenged, synthesized, or promoted to permanent knowledge.

**Use extraction layers to organize granularity**

Different types of content require different extraction approaches. Seven layers cover the full range:

| Layer | What it captures | Example note title |
|---|---|---|
| Knowledge | A specific fact, definition, or finding | "Working memory holds 4±1 chunks simultaneously" |
| Compression | The 20% of a source that carries 80% of its value | "Core argument of Thinking Fast and Slow in 3 claims" |
| Mental Model | A spatial or structural representation of how something works | "The dual-process model as a resource allocation problem" |
| Application | A technique or method derived from a concept | "How to use pre-mortems to surface hidden assumptions" |
| Artifact | A template, checklist, or reusable structure | "Decision journal template for high-stakes choices" |
| Decision | A criteria-based framework for choosing between options | "When to use rapid prototyping vs. research-first" |
| Diagnosis | A pattern for recognizing a failure mode | "Signs that a team is optimizing for output, not outcomes" |

Assigning every note to a layer before writing it forces the granularity question: am I capturing a fact, a model, a method, or a diagnosis? The answer shapes the note's structure and appropriate length.

**The split rule**

When in doubt, split. If a note contains two distinct ideas that could each stand alone as a claim, create two notes. Over-splitting is correctable — you can always merge notes later. Under-splitting is harder to fix because the merged ideas become load-bearing and difficult to separate once linked.

---

## Related

- [Source Overwhelm: The Unprocessed Inbox Problem](source-overwhelm.md) — granularity problems often start with capture habits
- [The Re-reading Trap: When Your Notes Fail as References](re-reading-trap.md) — poor granularity is a leading cause of re-reading
- [The Extraction Pipeline: Ingest → Index → Extract](extraction-pipeline.md) — how the extraction layers fit into the full pipeline
- [The Literature Note Graveyard](literature-note-graveyard.md) — poorly decomposed notes rarely mature into permanent knowledge
