# Part 2 — Hands-On Labs

---

## Lab 2.1 — The Elicitation Challenge {#lab-21}

**Module:** 2.1 — Knowledge Elicitation Techniques
**Duration:** 50 minutes | **Format:** Pairs

### Objective
Practice 3 elicitation techniques back-to-back and compare the quality of knowledge extracted by each.

### Setup
- Person A = Domain Expert (use your real work experience)
- Person B = Knowledge Engineer

---

### Round 1 — Structured Interview *(15 mins)*

Use only these question types:

1. *"What is the most common decision you make in your domain?"*
2. *"Walk me through a recent example of that decision."*
3. *"What factors do you consider? List them in priority order."*
4. *"What would make you decide differently?"*

After 15 minutes, write down: How many concrete IF-THEN rules could you extract?

---

### Round 2 — Think-Aloud *(15 mins)*

Give the expert a real task from their domain (e.g. review an architecture diagram, diagnose a problem, evaluate an option).

Expert narrates their thinking in real time while working. KE records key observations.

After 15 minutes, write down: How many rules emerged that DIDN'T come up in Round 1?

---

### Round 3 — Laddering *(10 mins)*

Take the most interesting rule from Round 1 or 2. Apply the Why/How ladder:

```
Start: "You said you [X] in this situation."
→ "Why do you do X rather than Y?"
→ "Why is that important?"
→ "How do you know when to stop doing X?"
→ "What would be the exception to this?"
```

---

### Debrief *(10 mins)*

| Question | Your Answer |
|---|---|
| Which technique gave the richest rules? | |
| Which technique surfaced tacit knowledge? | |
| What would you have missed with interviews alone? | |
| What follow-up sessions would you plan? | |

---

## Lab 2.2 — Extract Rules from a Document {#lab-22}

**Module:** 2.2 — Document & Text Mining
**Duration:** 40 minutes | **Format:** Individual

### Objective
Manually apply the document mining pipeline to a real text and extract structured rules.

### Input Document

Read this excerpt from a fictional cloud architecture guideline:

---

*"When designing a new microservices architecture, teams should always implement an API gateway as the single entry point for external traffic. The gateway must enforce authentication and rate limiting before requests reach any downstream service.*

*For database selection: if the application requires ACID transactions and data relationships are complex, use a relational database such as Azure SQL or AWS RDS. If the primary access pattern is key-value lookups with throughput exceeding 10,000 requests per second, DynamoDB or Cosmos DB should be preferred.*

*All services must implement health check endpoints. If a service fails three consecutive health checks, it should be automatically removed from the load balancer pool. Services should never be deployed to production without passing the full integration test suite.*

*For cost optimisation: when a workload runs for less than 15 minutes and is triggered by events, Lambda or Azure Functions is preferred over container-based solutions. Long-running batch processes exceeding 15 minutes should use Fargate or Azure Container Instances instead."*

---

### Task 1 — Identify Linguistic Markers *(10 mins)*

Highlight every word that signals a rule:
- Obligation: `must`, `should`, `always`, `never`, `required`
- Condition: `if`, `when`, `exceeds`, `fails`
- Action: `use`, `implement`, `deploy`, `prefer`

---

### Task 2 — Extract Rules *(20 mins)*

Convert each identified rule into structured format:

```
Rule R[n]:
Type: [HARD / SOFT / CONSTRAINT / BEST_PRACTICE]
IF:   [conditions]
THEN: [action or recommendation]
Source: "[exact quote from document]"
Confidence: [HIGH / MEDIUM / LOW]
```

How many rules can you extract from the passage?

---

### Task 3 — Validate *(10 mins)*

Review your rules and answer:

1. Which rules might be outdated in today's cloud landscape?
2. Which rules are too vague to be useful as written?
3. What follow-up questions would you ask an expert?

??? success "Sample Answer — Expected Rules"
    R1: IF traffic_type = external THEN implement API_gateway (HARD)
    R2: IF api_gateway THEN enforce auth + rate_limiting (HARD)
    R3: IF ACID_required AND complex_relations THEN use relational_DB (SOFT)
    R4: IF access_pattern = key-value AND throughput > 10000_rps THEN prefer DynamoDB/CosmosDB (SOFT)
    R5: ALL services MUST implement health_check (HARD)
    R6: IF health_checks_failed >= 3 THEN remove from load_balancer (HARD)
    R7: NEVER deploy to production WITHOUT integration_tests_passed (CONSTRAINT)
    R8: IF duration < 15min AND trigger = event THEN prefer Lambda/Functions (SOFT)
    R9: IF batch = true AND duration > 15min THEN use Fargate/ACI (SOFT)

---

## Lab 2.3 — Decision Tree Rule Discovery {#lab-23}

**Module:** 2.3 — ML for Knowledge Acquisition
**Duration:** 45 minutes | **Format:** Individual

### Objective
Build a simple decision tree from historical data and extract readable rules.

### Dataset

You have 12 historical cloud storage decisions from an architect:

