# Part 1 — Hands-On Labs

> **Complete one lab per module before moving to the next module.**
> Labs are designed to build practical, hands-on understanding — not just theoretical knowledge.

---

## Lab 1.1 — Spot the Knowledge Engineering {#lab-11}

**Module:** 1.1 — What is Knowledge Engineering?
**Duration:** 30 minutes | **Format:** Individual or pair activity

### Objective
Recognise where KE is already happening in real-world systems and distinguish it from traditional programming and Gen AI.

---

### Part A — Classify the System *(10 mins)*

For each system below, identify which category it belongs to:

- **[A]** Traditional Programming
- **[B]** Machine Learning
- **[C]** Generative AI
- **[D]** Knowledge Engineering

| # | System Description | Category |
|---|---|---|
| 1 | A tax filing app that calculates refunds using tax rate tables | |
| 2 | Netflix recommending movies based on viewing history | |
| 3 | ChatGPT answering a general knowledge question | |
| 4 | A bank's loan denial that states: *"Denied — because credit score < 650 AND debt ratio > 40%"* | |
| 5 | A GPS that reroutes around traffic in real time | |
| 6 | A medical system that says: *"Patient likely has pneumonia — Confidence: 82%. Rules fired: R3 → R7 → R12"* | |
| 7 | A spam filter trained on 1 million labelled emails | |
| 8 | An architecture tool that says: *"Use Azure Service Bus because your workload is event-driven with high message volume"* | |

??? success "Answers"
    1→A, 2→B, 3→C, 4→D, 5→B/D, 6→D, 7→B, 8→D

---

### Part B — Write Your Own Rules *(15 mins)*

Pick **one domain** from your own work experience. Write **3 IF-THEN rules** that capture expert knowledge.

```
Format:
IF   [condition(s)]
THEN [conclusion / action]
BECAUSE [the expert reasoning behind this rule]
```

**Example (Cloud Architecture domain):**

```
IF   workload_type = "event-driven"
     AND message_volume = "high"
     AND coupling_requirement = "loose"
THEN recommend = "Azure Service Bus"
BECAUSE Service Bus enables decoupled, reliable async messaging
        suitable for high-throughput event-driven architectures
```

---

### Part C — Reflection *(5 mins)*

1. Which systems in Part A were hardest to classify? Why?
2. Were your rules in Part B easy or hard to write? Did you find yourself writing "it depends"?
3. What would be harder to capture as an explicit rule in your domain?

---

## Lab 1.2 — The Knowledge Audit {#lab-12}

**Module:** 1.2 — Types of Knowledge
**Duration:** 45 minutes | **Format:** Individual then group discussion

### Objective
Classify knowledge from a real domain into types and understand how each type should be handled differently.

### Scenario
You are a Knowledge Engineer working with a Senior Cloud Solutions Architect. Your task is to begin capturing their expertise.

---

### Task 1 — Classify the Knowledge *(20 mins)*

For each architect statement, complete the classification:

**Statement 1:** *"AWS Lambda has a 15-minute maximum execution timeout"*

| | |
|---|---|
| Explicit or Tacit? | |
| Declarative or Procedural? | |
| Certain or Uncertain? | |

**Statement 2:** *"When a client says they want 'high availability', I can tell from their hesitation whether they actually understand the cost implications"*

| | |
|---|---|
| Explicit or Tacit? | |
| Declarative or Procedural? | |
| Certain or Uncertain? | |

**Statement 3:** *"To set up multi-region failover: first configure primary region, then set up replication, then configure health checks, then test failover"*

| | |
|---|---|
| Explicit or Tacit? | |
| Declarative or Procedural? | |
| Certain or Uncertain? | |

**Statement 4:** *"This architecture will probably have latency issues under high load — I've seen this pattern fail before"*

| | |
|---|---|
| Explicit or Tacit? | |
| Declarative or Procedural? | |
| Certain or Uncertain? | |

**Statement 5:** *"Azure is generally better for .NET workloads than AWS"*

| | |
|---|---|
| Explicit or Tacit? | |
| Declarative or Procedural? | |
| Certain or Uncertain? | |

??? success "Answers"
    | Statement | Explicit/Tacit | Declarative/Procedural | Certain/Uncertain |
    |---|---|---|---|
    | 1 | Explicit | Declarative | Certain |
    | 2 | Tacit | Declarative | Uncertain |
    | 3 | Explicit | Procedural | Certain |
    | 4 | Tacit | Declarative | Uncertain |
    | 5 | Explicit | Declarative | Uncertain |

---

### Task 2 — Capture Strategy *(15 mins)*

For each statement, fill in the strategy table:

| Statement | How to Capture | How to Represent | Risk if Wrong |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

---

### Task 3 — Reflection *(10 mins)*

1. Which statement was hardest to classify and why?
2. How would you validate Statement 4 which is based on past experience?
3. What happens if two architects disagree on Statement 5?

---

## Lab 1.3 — Design the KE Lifecycle {#lab-13}

**Module:** 1.3 — The KE Lifecycle
**Duration:** 50 minutes | **Format:** Team activity (2–3 people)

### Objective
Apply the KE lifecycle to a real problem by planning each phase with concrete activities.

### Scenario
Your company wants to build an intelligent system that helps solution architects recommend the right cloud architecture pattern for new projects. Currently this takes senior architects 2–3 days per recommendation.

**Goals:**
- Reduce decision time to 2 hours
- Make recommendations consistent across teams
- Enable junior architects to make expert-level decisions
- Provide explainable recommendations — not a black box

---

### Task — Plan the KE Lifecycle

Fill in each phase:

**Phase 1: Problem Analysis**

| Question | Your Answer |
|---|---|
| What is the exact problem scope? | |
| Who are the domain experts? | |
| What decisions must the system make? | |
| How will you measure success? | |
| What are the system boundaries? | |

