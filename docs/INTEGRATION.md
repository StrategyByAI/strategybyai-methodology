# Integration Guides

## Four Implementation Pathways

Strategy by AI scales from basic chat interface upload to enterprise agentic deployment. Each pathway uses the identical core methodology — technical sophistication adds automation and speed, not fundamental capability.

---

## Pathway 1: Basic — Direct Context Window Upload

**Technical requirement:** Any LLM chat interface (Claude, ChatGPT, Gemini, DeepSeek)
**Setup time:** Minutes
**Who this is for:** Individual strategists, small teams, first-time users

### How it works

1. Create a dedicated workspace (Claude Project, ChatGPT conversation, or equivalent)
2. Upload the relevant module file (plain UTF-8 text)
3. Specify the subject organisation
4. Follow the module's workflow prompts sequentially
5. Review and verify each output document before proceeding to the next module

### Platform-specific notes

**Claude (recommended for largest context):**
- Use Projects feature — upload module files to project knowledge base
- Module files persist across conversations within the project
- Start new conversations within the same project for each module to manage context

**ChatGPT:**
- Upload module files as attachments or to the conversation
- For GPT-4 and later: sufficient context window for single-module operation
- For multi-module work: upload preceding document outputs alongside the new module

**Gemini:**
- Upload module files directly to conversation
- Extended context window handles large modules effectively
- Export completed documents for upload into subsequent module sessions

### Context window management

Each module is a substantial text file (hundreds of pages). Strategies for managing context:

- **Single-module sessions:** Upload one module per session. When moving to the next module, start a new session with the new module plus the output documents from the previous module.
- **Document accumulation:** As the portfolio grows (34 documents by completion), upload only the documents the current module explicitly references — not the entire portfolio. The module sections specify which preceding documents are required.
- **Summary bridging:** For platforms with smaller context windows, summarise preceding document findings into a structured brief that carries forward the essential data without the full document text.

### Quality assurance

At basic level, human verification between modules is manual: the operator reads each document, checks evidence citations, validates classifications, and corrects errors before proceeding. This is the methodology's minimum quality requirement — no pathway eliminates it.

---

## Pathway 2: Intermediate — RAG Integration

**Technical requirement:** Vector database + retrieval pipeline + LLM API access
**Setup time:** Days to weeks
**Who this is for:** Organisations with existing document management systems, AI development teams

### Architecture

```
┌─────────────────────────────────────────────┐
│              Vector Database                 │
│                                              │
│  Methodology chunks    Org knowledge base    │
│  (modules, sections,   (internal docs,       │
│   prompt libraries)     financial data,      │
│                         market research)     │
└──────────────┬──────────────────┬────────────┘
               │                  │
               ▼                  ▼
        ┌──────────────────────────────┐
        │      Retrieval Pipeline       │
        │                              │
        │  Query routing: which module  │
        │  sections for which task?     │
        │                              │
        │  Context assembly: methodology│
        │  + org data + preceding docs  │
        └──────────────┬───────────────┘
                       │
                       ▼
                ┌──────────────┐
                │   LLM API    │
                │              │
                │  Structured  │
                │  generation  │
                └──────────────┘
```

### Chunking strategy

The methodology's modular structure maps naturally to RAG chunks:

**Level 1 — Module level:** Each module is a top-level retrieval unit. Query routing determines which module(s) are relevant to the current task.

**Level 2 — Section level:** Each numbered section within a module (e.g., 3.2 Classification of Foes, 5.9 Configuration of the War) is an independent retrieval unit. This is the primary chunking level — sections are self-contained analytical frameworks with clear boundaries.

**Level 3 — Subsection level:** For fine-grained retrieval, subsections (e.g., 3.2.4 Enemy definition, 6.4.1.2 Decision authority) provide specific definitions, criteria, or protocols.

### Metadata schema

Each chunk should carry metadata enabling intelligent retrieval:

```json
{
  "module": 3,
  "section": "3.2",
  "title": "Classification of Foes",
  "type": "framework",
  "outputs": ["Document 5", "Document 6"],
  "inputs_from": ["Document 1", "Document 2", "Document 3", "Document 4"],
  "concepts": ["alien", "rival", "adversary", "enemy", "confrontation character"],
  "audience_profiles": ["internal_expert", "external_investigator"]
}
```

