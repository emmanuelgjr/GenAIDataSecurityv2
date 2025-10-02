# OWASP GenAI Data Security Best Practices — v2 (Repo Skeleton)

This repository houses a community-driven, testable, and auditable set of best practices for securing data across LLMs and agentic systems.

## How we work
- **Lazy consensus**: 72h for non-urgent decisions; 24h for urgent fixes.
- **Definition of Done (DoD)** for any section/control:
  1) ≤150-word summary
  2) Normative MUST/SHOULD/MAY controls
  3) Mappings to NIST AI RMF, ISO/IEC 42001, MITRE ATLAS, OWASP LLM/Agentic T10
  4) Testability (audit checks or scripts; red/blue team verifications)
  5) References and example configs/snippets
  6) Changelog entry + ADR if relevant

## Structure
```
/docs
  /chapters
    01-intro.md
    02-traditional-vs-llm.md
    03-key-risks.md
    04-data-lifecycle-security.md
    05-practical-principles.md
    06-monitoring-auditing.md
    07-agentic-data-security.md
    08-secure-deployment.md
    09-governance-compliance.md
    10-future-trends.md
  /appendices
    A-controls-catalog.md
    B-threat-scenarios.md
    C-mappings-nist-iso-atlas.md
    D-glossary.md
/templates
  issue.md
  pr.md
  control.yaml
  risk.csv
/adrs
CODEOWNERS
CONTRIBUTING.md
SECURITY.md
LICENSE
```

## Contribution quick start
1. Open an issue using `/templates/issue.md`.
2. Fork + create a feature branch.
3. Implement changes ensuring DoD is satisfied.
4. Open a PR using `/templates/pr.md`.
