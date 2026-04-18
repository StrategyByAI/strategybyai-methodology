# Changelog

## [2.0.0] — 2026-04-18

### Analytical Discipline Correction — External Investigator Workflow

**The core change:** The external investigator workflow across all modules (Two through Six) now enforces a strict separation between the methodology's prescriptive output (the yardstick) and the subject's observable conduct. This resolves a systematic analytical contamination where AI-generated outputs could conflate the methodology's conclusions with the subject's actual position — producing reports that attributed the methodology's strategic determinations to the subject's own thinking.

**What was corrected:**

*New governance layer — "Part Three: Analytical Discipline for the External Investigator"*
- Created and inserted into the Audience Profiling document (98 lines)
- Contains: the Core Principle, the Three Analytical Voices (Voice 1 — methodology's prescription, Voice 2 — subject's observable conduct, Voice 3 — measured gap), Prohibited Formulations, the Module Six Framing Lock, the Summary Rule, Application Rules per module, and clarification of what Documents 21–24 are and are not

*Per-prompt corrections across five module workflows*
- Each prompt now carries a compact analytical discipline block (Analytical Discipline reference, Section Numbering instruction, Visualisation Requirement)
- All "Upload Subject's strategy formulation Documents 21-24 / Analyse Subject's positioning" instructions replaced with tripartite comparison framework (yardstick → observable execution → gap)
- Three-voice reframes applied to contamination-prone sections in Modules Three, Four, Five, and Six

*Module Six — largest structural change*
- New Prompt 18.5: Observable Execution Reconstruction — forces the investigator to reconstruct from OSINT what the subject actually did before any gap analysis begins, producing Documents 21′–24′ (a parallel document set mirroring Documents 21–24)
- All ten assessment prompts (19–28) rewritten around tripartite comparison: yardstick (Documents 21–24) vs. observable execution (Documents 21′–24′) vs. gap diagnosis
- Module Six Framing Lock embedded throughout: "the subject never adopted the yardstick; the methodology demonstrates what should have been done; what the subject actually did is measured against what should have been done"
- All 42+ Document Activation Protocols, crisis-point fork analyses, phase positioning assessments, and quantitative thresholds preserved intact
- Document output expanded: Documents 21′–24′ + 10 gap assessment reports (Documents 25–34)

*Voice discipline rules per module*
- Modules Two, Three, Four: Voice 2 dominant (observational — what the subject IS)
- Module Five: Voice 1 only (prescriptive — the methodology's yardstick)
- Module Six: All three voices in constant interplay

**Why it matters:**
- Eliminates the most common source of analytical contamination in AI-generated strategic intelligence
- Clients now receive three distinct objects: the yardstick, the observed position, and the diagnostic distance between them
- Machine-verifiable: automated checks can scan outputs for prohibited formulations before delivery
- Integration-ready: the Documents 21–24 / 21′–24′ parallel structure is API-friendly for platform deployment

→ [Full explanation: docs/ANALYTICAL-DISCIPLINE.md](docs/ANALYTICAL-DISCIPLINE.md)
## [1.0.0] — 2026-03-07

### Repository Complete

**Phase 1 — Foundation**
- README with complete repository overview
- Problem analysis: three structural failures in current AI strategy practice (docs/PROBLEM.md)
- Technical architecture: seven perspectives on methodology operation (docs/ARCHITECTURE.md)
- Document portfolio reference: complete 34-document structure (assets/tables/document_portfolio.md)
- CC BY-NC-SA 4.0 license

**Phase 2 — Demonstrations**
- Prompt + Module + Profiling interaction example (examples/prompt-module-interaction/)
- Module chain demonstration: identity through verdict (examples/module-chain/)
- Cross-verification between documents (examples/cross-verification/)
- Human verification protocol (examples/human-verification/)
- Tier-structured AI-human responsibility (examples/tier-responsibility/)
- Document activation protocols (examples/document-activation/)
- De Beers output samples: Documents 4, 7, 21, 24, 34 excerpts (examples/output-samples/)

**Phase 3 — Case Study**
- De Beers UK demonstration with key findings by module (docs/DEMONSTRATION.md)

**Phase 4 — Integration**
- Four implementation pathways: basic upload, RAG, fine-tuning, agentic (docs/INTEGRATION.md)

**Phase 5 — World Models**
- Strategic world models concept (world-models/CONCEPT.md)
- Architecture: general model and subject-specific instances (world-models/ARCHITECTURE.md)
- Python prototype: strategic state representation with De Beers instance (world-models/IMPLEMENTATION.md)

**Phase 6 — Community**
- Contributing guidelines (CONTRIBUTING.md)
- Changelog updated to 1.0.0
