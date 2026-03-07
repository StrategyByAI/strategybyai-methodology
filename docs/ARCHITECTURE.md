# Technical Architecture

## How Strategy by AI Works: Seven Perspectives

This document explains the methodology's technical operation from seven perspectives, each addressing a different architectural question. Together they provide complete understanding of how structured context methodology produces professional strategic intelligence.

---

## Perspective 1: Prompt + Module Section + Profiling → Output

Every intelligence document is produced by the interaction of three input components:

### Component A: Module Section

The relevant section of the methodology module provides the **analytical framework** — definitions, taxonomies, evaluation criteria, historical models for comparison, and structural requirements for the output.

Example: Module Three, Section 3.2 (Classification of Foes) provides:
- Four-status taxonomy: alien, rival, adversary, enemy
- Criteria distinguishing each status based on confrontation character
- Escalation trajectory indicators (ascending, stable, descending)
- Resource allocation ranges per threat level

### Component B: Workflow Prompt

The prompt from the module-specific workflow library provides the **specific instruction** — what to analyse, in what structure, with what evidence requirements, at what depth, and in what sequence.

Example: The Enemy Classification prompt specifies:
- Minimum entity count (20–30 significant actors)
- Classification depth per status level (enemies: 7–10 sentences; adversaries: 5–7; rivals: 5–6; aliens: 4–5)
- Evidence citation requirements (source, date, confidence level)
- Trajectory assessment and mutation timeline projection

### Component C: Audience Profiling

The audience profile calibrates the **analytical perspective** — whether the assessment is conducted as an internal expert with organisational access or an external investigator working from public information.

Example: External Investigator profiling specifies:
- OSINT-only evidence base (corporate filings, financial reports, industry research, trade press)
- Explicit acknowledgment of information gaps where insider data would improve assessment
- Confidence level assignments reflecting public-information limitations
- Recommendations for further intelligence collection

### How they combine

```
Module Section (Framework)
         +
Workflow Prompt (Instruction)  →  Intelligence Document
         +
Audience Profile (Perspective)
```

The module section tells the AI HOW to think about the problem. The prompt tells it WHAT to produce. The profile tells it FROM WHOSE PERSPECTIVE. None alone produces a professional output — the combination does.

→ [Annotated example](../examples/prompt-module-interaction/)

---

## Perspective 2: Module Chain — Output Feeds Input

The methodology operates as a sequential dependency chain where each module's output becomes the next module's input.

### The chain

```
Module Two          Module Three         Module Four          Module Five          Module Six
(Identity)    →     (Enemy)        →     (Situation)    →     (Strategy)     →     (Execution)
                                                                                       ↓
Docs 1–4            Docs 5–13           Docs 14–20           Docs 21–24          Docs 25–34
                                                                                       ↓
                                                                              References ALL
                                                                              Docs 1–24
```

### Specific feed points

**Identity → Enemy:**
Document 4 (Strategic Identity Profile) establishes mission-based enemy criteria. Document 5 (Hostile Environment Assessment) uses these criteria to classify entities: "Lab-grown producers classified as ENEMIES because their success makes De Beers' mission impossible." Without Document 4's mission definition, Document 5 cannot distinguish enemies from adversaries.

**Enemy → Situation:**
Document 8 (Resource Allocation Audit) calculates capacity requirements per enemy. Document 19 (Strategic Situation Assessment) incorporates this calculation into the overall situation reading. The finding "160–200% capacity required against 100% available" comes from Module Three but defines the Module Four situation.

**Situation → Strategy:**
Document 18 (Strategic Vectors) identifies the ultra-luxury segment as 60% favourable despite 65% overall unfavourable environment. Document 21 (War Definition) uses this finding to define the bounded war: concentrate on the 15% ultra-luxury market segment where competitive physics favour the organisation.

**Strategy → Execution:**
Document 24 (Strategy Integration) specifies four adjustment triggers and settlement conditions. Document 34 (Execution Synthesis) evaluates whether these triggers were activated and whether settlement orientation was maintained.

→ [Step-by-step chain demonstration](../examples/module-chain/)

---

## Perspective 3: Cross-Verification Between Documents

