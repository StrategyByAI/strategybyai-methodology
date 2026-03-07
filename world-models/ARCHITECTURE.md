# Strategy by AI as World Model Architecture

## From General Engine to Subject-Specific Instance

### The Two-Layer Architecture

Strategy by AI operates as a two-layer world model system:

**Layer 1 — General Strategic World Model (the engine)**

The methodology itself: six modules encoding how competitive environments behave in general. The strategic models library: 100+ historical cases providing validated patterns. The curated knowledge base: strategic literature providing theoretical foundations.

Together, these encode the "physics" of competitive struggle — escalation dynamics, culmination patterns, power vacuum formation, centre of gravity emergence, fog and friction effects, adaptation-stability tensions.

This layer is domain-agnostic. It applies to business competition, political campaigns, military conflict, and any other antagonistic environment. It is the equivalent of a physics engine that simulates gravity regardless of what objects are present.

**Layer 2 — Subject-Specific Strategic World Model (the instance)**

When the general model processes a specific subject, it produces a 34-document portfolio encoding that subject's competitive reality. The methodology (Layer 1) combined with the portfolio (Layer 2) creates a queryable world model for that specific subject.

```
Layer 1: General Model              Layer 2: Subject Instance
(Strategy by AI methodology)        (Methodology + De Beers portfolio)
                                    
Knows: enemies require 40–50%       Knows: De Beers has 4 enemies
capacity each                       requiring 160–200% capacity
                                    against 40% available
Knows: culmination follows          
resource trajectory                  Knows: De Beers peaks mid-2027,
                                    decisive moment late 2028
Knows: dislocation means            
competing where your advantages     Knows: De Beers' 6 asymmetries
matter and enemy's don't            work only above $20K retail
                                    
Can predict: general consequences   Can predict: specific consequences
of multi-front warfare              of De Beers launching Campaign 2
                                    on Botswana relationship given
                                    Feb 2025 agreement terms
```

**The subject-specific instance is the operational world model.** It is what an AI agent queries when making strategic decisions. It is what produces actionable predictions. It is what gets updated as the competitive environment evolves.

The general model without a subject instance is a reasoning framework. The subject instance without the general model is a data collection. Together, they are a strategic world model.

---

## State Representation: The 34-Document Portfolio

The portfolio encodes complete strategic world state across five dimensions:

### Dimension 1 — Identity State (Documents 1–4)

What the organisation is: mission, historically-built capabilities, doctrinal principles, and the coherence (or incoherence) between them.

```
De Beers instance:
  Mission: maintain natural diamond premium through provenance
  History: 138 years monopoly management → competitive transformation
  Doctrine: three contradictory implicit doctrines, no explicit doctrine
  Coherence: FUNDAMENTAL INCOHERENCE across all dimensions
```

This state constrains everything downstream. An organisation with incoherent identity cannot produce coherent enemy classifications — the model encodes this constraint.

### Dimension 2 — Hostile Environment State (Documents 5–13)

Who opposes the organisation: entity classifications, confrontation hierarchy, capacity requirements, enemy profiles, conflict characterisations, outcome scenarios, multi-front strategy, and monitoring indicators.

```
De Beers instance:
  Entities: 28 classified (4 enemy, 8 adversary, 9 rival, 7 alien)
  Capacity: 160–200% required vs 40% available
  Trajectory: 11 entities (39%) showing escalation probability
  Critical: Botswana transitioning adversary → enemy by Q4 2026
```

### Dimension 3 — Situation State (Documents 14–20)

What the competitive environment looks like: scene configuration across domains/time/space, actor-factor inventory, threats and risks, strategic trends, vectors, situation typology, and power dynamics.

```
De Beers instance:
  Scene: three theatres with different competitive physics
  Factors: 15 of 20 unfavourable (75%)
  Vectors: 65% unfavourable overall, 60% FAVOURABLE in ultra-luxury
  Typology: late Shaping / early Clash transition
  Power: five poles, fragmenting environment trending toward vacuum
```

### Dimension 4 — Strategy State (Documents 21–24)

What the organisation intends to do: war definition, objectives hierarchy, campaign architectures, and integrated strategy with principles and settlement conditions.

```
De Beers instance:
  War: Natural Diamond Premium Defence, 2025–2030, ultra-luxury bounded
  Objective: >$20K positioning, <5% volume, 25–30% margin by 2030
  Campaigns: 5 coordinated, $565–775M, 60 months
  Settlement: Victory 25–35%, Defeat 50–60%, Contingency 15–20%
```

### Dimension 5 — Execution State (Documents 25–34)

What is actually happening: nine execution dimensions assessed and graded, with activation registry documenting every evidence chain.

```
De Beers instance:
  Commitment: MARGINAL (3/5 components crossed)
  Command: DEFICIENT (no structure exists)
  Overall: F — 0/7 phases, 0/10 objectives, 0/9 targets
  Cost: $245–375M consumed, $0 strategic return
```

---

## Transition Dynamics: How State Changes

The module chain defines how one state produces the next. These are not arbitrary — they follow specific rules:

### Rule-governed transitions