**Phase 2: Knowledge Acquisition**

| Question | Your Answer |
|---|---|
| Which elicitation techniques will you use? | |
| How many expert sessions do you need? | |
| What documents or past cases will you analyse? | |
| How will you handle disagreement between experts? | |

**Phase 3: Knowledge Representation**

| Question | Your Answer |
|---|---|
| What representation method fits this problem? | |
| How will uncertainty be handled? | |
| Write one example rule: | |

**Phase 4: Validation**

| Question | Your Answer |
|---|---|
| How will you test the system? | |
| Name 3 test cases (past architecture decisions): | |
| What are your pass/fail criteria? | |

**Phase 5: Maintenance**

| Question | Your Answer |
|---|---|
| How often will the KB be reviewed? | |
| Who owns KB maintenance? | |
| How will new cloud services trigger KB updates? | |

---

### Deliverable
Present your plan (5 minutes). Highlight: biggest risk, most important phase, first milestone.

---

## Lab 1.4 — Build a Mini Expert System {#lab-14}

**Module:** 1.4 — Expert Systems
**Duration:** 60 minutes | **Format:** Individual with peer review

### Objective
Build a simple rule-based expert system — first on paper, then in pseudocode.

### Domain: Cloud Storage Selector
Build a mini expert system that recommends the right Azure/AWS storage service based on requirements.

---

### Step 1 — Define the Knowledge Base *(15 mins)*

**Pre-given facts:**

| Service | Best For |
|---|---|
| Azure Blob Storage | Unstructured data, files, images |
| Azure SQL Database | Relational, ACID transactions |
| Azure Cosmos DB | NoSQL, global distribution |
| AWS S3 | Object storage, static assets |
| AWS DynamoDB | Key-value, high throughput NoSQL |
| AWS RDS | Relational, managed SQL |

Write **6 IF-THEN rules** using this format:

```
Rule R[n]:
IF   [condition 1]
     AND [condition 2]
THEN recommend = "[Service Name]"
CONFIDENCE = [0.0 to 1.0]
```

---

### Step 2 — Define Working Memory *(10 mins)*

What questions does the system ask the user? Define the input:

| Question | Possible Values |
|---|---|
| What cloud platform? | Azure / AWS / No preference |
| What is the data type? | |
| Do you need ACID transactions? | |
| Is global distribution required? | |
| What is the expected throughput? | |

---

### Step 3 — Trace the Inference *(15 mins)*

Manually trace through your rules for these test cases:

**Test Case 1:** Cloud: Azure | Data: Unstructured | Transactions: No
- Rules fired:
- Recommended service:

**Test Case 2:** Cloud: AWS | Data: Key-Value | Throughput: High
- Rules fired:
- Recommended service:

**Test Case 3:** Cloud: No preference | Data: Structured | Transactions: Yes
- Rules fired:
- Recommended service:

---

### Step 4 — Write the Explanation *(10 mins)*

For Test Case 2, write what the Explanation Module should say:

```
"I recommend [SERVICE] because:
 - Rule [R?] fired because [condition was met]
 - Rule [R?] confirmed because [condition was met]
 - Confidence: [%]"
```

---

### Step 5 — Python Pseudocode (Bonus) *(10 mins)*

```python
def recommend_storage(cloud, data_type, transactions,
                       distribution, throughput):

    # Rule R1
    if cloud == "Azure" and data_type == "unstructured":
        return {
            "service": "Azure Blob Storage",
            "confidence": 0.95,
            "reason": "Rule R1: Azure + unstructured data"
        }

    # Add your remaining rules here...
    pass
```

---

## Lab 1.5 — Break the Bottleneck {#lab-15}

**Module:** 1.5 — The Knowledge Acquisition Bottleneck
**Duration:** 45 minutes | **Format:** Pairs (swap roles halfway)

### Objective
Experience the knowledge acquisition bottleneck firsthand, then practice advanced elicitation techniques.

### Role Assignment
- **Person A** = Domain Expert (use your own real work experience)
- **Person B** = Knowledge Engineer (must extract the knowledge)

---

### Round 1 — Bad Interview Technique *(10 mins)*

Knowledge Engineer asks **only** these questions:

1. "What do you do in your job?"
2. "What rules do you follow?"
3. "How do you make decisions?"

**After 10 minutes, discuss:**
- How much useful, specific, actionable knowledge did you get?
- Did the expert feel the questions helped them share real expertise?
- What went wrong?

---

### Round 2 — Good Elicitation Technique *(20 mins)*

Knowledge Engineer uses these five techniques:

| Technique | Example Question |
|---|---|
| **Concrete Case Method** | "Tell me about the last difficult decision you made. Walk me through exactly what you were thinking." |
| **Contrast Questions** | "What made Case A different from Case B? Why X in one but Y in the other?" |
| **Probe the Obvious** | "You said you 'just check' — what exactly do you check? What would make that check fail?" |
| **Edge Cases** | "When does your usual approach NOT work? What is the exception to your rule?" |
| **Confidence Probing** | "How sure are you about this? What would change your mind?" |

**After 20 minutes:** Compare what you learned vs Round 1.

---

### Round 3 — Document & Structure *(15 mins)*

KE Engineer documents findings:

1. **Three explicit IF-THEN rules** discovered
2. **One piece of tacit knowledge** identified — something the expert "just does"
3. **One "it depends" area** — what exactly does it depend on? Make it explicit.
4. **One conflict or uncertainty** in the expert's knowledge

---

### Debrief Questions

1. What was harder — being the expert or the KE engineer?
2. Which elicitation technique worked best?
3. How would you use an LLM to assist in this process?
4. How would you validate what you captured?