### Query routing logic

```
User query: "Classify competitors for [Organisation X]"

Route to:
  1. Module Three, Section 3.2 (classification framework)
  2. Module Three workflow prompt (enemy classification)
  3. Audience profile (internal/external)
  4. Documents 1–4 from Module Two (if already produced)
  
Assemble context → Generate Document 5
```

### Integration with organisational knowledge bases

The RAG architecture enables combining methodology retrieval with organisational data retrieval in the same context assembly:

- Methodology chunks provide the analytical framework
- Organisational documents provide the subject-specific data
- The LLM applies the framework to the data, producing the intelligence document

This eliminates the manual upload step of basic implementation while maintaining the same analytical rigour.

---

## Pathway 3: Advanced — Fine-Tuning

**Technical requirement:** Training infrastructure + evaluation framework + base model access
**Setup time:** Weeks to months
**Who this is for:** Organisations developing specialised strategic AI systems

### Training dataset structure

The methodology provides three categories of fine-tuning material:

**Category A — Concept definitions (200+ entries)**

```
Input:  "Define strategic enemy versus adversary"
Output: "An enemy is an entity whose fundamental business model or
         strategic objectives require your elimination, displacement,
         or radical transformation. An adversary contests peripheral
         assets but their success does not require your destruction.
         The distinction determines resource allocation: enemies
         require 40–50% capacity; adversaries require 25–35%."
```

**Category B — Analytical reasoning chains (100+ case studies)**

```
Input:  "Apply enemy classification to Netflix versus Blockbuster (2007)"
Output: [Structured classification with evidence, trajectory assessment,
         capacity calculation, following Module Three framework]
```

**Category C — Document generation examples (34 document templates)**

```
Input:  "Generate Strategic Identity Intelligence Profile for [Organisation]
         following Module Two Section 2.7 framework"
Output: [Complete document following prescribed structure with
         mission-history-doctrine integration, coherence matrix,
         readiness assessment, handoff certification]
```

### Evaluation benchmarks

Fine-tuned models should be evaluated against:

- **Classification accuracy:** Does the model correctly distinguish aliens/rivals/adversaries/enemies when given entity descriptions?
- **Structural compliance:** Does the model produce documents following the prescribed structure (sections, subsections, required elements)?
- **Cross-reference consistency:** Do outputs from different modules remain internally consistent?
- **Evidence discipline:** Does the model cite sources, assign confidence levels, and acknowledge gaps?
- **Reasoning chain completeness:** Can each conclusion be traced back through the analytical chain?

### Domain adaptation

The methodology is domain-agnostic — its frameworks apply to business, political, and military contexts. Fine-tuning enables domain specialisation:

- **Financial services:** Emphasis on regulatory environment analysis, market dynamics, and competitive intelligence specific to financial markets
- **Healthcare:** Emphasis on regulatory and policy environment, stakeholder complexity, and long-cycle strategic planning
- **Technology:** Emphasis on technology curve dynamics, platform competition, and rapid-cycle strategic adaptation
- **Political:** Emphasis on electoral dynamics, coalition formation, and public opinion as strategic terrain

Each domain adaptation uses the same core methodology with domain-specific examples and calibration in the training data.

---

## Pathway 4: Enterprise — Agentic Deployment

**Technical requirement:** Multi-agent orchestration platform + tool access + human-in-the-loop infrastructure
**Setup time:** Months
**Who this is for:** Organisations deploying autonomous strategic intelligence systems

### Multi-agent architecture

The methodology's six-module structure maps directly to agent roles:

```
┌──────────────────────────────────────────────────────────┐
│                    Orchestrator Agent                      │
│    Manages workflow, enforces quality gates, routes tasks  │
└────┬─────────┬──────────┬──────────┬──────────┬──────────┘
     │         │          │          │          │
     ▼         ▼          ▼          ▼          ▼
┌─────────┐┌─────────┐┌─────────┐┌─────────┐┌─────────┐
│Identity ││ Enemy   ││Situation││Strategy ││Execution│
│ Agent   ││ Agent   ││ Agent   ││ Agent   ││ Agent   │
│         ││         ││         ││         ││         │
│Module 2 ││Module 3 ││Module 4 ││Module 5 ││Module 6 │
│Docs 1–4 ││Docs 5–13││Docs14–20││Docs21–24││Docs25–34│
└─────────┘└─────────┘└─────────┘└─────────┘└─────────┘
```