Documents produced at different stages create a self-auditing network where findings verify (or contradict) each other.

### Verification pathways

```
Doc 4 (Identity)  ──predicts gaps──→  Doc 8 (Resources)  ──quantifies gaps──→  Doc 22 (Objectives)
       │                                     │                                        │
       │                                     │                                        │
       └─── If Doc 8 contradicts             └─── If Doc 22 ignores                  │
            Doc 4, analyst                        Doc 8 constraints,                   │
            returns to verify                     strategy is unrealistic               │
                                                                                       │
Doc 25 (Preparation) ←──measures whether gaps were addressed──────────────────────────┘
```

### How contradictions surface

If Document 4 identifies "retail capability gap" as critical but Document 8 shows minimal resource allocation to retail capability development, this contradiction is visible across the portfolio. The analyst investigates: either Document 4 overestimated the gap, or the organisation is underinvesting in a critical capability.

This cross-verification is not manual — it is structural. Because each document references preceding outputs, inconsistencies propagate visibly rather than remaining hidden in separate analysis silos.

### Example from De Beers assessment

- Document 4 diagnosed mission-history-doctrine incoherence
- Document 8 quantified the resource misallocation (60% to Anglo American vs 15% recommended)
- Document 19 classified the situation as late Shaping/early Clash transition
- Document 21 bounded the war to ultra-luxury segment based on vector analysis
- Document 25 measured preparation: 42% resource extraction gap
- Document 34 synthesised: the identity incoherence diagnosed in Document 4 manifested as the command absence graded in Document 26, which produced the zero execution graded in Document 34

Each finding is traceable backward through the chain. Each can be challenged at its source.

→ [Cross-verification examples](../examples/cross-verification/)

---

## Perspective 4: Human Verification Protocol

The methodology is not a black box. Human verification is a structural requirement at module boundaries.

### The verification cycle

```
AI produces document → Human reviews → Human verifies → Corrections fed back → Verified document
                                                                                      ↓
                                                                            Becomes input for
                                                                             next module
```

### What the human verifies

**Evidence accuracy:** Are the OSINT sources current? Are citations verifiable? Has the AI fabricated sources?

**Classification consistency:** Do enemy classifications match industry knowledge? Has the AI over- or under-classified entities?

**Completeness:** Are there entities missing from the hostile environment? Are there factors absent from the situation assessment?

**Internal coherence:** Do findings across sections contradict each other? Does the identity assessment in Section A align with the capability assessment in Section B?

### What the human does NOT do

The human does not replicate the AI's analysis. The AI's value is in processing hundreds of pages of framework, cross-referencing dozens of entities, and maintaining consistency across the entire portfolio. The human's value is in judgement: knowing when the AI's classification is wrong because it missed context that isn't in the public data, or when a finding is technically correct but strategically irrelevant.

→ [Verification protocol example](../examples/human-verification/)

---

## Perspective 5: Tier-Structured AI-Human Responsibility

Module Six distributes decision authority between AI and human across three tiers.

### The tier system

| Tier | Authority | Scope | AI role | Human role |
|------|-----------|-------|---------|------------|
| **1** | Human only | War-level decisions: strategy change, settlement, fundamental transformation | Analyses situation, activates documents, presents options with evidence | Decides |
| **2** | Shared | Operational decisions: campaign resource reallocation, objective priority adjustment | Proposes changes with document-grounded justification | Approves, modifies, or rejects |
| **3** | AI-guided | Tactical decisions: campaign-internal adjustments within allocated parameters | Executes within pre-established constraints, monitors outcomes | Oversees, intervenes when parameters breached |

### How tiers prevent two failure modes

**Failure mode 1 — AI overreach:** Without tier structure, an AI assistant might recommend strategy changes (Tier 1 decisions) with the same confidence it recommends tactical adjustments (Tier 3). The tier system forces the AI to classify each decision before acting: "This requires Tier 1 authority. I can provide analysis and options, but the human operator must decide."

**Failure mode 2 — Human bottleneck:** Without tier structure, every decision requires human approval, creating paralysis under pressure. Tier 3 delegation allows the AI to execute tactical adjustments within pre-established parameters without waiting for approval — essential during high-tempo execution when response time matters.

