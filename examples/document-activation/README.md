# Perspective 6: Document Activation Protocols

## Demonstration: How Module Six Systematically References All Preceding Documents

Module Six does not read preceding documents once and summarise them. It activates specific documents through prescribed protocols for each execution challenge, specifying WHICH documents, WHICH sections, and WHAT questions to ask.

---

## Protocol Structure

Each execution issue in Module Six triggers a defined activation:

```
Execution issue  →  Methodology section  →  Documents activated  →  Specific queries  →  Finding
```

---

## Example Protocols from De Beers Assessment (Document 34)

### Protocol 1 — Commitment Threshold

```
Activation reference: §6.1.4
Documents activated: 1, 2, 3, 21, 22, 23, 24

Queries:
  Doc 1: Does organisation demonstrate mission commitment beyond rhetoric?
  Doc 2: What historical pattern of commitment exists (persist vs abandon)?
  Doc 3: Does doctrine support sustained commitment under pressure?
  Doc 21: Has the war been formally committed to?
  Doc 22: Have objectives been resourced, not merely stated?
  Doc 23: Have campaigns been initiated, not merely designed?
  Doc 24: Have strategy change triggers been specified, indicating
          prepared commitment rather than open-ended exploration?

Finding: MARGINAL commitment — threshold crossed in 3 of 5 components.
De Beers staked reputation and accepted opportunity costs but failed
to deploy resources or establish organisational structure.
```

### Protocol 4 — Decision Authority

```
Activation reference: §6.4.1.2
Documents activated: 21, 22, 23, 24, 25

Queries:
  Doc 21: Does war definition establish clear Tier 1 decision boundaries?
  Doc 22: Does objectives hierarchy establish Tier 2 decision scope?
  Doc 23: Do campaign architectures establish Tier 3 authority limits?
  Doc 24: Does strategy integration specify adjustment triggers
          classifiable by decision tier?
  Doc 25: Does preparation assessment confirm command structure
          constituted to exercise tiered authority?

Finding: Documentary foundation ADEQUATE — Documents 21–24 collectively
establish clear decision frameworks. Operational translation DEFICIENT —
no war room constituted, no decision classification matrix operational,
no escalation protocols specified. The strategy has decision rules
but no decision-making apparatus to apply them.
```

### Protocol 10 — External Opposition

```
Activation reference: §6.5
Documents activated: 5, 6, 7, 9, 11, 19, 22

Queries:
  Doc 5: What is current opposition force characterisation?
  Doc 6: Has enemy hierarchy shifted since initial classification?
  Doc 7: Has confrontation intensity changed on any front?
  Doc 9: Have enemy capabilities evolved beyond profiled parameters?
  Doc 11: Which outcome scenarios are materialising?
  Doc 19: Has strategic situation assessment baseline shifted?
  Doc 22: Are strategic targets still accessible at predicted levels?

Finding: Opposition characterisation SOPHISTICATED at documentary
level — Module Three's 28-entity classification remains accurate.
Engagement with opposition: ZERO. All nine targets survive at
full capability. No enemy has been contested on any front.
```

---

## The Complete Activation Registry (Document 34)

Document 34 includes a full registry of all protocols executed across Documents 25–33:

| Protocol | Reference | Documents | Finding |
|----------|-----------|-----------|---------|
| 1 | Commitment §6.1.4 | 1, 2, 3, 21–24 | MARGINAL |
| 2 | Resource Extraction §6.10.3.3 | 8, 23 | 42% gap exceeds 30% critical threshold |
| 3 | Irreversibility §6.1.4.5–6 | 2, 3, 24 | PARTIAL management |
| 4 | Decision Authority §6.4.1.2 | 21–25 | Documentary adequate, operational DEFICIENT |
| 5 | Hierarchy Alignment §6.4.1.3–4 | 21–24 | Documentary coherent, operational MISALIGNED |
| 6 | System Robustness §6.4.2 | 2, 8, 16, 22–24, 26 | ZERO redundancy, ZERO backup protocols |
| 7 | Adaptive Authority §6.4.2 | 21, 23, 24 | Constraints adequate, leadership ABSENT |
| 8 | Command-Campaign Integration §6.4 | 22–24 | DYSFUNCTIONAL |
| 9 | Crisis Command §6.4 | 21, 23–26 | Path A/B fork UNRESOLVED |
| 10 | External Opposition §6.5 | 5–7, 9, 11, 19, 22 | Characterisation sophisticated, engagement ZERO |

Each protocol is traceable: you can verify which documents were queried, what was found, and how that finding contributed to the final verdict.

---

## Why This Matters for AI Developers

### Auditability

Every conclusion in Document 34 traces to a specific activation protocol, which traces to specific documents, which trace to specific evidence. This is the opposite of a black-box verdict — it is a transparent chain of reasoning.

### Reproducibility

The protocols are prescriptive. A different AI assistant, given the same 24 input documents and the same activation protocols, should produce substantially similar findings. The methodology constrains the AI's reasoning, making outputs reproducible rather than dependent on model personality.

### Agent implementation

Each activation protocol is a structured query against a document store:

```python
# Pseudocode for agentic implementation
def execute_protocol(protocol_ref, document_store):
    docs = protocol_ref.required_documents
    queries = protocol_ref.prescribed_queries
    
    findings = []
    for doc_id, query in zip(docs, queries):
        document = document_store.retrieve(doc_id)
        finding = analyze(document, query)
        findings.append(finding)
    
    return synthesize(findings, protocol_ref.resolution_criteria)
```

This directly implements the methodology's execution assessment as an automated workflow.

→ [Back to Architecture](../../docs/ARCHITECTURE.md) | [Next: Output Samples](../output-samples/)