| Data Type | Transactions | Global | Throughput | Expert Chose |
|---|---|---|---|---|
| Structured | Yes | No | Low | Azure SQL |
| Unstructured | No | No | Medium | Azure Blob |
| Key-Value | No | Yes | High | Cosmos DB |
| Structured | Yes | Yes | Medium | Cosmos DB |
| Unstructured | No | No | Low | Azure Blob |
| Key-Value | No | No | High | DynamoDB |
| Structured | No | No | Low | PostgreSQL |
| Key-Value | No | Yes | Very High | DynamoDB |
| Structured | Yes | No | High | Azure SQL |
| Unstructured | No | Yes | High | S3 |
| Key-Value | No | No | Low | Redis |
| Structured | No | Yes | Medium | Cosmos DB |

---

### Task 1 — Build the Decision Tree Manually *(20 mins)*

Draw a decision tree that correctly classifies all 12 decisions.

Start with: *"What is the first question that best splits the data?"*

Hint: Start with **Data Type** as the root split.

---

### Task 2 — Extract Rules *(15 mins)*

Convert each leaf of your tree into an IF-THEN rule:

```
Rule R[n]:
IF   data_type = [X]
     AND [other conditions]
THEN recommend = [service]
```

---

### Task 3 — Identify Gaps *(10 mins)*

1. What scenarios does your tree NOT cover?
2. What questions would you ask the expert to cover those gaps?
3. Are there any rules in your tree that seem surprising? Why?

---

## Lab 2.4 — LLM Knowledge Extraction {#lab-24}

**Module:** 2.4 — Knowledge Acquisition from LLMs
**Duration:** 40 minutes | **Format:** Individual

### Objective
Design effective prompts for LLM-based knowledge extraction and evaluate the outputs critically.

### Task 1 — Design an Extraction Prompt *(15 mins)*

You need to extract knowledge from a 50-page architecture best practices guide.

Write a complete LLM prompt that:
- Instructs the LLM to extract IF-THEN rules
- Requires source citation for every rule
- Asks for confidence rating
- Handles uncertainty explicitly

Use the template from Module 2.4 as a starting point, but customise it for a **cloud architecture** domain.

---

### Task 2 — Evaluate Sample LLM Output *(15 mins)*

Review this LLM-generated rule and identify any problems:

```
Rule R_CLOUD_47:
Type: HARD_RULE
IF:   application handles sensitive healthcare data
THEN: must use HIPAA-compliant cloud services
      and encrypt all data at rest and in transit
Source: [Unable to find specific source — general best practice]
Confidence: HIGH
```

Answer:
1. What is wrong with the Confidence rating here?
2. What is wrong with the Source field?
3. How would you handle this rule before adding it to the KB?
4. What question would you ask a domain expert about this rule?

---

### Task 3 — Gap Analysis Prompt *(10 mins)*

Write a prompt that asks an LLM to analyse this partial rule set and identify gaps:

```
Existing rules:
R1: IF workload = event-driven AND volume = high THEN use Service Bus
R2: IF workload = request-reply AND latency < 100ms THEN use REST
R3: IF batch = true AND size = large THEN use Storage Queue
```

Your prompt should ask the LLM to find: missing scenarios, potential conflicts, and questions for the domain expert.

---

## Lab 2.5 — Design a Full Acquisition Plan {#lab-25}

**Module:** 2.5 — Human-AI Collaborative Acquisition
**Duration:** 60 minutes | **Format:** Team (2–3 people)

### Objective
Design a complete knowledge acquisition plan for a real scenario using the full Human-AI pipeline.

### Scenario

Your company wants to build a KE system that automates cloud architecture recommendations for a professional services firm. You have access to:

- 200 past architecture documents (Word/PDF)
- 3 senior architects (available for max 4 hours total)
- 500 historical architecture decisions in a spreadsheet
- 2 junior architects who can help with validation

**Constraints:**
- Must be complete in 3 weeks
- Cannot use more than 4 hours of senior architect time
- Target: 100+ validated rules in the KB

---

### Deliverable: Complete Acquisition Plan

Fill in each phase:

**Phase 1 — Document Mining**

| Item | Your Answer |
|---|---|
| What documents to process first (prioritise)? | |
| What LLM prompt will you use? | |
| Expected rule yield? | |
| Who does this work? | |
| Timeline? | |

**Phase 2 — Gap Analysis**

| Item | Your Answer |
|---|---|
| How will you identify gaps? | |
| What are the likely gaps in architecture docs? | |
| How long will expert review of gaps take? | |

**Phase 3 — Targeted Expert Sessions**

| Item | Your Answer |
|---|---|
| How many sessions? (remember: 4 hour total limit) | |
| Which technique for each session? | |
| What topics will each session cover? | |

**Phase 4 — ML Validation**

| Item | Your Answer |
|---|---|
| What ML technique will you use on the 500 decisions? | |
| What will you do with discrepancies found? | |

**Phase 5 — Expert Review**

| Item | Your Answer |
|---|---|
| Who reviews (junior or senior architects)? | |
| How many rules do you expect to validate? | |
| What are your accept/reject criteria? | |

**Present your plan (5 minutes). Highlight: biggest risk, key assumption, first milestone.**