### De Beers example

- **Tier 1:** Whether to pursue strategic buyer acquisition (LVMH, Richemont) versus financial buyer — fundamental war-level decision changing the entire strategy's viability
- **Tier 2:** Reallocating resources between Brand Transformation campaign (25–30%) and Distribution Optimisation campaign (35–40%) based on early results
- **Tier 3:** Adjusting counter-narrative messaging within the allocated 10–15% capacity budget in response to a specific LGD sustainability claim

→ [Tier responsibility demonstration](../examples/tier-responsibility/)

---

## Perspective 6: Document Activation Protocols

Module Six does not reference preceding documents generically. It activates them through prescribed protocols specifying WHICH documents, WHICH sections, and WHAT questions to ask.

### Protocol structure

Each execution challenge triggers a specific activation:

```
Execution Issue          → Prescribed Documents     → Specific Questions
─────────────────────────────────────────────────────────────────────
Command structure        → Docs 21, 22, 23, 24, 25  → "Does decision authority
adequacy                                               exist for each tier?"

Friction management      → Docs 2, 8, 16, 23        → "What friction sources
capacity                                               does history predict?"

Culmination prediction   → Docs 8, 23, 24           → "When does resource
                                                       trajectory cross the
                                                       exhaustion threshold?"
```

### Document 34's Activation Registry

The final synthesis document (Document 34) includes a complete Activation Registry documenting every protocol executed across Documents 25–33: which documents were activated, what was found, and how findings contributed to the verdict.

In the De Beers assessment, 20+ protocols were executed. Each produced specific findings citing specific documents with specific evidence. The F-grade verdict is not a subjective judgement — it is the output of 20+ document-grounded assessments, each traceable to its activation protocol.

→ [Activation registry excerpt](../examples/document-activation/)

---

## Perspective 7: Quality Gates Between Modules

The methodology prevents proceeding on insufficient analytical foundations.

### How quality gates work

Each module's concluding document includes a **readiness assessment** for subsequent modules. This assessment rates whether the current module's output provides sufficient foundation for the next stage.

### Example from De Beers assessment

Document 4 (Strategic Identity Profile) concluded:

| Next module | Readiness | Rationale |
|-------------|-----------|-----------|
| Module Three (Enemy-Making) | **MODERATE** | Can proceed with provisional classification |
| Module Four (Situation) | **WEAK** | Can proceed with doctrine gap acknowledged |
| Module Five (Strategy Formulation) | **CRITICAL WEAKNESS** | Requires identity integration |

The assessment did not stop at Module Two — it proceeded with explicit acknowledgment of the identity gap, treating Module Three classifications as provisional pending ownership transition resolution.

### Why this matters technically

Without quality gates, a flawed Module Two output (incorrect mission definition) would propagate through the entire portfolio: wrong enemies classified, wrong situation assessed, wrong strategy formulated, wrong execution graded. The quality gate forces the analyst to acknowledge foundation weaknesses before building on them.

For AI agent implementations, quality gates translate directly to workflow checkpoints: the agent assesses output quality against prescribed criteria before triggering the next module's workflow.

---

## Summary: The Complete Technical Flow

```
Input: Subject Organisation + Public/Proprietary Data
  │
  ▼
Module Two ──→ Docs 1–4 ──→ Quality Gate ──→ Human Verification
  │                                                    │
  ▼                                                    ▼
Module Three ──→ Docs 5–13 ──→ Quality Gate ──→ Human Verification
  │                                                    │
  ▼                                                    ▼
Module Four ──→ Docs 14–20 ──→ Quality Gate ──→ Human Verification
  │                                                    │
  ▼                                                    ▼
Module Five ──→ Docs 21–24 ──→ Quality Gate ──→ Human Verification
  │                                                    │
  ▼                                                    ▼
Module Six ──→ Docs 25–34 ──→ Document Activation Protocols
  │                                  │
  ▼                                  ▼
Execution Governance         Final Verdict (Doc 34)
(Tier 1/2/3 authority)       with Activation Registry
```

→ [Problem analysis](PROBLEM.md) | [Demonstrated results](DEMONSTRATION.md) | [Integration guides](INTEGRATION.md)
