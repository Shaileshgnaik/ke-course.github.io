# Part 1 — Quiz & Assessment

> **Module quizzes** test understanding of individual modules.
> The **Part 1 Assessment** is the end-of-part exam covering all 5 modules.

---

## Module 1.1 Quiz {#module-11-quiz}
**What is Knowledge Engineering?**

---

**Q1.** Who coined the term "Knowledge Engineering"?

- A) Alan Turing
- B) Edward Feigenbaum ✅
- C) John McCarthy
- D) Marvin Minsky

---

**Q2.** Which best describes Knowledge Engineering?

- A) Programming computers using statistical models
- B) Training neural networks on large datasets
- C) Capturing and applying human expertise in computer systems ✅
- D) Generating text using large language models

---

**Q3.** Which is a key advantage of KE over Gen AI?

- A) KE generates more creative responses
- B) KE requires less domain expertise to build
- C) KE provides explainable, auditable reasoning ✅
- D) KE works better with large unstructured datasets

---

**Q4.** The first successful knowledge-based system was:

- A) MYCIN
- B) XCON
- C) DENDRAL ✅
- D) ChatGPT

---

**Q5.** In a modern KE + Gen AI hybrid, what role does the Knowledge Base play?

- A) It replaces the LLM entirely
- B) It generates natural language responses
- C) It provides structured guardrails and facts to reduce LLM hallucinations ✅
- D) It trains the neural network weights

---

**Q6 (Short Answer).** In 2–3 sentences, explain the difference between Knowledge Engineering and Machine Learning. When would you choose KE over ML?

---

**Q7 (Short Answer).** A hospital wants to build a system to recommend treatments to doctors. Why would KE be more appropriate than a pure Gen AI solution?

---

## Module 1.2 Quiz {#module-12-quiz}
**Types of Knowledge**

---

**Q1.** A surgeon's ability to "sense" complications during an operation is best classified as:

- A) Explicit knowledge
- B) Declarative knowledge
- C) Tacit knowledge ✅
- D) Procedural knowledge

---

**Q2.** "Water boils at 100°C at sea level" is an example of:

- A) Tacit, uncertain knowledge
- B) Explicit, certain, declarative knowledge ✅
- C) Procedural, uncertain knowledge
- D) Shallow, implicit knowledge

---

**Q3.** A step-by-step guide for configuring a firewall is best described as:

- A) Declarative knowledge
- B) Tacit knowledge
- C) Procedural knowledge ✅
- D) Deep knowledge

---

**Q4.** Which knowledge type is HARDEST to capture in KE?

- A) Explicit knowledge
- B) Declarative knowledge
- C) Certain knowledge
- D) Tacit knowledge ✅

---

**Q5.** Fuzzy logic is best suited to handle:

- A) Explicit, certain knowledge
- B) Procedural knowledge
- C) Uncertain, probabilistic knowledge ✅
- D) Deep, structural knowledge

---

**Q6 (Scenario).** An experienced credit analyst says: *"When I look at an application, I can tell within 30 seconds whether it's risky — it's hard to explain exactly why."*

A) What type of knowledge is this?
B) Why is it valuable for a KE system?
C) How would you capture it?
D) What are the risks if you capture it incorrectly?

---

**Q7 (Scenario).** Two experts disagree:
- Expert A: "Always use relational DB for financial data"
- Expert B: "NoSQL is fine for financial data if schema evolves frequently"

How would you handle this conflict in your Knowledge Base?

---

## Module 1.3 Quiz {#module-13-quiz}
**The KE Lifecycle**

---

**Q1.** What is the correct order of the KE lifecycle?

- A) Represent → Acquire → Validate → Deploy → Maintain
- B) Acquire → Represent → Validate → Deploy → Maintain ✅
- C) Validate → Acquire → Represent → Deploy → Maintain
- D) Deploy → Acquire → Represent → Validate → Maintain

---

**Q2.** Which lifecycle phase is most often underestimated in KE projects?

- A) Knowledge Acquisition
- B) Knowledge Representation
- C) Validation
- D) Maintenance ✅

---

