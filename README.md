# Deep Reading Coach / 深度读书教练

A Claude Code skill that turns reading into active learning. Instead of passive highlighting, it diagnoses the type of book you're reading and runs the most effective learning protocol for that type.

一个 Claude Code skill，把读书变成主动学习。先诊断书的类型，再按类型选最高效的学习流程。

## Core Principle

**Learning = building retrievable, transferable mental models.**

Different books carry different forms of knowledge. The coaching approach should match.

第一性原理：学习 = 在脑中建立**可提取、可迁移的模型**。不同书装的是不同形态的知识，建模方式也不同。先诊断，再开方。

## How It Works

### Step 0: Diagnosis (once per book)

The coach browses the table of contents, preface, and conclusion to classify the book:

| Type | Examples | Mode |
|------|----------|------|
| **A. Narrative / Decision** | History, biography, business cases, investing | Predict & Compare |
| **B. Conceptual** | Economics, psychology, statistics | Explain & Connect |
| **C. Skill / How-to** | Programming, SQL, trading strategies, writing | Read Less, Practice More |
| **D. Argument** | Books with a thesis, e.g. *Antifragile* | Deconstruct & Challenge |
| **E. Reference** | Manuals, encyclopedias | Build an Index |
| **F. Literary** | Novels, essays, poetry | Slow Read & Feel |

Then asks: "After finishing this book, what do you want to be able to **do**?" — judge / explain / operate / refute / look up / enjoy.

Mixed-type books switch modes chapter by chapter.

## The 6 Modes

### Mode A: Predict & Compare (Narrative / Decision)

Like a strategist briefing a lord on history — set up the situation, stop before the decision point, never spoil.

1. **Pre-test**: 2-3 questions the chapter will answer (no answers given)
2. **Setup**: Who, what situation, what cards they hold, what pressure they face
3. **Predict**: "If you were X, what would you do? Why?" — both reader and coach predict, logged in a Prediction Tracker
4. **Reveal**: What actually happened + compare predictions — hit / partial / miss, analyze why
5. **Deep dive** (rotate): counterfactual / red-blue adversarial / connect to today
6. **Feynman retell**: Reader explains the causal chain in 3 sentences
7. **Summary**: TL;DR + key figures + updated tracker

### Mode B: Explain & Connect (Conceptual)

1. **Pre-test**: Reader explains the core concept in their own words (mistakes welcome)
2. **Teach**: Analogies and examples
3. **Feynman retell**: Reader re-explains, coach asks "why" until the logic chain is complete
4. **Find boundaries**: "When does this concept break down?" — reader provides a counterexample
5. **Concept map**: Connect this chapter's concepts to previous ones
6. **Summary**: Concept card — definition, analogy, counterexample, relationships

### Mode C: Read Less, Practice More (Skill / How-to)

1. Extract **1 actionable item** per chapter, skim the rest
2. **Immediate practice**: A task using the reader's real work or project
3. **Feedback**: Compare output to the book's method
4. **Error log**: Track mistakes and corrections, review periodically

Reading more carefully ≠ learning more effectively. Don't over-analyze skill books.

### Mode D: Deconstruct & Challenge (Argument)

1. **Extract**: Reader states the chapter's core claim in one sentence
2. **Deconstruct**: List supporting evidence — data, case studies, analogies, or authority
3. **Red-blue adversarial**: Coach gives the strongest rebuttal, reader defends; then swap
4. **Verdict**: Reader judges under what conditions the claim holds, confidence level 0-100%
5. **Summary**: Claim -> Evidence -> Strongest rebuttal -> My position

### Mode E: Build an Index (Reference)

- Don't read cover to cover
- Browse the TOC, build a "what problem -> which chapter" index
- Deep-read only when a specific question arises

### Mode F: Slow Read & Feel (Literary)

- Minimal engineering-style analysis. Focus on feeling and discussion
- 1-2 questions per session: most striking passage, why a character moved you, what's special about the author's language
- Close-read original text, savor the language itself

## Universal Module: Notable Quotes

Available in any mode:
- Pick 1-2 beautifully written sentences from the original text
- Analyze word choice, sentence structure, context
- Reader writes a sentence in the same structure about their own field, then polish together

## Spaced Review

Every 3 chapters, start by recalling previous chapters without the book:
- Mode A: Causal chains
- Mode B: Concept relationships
- Mode C: Action items
- Mode D: Claims and evidence

Fill in the gaps.

## Energy Management

- Save deep reading for ~20% of books (the core ones). Skim the rest or read key chapters only
- If the reader is investing more effort than a book deserves, say so honestly

---

## Installation

Copy the `SKILL.md` file to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/deep-reading-coach
cp SKILL.md ~/.claude/skills/deep-reading-coach/
```

Then invoke the skill in Claude Code when starting a new book.

## Iron Rules

1. **The reader must generate**: Predict, retell, write, refute — reader goes first. Coach only asks, compares, and corrects. Give hints when stuck, never answers.
2. Facts follow the original book. Anything not in the book is labeled "supplementary."
3. Keep original quotes short; focus on explanation and paraphrase.
4. Use analogies liberally. Lead with TL;DR.

---

Built by [daac](https://daac-solo.github.io) (dumb as a chicken) — philosophy first, code second.
