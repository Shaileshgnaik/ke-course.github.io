# Part 2 — Slide Outlines

---

## Module 2.1 Slide Outline {#module-21-slide-outline}
**"Knowledge Elicitation Techniques"** | ~10 slides

**Slide 1 — Title:** Knowledge Elicitation Techniques
- Subtitle: Getting knowledge out of expert minds

**Slide 2 — Opening Hook**
- Headline: *"You just know it when you see it" — The Expert's Dilemma*
- Visual: Expert head → empty notepad → question mark
- Callout: Your job is to make "I just know" into something a machine can use

**Slide 3 — The Elicitation Toolkit Overview**
- Headline: 6 Techniques, Each for a Different Situation
- Visual: Spectrum bar from Low Structure to High Structure
- Techniques listed: Observation → Think-Aloud → Interview → Laddering → Repertory Grid → Constrained Processing

**Slide 4 — Structured Interviews**
- Headline: Good Questions vs Bad Questions
- Two-column: Bad question examples (left) | Good question examples (right)
- Key rule: Always ask about specific cases, never abstract rules

**Slide 5 — Think-Aloud Protocol**
- Headline: Capture What They DO, Not What They THINK They Do
- Visual: Expert at whiteboard with speech bubbles showing real-time narration
- Callout: Retrospective interviews vs real-time think-aloud comparison

**Slide 6 — Laddering**
- Headline: Keep Asking WHY Until You Hit Bedrock
- Visual: Ladder diagram going deeper with each WHY question
- Show the full laddering example from the module

**Slide 7 — Repertory Grid**
- Headline: Triads Surface Hidden Criteria
- Visual: Three cards (A, B, C) with "Which two are similar?"
- Show how bipolar constructs are formed

**Slide 8 — Choosing the Right Technique**
- Headline: Match Technique to Knowledge Type
- Visual: Decision table (situation → technique)

**Slide 9 — Common Mistakes**
- Headline: 6 Mistakes That Ruin Elicitation Sessions
- Visual: 6 red warning cards with mistake + fix

**Slide 10 — Key Takeaways**

---

## Module 2.2 Slide Outline {#module-22-slide-outline}
**"Document & Text Mining"** | ~9 slides

**Slide 1 — Title:** Document & Text Mining for KE

**Slide 2 — The Untapped Gold Mine**
- Headline: Decades of Knowledge Locked in Documents
- Visual: Stacks of documents → structured rules
- Callout: Extract knowledge without using expert time

**Slide 3 — The Pipeline**
- Headline: 5 Stages from Raw Text to Structured Knowledge
- Visual: Mermaid-style pipeline flow
- Stages: Pre-process → NER → Relations → Rules → Validate

**Slide 4 — NER in Action**
- Headline: Finding the Building Blocks of Rules
- Visual: Annotated text with entity labels highlighted
- Entity types: TECHNOLOGY, METRIC, THRESHOLD, CONDITION, ACTION

**Slide 5 — Linguistic Markers**
- Headline: Words That Signal Rules
- Visual: Two-column table: word → rule type
- must/always = HARD, should = SOFT, if/when = CONDITION

**Slide 6 — Rule Extraction Example**
- Headline: From Paragraph to Structured Rule
- Before: raw document text
- After: formatted IF-THEN rule with confidence

**Slide 7 — Why Validation is Mandatory**
- Headline: Documents Can Be Wrong, Outdated, or Ambiguous
- Three risk cards: Outdated | Incorrect | Ambiguous
- Show validation workflow

**Slide 8 — Tools**
- Headline: Your Document Mining Toolkit
- 6 tool cards with name, use case, language

**Slide 9 — Key Takeaways**

---

## Module 2.3 Slide Outline {#module-23-slide-outline}
**"ML for Knowledge Acquisition"** | ~8 slides

**Slide 1 — Title:** ML for Knowledge Acquisition