```
Identity state change       →  Enemy classifications may change
  (e.g., mission revision)      (new mission creates new enemies)

Enemy trajectory change     →  Situation assessment shifts
  (e.g., Botswana escalates)    (situation becomes more hostile)

Situation vector shift      →  Strategy may require adjustment
  (e.g., ultra-luxury collapses) (war definition changes)

Strategy trigger activated  →  Execution assessment re-evaluates
  (e.g., ownership resolved)    (new capability enables campaigns)
```

### Transition example: What happens if De Beers launches Campaign 2?

An AI agent with the De Beers strategic world model can simulate:

```
Action: Launch Campaign 2 (Distribution Optimisation)
  — Terminate 1,800 of 2,000 Sightholder partnerships
  — Begin flagship boutique programme in 15–20 cities

State changes predicted:

  Identity state: Mission clarity increases (commitment to ultra-luxury
  visible through action). Doctrine crystallises around brand doctrine.
  
  Hostile environment state:
    — Sightholder community: some escalate from rival to adversary
      (lost revenue, relationship destruction)
    — Botswana (Enemy 4): interprets as either commitment signal
      (positive — De Beers investing in premium future) or instability
      signal (negative — destroying established distribution).
      Prediction depends on whether Botswana perceives ultra-luxury
      pivot as enhancing or threatening their revenue share.
    — LGD producers (Enemy 1): cannot replicate flagship boutique
      model (no heritage, no craftsmanship narrative for physical
      retail). Competitive pressure in ultra-luxury DECREASES.
  
  Situation state:
    — Ultra-luxury theatre: De Beers presence strengthens
    — Mass/premium theatres: De Beers withdraws (by design)
    — Trend vectors: heritage-resilience trend reinforced
  
  Execution state:
    — Campaign 2 status: ACTIVE (currently: not launched)
    — Resource allocation: 35–40% committed (currently: 0%)
    — Capacity available for other campaigns: decreases
    — Culmination timeline: accelerates (resource consumption begins)
```

This simulation is possible because the world model contains: the current state (portfolio), the transition rules (methodology), and the entity-specific dynamics (enemy profiles with trajectory assessments).

A standalone LLM could generate a similar narrative — but without state persistence, consistency enforcement, or transition rules, it might simultaneously predict that Botswana views the move positively AND that it accelerates resource nationalism. The world model prevents this contradiction because Document 5's enemy profile and Document 9's strategic profile encode Botswana's trajectory consistently.

---

## Counterfactual Reasoning

The world model enables "what if" exploration:

```
Query: "What if De Beers had launched Campaign 1 (Brand Transformation)
        in Q1 2026 as planned?"

The model simulates forward from the counterfactual action:
  — Brand positioning begins shifting (identity state changes)
  — Consumer perception data starts accumulating (situation state updates)
  — LGD producers must respond to heritage narrative (enemy state changes)
  — Resource consumption begins (execution state: capacity allocated)
  — Culmination timeline engages (Document 30 predictions activate)

Versus actual state:
  — No campaign launched. No state changes. Resources consumed by
    Anglo management. Culmination approaches without engagement.

Counterfactual comparison reveals: 15 months of positioning lost.
The model quantifies this as competitive deterioration — LGD market
share advanced from 18% to 25–30% during the inaction period, each
percentage point increasing the difficulty of establishing ultra-luxury
differentiation.
```

This is strategic world model reasoning: maintaining state, applying transition rules, comparing actual versus counterfactual trajectories, and quantifying the consequences of actions and inactions.

---

## Consistency Enforcement

The cross-reference network between documents creates a constraint system:

```
Constraint 1: Capacity cannot exceed 100%
  If campaign allocations sum to >100%, the model flags inconsistency
  
Constraint 2: Enemy classifications must align with mission
  If Entity X is classified as ENEMY, its business model must be
  incompatible with the mission defined in Document 1
  
Constraint 3: Strategy must respect capacity constraints
  If Document 8 shows 40% available capacity, Document 23 cannot
  allocate 80% to campaigns without acknowledging the gap
  
Constraint 4: Execution assessment must reference strategy
  If Document 34 grades execution, it must measure against the
  specific campaigns, targets, and timelines in Documents 21–24
```

These constraints are what distinguish a world model from a narrative generator. An LLM generating a strategic narrative might violate all four constraints across a long conversation. A strategic world model enforces them structurally.

---

## Summary: The Instance Is the Operational World Model

The general model (Strategy by AI methodology) provides the engine: transition rules, constraint logic, analytical frameworks, and historical pattern library.

The subject instance (methodology + 34-document portfolio) provides the operational world model: queryable state, predictable transitions, testable counterfactuals, and enforced consistency.

**For AI developers:** The instance architecture is what you build. Your system produces strategic world model instances for whatever subjects your users analyse. Each instance is a queryable, updatable, self-consistent representation of a specific competitive environment.

**For the current frontier:** Physical world models predict what happens when you apply force to objects. Strategic world models predict what happens when organisations take actions against enemies. The physics is different. The architecture is the same. Strategy by AI provides the strategic physics.

→ [Concept: why strategic world models are needed](CONCEPT.md) | [Python prototype: building instances](IMPLEMENTATION.md)
