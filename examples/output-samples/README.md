# Perspective 1: How Prompt + Module Section + Profiling Produce an Intelligence Document

## Demonstration: Document 5 — Hostile Environment Intelligence Assessment

This example shows how three input components combine to produce a specific intelligence document. The subject is De Beers UK. The output is Document 5 — the hostile environment assessment classifying 28 entities across four threat levels.

---

## Component A: Module Section

**Source:** Module Three, Section 3.2 (Classification of Foes)

The module section provides the analytical framework. For enemy classification, it defines:

**Four-status taxonomy:**
- **Alien** — latent, future threat; impact not yet directly felt
- **Rival** — parallel competition; their success does not require your destruction
- **Adversary** — active confrontation over significant assets; survivable
- **Enemy** — fundamental business model or strategic objectives require your elimination; existential; compromise impossible

**Classification criteria:**
- Status determined by confrontation *character*, not competitive *intensity*
- Each classification includes confidence assessment (HIGH / MEDIUM / LOW)
- Each requires evidence citations with specific sources and dates
- Trajectory assessment required: escalating / stable / de-escalating

**Analytical depth per status:**
- Enemies: 7–10 sentences with full evidence chain
- Adversaries: 5–7 sentences
- Rivals: 5–6 sentences
- Aliens: 4–5 sentences

> **What this component contributes:** The intellectual structure — HOW to think about competitive entities. Without it, the AI produces generic "competitor analysis" treating all entities equally.

---

## Component B: Workflow Prompt

**Source:** Module Three workflow library — Enemy Classification prompt

The workflow prompt provides the specific instruction. Key directives include:

- Identify minimum 20–30 significant hostile entities
- Classify each using Module Three Section 3.2 criteria
- Synthesise OSINT with Module Two outputs (Documents 1–4)
- Produce confrontation hierarchy mapping existential importance against intensity
- Calculate resource allocation requirements per threat level
- Project mutation timelines (when entities may change status)
- Assess intrinsic hostility drivers (structural vs contingent)

> **What this component contributes:** The operational instruction — WHAT to produce, in what structure, at what depth. Without it, the AI has the framework but no direction for applying it.

---

## Component C: Audience Profiling

**Source:** External Investigator profile

The audience profile calibrates the analytical perspective:

- **Evidence base:** OSINT only — corporate filings, financial reports, industry research, trade press, government statements
- **Access assumption:** No insider data, no proprietary intelligence
- **Confidence calibration:** Reflect public-information limitations in all assessments
- **Gap acknowledgment:** Explicitly note where insider data would improve classification
- **Recommendation scope:** Include intelligence collection recommendations for gaps identified

> **What this component contributes:** The analytical perspective — FROM WHOSE VIEWPOINT the assessment is conducted. An internal expert profile would produce different confidence levels, different evidence citations, and different gap acknowledgments.

---

## The Output: Document 5 (Excerpt)

When all three components combine, the AI produces output like this:

### Executive Summary (excerpt)

```
Total Entities Classified: 28 significant hostile actors
Status Distribution:
  ENEMIES (Existential Threats):   4 entities
  ADVERSARIES (Peripheral Threats): 8 entities
  RIVALS (Third-Party Competition): 9 entities
  ALIENS (Latent/Emerging Threats): 7 entities

Overall Assessment Confidence: MEDIUM-HIGH
Confidence Distribution: 43% HIGH, 46% MEDIUM, 11% LOW
```

### Enemy Classification Example: Government of Botswana

```
Status: ADVERSARY escalating to ENEMY
Trajectory: ESCALATING RAPIDLY
Confidence: MEDIUM-HIGH

Evidence chain:
- February 2025 sales agreement structures progressive control transfer:
  30%→40%→50% ODC allocation by 2035
- President Boko explicitly stated ambition for "full control over
  strategic asset and value chain including marketing" (July 2025)
- Botswana-Angola ministerial coordination meeting (November 2025)
  sparked speculation about coordinated producer bloc formation
- Historical pattern: resource-rich developing nations progressively
  asserting sovereignty (Chile copper, Venezuela oil, DRC cobalt,
  Indonesia nickel) following identical trajectory

Enemy status justification: Botswana's optimisation (maximum domestic
value capture) requires De Beers' strategic autonomy elimination.
Mutually exclusive interest structure defines enemy status per
Module Three Section 3.2.4 taxonomy.
```

### What makes this output different from generic AI analysis

| Generic AI output | Strategy by AI output |
|---|---|
| "Botswana is a key partner facing tensions" | Classifies Botswana as adversary escalating to enemy with specific timeline and evidence |
| No confidence level | MEDIUM-HIGH confidence with justification |
| No source citations | Five specific OSINT sources with dates |
| No historical pattern | Maps to resource nationalism trajectory across four countries |
| No methodology reference | Traces classification to Module Three Section 3.2.4 criteria |
| No capacity calculation | Contributes to 160–200% total enemy capacity requirement |

---

## Key Takeaway

The module section prevents the AI from treating all competitors equally. The workflow prompt ensures systematic coverage (28 entities, not 5–6 obvious ones). The audience profile ensures honest confidence assessment. Together, they produce intelligence that generic prompting cannot.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Module Chain](../module-chain/)
