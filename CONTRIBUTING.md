# Contributing to Strategy by AI

## How to Contribute

We welcome contributions that expand the methodology's demonstrated applications, improve technical integration documentation, and advance the strategic world models concept.

---

## What We're Looking For

### Case Study Contributions

The De Beers UK assessment demonstrates the methodology on one subject. Additional case studies — applying Strategy by AI to other organisations, political entities, or competitive situations — strengthen the methodology's demonstrated applicability.

**What makes a good case study contribution:**
- Applies the full methodology (Modules Two through Six) or a clearly bounded subset
- Uses publicly available information (OSINT)
- Follows the document portfolio structure (Documents 1–34 or the relevant subset)
- Includes evidence citations with sources and dates
- Acknowledges limitations and information gaps honestly

**How to contribute a case study:**
1. Produce the assessment using the Strategy by AI methodology (available at [strategybyai.org](https://strategybyai.org))
2. Prepare selected excerpts demonstrating key findings (not the complete portfolio — follow the same excerpt approach used for the De Beers demonstration)
3. Open a pull request with excerpts placed in `examples/output-samples/` with a clear naming convention: `[subject]_[document]_excerpt.md`
4. Include a brief README explaining the subject, scope, and key findings

### Integration Examples

Technical demonstrations of the methodology deployed in specific architectures help other developers implement Strategy by AI in their own systems.

**Contributions we'd value:**
- RAG implementation examples with specific vector databases (Pinecone, Weaviate, Chroma, etc.)
- Agentic workflow implementations using specific frameworks (LangChain, CrewAI, AutoGen, etc.)
- Fine-tuning results with specific base models
- Platform-specific setup guides beyond Claude/ChatGPT/Gemini

**How to contribute an integration example:**
1. Place your implementation in `integration/[pathway]/` under the relevant pathway
2. Include a README explaining the architecture, dependencies, and setup steps
3. Include working code or configuration files
4. Document any limitations or platform-specific considerations

### World Models Development

The strategic world models concept is at an early stage. Contributions that advance the architecture, implement transition dynamics, or build simulation capabilities are particularly valuable.

**Contributions we'd value:**
- Extensions to the Python state representation (new query methods, additional consistency checks)
- Transition function implementations (predicting state changes from proposed actions)
- Visualisation tools for strategic state (dashboards, network graphs, timeline views)
- Comparative analysis tools (querying multiple subject instances against each other)
- Benchmarks comparing strategic world model predictions against actual outcomes

**How to contribute to world models:**
1. Place your work in `world-models/` with clear documentation
2. If extending the Python prototype, maintain backward compatibility with existing class structure
3. Include tests demonstrating your contribution works
4. Document the strategic reasoning behind technical decisions — this is a methodology repository, not just a code repository

---

## How to Submit

1. **Fork** the repository
2. **Create a branch** for your contribution (`git checkout -b contribution/your-description`)
3. **Make your changes** following the guidelines above
4. **Test** that all existing links and references still work
5. **Submit a pull request** with a clear description of what you're contributing and why

---

## Standards

### Documentation quality
- Write for the GitHub audience: precise, technically specific, no marketing language
- Include diagrams or code examples where they clarify architecture
- Reference specific methodology sections (by module and section number) where relevant
- Acknowledge limitations honestly

### Code quality
- Python code should run on Python 3.9+
- Include docstrings explaining strategic reasoning, not just technical function
- No external dependencies beyond Python standard library for core classes (additional dependencies acceptable for integration examples with clear documentation)

### Attribution
- Cite the Strategy by AI methodology when referencing its frameworks
- Credit original sources for any OSINT evidence used in case studies
- If your contribution builds on someone else's work in this repository, acknowledge it

---

## What We Don't Accept

- **Methodology files.** The core methodology (modules, full prompt libraries, workflows) is a commercial product and should not be uploaded to this repository.
- **Unsubstantiated claims.** Assertions about organisations or individuals must cite evidence.
- **Marketing content.** This repository demonstrates the methodology through technical documentation and evidence. Promotional language does not belong here.
- **AI-generated filler.** Contributions should reflect genuine analytical or technical work. Padding with generic AI-generated content contradicts the repository's purpose of demonstrating structured, rigorous AI application.

---

## Questions

For questions about contributing, open an issue in the repository or contact us through [strategybyai.org](https://strategybyai.org).

For questions about the methodology itself, visit [strategybyai.org/blog](https://strategybyai.org/blog/) or the [YouTube channel](https://youtube.com/@strategybyai).
