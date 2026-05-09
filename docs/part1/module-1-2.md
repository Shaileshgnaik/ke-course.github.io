# Module 1.2 — Types of Knowledge

---

## Why Types of Knowledge Matter

!!! warning "Before You Engineer Knowledge, You Must Understand What Kind You Are Dealing With"
    Different types of knowledge require different acquisition strategies, different representation methods, and different validation approaches. Getting this wrong wastes months of effort.

---

## The Iceberg Model

```
                    ╔══════════════════════╗
        Above       ║                      ║
        Water   ────║  EXPLICIT KNOWLEDGE  ║ ← Written manuals, documented rules,
                    ║                      ║   databases, SOPs, regulations
                    ╚══════════════════════╝
════════════════════════════════════════════════════════════
             ╔══════════════════════════════════════════╗
      Below  ║                                          ║
      Water  ║           TACIT KNOWLEDGE                ║ ← The hard part
             ║                                          ║
             ║  Intuition, experience, judgment,        ║
             ║  "feel", know-how, pattern recognition   ║
             ╚══════════════════════════════════════════╝
```

> **KE's hardest job:** surfacing what lives below the waterline.

---

## Type 1 — Explicit vs Tacit Knowledge

=== "Explicit Knowledge"
    **Can be articulated, written, and documented.**

    - Blood pressure > 140 mmHg = hypertension
    - AWS Lambda has a 15-minute execution timeout
    - IF credit_score < 650 THEN flag_for_manual_review

    **How to capture:** Document analysis, structured interviews, SOPs
    **How to represent:** IF-THEN rules, ontologies, fact stores

=== "Tacit Knowledge"
    **Difficult to express — learned through years of experience.**

    - A doctor "sensing" something is wrong before test results arrive
    - A network engineer who knows a log "looks suspicious"
    - A chef who knows when the sauce is exactly right

    **How to capture:** Think-aloud protocols, observation, case analysis
    **How to represent:** Case-based reasoning, probabilistic rules, fuzzy logic

!!! danger "The Core KE Challenge"
    Most of an expert's **most valuable** knowledge is tacit. They cannot fully explain it. Your job as a Knowledge Engineer is to surface it.

---

## Type 2 — Declarative vs Procedural Knowledge

| | Declarative | Procedural |
|---|---|---|
| **Meaning** | Knowledge *about* things | Knowledge *how* to do things |
| **Nature** | Facts, concepts, relationships | Steps, processes, methods |
| **Example** | "Diabetes is a chronic disease" | "To diagnose diabetes: 1) check fasting glucose, 2) if >126 repeat, 3) check A1C..." |
| **Representation** | Ontologies, knowledge graphs, facts | Rules, decision trees, workflows |

---

## Type 3 — Shallow vs Deep Knowledge

=== "Shallow Knowledge"
    **Surface-level pattern matching — no understanding of WHY.**

    *"Patients with symptom X usually have disease Y."*

    - Fast to acquire and represent
    - Brittle — breaks on edge cases
    - How most Gen AI operates today

=== "Deep Knowledge"
    **Understanding of underlying causes and mechanisms.**

    *"Bacteria produce toxin Y which disrupts cell membrane Z, causing symptom X."*

    - Slower to acquire — requires real domain expertise
    - Robust — handles novel situations
    - Required for true expert system behaviour

!!! tip "Rule of Thumb"
    If your system must handle edge cases, exceptions, and novel situations — invest in deep knowledge. If it handles routine, predictable scenarios — shallow may suffice.

---

## Type 4 — Certain vs Uncertain Knowledge

```
Certain ──────────────────────────────────────── Uncertain
   │                                                  │
   │  "Water boils at 100°C       "Patient probably  │
   │   at sea level"               has condition X   │
   │   (always true)               (85% likely)"     │
   │                                                  │
Absolute              Probabilistic             Fuzzy
IF-THEN rules         Bayesian networks         Fuzzy logic
Logical axioms        Certainty factors         Membership functions
```

---

## The Knowledge Pyramid

```
                    ▲
                   /W\        WISDOM
                  /   \       "Knowing what matters"
                 /─────\
                / E x p \     EXPERTISE
               / e r t i \    "Applying knowledge in context"
              /───────────\
             / K n o w l e \  KNOWLEDGE
            / d g e         \ "Understanding relationships"
           /─────────────────\
          / I n f o r m a t i \ INFORMATION
         / o n                 \"Making sense of data"
        /─────────────────────── \
       /   D a t a                \ DATA
      /   "Raw facts & numbers"    \
     ▼─────────────────────────────▼

KE operates at the Knowledge → Expertise level
```

---

## Practical Classification Exercise

Try classifying these statements from a Cloud Architect:

| Statement | Explicit/Tacit | Declarative/Procedural | Certain/Uncertain |
|---|---|---|---|
| "Azure Service Bus max message size is 256KB" | Explicit | Declarative | Certain |
| "I can tell a poorly designed microservice from how the team describes it" | Tacit | Declarative | Uncertain |
| "To set up CI/CD: configure pipeline, add stages, add approval gates" | Explicit | Procedural | Certain |
| "This architecture will probably have latency issues under load" | Tacit | Declarative | Uncertain |
| "Azure is usually better for .NET workloads than AWS" | Explicit | Declarative | Uncertain |

---

## Key Takeaways

- [x] Explicit knowledge is easy to capture; **tacit knowledge is harder but most valuable**
- [x] Declarative = **WHAT** things are · Procedural = **HOW** to do things
- [x] Deep knowledge is more powerful than shallow — but harder to engineer
- [x] Real-world expertise is rarely certain — KE must handle **uncertainty**
- [x] KE converts Data → Information → Knowledge → Expertise

---

## What's Next

[Module 1.3 — The KE Lifecycle →](module-1-3.md){ .md-button .md-button--primary }

---

*Ready to test yourself? → [Module 1.2 Quiz](assessment.md#module-12-quiz)*
*Hands-on practice? → [Lab 1.2](labs.md#lab-12)*