**Slide 2 — The Core Idea**
- Headline: Learn Rules From 10,000 Past Decisions
- Visual: Spreadsheet of decisions → Decision Tree → Rules
- Callout: No need to ask experts to articulate — learn from what they did

**Slide 3 — Decision Tree Induction**
- Headline: The Most KE-Friendly ML Technique
- Visual: Actual decision tree diagram
- Show: Training data → Tree → Extracted rules

**Slide 4 — Association Rule Mining**
- Headline: Discovering Co-occurrence Patterns
- Visual: Support/Confidence/Lift formula cards
- Show IT incident example

**Slide 5 — Feature Importance**
- Headline: What Does the Expert Actually Weigh?
- Visual: Horizontal bar chart of feature importance
- Callout: Use this to focus your interview sessions

**Slide 6 — The ML-to-Rules Pipeline**
- Visual: Full pipeline flowchart from Module 2.3
- Highlight: discrepancy loop back to expert interview

**Slide 7 — Limitations**
- Headline: ML Alone Is Not Enough
- Visual: 5 limitation cards with impact and solution

**Slide 8 — Key Takeaways**

---

## Module 2.4 Slide Outline {#module-24-slide-outline}
**"Knowledge Acquisition from LLMs"** | ~9 slides

**Slide 1 — Title:** Knowledge Acquisition from LLMs

**Slide 2 — The Game Changer**
- Headline: LLMs Reduce Expert Time by 80%
- Visual: Before (expert reads 200 docs) vs After (LLM reads docs, expert validates)

**Slide 3 — Method 1: Document Extraction**
- Headline: Feed Documents, Get Candidate Rules
- Visual: Prompt template → structured rule output
- Show the before/after example from the module

**Slide 4 — Method 2: Intelligent Interviewer**
- Headline: The LLM That Asks the Right Follow-Up Questions
- Visual: Conversation transcript showing LLM probing for edge cases

**Slide 5 — Method 3: Gap Identification**
- Headline: What Is Our KB Missing?
- Visual: KB gaps analysis output from Module 2.4

**Slide 6 — Method 4: Rule Formalisation**
- Headline: Expert Speaks → LLM Structures → Expert Validates
- Visual: 3-step flow with example

**Slide 7 — Managing the Risks**
- Headline: 4 Risks and How to Mitigate Them
- Visual: 4 risk cards: Hallucination, Outdated, Confident+Wrong, Bias

**Slide 8 — The Validation Workflow**
- Visual: Full acquisition flowchart from Module 2.4

**Slide 9 — Key Takeaways**

---

## Module 2.5 Slide Outline {#module-25-slide-outline}
**"Human-AI Collaborative Acquisition"** | ~8 slides

**Slide 1 — Title:** Human-AI Collaborative Acquisition

**Slide 2 — Why No Single Technique Is Enough**
- Visual: 4-quadrant table: technique → what it misses
- Callout: The solution is a layered pipeline

**Slide 3 — The Full Pipeline**
- Visual: Full mermaid flowchart from Module 2.5
- 6 phases with timeline estimates

**Slide 4 — Phase 1 & 2: Documents First**
- Headline: Extract 60-80% of Rules Before Any Expert Time
- Visual: Document stack → candidate rules → gap analysis
- Key stat: Expert time = 0 in these phases

**Slide 5 — Phase 3: Targeted Expert Sessions**
- Headline: 3-4 Hours Instead of 20-30 Hours
- Visual: Venn diagram — what gaps remain after Phase 1/2
- Show: Interview topics come directly from gap analysis

**Slide 6 — Handling Disagreement**
- Headline: When Experts Contradict Each Other
- Visual: Three option cards: CF | Context Conditions | Delphi

**Slide 7 — Acquisition Plan Template**
- Visual: Filled-in template from Module 2.5
- Show as a planning tool for students' own projects

**Slide 8 — Key Takeaways + Part 2 Summary Table**
- Final table: Module → Technique → Best For
