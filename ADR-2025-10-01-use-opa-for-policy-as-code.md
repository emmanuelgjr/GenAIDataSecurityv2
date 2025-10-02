# ADR-2025-10-01-use-opa-for-policy-as-code

## Context
We need deterministic, reviewable enforcement for agent tool calls and data-access decisions.

## Decision
Adopt Open Policy Agent (OPA/Rego) for policy-as-code across agent components and CI/CD.

## Consequences
+ Centralized, testable policies
- Learning curve for contributors
