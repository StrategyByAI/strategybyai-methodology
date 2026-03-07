# Strategy World Models

## A New Class of World Model for Competitive Reasoning

Current world models (DeepMind Genie 3, NVIDIA Cosmos, Meta V-JEPA 2, World Labs Marble) focus on physical environments — predicting how objects behave under gravity, inertia, and spatial dynamics. They answer: "If I apply force X to object Y in environment Z, what happens?"

An undeveloped parallel domain exists: **strategic world models** — internal models of how competitive environments behave. They should answer: "If organisation A takes action X against enemy B in situation C, what happens?"

LLMs have implicit strategic knowledge from training data. They "know" about competitive dynamics, escalation patterns, and resource constraints. But like their implicit physical knowledge, this understanding is unreliable — it hallucinates impossible outcomes, contradicts itself across reasoning steps, and cannot maintain consistency over multi-step strategic planning.

Strategy by AI provides the structured framework that converts implicit strategic knowledge into explicit, auditable, self-consistent strategic world models.

---

## How It Works

Strategy by AI operates as a **general strategic world model** — encoding how competitive environments behave across any domain. When applied to a specific subject, it produces a **subject-specific strategic world model** — a queryable representation of that subject's competitive reality.

The general model is the engine. The subject-specific model is the engine running on particular data.

```
General Strategic World Model          Subject-Specific World Model
(Strategy by AI methodology            (Methodology + 34-document
 + strategic models library             portfolio for Organisation X)
 + curated knowledge base)
         │                                        │
         │                                        │
         ▼                                        ▼
Encodes: how competitive               Encodes: how THIS organisation's
environments behave in general          competitive environment behaves
                                        specifically
         │                                        │
         ▼                                        ▼
Predicts: escalation dynamics,          Predicts: if De Beers launches
culmination patterns, power             Campaign 2, what happens to
vacuum formation — for ANY subject      Botswana relationship? When does
                                        capability peak relative to
                                        decisive engagement?
```

This mirrors physical world models exactly. NVIDIA Cosmos is a general physics engine. Load a specific environment, and you get a specific simulation. Nobody debates whether Cosmos or the simulation is "the real world model" — Cosmos is the general model, the simulation is an instance. Strategy by AI is the general strategic model. The De Beers portfolio is an instance.

---

## Contents

| Document | What it covers |
|----------|---------------|
| [CONCEPT.md](CONCEPT.md) | Why strategic reasoning needs world models — the gap between LLM knowledge and strategic prediction |
| [ARCHITECTURE.md](ARCHITECTURE.md) | How Strategy by AI maps to world model architecture — state, transitions, actions, counterfactuals, consistency |
| [IMPLEMENTATION.md](IMPLEMENTATION.md) | Python prototype: strategic state representation for building subject-specific world models |

→ [Back to README](../README.md)
