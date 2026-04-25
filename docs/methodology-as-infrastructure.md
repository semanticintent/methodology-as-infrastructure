# Methodology-as-Infrastructure: From Framework to Runtime

**Michael Shatny**
ORCID: [0009-0006-2011-3258](https://orcid.org/0009-0006-2011-3258)

March 2026

---

## Abstract

Methodologies are traditionally descriptive — documents that explain *how* to think about a problem but leave execution to human interpretation. This paper proposes **Methodology-as-Infrastructure (MaI)**: the concept that analytical methodologies can be compiled into deterministic execution layers, transforming frameworks from documents people read into runtime infrastructure that systems build upon.

Using CAL (Cascade Analysis Language) as the primary case study, we demonstrate how a 6-dimensional cascade analysis methodology was encoded into a domain-specific language with 10 keywords, 3 formulas, and a PEG parser — producing a deterministic pipeline that operates identically across domains without modification. 42 cross-industry case studies validate the approach across technology, sports, healthcare, finance, and domain-specific languages themselves.

The concept extends the established "-as-a-Service" and "-as-Code" paradigms into a new category: methodology that becomes the infrastructure other systems build upon.

---

## 1. The Problem: Methodologies Are Documents, Not Systems

Analytical methodologies — from Six Sigma to SWOT to Porter's Five Forces — share a common limitation: they describe *what to analyze* but leave *how to execute* to the practitioner. This creates three systemic problems:

**1.1 Non-determinism.** Two analysts applying the same methodology to the same data will produce different results. The methodology specifies dimensions and concepts but not computation. Outcomes depend on interpretation, experience, and cognitive bias.

**1.2 Open-loop execution.** Most methodologies are one-directional: analyze, then recommend. There is no feedback mechanism to measure the gap between the methodology's intent and the actual performance observed. The loop never closes.

**1.3 Non-composability.** Methodologies cannot be chained, piped, or integrated into automated systems. A SWOT analysis cannot feed into a decision engine without human translation. The methodology exists outside the system it is meant to inform.

These limitations are not bugs — they are consequences of methodologies being *descriptive* rather than *executable*. The question this paper addresses: **What happens when a methodology becomes code?**

---

## 2. The Concept: Methodology-as-Infrastructure

### 2.1 Definition

**Methodology-as-Infrastructure (MaI)** is the practice of encoding an analytical methodology into a deterministic, executable runtime layer that other systems can build upon — without requiring human interpretation at execution time.

MaI is distinct from adjacent concepts:

| Paradigm | What it encodes | Execution model |
|---|---|---|
| Infrastructure-as-Code | Server provisioning | Declarative config → cloud resources |
| Policy-as-Code | Compliance rules | Rule evaluation → pass/fail |
| Configuration-as-Code | System settings | Key-value → runtime behavior |
| **Methodology-as-Infrastructure** | **Analytical framework** | **Methodology → deterministic analysis → decisions** |

The key distinction: MaI encodes *how to think about a problem*, not just how to provision resources or enforce rules.

### 2.2 Requirements

For a methodology to qualify as infrastructure, it must satisfy four properties:

1. **Deterministic.** Same input, same output. No interpretation variance.
2. **Closed-loop.** Built-in measurement of the gap between intent and performance (not just analysis, but assessment of the analysis).
3. **Domain-agnostic.** The methodology is fixed; the data is variable. The same pipeline processes a corporate crisis and a trading signal.
4. **Composable.** Output of one stage feeds the next. The pipeline can be integrated into larger systems without human translation.

### 2.3 The "-as-Infrastructure" Distinction

The "-as-a-Service" paradigm (SaaS, PaaS, IaaS) abstracts complexity behind APIs. The "-as-Code" paradigm (IaC, PaC) makes configuration versionable and reproducible. MaI goes further: it makes *analytical reasoning* versionable, reproducible, and executable.

A methodology encoded as infrastructure is:
- **Citable** — versioned, with DOI, traceable to its author
- **Forkable** — others can extend or adapt the methodology
- **Executable** — runs without human interpretation
- **Auditable** — every decision has a deterministic trace

---

## 3. Case Study: CAL (Cascade Analysis Language)

### 3.1 The Methodology

The Cormorant Foraging Framework [1] provides a multi-layered architecture for intelligence systems, organized around six dimensions (the 6D Methodology [2]):

- **D1** Customer Impact
- **D2** Employee/Operational Workforce
- **D3** Revenue/Financial
- **D4** Regulatory/Compliance
- **D5** Quality/Brand
- **D6** Operational/Supply Chain

The methodology specifies a five-stage pipeline: **Sense → Analyze → Measure → Decide → Act.**

### 3.2 The Compilation

CAL [3] encodes this methodology into a domain-specific language with:

- **10 keywords** mapping directly to methodology layers: `FORAGE`, `DIVE`, `PERCH`, `LISTEN`, `WAKE`, `CHIRP`, `TRACE`, `SURFACE`, `DRIFT`, `FETCH`
- **3 formulas** providing deterministic computation:
  - 3D Lens: `(Sound × Space × Time) / 10`
  - DRIFT: `Methodology - Performance`
  - FETCH: `Chirp × |DRIFT| × Confidence`
- **PEG parser** producing an AST from CAL scripts
- **Deterministic executor** that processes the AST against any data source via pluggable adapters

The keywords are not arbitrary — each maps to a specific layer of the methodology:

| Keyword | Methodology Layer | Function |
|---|---|---|
| FORAGE | Sense | Scan for entities matching criteria |
| DIVE | Analyze | Deep-dive into specific dimensions |
| PERCH | Analyze | Establish observation point |
| LISTEN | Sense | Monitor for signals |
| WAKE | Sense | Trigger on threshold breach |
| CHIRP | Act | Emit alert or notification |
| TRACE | Analyze | Follow cascade pathway |
| SURFACE | Measure | Extract results |
| DRIFT | Measure | Quantify methodology-performance gap |
| FETCH | Decide | Compute action score, determine response |

### 3.3 The Infrastructure Property

A CAL script is methodology made executable:

```cal
FORAGE entities WHERE sound > 7
ACROSS D1, D2, D3, D5, D6
DEPTH 3
SURFACE cascade_map

DRIFT cascade_map METHODOLOGY 85 PERFORMANCE 35
FETCH cascade_map THRESHOLD 1000
ON EXECUTE CHIRP critical "Act now"
```

This script encodes: scan for high-signal entities across five dimensions, map cascade depth to 3 levels, measure the gap between expected and actual performance (DRIFT = 50), compute an action score, and if the threshold is met, execute the response.

The same script structure processes a corporate crisis, a sports franchise collapse, or a technology adoption pattern. The methodology is fixed. The data adapters change.

### 3.4 Validation: 42 Case Studies

42 published case studies [4] validate the approach across domains:

- **Technology:** SaaS platform failures, open-source adoption cascades, AI tool commoditization
- **Sports:** Franchise management failures (NHL, NFL, MLB)
- **Healthcare:** Organizational cascade patterns
- **Finance:** Market signal analysis
- **Self-referential:** CAL analyzing its own cascade pattern (UC-038)

Each case study applies the identical pipeline — same keywords, same formulas, same executor — to different domain data. The consistency of results across domains demonstrates the infrastructure property: the methodology layer is domain-agnostic.

---

## 4. The Semantic Intent Pattern

### 4.1 AI Integration Without Fine-Tuning

A critical implementation detail: CAL operates within AI systems through the **Semantic Intent** pattern [5] — embedding scoring rubrics and methodology directly into MCP (Model Context Protocol) tool definitions. The AI reads the methodology from the tool schema, applies it to the data, and produces structured output.

This means:
- **Zero fine-tuning** — the methodology is in the tool definition, not the model weights
- **Zero external API calls** — the AI context window is the execution environment
- **Full auditability** — the rubric is visible in the tool schema

### 4.2 Implications

The Semantic Intent pattern demonstrates that methodology-as-infrastructure is compatible with AI-native architectures. The methodology doesn't compete with the AI — it provides the structured layer the AI executes within.

---

## 5. Discussion

### 5.1 When Does a Methodology Qualify?

Not every methodology can or should become infrastructure. MaI is appropriate when:

- The methodology has **quantifiable dimensions** (not purely qualitative)
- Analysis follows a **repeatable pipeline** (not ad-hoc exploration)
- Decisions can be **threshold-driven** (not purely judgment-based)
- The methodology is **domain-agnostic** in structure (dimensions flex, pipeline is fixed)

Methodologies like SWOT (qualitative, no computation) or brainstorming frameworks (divergent, non-deterministic) are poor candidates. Methodologies like risk scoring, cascade analysis, or signal detection are strong candidates.

### 5.2 The Credit Problem

Open-source infrastructure faces an attribution challenge: the more successful the infrastructure, the more invisible the creator becomes. Linux powers the internet; few users know Linus Torvalds. .netTiers generated data access layers for enterprise applications; its contributors remained anonymous behind handles.

MaI addresses this through:
- **DOIs** — immutable, timestamped academic citations
- **ORCID** — author identity linked across all publications
- **CITATION.cff** — machine-readable attribution in every repository
- **Case studies** — a body of evidence that demonstrates the methodology in action, not just the code

The combination of open-source accessibility and academic citation infrastructure creates a model where the methodology can be freely used while attribution remains permanent. Section 2.2 defines composability as output feeding the next stage without human translation. The citation chain is that property made visible: the paper's DOI propagates forward through every downstream runtime automatically, without anyone deciding to carry it. See Appendix B.

### 5.3 Relationship to Existing Paradigms

MaI sits at the intersection of several established fields:

- **Domain-Specific Languages (DSLs):** CAL is a DSL, but MaI is not limited to DSLs. A methodology could be encoded as a library, a protocol, or a configuration schema.
- **Knowledge Engineering:** MaI shares the goal of making expert knowledge executable, but differs in targeting *methodological reasoning* rather than domain facts.
- **Computational Social Science:** MaI provides deterministic tools for analyzing organizational and social phenomena, complementing statistical approaches.

---

## 6. Conclusion

Methodology-as-Infrastructure proposes that the boundary between "how to think" and "how to execute" is artificial. When a methodology is rigorous enough to be deterministic, it can be compiled into a runtime layer that other systems build upon.

CAL demonstrates this with 10 keywords, 3 formulas, 42 case studies, and a working runtime. The methodology didn't describe cascade analysis — it *became* cascade analysis infrastructure.

The concept is not limited to CAL or cascade analysis. Any methodology that satisfies the four properties (deterministic, closed-loop, domain-agnostic, composable) is a candidate for compilation into infrastructure. The tools exist: PEG parsers, MCP protocols, Zenodo DOIs, and AI systems capable of executing structured methodologies from tool definitions.

The question is no longer whether methodologies *can* become infrastructure. The question is which methodologies *should*.

---

## References

[1] M. Shatny, "Cormorant Foraging Framework: A Multi-Layered Architecture for Intelligence Systems," 2026. DOI: [10.5281/zenodo.18904952](https://doi.org/10.5281/zenodo.18904952)

[2] M. Shatny, "6D Foraging Methodology: Strategic Dimensional Discovery," 2025. DOI: [10.5281/zenodo.18209946](https://doi.org/10.5281/zenodo.18209946)

[3] M. Shatny, "CAL Runtime: Cormorant Agentic Language Execution Engine," 2026. DOI: [10.5281/zenodo.18905193](https://doi.org/10.5281/zenodo.18905193)

[4] M. Shatny, "StratIQX Case Studies: 6D Cascade Analysis," 2025-2026. Available: [https://intelligence.stratiqx.com](https://intelligence.stratiqx.com)

[5] M. Shatny, "Semantic Intent SSOT," 2025. DOI: [10.5281/zenodo.17114972](https://doi.org/10.5281/zenodo.17114972)

---

## Appendix A: The Self-Referential Validation

UC-038 ("The Self-Referential Cascade") applied CAL's own methodology to analyze CAL's development. The analysis found:

- **6/6 dimensions amplified** (D4 moderate at 42, remaining 5 strong at 55-78)
- **DRIFT score: 50** (Methodology 85, Performance 35) — indicating significant untapped potential
- **FETCH score: 2,405** (Chirp 61.7 × |DRIFT| 50 × Confidence 0.78) — well above the EXECUTE threshold of 1,000
- **Cascade multiplier: 6×-10×** (Severe range)

The language exhibited the cascade pattern it was designed to detect — validating both the methodology and the infrastructure encoding simultaneously.

---

## Appendix B: The Ecosystem as Composability Proof

Section 2.2 defines four properties that a methodology must satisfy to qualify as infrastructure. Three of them — deterministic, closed-loop, domain-agnostic — can be demonstrated by running CAL against data and inspecting the output. The fourth, **composability**, is harder to demonstrate in a single execution. Composability means the output of one stage feeds the next without human translation.

The citation chain across the MaI ecosystem is that property made concrete.

Each runtime that instantiates the MaI pattern carries a `CITATION.cff` that references this paper by DOI. The chain as of April 2026:

| Runtime | DOI | References this paper |
|---|---|---|
| CAL Runtime | 10.5281/zenodo.18905193 | Yes — via CITATION.cff |
| Phoenix Runtime | 10.5281/zenodo.19360782 | Yes — via CITATION.cff |
| EMBER | 10.5281/zenodo.19751387 | Yes — via CITATION.cff |
| Strata Runtime | 10.5281/zenodo.19768151 | Yes — via CITATION.cff |

No human decided to carry the citation forward at each step. The CITATION.cff standard made it automatic — a machine-readable contract that propagates with the artifact. When a new runtime is built in this ecosystem, the citation is inherited by convention, not by choice.

This is composability. The paper's DOI is the output of stage zero. Every downstream runtime is a subsequent stage that consumes it. The chain grows without human translation at each joint.

It also closes the loop on Section 5.2. The credit problem in open-source infrastructure is that attribution degrades as distance from the source increases. The citation chain inverts that: the more runtimes that instantiate the MaI pattern, the more times the paper is cited, and the more permanent the attribution becomes. Success amplifies attribution rather than eroding it.

The ecosystem does not merely *apply* the MaI thesis. It *demonstrates* it.
