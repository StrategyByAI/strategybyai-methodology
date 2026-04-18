# Analytical Discipline: The v2.0 Correction

**Version 2.0 of the external investigator workflow resolves a systematic analytical contamination that affected all output documents. This page explains what was wrong, what was fixed, and what it means for users and integrators.**

---

## The Problem

When an AI system analyses an organisation's strategic execution using a structured methodology, it operates with two distinct analytical objects:

1. **The methodology's prescription** — what the methodology determines as the correct strategy for this subject (the yardstick)
2. **The subject's observable conduct** — what the subject has actually done, reconstructed from open-source intelligence

These are separate things. The yardstick is the methodology's output. The subject's conduct is an empirical observation. They must remain separate throughout every analytical step, every output document, every conclusion delivered to the client.

The v1.0 external investigator workflow allowed these two objects to blur. Not through analytical error, but through subtle linguistic drift that AI-operated workflows are especially prone to:

| What the AI wrote | What it actually meant |
|---|---|
| "The subject's centre of gravity is X" | The methodology identifies X as the centre of gravity for the correct strategy |
| "The subject's campaign architecture consists of three campaigns" | The methodology formulates a three-campaign architecture as the yardstick |
| "The subject's strategic objective is market consolidation" | The methodology determines market consolidation as the correct objective |
| "The subject failed to execute its strategy" | The subject didn't follow the yardstick — but the subject never adopted the yardstick |

The prescription became the description. The yardstick became the measured object. And the client received a report that looked precise but contained a foundational error.

---

## The Fix: Three Analytical Voices

Every output document across all modules now maintains three distinct analytical voices:

### Voice 1 — The Methodology's Voice (prescriptive yardstick)

What the methodology determines as correct.

```
✅ "The methodology determines that..."
✅ "The correct strategy for this subject is..."
✅ "Strategy by AI's formulated strategy prescribes..."
✅ "The methodology identifies the centre of gravity for the correct strategy..."
```

### Voice 2 — The Observational Voice (empirical description)

What the subject's observable conduct indicates about its leadership's actual position.

```
✅ "The subject's observable conduct indicates..."
✅ "The subject's operational pattern suggests its leadership operates as if..."
✅ "What can be deduced from the subject's actions is..."
✅ "The observed behaviour is consistent with a leadership that..."
```

### Voice 3 — The Gap Voice (diagnostic comparison)

The measured distance between the yardstick and the observed conduct.

```
✅ "Where the methodology prescribes X, the subject's actions indicate Y — the gap is..."
✅ "The distance between the methodology's prescription and the subject's observed conduct reveals..."
✅ "The yardstick identifies T1 as the priority target; the subject's resource flow suggests T8 — an inversion that..."
```

### Prohibited Formulations

These blur the line between the yardstick and the subject. They must never appear:

```
❌ "The subject's strategy requires..." (when meaning: the correct strategy requires)
❌ "The subject's centre of gravity is..." (when meaning: the methodology identifies the CoG)
❌ "The subject needs to..." / "must..." / "should..." (when meaning: the yardstick prescribes)
❌ "The subject failed to execute its strategy" (the subject never adopted the yardstick)
```

---

## The New Architecture: Observable Execution Reconstruction

The most significant structural addition is **Prompt 18.5** — inserted into Module Six before any execution assessment begins.

### Before (v1.0)

```
Module Five → Documents 21–24 (the yardstick)
                    ↓
Module Six → Prompts 19–28 assess "the subject's execution" 
             against Documents 21–24 (conflated)
```

### After (v2.0)

```
Module Five → Documents 21–24 (the yardstick)
                    ↓
Prompt 18.5 → Documents 21′–24′ (observable execution reconstruction from OSINT)
                    ↓
Prompts 19–28 → Tripartite comparison:
                 Yardstick (21–24) vs. Observable Execution (21′–24′) vs. Gap
```

### Documents 21′–24′

