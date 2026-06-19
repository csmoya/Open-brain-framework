---
module: module-2-extraction
related_skills:
  - open-brain-extract
  - open-brain-index
  - open-brain-ingest
last_updated: 2026-06-19
---

# The Extraction Pipeline: Ingest → Index → Extract

## What It Is

The extraction pipeline is a three-phase process for turning raw sources — books, articles, PDFs, research papers — into structured, reusable knowledge. Each phase has a distinct purpose, a defined output, and a clear handoff to the next phase.

The pipeline exists because the three core problems in knowledge extraction are distinct and require different cognitive modes: deciding what to process (triage), mapping what's in a source (indexing), and distilling insights from it (extraction). Collapsing these three operations into a single undifferentiated "reading session" is the root cause of source overwhelm, the re-reading trap, and poorly granulated notes.

The pipeline separates them.

---

## Phase 1: Ingest — Triage Before You Capture

The ingest phase happens before any reading. Its purpose is to make a commitment decision: how much of your extraction capacity is this source worth?

Every source that enters your system gets assigned a tier:

| Tier | Criteria | What it triggers |
|---|---|---|
| TOP | Core to a domain you actively work in; you'll reference it multiple times; contains frameworks or models you want to apply | Full pipeline: index + extract |
| INTERESTING | Relevant and worth one pass; yields a handful of useful ideas but isn't foundational | Highlights only; brief note on key claims |
| SKIP | Interesting in the moment but not domain-relevant; a single data point or passing reference | Link only, or discard |

The triage decision should take under 60 seconds. Read the abstract, the introduction's first three paragraphs, and the conclusion. You are not evaluating comprehensiveness — you are evaluating relevance to your current domains of work. If you can't assign a tier in 60 seconds, the source is almost certainly INTERESTING or SKIP.

**What this prevents**: Treating a landmark book and a blog post identically. Spending 2 hours on a source that deserved 10 minutes. The guilt accumulation of a queue full of equally-weighted obligations.

---

## Phase 2: Index — Map the Source Before Extracting From It

For TOP-tier sources only, build a structured knowledge map before writing individual notes.

A source index is not a summary. It does not tell you what the source is about in general terms. It tells you what's *in* the source and where — a navigable structure that allows you to locate specific arguments, frameworks, and claims without re-reading the source.

A source index for a book typically covers:
- The central argument in one sentence
- The 4–8 major supporting claims, in order
- The key frameworks or models introduced and where they appear
- Which sections cover which sub-topics (so future-you can navigate directly)
- Anything explicitly out of scope (helps prevent false expectations from the notes)

**Why index before extracting**: The index forces a structural pass through the source before atomic extraction begins. This means individual notes are written with the source's full architecture in mind — you know which claims are central vs. peripheral, which sections are load-bearing vs. illustrative. Without an index, extraction tends to over-weight early chapters (where you had the most attention) and under-weight later synthesis sections.

The index also serves as the permanent reference artifact that eliminates re-reading. Once you have a source index, you can answer "what did this book say about X?" in under a minute without opening the original.

---

## Phase 3: Extract — Turn the Source into Atomic Notes

Extraction is the process of distilling the source into discrete, reusable knowledge units — one note per insight, written at a granularity that allows each note to be linked, challenged, and synthesized independently.

Extraction targets seven layers of content:

| Layer | What to capture | Note length |
|---|---|---|
| Knowledge | Specific facts, definitions, research findings | 1–3 sentences |
| Compression | The core argument or essential 20% of the source | 100–200 words |
| Mental Model | How a concept works as a structure or mechanism | 50–150 words + optional diagram |
| Application | A technique or method the source describes | 100–300 words |
| Artifact | A reusable template, checklist, or framework | Variable (structured) |
| Decision | Criteria for choosing between options | 50–200 words |
| Diagnosis | A pattern for recognizing a failure mode | 50–150 words |

Not every source produces notes in every layer. A technical how-to produces mainly Applications. A conceptual book produces mainly Knowledge, Mental Models, and Compressions. The layer assignments are a guide to what to look for, not a quota to fill.

**Quality gate**: After extraction, run the replace test. Using only your notes, answer 5 questions about the source's key ideas without looking at the original. If your notes can't answer 4 out of 5, identify the gap type (mechanism, application, boundary condition, distinction, evidence) and fill it before marking the source complete.

---

## The Process

| Phase | Input | Output | Time estimate |
|---|---|---|---|
| Ingest | Raw source (URL, PDF, book, article) | Tier assignment + inbox entry | < 5 minutes |
| Index | TOP-tier source | Structured knowledge map | 20–45 minutes |
| Extract | Indexed source | Atomic notes across relevant layers | 45–90 minutes (book), 15–30 minutes (article) |

Total time for a TOP-tier book: 1.5–2.5 hours. This is not a full re-read. It is a structured pass guided by the index, targeting specific layers, with the replace test as the quality check.

---

## Cadence

**Ingest**: At capture time. Never save a source without assigning a tier. The triage decision costs 60 seconds. Deferring it costs your future attention every time you see the source in your queue.

**Index**: Before beginning any extraction session on a new TOP-tier source. The index is the session plan.

**Extract**: In dedicated sessions of 60–90 minutes. Do not attempt to extract while reading for the first time — the first read is for comprehension, the extraction session is for distillation.

---

## What It Is Not

**Not speed-reading**: The pipeline does not require reading faster. It requires reading with more specific extraction targets. You will likely read some sections more carefully (those covering frameworks and mechanisms) and some sections less carefully (narrative examples, transition sections) than you would in a normal read-through.

**Not highlights collection**: Saving highlights to Readwise or Kindle is not extraction. Highlights capture what the author said. Extraction produces notes about what the ideas mean — in your own words, in a structure that serves your future thinking rather than the author's narrative.

**Not AI summarization**: Running a PDF through an AI summarizer produces a compression of the original text. It does not produce the layer-specific, claim-titled notes that allow future synthesis. Summaries are useful for triage (deciding if a source is TOP/INTERESTING/SKIP) — they are not a substitute for the extraction phase.

**Not a one-time activity**: A source's value to your vault changes as your domains evolve. A source you processed as INTERESTING two years ago might warrant full extraction now that you're working intensively in that domain. The pipeline can be re-run at higher depth.

---

## Measuring Impact

| Metric | Healthy range | What it indicates |
|---|---|---|
| Extraction rate | > 80% of TOP-tier sources fully extracted within 2 weeks of ingest | Pipeline is keeping up with capture |
| Re-reading rate | < 2 returns to any processed source per month | Source indices are doing their job |
| Replace test pass rate | > 80% of questions answerable from notes alone | Extraction depth is sufficient |
| Queue age | No unprocessed TOP-tier source older than 30 days | Triage is preventing accumulation |

---

## Related

- [Source Overwhelm: The Unprocessed Inbox Problem](source-overwhelm.md) — what the ingest phase prevents
- [Atomic Note Decomposition: Getting the Granularity Right](atomic-note-decomposition.md) — the theory behind the extraction layer model
- [The Re-reading Trap: When Your Notes Fail as References](re-reading-trap.md) — what the index phase prevents
- [The Maturation Ladder: From Captured to Owned](maturation-ladder.md) — what happens to extraction outputs downstream