### Agent role specification

**Identity Agent (Module Two):**
- Tools: OSINT search, corporate filings retrieval, financial data access
- Output: Documents 1–4
- Quality gate: Readiness assessment for Module Three
- Human checkpoint: Identity verification before enemy classification proceeds

**Enemy Agent (Module Three):**
- Tools: Competitive intelligence databases, news monitoring, government records
- Input: Documents 1–4 (verified)
- Output: Documents 5–13
- Quality gate: Capacity calculation validation
- Human checkpoint: Enemy classification review

**Situation Agent (Module Four):**
- Tools: Market data feeds, trend analysis, geopolitical monitoring
- Input: Documents 1–13 (verified)
- Output: Documents 14–20
- Quality gate: Vector calculation and situation typology validation
- Human checkpoint: Situation assessment review

**Strategy Agent (Module Five):**
- Tools: Scenario modelling, resource optimisation, historical case retrieval
- Input: Documents 1–20 (verified)
- Output: Documents 21–24
- Quality gate: Strategy coherence verification across all four documents
- Human checkpoint: Strategy approval (Tier 1 decision)

**Execution Agent (Module Six):**
- Tools: Performance monitoring, document activation engine, alert system
- Input: Documents 1–24 (verified) + real-time organisational data
- Output: Documents 25–34 (continuous assessment)
- Authority: Tier 3 autonomous, Tier 2 proposal, Tier 1 analysis only
- Human checkpoint: Continuous oversight with Tier 1/2 approval gates

### Quality gate implementation

Each agent-to-agent handoff passes through a quality gate:

```python
# Pseudocode for quality gate
def quality_gate(agent_output, next_module):
    readiness = assess_readiness(agent_output, next_module)
    
    if readiness == "READY":
        return proceed(agent_output)
    elif readiness == "MODERATE":
        log_warning("Proceeding with acknowledged gaps")
        return proceed(agent_output, with_caveats=True)
    elif readiness in ["WEAK", "CRITICAL"]:
        return request_human_review(agent_output, readiness)
```

### Human-in-the-loop integration

The tier responsibility system (Module Six) translates directly to agent authority levels:

| Tier | Agent behaviour | Human interaction |
|------|----------------|-------------------|
| 1 | Agent halts, presents analysis and options | Human decides via approval interface |
| 2 | Agent proposes action with justification | Human approves/modifies via review queue |
| 3 | Agent executes within parameters, logs action | Human reviews in periodic oversight cycle |

This ensures that strategic decisions requiring human judgement (Tier 1) are never delegated to autonomous agents, while routine tactical adjustments (Tier 3) proceed without human bottleneck.

---

## Choosing Your Pathway

| Factor | Basic | RAG | Fine-Tuning | Agentic |
|--------|-------|-----|-------------|---------|
| Setup time | Minutes | Days–weeks | Weeks–months | Months |
| Technical skill | None | Moderate | High | High |
| Automation | Manual | Semi-automated | Automated generation | Autonomous |
| Cost | LLM subscription only | Infrastructure + LLM | Training compute + LLM | Full stack |
| Output quality | High (human-guided) | High (retrieval-enhanced) | High (if well-trained) | High (if well-architected) |
| Best for | Individual analysts, first use | Teams with existing AI infrastructure | Organisations building strategic AI products | Enterprise continuous strategic intelligence |

**Recommendation:** Start with Basic. Validate the methodology's value with your specific use case. Scale to intermediate/advanced/enterprise as organisational need and technical capability justify the investment.

---

## Get the Methodology

All four pathways use the same core methodology, available at [strategybyai.org](https://strategybyai.org).

→ [Back to README](../README.md) | [Problem analysis](PROBLEM.md) | [Technical architecture](ARCHITECTURE.md) | [Demonstrated results](DEMONSTRATION.md)
