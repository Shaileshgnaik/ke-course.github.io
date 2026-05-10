# Part 2 — Quiz & Assessment

---

## Module 2.1 Quiz {#module-21-quiz}
**Knowledge Elicitation Techniques**

**Q1.** Which elicitation technique asks the expert to narrate their thinking while performing a real task?

- A) Structured Interview
- B) Think-Aloud Protocol ✅
- C) Repertory Grid
- D) Delphi Method

**Q2.** An expert says: *"I choose the right database — it just depends."* What is the BEST follow-up?

- A) "Can you give me a yes or no answer?"
- B) "Depends on what, exactly?" ✅
- C) "Can you write down your rules?"
- D) "Let's move on to the next question."

**Q3.** The Laddering technique is best for:

- A) Building consensus among multiple experts
- B) Extracting tacit knowledge through task observation
- C) Understanding the deep causal WHY behind decisions ✅
- D) Discovering hidden decision criteria using triads

**Q4.** The Repertory Grid technique works by:

- A) Presenting triads of cases and asking "which two are similar?" ✅
- B) Asking structured yes/no questions
- C) Observing the expert in their natural work environment
- D) Mining historical decision logs

**Q5.** The Delphi Method is used when:

- A) The expert cannot articulate their reasoning
- B) You have multiple experts who disagree and need consensus ✅
- C) Historical decision data is available
- D) Documents contain the required knowledge

**Q6 (Short Answer).** You are eliciting knowledge from a senior DevOps engineer. In your first interview they give only vague answers. Name 2 techniques you would use in the follow-up session and explain why.

**Q7 (Scenario).** An expert keeps saying *"It depends on the context"* without elaborating. Write 3 specific follow-up questions that would extract the actual decision criteria.

---

## Module 2.2 Quiz {#module-22-quiz}
**Document & Text Mining**

**Q1.** What is the correct order of the document mining pipeline?

- A) Extract → Validate → Pre-process → NER → Rules
- B) Pre-process → NER → Relations → Rules → Validate ✅
- C) Validate → Pre-process → NER → Rules → Extract
- D) NER → Pre-process → Rules → Relations → Validate

**Q2.** The word "must" in a document most likely maps to:

- A) A soft rule with low confidence
- B) A best practice recommendation
- C) A hard constraint with confidence = 1.0 ✅
- D) An uncertain observation

**Q3.** Why is expert validation mandatory after document mining?

- A) Documents are always written in the wrong format
- B) NLP tools cannot extract text from PDFs
- C) Documents may be outdated, incorrect, or ambiguous ✅
- D) Expert validation is optional — it's just best practice

**Q4.** Named Entity Recognition (NER) in KE is used to:

- A) Train a classification model on historical data
- B) Identify and classify key terms like services, thresholds, and conditions ✅
- C) Convert documents from PDF to text
- D) Generate rules automatically without human review

**Q5 (Short Answer).** A document says: *"Teams should prefer serverless for short-duration event-triggered workloads."* Extract this as a structured IF-THEN rule with a confidence rating. Explain your confidence choice.

---

## Module 2.3 Quiz {#module-23-quiz}
**ML for Knowledge Acquisition**

**Q1.** Which ML technique produces the most human-readable rules for KE?

- A) Deep Neural Network
- B) Random Forest
- C) Decision Tree ✅
- D) Support Vector Machine

**Q2.** In Association Rule Mining, "confidence" means:

- A) How often the pattern appears in the dataset
- B) How much better than random chance the rule performs
- C) How often the rule is correct when conditions are met ✅
- D) The accuracy of the ML model overall

**Q3.** What is the most important limitation of ML-based knowledge acquisition?

- A) ML models are too slow for production use
- B) ML cannot handle more than 10 features
- C) ML learns from past data which may contain mistakes or bias ✅
- D) ML always requires more than 1 million training examples

**Q4.** Feature importance from a Random Forest model tells you:

- A) Which rules to remove from the knowledge base
- B) Which factors the expert actually considers most in their decisions ✅
- C) The confidence level of each extracted rule
- D) Which documents to mine next

**Q5 (Scenario).** You have 3,000 historical loan approval decisions. Describe how you would use ML to extract knowledge from this data AND what you would do with the extracted rules before adding them to a production KB.

---

## Module 2.4 Quiz {#module-24-quiz}
**Knowledge Acquisition from LLMs**

