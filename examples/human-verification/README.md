# Perspective 4: Human Verification Protocol

## Demonstration: How the Human Operator Validates AI Output Between Modules

The methodology is not a black box. Human verification at module boundaries is a structural requirement, not an optional quality step.

---

## The Verification Cycle

```
AI produces     →  Human reviews  →  Human corrects  →  Verified document
document           evidence,          if needed           becomes input for
                   classifications,                       next module
                   completeness
```

---

## Example: Verifying Document 5 (Hostile Environment Assessment)

After the AI produces Document 5 classifying 28 entities, the human operator verifies across four dimensions:

### 1. Evidence Accuracy

The operator checks: Are the OSINT sources real and current?

```
AI citation: "President Boko explicitly stated ambition for 'full control
over strategic asset and value chain including marketing'
(July 2025, DiscoveryAlert)"

Human verification:
✓ Source exists and is accessible
✓ Quote is accurately represented
✓ Date is correct
✓ Context is not misleading
```

If the AI fabricated a source or misrepresented a quote, the operator catches it here. The methodology's requirement for specific citations with dates makes fabrication detectable.

### 2. Classification Consistency

The operator checks: Do the four-level classifications match industry knowledge?

```
AI classification: Botswana — ADVERSARY escalating to ENEMY
Confidence: MEDIUM-HIGH

Human assessment:
✓ Adversary-to-enemy trajectory consistent with resource nationalism pattern
✓ February 2025 agreement terms confirm progressive control transfer
? Consider: Is the escalation timeline realistic? Should "Q4 2026"
  be adjusted based on recent political developments?
→ ACCEPTED with note: monitor Botswana electoral cycle impact
```

### 3. Completeness

The operator checks: Are there entities missing?

```
AI inventory: 28 entities classified

Human review:
✓ All major luxury competitors present
✓ Lab-grown producers represented as collective (appropriate)
? Missing: Secondary market / resale platforms (The RealReal, Vestiaire)
  — should these be classified as aliens or rivals?
→ CORRECTION: Add secondary market platforms as ALIENS with
  3–5 year rival escalation timeline
```

### 4. Internal Coherence

The operator checks: Do findings across sections contradict each other?

```
Section A: Anglo American classified as ENEMY consuming 60% capacity
Section B: Resource allocation recommends 15% for Anglo management

Human check: These are consistent — the gap between 60% actual and
15% recommended IS the finding. No contradiction.

Section C: Luxury competitors allocated 38% combined
Section D: Recommended allocation for adversaries: 21–32%

Human check: 38% exceeds recommended range — consistent with the
over-allocation finding. No contradiction.
```

---

## What the Human Does NOT Do

The human does not replicate the AI's analysis. Processing 28 entities against a four-level taxonomy with trajectory assessments, capacity calculations, and cross-referenced evidence chains would take a human analyst weeks. The AI does this in minutes.

The human provides what the AI cannot: judgement about whether the formal analysis matches reality. The AI correctly applies Module Three criteria. The human knows whether the result makes sense given context the public data might not capture.

---

## Verification Output

After verification, the operator produces a brief verification note appended to the document:

```
HUMAN VERIFICATION: Complete
Date: [date]
Entities verified: 28/28
Classifications challenged: 0
Corrections applied: 1 (secondary market platforms added as ALIENS)
Evidence spot-checked: 8 citations verified against original sources
Assessment: Document 5 accepted as input for Module Four
```

This verified document now feeds Module Four with documented quality assurance.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Tier Responsibility](../tier-responsibility/)
