---
module: module-2-extraction
related_skills:
  - open-brain-extract
  - open-brain-index
last_updated: 2026-06-19
---

# The Re-reading Trap: When Your Notes Fail as References

## The Problem

You read a book carefully. You took notes. You marked it "processed." Six months later, a conversation or a project brings up exactly the topic that book covered. You go to your notes — and find they're not enough. The notes tell you the book was about feedback loops, but they don't give you the specific mechanism you need right now. So you go back to the PDF. You find the passage. You read it again. You've now read this book twice, and your notes still don't capture what you actually needed.

This is the **re-reading trap**: returning to a source you've already "processed" because your notes don't actually replace the source as a reference tool. It's the clearest signal that extraction failed — not because you didn't work, but because you worked without the right goal.

A properly extracted source should make re-reading unnecessary for 95% of future reference needs. If you're regularly returning to processed sources, you don't have a memory problem. You have an extraction problem. The book is doing the job your notes were supposed to do.

---

## Why It Happens

### Extraction without structure

The most common form of failed extraction is capturing ideas without capturing their structure. You note that a book says "systems have feedback loops" and "leverage points exist at key nodes." Both statements are accurate. Neither is useful without knowing: what distinguishes a feedback loop from a linear chain? What makes a node a leverage point vs. a passive element? The concepts are in your notes; the mechanism — the part you'll need when applying the idea — is not.

Good extraction captures not just what a source says, but the structural relationships between its claims. Isolated claims age poorly. Structured arguments remain navigable.

### No source compression layer

A book contains hundreds of ideas. Not all of them are equally important. Without a deliberate compression pass — a structured map of the source's key arguments, their relationships, and their coverage — your notes are a flat list of highlights. A flat list requires you to read all of it to find any of it. A structured map lets you navigate directly to the relevant section.

The compression layer is what allows you to ask "what did this book say about X?" and get a useful answer in 30 seconds rather than re-scanning 200 highlights.

### Wrong extraction targets

Many PKM practitioners optimize for highlighting quotes rather than distilling principles. A quote captures what an author said. A principle captures what the quote means in a form that generalizes beyond the source. "The map is not the territory" (quote) vs. "Representations of reality always omit the features that make reality complex — and those omissions are where decisions go wrong" (principle). The quote sends you back to the book to understand context. The principle is self-contained.

---

## How to Detect It

| Signal | What to measure |
|---|---|
| Re-open rate | How many times in the last month did you open a source you've already marked as processed? More than 2-3 times suggests systematic extraction failure. |
| Self-sufficiency test | Pick 5 claims from your processed sources. Can you explain the mechanism behind each claim using only your notes? Or do the notes just record that the claim exists? |
| Source index coverage | What percentage of your processed sources have a structured outline (key arguments, coverage map) vs. only raw highlights or scattered notes? |
| Time to answer | When a question arises about a processed source, how long does it take to get a satisfying answer from your notes alone? More than 5 minutes suggests the extraction wasn't structured for retrieval. |

---

## How to Fix It

**Build source outlines before full extraction**

For any source worth full extraction, create a structured knowledge map before writing individual notes. This is not a summary — it's a navigational index. A source outline for a book might cover: the central argument in one sentence, the 4-6 major claims that support it, the key frameworks introduced, and which chapters or sections cover which sub-topics.

The outline serves two functions: it guides extraction (so you know which sections to prioritize) and it replaces the source's table of contents for future reference (so you can navigate without re-reading).

**Extract principles, not quotes**

For each highlighted passage, ask: what is the generalizable principle this passage expresses? Write the note around the principle, not the quote. The original quote can appear as supporting evidence, but the note's title and lead sentence should be the principle in your own words. If you can't restate it in your own words, you don't understand it well enough to extract it yet — and that's valuable information.

**Apply the replace test**

After completing extraction on any source, run the replace test: without looking at the original, answer 5 questions about the source's key ideas using only your notes. If your notes can't answer 4 out of 5, extraction is incomplete. Identify which types of questions fail (mechanisms? applications? boundary conditions?) and go back to fill those gaps specifically.

| Question type | Example | What it tests |
|---|---|---|
| Mechanism | "How does X actually work?" | Whether you extracted the structural logic, not just the claim |
| Application | "When would I use this?" | Whether you extracted practical context |
| Boundary | "When does X break down?" | Whether you extracted the limits of the claim |
| Distinction | "How is X different from Y?" | Whether you extracted comparative structure |
| Evidence | "What's the evidence for X?" | Whether you extracted the basis for the claim |

---

## Related

- [Atomic Note Decomposition: Getting the Granularity Right](atomic-note-decomposition.md) — poorly granulated notes cause re-reading
- [Source Overwhelm: The Unprocessed Inbox Problem](source-overwhelm.md) — the re-reading trap is what awaits rushed extraction
- [The Extraction Pipeline: Ingest → Index → Extract](extraction-pipeline.md) — the pipeline that makes source outlines systematic
