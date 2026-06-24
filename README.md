# Enterprise AI Agent Governance & TRiSM Framework

A practical toolkit for Platform Engineering and Security teams to discover, govern, and secure autonomous AI agents. Unlike passive SaaS applications (Shadow IT), AI agents introduce active operational risk through autonomous read/write execution and cross-cloud API handshakes. This repository provides the frameworks, registry templates, and lifecycle controls needed to secure non-human identities. Last updated: June 2026.

### What's in this repo:
* [The AI Agent Sprawl Threat](#the-ai-agent-sprawl-threat)
* [The Governance Framework & Lifecycle](#the-governance-framework--lifecycle)
* [Building the Agent Registry (CMDB)](#building-the-agent-registry-cmdb)
* [Surviving the EU AI Act Audit](#surviving-the-eu-ai-act-audit)
* [Quick Reference Assets](#quick-reference-assets) (CSV templates & checklists)

---

## The AI Agent Sprawl Threat

Shadow IT involves passive, unsanctioned applications. AI agent sprawl involves non-human identities possessing active read and write permissions, making independent system decisions without direct human oversight. The most dangerous vectors today are low-code automation tools and unauthorized **Model Context Protocol (MCP)** servers, which allow open-source LLM clients to bridge directly into local file systems and databases.

**Key Threat Vectors:**
* **OAuth Token Sprawl:** Agents autonomously provisioning persistent access keys to keep background connections active.
* **Recursive Logic Loops:** Poorly prompted agents racking up thousands of dollars in hidden API/compute costs over a single weekend.
* **Lateral Movement:** Over-permissioned agents acting as access points for data exfiltration.

**Full breakdown:** [Shadow AI Agents: Find Them Before Auditors Do](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/shadow-ai-agent-governance.html)

---

## The Governance Framework & Lifecycle

Attempting to universally block generative AI endpoints fails, driving staff to personal devices and completely eliminating IT visibility. True enterprise protection requires adaptive, risk-tiered guardrails mapped to the **NIST AI RMF** (Govern, Map, Measure, Manage). 

An agent's operational lifespan is highly dynamic and requires strict controls from provisioning to retirement:

1. **Identity Provisioning:** Issuing unique, cryptographically verifiable non-human identities separate from human IAM.
2. **Granular Scoping:** Restricting authorization to specific records and unique API methods (Least Privilege).
3. **Runtime Monitoring:** Deploying AI TRiSM layers to analyze prompt logic and token consumption.
4. **The Kill Switch:** An un-bypassable operational control to instantly revoke cryptographic tokens if an agent hallucinates or goes rogue.

**Full breakdown:** [AI Agent Lifecycle: From Provisioning to Retirement](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-lifecycle-management.html)

---

## Building the Agent Registry (CMDB)

You cannot manage what you cannot see. Traditional CMDBs track static IT assets; an AI Agent Registry must track dynamic, behavioral entities. Manual spreadsheets fail within weeks due to the speed of low-code deployments. This requires automated cross-cloud discovery.

**Mandatory Registry Fields:**

| Field | Purpose | Audit Requirement |
| :--- | :--- | :--- |
| **Agent Identity ID** | Cryptographic tracking of the non-human entity | Identity mapping |
| **Human Owner** | Specific business unit leader (Never generic "IT") | Accountability |
| **Foundational Model** | Underlying LLM dependency (e.g., GPT-4o, Claude 3.5) | Dependency tracking |
| **API Scopes** | Exact read/write permissions mapped to databases | Least-privilege proof |
| **Kill Switch Status** | Verification of automated termination protocol | Risk mitigation |

**Full breakdown:** [How to Build an AI Agent Registry That Holds](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-registry-inventory.html)

---

## Surviving the EU AI Act Audit

With General Purpose AI (GPAI) enforcement milestones hitting critical phases by August 2026, regulators are explicitly targeting active, non-human identities. Non-compliance under the EU AI Act can trigger penalties reaching up to **35 million Euros or 7% of worldwide annual turnover**.

Auditors do not accept generic acceptable-use policies. They demand immutable artifacts:
* Automated cross-cloud discovery logs.
* Documented human ownership assignments.
* Proof that emergency operational kill switches have been successfully tested in production.

**Full breakdown:** [Will Your AI Agents Survive an EU AI Act Audit?](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-governance-audit-compliance.html)

---

## Quick Reference Assets

Standalone resources to operationalize agent governance in your enterprise:

* [`data/ai-agent-registry-template.csv`](data/ai-agent-registry-template.csv) - A ready-to-use CSV template containing all mandatory metadata fields required to pass an ISO 42001 / EU AI Act inventory audit.
* [`LIFECYCLE-CHECKLIST.md`](LIFECYCLE-CHECKLIST.md) - A step-by-step checklist for Platform Engineers, spanning identity provisioning to automated decommissioning.
* [`TRISM-EVALUATION.md`](TRISM-EVALUATION.md) - A dense cheatsheet on evaluating AI Trust, Risk, and Security Management (TRiSM) platforms vs. legacy CASB tools, including notes on Microsoft Agent 365.

---

## Sources & Deeper Reading

All data, frameworks, and compliance benchmarks in this repository are sourced from the Agile Leadership Day Enterprise Playbook:

* [AI Agent Sprawl: The Risk Nobody Is Tracking](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/what-is-ai-agent-sprawl.html)
* [Enterprise AI Agent Sprawl: Governance Playbook](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/enterprise-ai-agent-sprawl-governance.html)
* [Shadow AI Agents: Find Them Before Auditors Do](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/shadow-ai-agent-governance.html)
* [The AI Agent Governance Framework, Step by Step](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-governance-framework.html)
* [AI Agent Lifecycle: From Provisioning to Retirement](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-lifecycle-management.html)
* [How to Build an AI Agent Registry That Holds](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-registry-inventory.html)
* [Will Your AI Agents Survive an EU AI Act Audit?](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-agent-governance-audit-compliance.html)
* [AI TRiSM Tools: What Actually Governs Agents](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/ai-trism-tools-comparison.html)
* [Microsoft Agent 365 Review: Control Plane or Hype?](https://agileleadershipdayindia.org/blogs/enterprise-ai-agent-sprawl-governance/microsoft-agent-365-review.html)

---

## Contributing / Corrections
Regulatory frameworks (EU AI Act, NIST RMF, ISO 42001) and TRiSM capabilities evolve rapidly. If you spot an outdated compliance benchmark or have an addition to the lifecycle checklist, please open an Issue or submit a Pull Request.

---
*Created by [Ayush Bisht](https://agileleadershipdayindia.org), Content Engineer and AI Tools Specialist at AgileWow.*
