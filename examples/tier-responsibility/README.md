# Perspective 5: Tier-Structured AI-Human Responsibility

## Demonstration: How Decision Authority Is Distributed in Module Six

Module Six does not treat all decisions equally. It classifies every decision by tier, assigning explicit authority to either the AI assistant, the human operator, or both — preventing AI overreach on critical decisions and human bottleneck on routine ones.

---

## The Three Tiers

| Tier | Scope | AI authority | Human authority |
|------|-------|-------------|----------------|
| **1** | War-level: strategy change, settlement, fundamental transformation | Analyse, activate documents, present options with evidence | **DECIDE** |
| **2** | Operational: campaign resource reallocation, objective priority adjustment | Propose changes with document-grounded justification | **APPROVE, MODIFY, or REJECT** |
| **3** | Tactical: campaign-internal adjustments within allocated parameters | Execute within pre-established constraints, monitor | **OVERSEE** |

---

## De Beers Examples by Tier

### Tier 1 — Human Decides

**Decision:** Whether to pursue LVMH/Richemont as strategic buyer versus accept financial buyer for Anglo American divestiture.

**Why Tier 1:** This changes the fundamental war. A strategic buyer (luxury conglomerate) extends the capability timeline by providing execution infrastructure, patient capital, and brand management expertise. A financial buyer (private equity) shortens the timeline through cost optimisation pressure. Document 21's war definition and Document 24's settlement conditions change entirely depending on this decision.

**AI role:**
```
TIER 1 ANALYSIS:
Documents activated: 2, 4, 21, 24, 30

Path A — Strategic buyer:
  Capability timeline extends to 2032+
  Culmination-centre alignment: ACHIEVABLE
  Victory probability: increases from 25–35% to 40–55%
  Cost: premium price, extended transition, integration risk

Path B — Financial buyer:
  Capability timeline compresses to 2028
  Culmination-centre alignment: FATAL MISALIGNMENT
  Victory probability: decreases to 10–20%
  Cost: lower price, rapid extraction, strategic abandonment risk

RECOMMENDATION: Path A materially alters war mathematics.
This is a Tier 1 decision. Human operator must decide.
```

**Human role:** Evaluate the analysis. Decide. The AI cannot make this choice — it changes the nature of the war the organisation fights.

---

### Tier 2 — AI Proposes, Human Approves

**Decision:** Reallocate 5% capacity from Brand Transformation campaign (currently 25–30%) to Botswana Partnership campaign (currently 10–15%) based on accelerating resource nationalism signals.

**Why Tier 2:** This adjusts operational resource distribution between campaigns without changing the war definition or supreme objective. It responds to Document 13's early warning indicators (Botswana-Angola coordination) by strengthening one campaign at another's expense.

**AI role:**
```
TIER 2 PROPOSAL:
Documents activated: 8, 13, 23

Trigger: Early warning indicator — Botswana-Angola ministerial
coordination meeting (November 2025, Mining.com) signals accelerated
resource nationalism timeline.

Proposed adjustment:
  Brand Transformation: 25–30% → 20–25% (defer heritage campaign
  Phase 2 by one quarter)
  Botswana Partnership: 10–15% → 15–20% (accelerate diplomatic
  engagement and supply contract negotiation)

Justification: Document 13 escalation indicator crossed threshold.
Document 23 campaign dependencies show Botswana supply security is
prerequisite for all other campaigns.

Impact: Delays brand repositioning by ~3 months. Secures supply
foundation without which brand repositioning is moot.

AWAITING APPROVAL: This is a Tier 2 decision. Human operator
must approve, modify, or reject.
```

**Human role:** Evaluate whether the 3-month brand delay is acceptable given the supply security urgency. Approve as proposed, modify the percentages, or reject with rationale.

---

### Tier 3 — AI Executes, Human Oversees

**Decision:** Adjust counter-narrative messaging emphasis from environmental sustainability claims to cultural heritage emphasis within the allocated 10–15% capacity budget.

**Why Tier 3:** This is a tactical adjustment within a single campaign's allocated resources. It does not change resource allocation between campaigns (Tier 2) or the war definition (Tier 1). It responds to observed LGD marketing shifts by adjusting messaging emphasis.

**AI role:**
```
TIER 3 EXECUTION:
Campaign: Counter-Narrative (10–15% capacity)
Adjustment: Shift messaging emphasis ratio from 60/40
(sustainability/heritage) to 40/60 (sustainability/heritage)

Trigger: LGD producers have pre-empted sustainability critique
through third-party environmental audits (Q2 2026 press coverage).
Sustainability attack vector losing effectiveness. Heritage
differentiation showing higher engagement metrics.

Action taken within allocated parameters. No resource reallocation
required. Monitoring for effectiveness over 30-day cycle.

HUMAN OVERSIGHT NOTE: This adjustment is logged. Human operator
will review in next weekly execution review.
```

**Human role:** Review in regular oversight cycle. Intervene if the adjustment produces unintended effects or if the messaging shift contradicts brand positioning established in the Brand Transformation campaign.

---

## Why Tiers Matter for AI System Design

### Preventing AI overreach

Without tiers, an AI assistant might present a Tier 1 recommendation (change the entire strategy) with the same confidence and format as a Tier 3 adjustment (tweak messaging). The operator has no signal indicating which decisions require their deep engagement.

### Preventing human bottleneck

Without tiers, every decision requires human approval — including dozens of Tier 3 tactical adjustments per week during active execution. The operator becomes a bottleneck, approving routine adjustments while Tier 1 decisions queue behind them.

### For agentic implementations

Tiers translate directly to agent authority levels:
- Tier 1: Agent must halt and request human input
- Tier 2: Agent proposes and waits for approval signal
- Tier 3: Agent executes autonomously within defined parameters, logs action, surfaces in periodic review

This is directly implementable in any agent framework supporting human-in-the-loop checkpoints.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Document Activation](../document-activation/)
