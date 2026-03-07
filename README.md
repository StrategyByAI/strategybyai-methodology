# Strategy by AI

**A structured methodology that transforms AI assistants into strategic analysts capable of formulating and governing strategy — not just advising.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## The Problem

Current AI strategy tools automate the monitoring of strategies made before AI entered the picture. They digitise goal tracking, OKR management, and performance dashboards — automating existing processes rather than generating new strategic patterns that exploit AI's unique capabilities.

Three structural failures define the current state of AI strategic practice:

1. **Automation without innovation** — AI tracks strategies humans already made. It does not formulate new strategies using its accumulated knowledge across thousands of historical cases and its capacity to cross-reference hundreds of variables simultaneously.

2. **Advisory without governance** — AI analyses and recommends. It does not co-govern execution. The gap between AI recommendation and organisational action is where most strategies die.

3. **Monitoring without formulation** — AI is strongest at endpoints (data gathering, performance dashboards) and weakest in the middle: the intellectual work of defining wars, setting objectives, designing campaigns, selecting targets, and allocating resources.

→ [Full analysis of these failures](docs/PROBLEM.md)

---

## What Strategy by AI Does

Strategy by AI is a structured context methodology derived from general and military strategic science, adapted for business and political competition. It transforms any Large Language Model into a strategic analyst that performs the complete strategic cycle — not just the parts current tools handle.

### Six Integrated Modules

| Module | Function | Output |
|--------|----------|--------|
| **One** | Strategic foundation | Conceptual preparation for human operators |
| **Two** | Identity analysis | 4 documents: mission, history, doctrine, identity profile |
| **Three** | Enemy classification | 9 documents: hostile environment, foe matrix, hierarchy, profiles, scenarios |
| **Four** | Situation assessment | 7 documents: scene configuration, actors, threats, trends, vectors, power poles |
| **Five** | Strategy formulation | 4 documents: war definition, objectives, campaigns, integration |
| **Six** | Execution governance | 10 documents: commitment, command, cohesion, tempo, friction, centre of gravity, culmination, fog/chaos, adaptation, termination + synthesis |

**34 cross-referenced documents.** Each references preceding outputs. Each contains auditable evidence chains. Each is verifiable by human operators.

→ [Technical architecture](docs/ARCHITECTURE.md)

---

## Demonstrated Results: De Beers UK

Complete 34-document strategic assessment of De Beers UK Limited, produced by a single AI assistant using the Strategy by AI methodology from publicly available information.

**Key findings:**
- **28 hostile entities** classified across four threat levels (alien → rival → adversary → enemy)
- **4 existential enemies** identified, requiring 160–200% organisational capacity against 100% available
- **5 coordinated campaigns** designed: $565–775M over 60 months
- **9 strategic targets** identified and prioritised with accessibility, criticality, and offence-defence assessment
- **Execution grade: F** — six of seven dimensions rated Deficient; zero campaigns launched; zero targets engaged; $245–375M consumed for zero strategic return

The assessment diagnosed a paradox conventional analysis does not produce: sophisticated documentary strategy coexisting with near-zero operational execution. The methodology identified the root cause (command structure absence), predicted culmination timing (capability peak 15 months before decisive engagement), and calculated that without a strategic buyer extending the capability timeline, the mathematics produce fatal culmination-centre misalignment.

→ [Case study evidence with selected document excerpts](docs/DEMONSTRATION.md)

---

## How It Works Technically

### Seven Architectural Perspectives

| # | Perspective | What it demonstrates |
|---|-------------|---------------------|
| 1 | [Prompt + Module + Profiling → Output](examples/prompt-module-interaction/) | How three input components produce a specific intelligence document |
| 2 | [Module Chain](examples/module-chain/) | How each module's output feeds the next module's input |
| 3 | [Cross-Verification](examples/cross-verification/) | How documents from different stages verify each other |
| 4 | [Human Verification](examples/human-verification/) | How the human operator validates AI output between modules |
| 5 | [Tier Responsibility](examples/tier-responsibility/) | How AI-human decision authority is distributed in Module Six |
| 6 | [Document Activation](examples/document-activation/) | How Module Six systematically activates all preceding documents |
| 7 | Quality Gates | How readiness assessments prevent proceeding on insufficient foundations |

→ [Full technical architecture](docs/ARCHITECTURE.md)

---

## Implementation Pathways

Strategy by AI works with any LLM with sufficient context window — Claude, ChatGPT, Gemini, DeepSeek, and others. Four deployment levels:

| Level | Method | Technical requirement |
|-------|--------|---------------------|
| **Basic** | Direct context window upload | Any LLM chat interface |
| **Intermediate** | RAG integration | Vector database + retrieval pipeline |
| **Advanced** | Fine-tuning | Training infrastructure + evaluation framework |
| **Enterprise** | Agentic deployment | Multi-agent orchestration platform |

→ [Integration guides](docs/INTEGRATION.md)

---

## Strategy World Models

Current world models (DeepMind Genie 3, NVIDIA Cosmos, Meta V-JEPA 2) focus on physical environments — gravity, inertia, spatial dynamics. An undeveloped parallel domain exists: **strategic world models** — internal models of how competitive environments behave.

Strategy by AI provides the architectural foundation:

- **State representation** — The 34-document portfolio encodes complete strategic world state across five dimensions (identity, hostile environment, situation, strategy, execution)
- **Transition dynamics** — Module chains define explicit rules governing how one state produces the next
- **Action prediction** — Campaign architectures specify actions; execution assessment predicts consequences
- **Counterfactual reasoning** — Scenario modelling and settlement conditions enable "what if" simulation
- **Consistency enforcement** — Cross-referencing creates a constraint network preventing the hallucination and drift that plague standalone LLM reasoning

→ [Strategy world models: concept, architecture, implementation path](world-models/)

---

## Repository Contents

```
strategybyai-methodology/
├── docs/
│   ├── PROBLEM.md           # What's wrong with AI strategy today
│   ├── ARCHITECTURE.md      # Technical architecture (7 perspectives)
│   ├── DEMONSTRATION.md     # De Beers case — selected evidence
│   └── INTEGRATION.md       # Four implementation pathways
├── examples/                # Working demonstrations with De Beers excerpts
├── integration/             # Platform-specific deployment guides
├── world-models/            # Strategic world model concept and prototype
├── assets/                  # Diagrams and reference tables
└── LICENSE.md
```

**What is NOT in this repository:** The core methodology (module files, full prompt libraries, full workflows, audience profiling documents). These are available at [strategybyai.org](https://strategybyai.org).

This repository demonstrates *what* the methodology does and *how* it works technically. The methodology itself — the reasoning framework that produces these results — is the commercial product.

---

## Get the Methodology

**[strategybyai.org](https://strategybyai.org)** — one-time purchase, permanent ownership, any LLM platform. No subscription. No proprietary infrastructure. No consulting dependency.

---

## Resources

- **Website:** [strategybyai.org](https://strategybyai.org)
- **YouTube:** [Strategy by AI Channel](https://youtube.com/@strategybyai) — methodology demonstrations
- **LinkedIn:** [StrategyByAI](https://linkedin.com/company/strategybyai)
- **Blog:** [strategybyai.org/blog](https://strategybyai.org/blog/) — methodology philosophy
- **Author:** [Vladimir Shirogorov](https://linkedin.com/in/vladimir-shirogorov-135ba8215/)

---

## License

Repository documentation is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). You may share and adapt this material for non-commercial purposes with attribution.

The Strategy by AI methodology itself (not contained in this repository) is separately licensed. See [strategybyai.org](https://strategybyai.org) for methodology licensing terms.