**Q3.** The role primarily responsible for extracting knowledge from domain experts is the:

- A) End User
- B) System Developer
- C) Knowledge Engineer ✅
- D) Project Manager

---

**Q4.** During which phase would you discover that two rules contradict each other?

- A) Acquisition
- B) Representation
- C) Validation ✅
- D) Deployment

---

**Q5.** Why does the KE lifecycle loop back from Maintenance to Acquisition?

- A) Because the system always fails after deployment
- B) Because domains evolve and knowledge must be kept current ✅
- C) Because validation always finds errors
- D) Because the first acquisition is always incomplete

---

**Q6 (Short Answer).** You are hired to build a KE system for a bank's loan approval process. Describe what you would do in the **Problem Analysis** phase. What 3 key questions must you answer before starting acquisition?

---

**Q7 (Short Answer).** Why is it important to separate Problem Analysis from Knowledge Acquisition? What risks arise from skipping Problem Analysis?

---

## Module 1.4 Quiz {#module-14-quiz}
**Expert Systems**

---

**Q1.** An Expert System consists of:

- A) Neural network + training data + GPU
- B) Knowledge Base + Inference Engine + Explanation Module ✅
- C) Database + API + User Interface
- D) LLM + Vector Store + Retrieval Layer

---

**Q2.** Which Expert System diagnosed bacterial infections and pioneered certainty factors?

- A) DENDRAL
- B) XCON
- C) MYCIN ✅
- D) PROSPECTOR

---

**Q3.** The Explanation Module answers:

- A) "What data was in the training set?"
- B) "Which neural network layer activated?"
- C) "WHY was this conclusion reached?" ✅
- D) "What is the model's accuracy score?"

---

**Q4.** Forward chaining means:

- A) Starting from the goal and finding supporting facts
- B) Starting from known facts and deriving conclusions ✅
- C) Applying fuzzy logic to uncertain rules
- D) Querying the knowledge base backwards

---

**Q5.** The biggest commercial benefit of XCON was:

- A) It diagnosed cancer in patients
- B) It discovered a mineral deposit worth $100M
- C) It saved DEC $40 million per year in configuration errors ✅
- D) It translated documents between languages

---

**Q6 (Design Question).** Design a simple Expert System for recommending Azure vs AWS for a given project.

Write:
A) 3 facts that would go in the Knowledge Base
B) 2 IF-THEN rules
C) What the Explanation Module would say for one recommendation
D) One limitation of this system

---

**Q7 (Short Answer).** A manager says: *"Why do we need the Explanation Module? Just give me the answer."* How would you justify it, especially in a regulated industry like finance or healthcare?

---

## Module 1.5 Quiz {#module-15-quiz}
**The Knowledge Acquisition Bottleneck**

---

**Q1.** The "Knowledge Acquisition Bottleneck" refers to:

- A) The slow speed of inference engines
- B) The difficulty of extracting expert knowledge into a structured format ✅
- C) The limited storage capacity of knowledge bases
- D) The cost of hiring domain experts

---

**Q2.** Which technique asks an expert to narrate their thinking in real time?

- A) Structured interview
- B) Delphi method
- C) Think-aloud protocol ✅
- D) Repertory grid

---

**Q3.** Why do experts often struggle to explain their own expertise?

- A) They are unwilling to share knowledge
- B) Their expertise has become subconscious tacit knowledge ✅
- C) They do not understand the domain deeply enough
- D) The knowledge engineering tools are too complex

---

**Q4.** Which modern approach uses AI to assist in knowledge elicitation?

- A) Backward chaining
- B) LLMs as knowledge extractors ✅
- C) Forward chaining
- D) Bayesian networks

---

**Q5.** When two experts disagree on a rule, the best KE approach is:

- A) Always choose the more senior expert
- B) Discard both opinions and use ML instead
- C) Document both views and use certainty factors or context conditions to handle both ✅
- D) Ask the end user to decide

---

**Q6 (Scenario).** You are capturing the knowledge of a 20-year veteran network security engineer. In your first interview they say: *"When I look at a network log, I just KNOW if something looks suspicious."*