**Q1.** When an LLM cannot find a source for a rule it extracted, you should:

- A) Trust the rule — LLMs are generally accurate
- B) Discard the rule immediately
- C) Flag it as unverified and send it to expert validation ✅
- D) Lower the confidence rating and add it anyway

**Q2.** LLMs are LEAST reliable for:

- A) Extracting rules from documents
- B) Generating interview follow-up questions
- C) Domain-specific knowledge that post-dates their training ✅
- D) Reformatting expert statements into rule syntax

**Q3.** The main advantage of using an LLM as an intelligent interviewer is:

- A) It replaces the need for domain experts entirely
- B) It asks follow-up questions that uncover tacit knowledge more effectively ✅
- C) It always produces 100% accurate rules
- D) It validates rules against historical data automatically

**Q4.** Which prompt technique reduces hallucination risk in LLM knowledge extraction?

- A) Asking the LLM to rate its confidence only
- B) Requiring the LLM to cite the source sentence for every rule ✅
- C) Using a longer, more detailed prompt
- D) Running the LLM multiple times and averaging

**Q5 (Short Answer).** A colleague says: *"Let's just use Claude to extract all our rules and skip the expert interviews."* What are the 3 key risks of this approach and how would you address each?

---

## Part 2 — Final Assessment {#part-2-assessment}

> **Complete this after finishing all 5 modules and labs.**
> Passing score: 75% or above to proceed to Part 3.

---

### Section 1 — True / False *(10 marks)*

| # | Statement | T/F |
|---|---|---|
| 1 | Think-aloud protocol captures what experts think they do, not what they actually do. | |
| 2 | Documents are always accurate and up-to-date sources of knowledge. | |
| 3 | Decision Trees are the most KE-friendly ML technique because they produce readable rules. | |
| 4 | LLM-extracted rules should be added directly to a production KB without validation. | |
| 5 | The Delphi Method is used to build consensus among multiple disagreeing experts. | |
| 6 | "Must" in a document maps to a soft rule with low confidence. | |
| 7 | ML feature importance reveals which factors experts actually weigh most in decisions. | |
| 8 | The Human-AI pipeline reduces expert time by focusing interviews only on knowledge gaps. | |
| 9 | Laddering is best for surfacing hidden decision criteria through triads of cases. | |
| 10 | Expert validation is the final quality gate regardless of which acquisition method was used. | |

??? success "Answers"
    1-F, 2-F, 3-T, 4-F, 5-T, 6-F, 7-T, 8-T, 9-F, 10-T

---

### Section 2 — Scenario Questions *(20 marks)*

**Scenario 1 (10 marks)**

A global bank wants to build a KE system encoding their credit risk assessment process. They have: 5 senior analysts (max 6 hours available), 10,000 historical loan decisions, 30 internal policy documents, and 2 junior analysts for support.

**A)** Which 3 acquisition techniques would you use and in what order? Justify each choice. *(4 marks)*

**B)** Design the interview approach for one senior analyst session (45 minutes). What technique? What questions? What output? *(3 marks)*

**C)** The ML analysis of 10,000 decisions shows a pattern: *loans to applicants in a specific postcode area are rejected at 3x the rate of others*. What do you do with this finding? *(3 marks)*

---

**Scenario 2 (10 marks)**

You use an LLM to extract rules from a 200-page cloud architecture guide. The LLM returns 180 candidate rules. 40 of them have no source citation.

**A)** How do you handle the 40 uncited rules? *(2 marks)*

**B)** You notice Rule R47 says: *"Always use Kubernetes for containerised workloads"* but your expert says this is outdated — serverless is now preferred for most workloads. What does this reveal about document mining risk, and how do you resolve it? *(4 marks)*

**C)** Design a gap analysis prompt you would send to the LLM after completing document extraction. What 3 things should it identify? *(4 marks)*

---

### Score Guide

| Score | Result | Recommendation |
|---|---|---|
| 90–100% | Excellent | Ready for Part 3 |
| 75–89% | Good | Review weaker modules, then proceed |
| 60–74% | Satisfactory | Re-read Modules 2.1 and 2.4 |
| Below 60% | Needs Review | Revisit all of Part 2 |

---

[Proceed to Part 3 →](../course-overview.md){ .md-button .md-button--primary }
[Back to Part 2 Overview →](index.md){ .md-button }
