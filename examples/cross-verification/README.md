# Perspective 3: Cross-Verification Between Documents

## Demonstration: How Documents From Different Stages Verify Each Other

Documents produced at different stages of the methodology create a self-auditing network. Findings from Module Two can be checked against findings from Module Four. Predictions from Module Three can be tested against assessments from Module Six. This cross-referencing is structural — it happens because documents reference each other, not because someone manually compares them.

---

## Verification Chain 1: Identity → Resources → Objectives → Preparation

```
Doc 4 (Module Two)     Doc 8 (Module Three)    Doc 22 (Module Five)    Doc 25 (Module Six)
Identity Profile   →   Resource Audit      →   Objectives Matrix  →   Preparation Assessment
                                                                            
PREDICTS               QUANTIFIES              ACKNOWLEDGES            MEASURES
capability gaps        resource deficit         constraints             whether gaps addressed
```

### How it works in the De Beers case

**Document 4** diagnosed: "Every capability mission requires is organizational weakness; every capability history provided is obsolete or counterproductive."

**Document 8** quantified: 60% capacity consumed by Anglo American vs 15% recommended. Four enemies requiring 160–200% capacity. Effective available: 40%.

**Document 22** acknowledged these constraints: Formally excluded LGD cost advantage as a target (accessibility: 0/10). Designed objectives achievable within the 40% available capacity window.

**Document 25** measured: 42% resource extraction gap persists. Zero reallocation from Anglo management to strategic campaigns. The gap Document 4 predicted and Document 8 quantified was NOT addressed in preparation.

### What this reveals

If Document 22 had ignored Document 8's constraints and set objectives requiring 80% capacity, the inconsistency would be visible across the chain. If Document 25 had found the gap closed, it would validate the preparation phase. The cross-referencing makes both alignment and contradiction explicit.

---

## Verification Chain 2: Enemy Classification → Situation → War Definition → Verdict

```
Doc 5 (Module Three)    Doc 19 (Module Four)    Doc 21 (Module Five)    Doc 34 (Module Six)
Hostile Environment →   Situation Report    →   War Definition      →   Final Verdict

CLASSIFIES              INCORPORATES            BOUNDS                  GRADES
28 entities, 4 enemies  into situation reading   the war accordingly     execution against plan
```

### How it works in the De Beers case

**Document 5** classified four enemies and calculated 160–200% capacity requirement.

**Document 19** incorporated this into the situation reading: "late Shaping / early Clash transition" with the organisation possessing less than 40% of required capacity.

**Document 21** used the situation to bound the war: abandon 85% of the market (mass and premium segments) to concentrate on the 15% ultra-luxury segment where only two of four enemies operate at full strength.

**Document 34** graded: Zero campaigns launched in the bounded war. Zero targets engaged. The war was defined but never fought.

### Cross-verification test

If Document 21 had defined the war as "compete across all segments" despite Document 5's capacity mathematics showing this is impossible, the inconsistency would be flagged — either at the human verification stage between modules or visibly in Document 34 when execution fails against an impossible strategy.

---

## Verification Chain 3: Doctrine → Campaigns → Execution

```
Doc 3 (Module Two)      Doc 23 (Module Five)    Doc 32 (Module Six)
Doctrine Report     →   Campaign Architecture → Adaptation Assessment

DIAGNOSES               DESIGNS                 EVALUATES
doctrinal confusion     campaigns based on      adaptation capacity given
                        inferred doctrine       doctrinal absence
```

### How it works in the De Beers case

**Document 3** diagnosed three contradictory implicit doctrines: monopoly control, defensive brand, financial optimisation. No explicit doctrine exists.

**Document 23** designed campaigns acknowledging this gap: Brand Transformation campaign (25–30% capacity) is designed to resolve the brand-vs-financial doctrine contradiction by committing to heritage positioning.

**Document 32** evaluated: Adaptation capacity rated MARGINAL. The organisation maintained the correct strategic direction (credit) but lacks the doctrinal foundation to distinguish "adaptation within strategy" from "strategy abandonment" — exactly the problem Document 3 diagnosed.

---

## How Contradictions Surface

The cross-verification network has a critical property: contradictions **propagate visibly**.

If Document 4 claims De Beers has strong retail capability but Document 8 shows zero retail investment, the contradiction appears when both documents are referenced by Document 22 (which must set objectives within actual capabilities, not claimed ones).

If Document 19 classifies the situation as "favourable" but Document 5 shows four existential enemies, the contradiction appears when Document 21 attempts to define a war — you cannot define a bounded defensive war in a situation classified as favourable.

In generic AI analysis, contradictions remain hidden because each analysis is independent. In the Strategy by AI portfolio, contradictions surface because documents must reference each other. This is the structural advantage of a cross-referenced portfolio over standalone reports.

---

## For AI Developers

The cross-verification network is implementable as a consistency checking system:

```
For each document D:
  For each claim C in D:
    Find all documents referencing C
    Check: do referencing documents treat C consistently?
    If inconsistency detected: flag for human review
```

This is not hypothetical — it is what the methodology's human verification protocol requires at each module boundary. Automating it is a natural extension for agentic implementations.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Human Verification](../human-verification/)