| Document | Mirrors | Content |
|---|---|---|
| **21′** Observable War Conduct | Doc 21 War Definition | What war does the subject appear to be fighting? |
| **22′** Observable Objectives | Doc 22 Objectives Matrix | What objectives does the subject's resource allocation reveal? |
| **23′** Observable Operations | Doc 23 Campaign Architecture | What campaign-like activities does the subject conduct? |
| **24′** Observable Integration | Doc 24 Strategy Integration | Does the subject's execution cohere into an identifiable pattern? |

These are **Voice 2 documents** — observational, evidence-grounded, never importing the yardstick's categories as the subject's own. The subject may not operate with the yardstick's categories at all.

---

## The Module Six Framing Lock

A specific constraint governing all Module Six content:

> Strategy by AI formulated the ideal strategy (the yardstick) in Module Five. The subject never adopted it and executed something categorically different. Never imply the subject designed a strategy and executed it poorly by mixing the methodology's yardstick with the subject's execution of its own vision. The correct framing: the methodology demonstrates what should have been done; what the subject actually did is measured against what should have been done.

**"ADVANCED analytical maturity"** must not be applied to the subject by reference to the yardstick. It can be applied only to the subject's own analytical capacity if it appears advanced.

---

## Voice Dominance by Module

| Module | Primary Voice | Explanation |
|---|---|---|
| **Two** (Identity) | Voice 2 | Describing what the subject IS from observable evidence |
| **Three** (Enemy-making) | Voice 2 | Mapping the subject's observable hostile environment |
| **Four** (Situation) | Voice 2 | Reconstructing the subject's strategic situation |
| **Five** (Strategy) | Voice 1 only | Producing the yardstick — no gap analysis |
| **Six** (Execution) | All three | Yardstick → Observation → Gap in constant interplay |

---

## What the Client Receives (v2.0)

Three distinct objects, not one:

1. **The Yardstick Strategy** (Documents 21–24) — what the methodology determines as correct for this subject
2. **The Observable Execution** (Documents 21′–24′) — what the subject has actually done, reconstructed from OSINT
3. **The Gap Diagnosis** (Reports 1–10 / Documents 25–34) — the measured distance between them across ten execution dimensions, and what the gap reveals about the subject's institutional strategic capacity

The client decides what to do with this intelligence. The investigator does not advise the subject.

---

## Impact on the De Beers Demonstration

The v1.0 De Beers assessment in the [demonstration](DEMONSTRATION.md) was produced before this correction. If regenerated under v2.0 rules:

- The execution grade (F across six dimensions) would be reframed as a **gap measurement**: the distance between what the methodology prescribes and what De Beers UK observably did
- The "command structure absence" finding would be Voice 2 (observable conduct indicates no identifiable command structure for strategic execution) measured against Voice 1 (the yardstick prescribes a specific command structure)
- The culmination-centre misalignment finding would be Voice 3: "Where the methodology determines capability peak should align with decisive engagement at month M, De Beers UK's observable resource trajectory suggests peak occurred N months before any engagement was attempted — the misalignment gap is fatal"

The analytical conclusions remain the same. The framing becomes defensible.

---

## Integration Implications

For platform integrators, the v2.0 corrections provide:

| Feature | Integration value |
|---|---|
| **Three-voice framework** | Machine-verifiable constraint — automated checks can scan for prohibited formulations |
| **Documents 21–24 / 21′–24′ parallel structure** | Two indexed document sets, compared systematically — a data pipeline, not a prose exercise |
| **Ten-dimensional gap measurement** | Structured output suitable for APIs, dashboards, scoring systems |
| **42+ Document Activation Protocols** | Tool-call specifications for agentic automation |
| **Module Six Framing Lock** | Constitutional constraint for AI alignment frameworks |

→ See [INTEGRATION.md](INTEGRATION.md) for deployment pathways.

---

## What Is NOT in This Repository

The corrected workflow files (Module Two through Six external investigator prompts, version 2.0) are part of the commercial methodology available at [strategybyai.org](https://strategybyai.org). This document explains the correction's logic and architecture. The implementation is in the methodology itself.

---

*This correction affects the external investigator workflow only. The internal expert workflow operates under different analytical assumptions (the subject's leadership has adopted the methodology) and is not subject to the yardstick/observation separation requirement.*
