# Perspective 2: Module Chain — How Output Feeds Input

## Demonstration: The Five-Step Chain from Identity to Verdict

Each module's output becomes the next module's input. This creates a dependency chain where analytical foundations build cumulatively. Removing or corrupting any link degrades everything downstream.

---

## The Chain

```
Module Two ──→ Module Three ──→ Module Four ──→ Module Five ──→ Module Six
(Identity)     (Enemy)          (Situation)     (Strategy)     (Execution)
Docs 1–4       Docs 5–13        Docs 14–20      Docs 21–24     Docs 25–34
```

---

## Step 1 → 2: Identity Feeds Enemy Classification

### What Module Two produces (Document 4 excerpt)

```
CRITICAL FINDING: De Beers UK lacks authentic integrated strategic
identity. Organization exhibits identity crisis where mission aspirations,
historical constraints, and doctrinal absence create strategic vacuum.

ENEMY CLASSIFICATION CRITERIA (Handoff to Module Three):
  Premium Destruction Threat     → ENEMIES
  Production Access Threat       → ENEMIES
  Competitive Substitution       → ADVERSARIES
  Peripheral Competition         → RIVALS
  Future Potential Threats       → ALIENS
```

### How Module Three uses it

Document 4's mission definition determines WHO qualifies as an enemy. Without knowing that De Beers' mission is "maintain natural diamond premium pricing through provenance-based differentiation," the AI cannot distinguish between entities that threaten the mission (enemies) and entities that merely compete in adjacent spaces (rivals).

**Specific feed:** Document 4's mission-based enemy criteria become Document 5's classification framework. Lab-grown producers are classified as ENEMIES because their business model requires the destruction of natural diamond premiums — this classification is impossible without Document 4's mission definition.

---

## Step 2 → 3: Enemy Feeds Situation Assessment

### What Module Three produces (Document 8 excerpt)

```
CAPACITY MATHEMATICS:
  Each enemy-level threat requires 40–50% organisational capacity.
  Four enemies × 40–50% = 160–200% total requirement.
  De Beers has 100% capacity.
  60% consumed by Anglo American divestiture.
  Effective available capacity: 40%.
  Gap: 120–160% capacity deficit.
```

### How Module Four uses it

Document 8's capacity calculation feeds directly into Document 19 (Strategic Situation Assessment). The situation is not merely "competitive" — it is structurally impossible under current resource allocation. This shapes the entire situation reading: the strategic environment is not unfavourable by degree, it is mathematically unworkable.

**Specific feed:** Document 8's "160–200% required vs 40% available" becomes the central constraint in Document 19's situation classification. Module Four's finding that the situation is "late Shaping / early Clash transition" incorporates the fact that De Beers enters the Clash phase with capacity to address roughly one-quarter of its existential threat load.

---

## Step 3 → 4: Situation Feeds Strategy Formulation

### What Module Four produces (Document 18 excerpt)

```
STRATEGIC VECTORS:
  Overall environment: 65% unfavourable force
  Mass market (<$5,000):  85% unfavourable — LGD-dominated
  Premium ($5K–$20K):     60% unfavourable — contested, declining
  Ultra-luxury (>$20K):   60% FAVOURABLE — heritage-resilient

SITUATION TYPOLOGY: Late Shaping / early Clash transition
CRITICAL JUNCTURES: Q2–Q4 2026
```

### How Module Five uses it

Document 18's vector analysis reveals that the only defensible theatre is ultra-luxury. This finding — invisible without systematic vector calculation across market segments — becomes Document 21's war definition: concentrate 75–85% of capacity on the 15% ultra-luxury segment.

**Specific feed:** The "60% favourable in ultra-luxury vs 65% unfavourable overall" finding from Document 18 becomes the mathematical justification for strategic dislocation in Document 21. Without Module Four's segmented vector analysis, the strategy would either target the entire market (fatal dispersion) or retreat entirely (unnecessary surrender).

---

## Step 4 → 5: Strategy Feeds Execution Assessment

### What Module Five produces (Document 24 excerpt)

```
INTEGRATED STRATEGY STATEMENT:
  De Beers UK executes ultra-luxury niche defensive concentration through
  strategic dislocation from LGD-dominated mass market to heritage-
  favourable ultra-luxury segment.

  Five campaigns. $565–775M. 60 months.
  Settlement: Victory 25–35%. Defeat 50–60%. Contingency 15–20%.

  STRATEGY CHANGE TRIGGERS:
  1. Ownership resolution producing strategic buyer with execution capability
  2. Ultra-luxury segment collapse below $6B addressable market
  3. Botswana partnership termination
  4. Technology disruption eliminating provenance verification capability
```

### How Module Six uses it

Document 24's strategy integration becomes the baseline against which ALL execution is measured. Module Six does not assess execution in the abstract — it measures specific organisational behaviour against specific documented plans.

**Specific feed:** Document 24's four strategy change triggers become the criteria Module Six monitors. Document 34's verdict that zero triggers were activated, zero campaigns were launched, and zero objectives were pursued is a direct comparison between Document 24's design and observed organisational reality.

---

## Step 5: Execution References ALL Preceding Documents

Module Six is unique: it does not just reference the immediately preceding module. It activates documents from the ENTIRE portfolio through prescribed activation protocols.

```
Document 34 Activation Registry (excerpt):

Protocol 1 — Commitment Threshold (§6.1.4):
  Documents Activated: 1, 2, 3, 21, 22, 23, 24
  Finding: MARGINAL commitment

Protocol 4 — Decision Authority (§6.4.1.2):
  Documents Activated: 21, 22, 23, 24, 25
  Finding: Documentary ADEQUATE, operational DEFICIENT

Protocol 10 — External Opposition (§6.5):
  Documents Activated: 5, 6, 7, 9, 11, 19, 22
  Finding: Opposition characterisation SOPHISTICATED,
           engagement ZERO
```

The chain is not linear at this stage — it is a network, with Module Six reaching back across the entire portfolio to produce its verdict.

---

## Why the chain matters technically

**For developers:** The chain creates a data dependency graph. Each document has explicit inputs (preceding documents) and explicit outputs (findings feeding forward). This is directly implementable as a workflow DAG in agentic systems.

**For architects:** The chain creates natural quality checkpoints. Each module boundary is a verification point where human operators or automated quality gates can validate output before it propagates downstream.

**For users:** The chain means errors are traceable. If Document 34's verdict seems wrong, you trace backward: which execution finding? Based on which activation protocol? Referencing which strategy document? Derived from which situation assessment? Built on which enemy classification? Grounded in which identity analysis? Every conclusion has an evidence chain back to Module Two.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Cross-Verification](../cross-verification/)