A) What type of knowledge is this?
B) Which elicitation technique would you use next?
C) Write 2 follow-up questions you would ask.
D) How would you validate what you capture?

---

**Q7 (Short Answer).** How do LLMs help solve the Knowledge Acquisition Bottleneck? What new risks do they introduce? How would you mitigate those risks?

---

---

## Part 1 — Final Assessment {#part-1-assessment}

> **Complete this assessment after finishing all 5 modules and labs.**
> Passing score: 75% or above to proceed to Part 2.

---

### Section 1 — True / False *(10 marks)*

| # | Statement | T/F |
|---|---|---|
| 1 | Knowledge Engineering and Machine Learning are the same thing. | |
| 2 | Tacit knowledge is harder to capture than explicit knowledge. | |
| 3 | An Expert System can explain WHY it reached a conclusion. | |
| 4 | The KE lifecycle ends at deployment. | |
| 5 | MYCIN was the first Expert System and was built to configure computers. | |
| 6 | Forward chaining is data-driven reasoning. | |
| 7 | Gen AI systems are always more accurate than KE systems in narrow domains. | |
| 8 | The Knowledge Acquisition Bottleneck is caused primarily by a lack of technology. | |
| 9 | Procedural knowledge describes HOW to do something. | |
| 10 | In a KE project, the Knowledge Engineer must be a domain expert themselves. | |

??? success "Answers"
    1-F, 2-T, 3-T, 4-F, 5-F, 6-T, 7-F, 8-F, 9-T, 10-F

---

### Section 2 — Multiple Choice *(10 marks, 1 per question)*

1. Who coined the term "Knowledge Engineering"? *(from 1.1)*
2. Which knowledge type is hardest to capture? *(from 1.2)*
3. Which lifecycle phase is most often underestimated? *(from 1.3)*
4. What does the Explanation Module answer? *(from 1.4)*
5. Which technique asks an expert to narrate their thinking in real time? *(from 1.5)*
6. The first successful knowledge-based system was? *(from 1.1)*
7. "A step-by-step diagnostic workflow" is an example of what knowledge type? *(from 1.2)*
8. Forward chaining is best for? *(from 1.4)*
9. Why does the lifecycle loop from Maintenance back to Acquisition? *(from 1.3)*
10. LLMs help solve the bottleneck by? *(from 1.5)*

---

### Section 3 — Scenario Questions *(20 marks)*

---

**Scenario 1 (10 marks)**

Deepa Naik is a Senior Cloud Engineer at Accenture with 12 years of Azure and AWS experience. Her company wants to build a KE system that captures her cloud architecture expertise so junior engineers can get expert-level recommendations.

**Answer ALL of the following:**

**A)** What types of knowledge (explicit, tacit, declarative, procedural) would you expect to find in Deepa's expertise? Give one example of each. *(4 marks)*

**B)** What lifecycle phases would this KE project go through? Identify the single hardest phase and explain why. *(3 marks)*

**C)** Write 2 IF-THEN rules that might come from Deepa's expertise in cloud architecture. *(3 marks)*

---

**Scenario 2 (10 marks)**

A healthcare company wants to encode the expertise of their Chief Medical Officer into an Expert System for diagnosing common respiratory conditions.

**Answer ALL of the following:**

**A)** What components would the Expert System need? Describe each component's role. *(3 marks)*

**B)** The CMO says: *"I just know when something is serious."* What type of knowledge is this, and what elicitation technique would you use to capture it? *(3 marks)*

**C)** Why is the Explanation Module especially critical in a medical Expert System? What could go wrong without it? *(4 marks)*

---

### Score Guide

| Score | Result | Recommendation |
|---|---|---|
| 90–100% | Excellent | Ready for Part 2 |
| 75–89% | Good | Review weaker modules, then proceed |
| 60–74% | Satisfactory | Re-read Modules 1.2 and 1.5 before proceeding |
| Below 60% | Needs Review | Revisit all of Part 1 before Part 2 |

---

[Proceed to Part 2 →](../course-overview.md){ .md-button .md-button--primary }
[Back to Part 1 Overview →](index.md){ .md-button }
