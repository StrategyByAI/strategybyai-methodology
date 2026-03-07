# Why Strategic Reasoning Needs World Models

## The Gap Between LLM Knowledge and Strategic Prediction

### What LLMs know about strategy

Large Language Models are trained on vast strategic literature — Sun Tzu, Clausewitz, Svechin, modern competitive analysis, thousands of business case studies, decades of military history, political campaign documentation. This training creates implicit strategic knowledge: the model "knows" that monopolies fragment, that resource nationalism escalates, that organisations facing multi-front wars must concentrate forces, that capability has a peak after which decline follows.

### What LLMs cannot do with that knowledge

Ask an LLM "What should De Beers do about lab-grown diamonds?" and you get a plausible answer. Ask it again in a different conversation and you get a different plausible answer. Ask it to reconcile the two and it produces a third answer that may contradict both.

The problem is not knowledge — it is consistency, persistence, and prediction over multi-step reasoning chains.

**Consistency:** An LLM might classify Botswana as a "partner" in one paragraph and a "threat" in the next, because each token is predicted independently without an internal model enforcing that classifications persist.

**Persistence:** An LLM has no state between queries. It cannot remember that it classified four enemies requiring 160% capacity and then apply that constraint when formulating a strategy five prompts later — unless the entire reasoning chain is maintained in context.

**Prediction:** An LLM can generate plausible-sounding predictions, but cannot simulate multi-step consequences: "If De Beers launches Campaign 2 (Distribution Optimisation), which terminates 1,800 Sightholder partnerships, how does this affect Enemy 4 (Botswana) given Botswana's resource nationalism trajectory and the February 2025 sales agreement terms?" This requires combining current state, transition rules, and entity-specific dynamics — exactly what a world model does.

### The parallel with physical world models

Yann LeCun's argument for physical world models applies directly to strategic reasoning:

> "You can imagine a sequence of actions you might take, and your world model will allow you to predict what the effect of the sequence of actions will be on the world."

Replace "physical world" with "competitive environment":

- A physics world model predicts: "If I drop this ball, gravity accelerates it at 9.8 m/s²"
- A strategic world model should predict: "If De Beers terminates 1,800 Sightholders, distribution capacity drops 90% within 18 months, revenue drops 60–70% before flagship boutiques generate replacement revenue, and Botswana interprets the disruption as evidence of strategic instability, accelerating its timeline for asserting full control"

The first prediction requires a physics engine that enforces gravity. The second prediction requires a strategic engine that enforces competitive dynamics — escalation trajectories, resource constraints, enemy response patterns, and capacity mathematics.

That strategic engine is what Strategy by AI provides.

---

## What a Strategic World Model Must Do

Drawing from both physical world model requirements and strategic reasoning needs:

### 1. Maintain state

The model must represent the current state of the competitive environment — who the actors are, what resources they command, what their trajectories are, what the situation looks like across temporal, spatial, and functional dimensions.

In Strategy by AI: The 34-document portfolio IS the state representation. It encodes organisational identity (Documents 1–4), hostile environment (Documents 5–13), strategic situation (Documents 14–20), strategic design (Documents 21–24), and execution status (Documents 25–34).

### 2. Predict transitions

The model must predict how the state changes when actions occur — or when actions fail to occur.

In Strategy by AI: Module chains define transition rules. When an organisation's identity changes (Module Two state), its enemy classifications may change (Module Three state). When enemy trajectories escalate (Module Three state), the situation assessment shifts (Module Four state). These are not arbitrary — they follow specific rules encoded in the methodology's sections.

### 3. Enable counterfactual reasoning

The model must answer "what if" questions — exploring alternative actions and their predicted consequences without committing to them.

In Strategy by AI: Document 11 (Outcome Scenarios) models victory, defeat, and contingency outcomes. Document 24 specifies settlement conditions with probabilities. The tier system enables the AI to propose Tier 2 actions and model their consequences before the human operator approves.

### 4. Enforce consistency

The model must prevent contradictions that standalone LLM reasoning produces — ensuring that a classification made in Module Three remains consistent with assessments made in Module Six.

In Strategy by AI: Cross-referencing between documents creates a consistency constraint network. Document 34's activation registry traces every verdict back through specific documents with specific evidence. Contradictions propagate visibly rather than remaining hidden.

### 5. Support planning

The model must enable forward planning — sequencing actions across time with resource constraints, dependencies, and timing requirements.

In Strategy by AI: Document 23 (Campaign Architecture) specifies five campaigns with sequencing, dependencies, resource allocations, and timelines. Document 30 (Culmination Assessment) predicts when capability peaks relative to decisive engagement — enabling the planner to determine whether the sequence of actions can achieve the objective before resources are exhausted.

---

## What exists today versus what is needed

| Capability | Physical world models (2025–26) | Strategic world models (needed) |
|---|---|---|
| State representation | 3D scenes, object properties, spatial relationships | Competitive environment: actors, resources, trajectories, situations |
| Transition prediction | Physics simulation: gravity, collisions, fluid dynamics | Competitive simulation: escalation, resource depletion, capability culmination |
| Counterfactual reasoning | "What if I move this object?" | "What if we launch this campaign?" |
| Consistency enforcement | Physics constraints: objects cannot overlap, energy conserves | Strategic constraints: capacity cannot exceed 100%, enemy classifications must align with mission |
| Planning support | Robot path planning, autonomous vehicle navigation | Campaign sequencing, resource allocation, timing optimisation |
| **Current status** | Active development by DeepMind, NVIDIA, Meta, World Labs, AMI Labs | **No systematic framework exists — except Strategy by AI** |

→ [How Strategy by AI maps to world model architecture](ARCHITECTURE.md) | [Python prototype](IMPLEMENTATION.md)
