# Appendix C — Framework Mappings

This appendix provides baseline mappings for LLM & Agentic Data Security controls (v2).  
Each control is mapped to **NIST AI RMF functions**, **ISO/IEC 42001 clauses**, **MITRE ATLAS tactics**, and **OWASP LLM/Agentic Top 10** entries.

---

| Control ID | NIST AI RMF Function | ISO/IEC 42001 | MITRE ATLAS | OWASP Top 10 (LLM/Agentic) | Notes |
|------------|----------------------|---------------|-------------|----------------------------|-------|
| **CTRL-ENC-01 Encryption** | Govern / Manage | 8.3 Data Mgmt | ATLAS:T1620 Data Exfiltration | LLM06 Sensitive Info Disclosure | Encrypt all sensitive data at rest & in transit |
| **CTRL-AC-02 Access Control** | Govern / Manage | 7.1 Access Mgmt | ATLAS:T1606 Unauthorized Access | LLM04 Access Control Failures | ABAC/RBAC, SoD, JIT access |
| **CTRL-OUT-03 Output Moderation** | Govern / Map | 8.5 Output Mgmt | ATLAS:T1602 Prompt Injection | LLM01 Prompt Injection, LLM06 Sensitive Disclosure | Redact/block PII before delivery |
| **AGT-01 Prompt & Policy Integrity** | Govern / Map | 6.2 Policy Mgmt | ATLAS:T1602 Prompt Injection | LLM01 Prompt Injection | Require signed system prompts & runtime verification |
| **AGT-02 Memory Minimization & Encryption** | Govern / Manage | 8.3 Data Mgmt | ATLAS:T1617 Data Poisoning | LLM06 Sensitive Info Disclosure | Encrypt vector DB + redact/tokenize PII |
| **AGT-03 Tool Sandboxing** | Govern / Measure | 7.1 Controls | ATLAS:T1608 Malicious Tool Use | Agentic-03 | Restrict tool egress + schema validation |
| **AGT-04 Scoped Credentials** | Govern / Manage | 7.2 Identity Mgmt | ATLAS:T1606 Unauthorized Access | Agentic-04 | Short-lived tokens, JIT provisioning |
| **AGT-05 Least-Privilege Data Access** | Govern / Manage | 7.3 Data Security | ATLAS:T1606 Unauthorized Access | Agentic-02 | Deny-by-default queries, sensitivity labels |
| **AGT-06 Output Moderation & Redaction** | Govern / Map | 8.5 Output Mgmt | ATLAS:T1602 Prompt Injection | LLM06 Sensitive Disclosure | Policy-based redaction before delivery |
| **AGT-07 Behavior & Anomaly Monitoring** | Govern / Measure | 9.2 Monitoring | ATLAS:T1621 Anomaly Detection | LLM08 Monitoring Gaps | Schema logs, drift detection |
| **AGT-08 Incident Response for Agents** | Govern / Manage | 9.3 IR Mgmt | ATLAS:T1615 Impact Response | LLM07 Incident Response | Playbooks for memory purge, key rotation |
| **AGT-09 Supply Chain Hygiene** | Govern / Map | 6.4 Supply Chain Security | ATLAS:T1584 Dependency Abuse | LLM05 Supply Chain | Use SLSA + Cosign verify |
| **AGT-10 Adversarial Testing** | Govern / Measure | 9.4 Testing | ATLAS:T1602 Prompt Injection, T1617 Data Poisoning | LLM09 Testing & Evaluation Gaps | Red-team prompts, fuzzing |
| **AGT-11 PQC Readiness** | Govern / Map | 8.7 Cryptography | ATLAS:T1622 Cryptographic Weakness | Agentic-07 | Hybrid KEMs for long-lived keys |
| **AGT-12 Privacy by Design** | Govern / Map | 8.8 Privacy | ATLAS:T1617 Data Poisoning | LLM06 Sensitive Disclosure | PETs, DP, privacy impact assessments |

---

**Notes:**
- NIST AI RMF functions: Govern, Map, Measure, Manage.
- ISO/IEC 42001 clauses approximated from draft structure.
- MITRE ATLAS tactics aligned to adversarial ML behaviors.
- OWASP Top 10 entries: 2026 LLM & Agentic draft IDs.
