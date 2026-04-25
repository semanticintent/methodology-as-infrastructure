# Methodology-as-Infrastructure: From Framework to Runtime

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18946631.svg)](https://doi.org/10.5281/zenodo.18946631)

**Author:** Michael Shatny ([ORCID](https://orcid.org/0009-0006-2011-3258))

Methodologies are traditionally documents. This paper proposes they can be compiled into deterministic execution layers — infrastructure that other systems build upon.

## Read the Paper

- [Methodology-as-Infrastructure](docs/methodology-as-infrastructure.md)

## Key Argument

| Traditional Methodology | Methodology-as-Infrastructure |
|---|---|
| Describes what to analyze | Executes the analysis |
| Open loop (no feedback) | Closed loop (DRIFT measurement) |
| Domain-specific application | Domain-agnostic pipeline |
| Human interpretation required | Deterministic computation |
| Non-composable | Pipeable into larger systems |

## Evidence Base

- **CAL Runtime** — first MaI implementation, DSL encoding the Cormorant Foraging methodology ([DOI](https://doi.org/10.5281/zenodo.18905193))
- **Phoenix Runtime** — seven-agent legacy modernization pipeline ([DOI](https://doi.org/10.5281/zenodo.19360782))
- **EMBER** — shared artifact language across the MaI ecosystem ([DOI](https://doi.org/10.5281/zenodo.19751387))
- **Strata Runtime** — five-agent database archaeology pipeline ([DOI](https://doi.org/10.5281/zenodo.19768151))
- **42 case studies** — cross-industry CAL validation ([StratIQX](https://intelligence.stratiqx.com))
- **11 DOIs** — immutable academic record across the full stack

See **Appendix B** in the paper: each downstream runtime's `CITATION.cff` references this paper automatically — the citation chain is itself a demonstration of the composability property defined in Section 2.2.

## Related Work

- [Cormorant Foraging Framework](https://doi.org/10.5281/zenodo.18904952)
- [6D Foraging Methodology](https://doi.org/10.5281/zenodo.18209946)
- [CAL Documentation](https://cal.cormorantforaging.dev)
- [Semantic Intent SSOT](https://doi.org/10.5281/zenodo.17114972)

## License

MIT
