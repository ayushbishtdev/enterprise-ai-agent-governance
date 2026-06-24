# AI Agent Lifecycle & Governance Checklist

Traditional application logging only captures system uptime or errors. Autonomous models require behavioral monitoring and strict lifecycle gates. Use this checklist during PI Planning or architectural reviews.

## 1. Identity & Provisioning
- [ ] **Non-Human Identity Issuance:** Agent is assigned a dedicated, cryptographically secure machine identity (distinct from any human user account).
- [ ] **Human Accountability:** A specific business unit leader is documented as the owner. (No generic "IT" ownership).
- [ ] **NIST Mapping:** Risk tier established (Low/Medium/High) based on NIST AI RMF context.

## 2. Agent Identity Scoping (Least Privilege)
- [ ] **Atomic Permissions:** Agent is locked to explicit API methods (e.g., `Read-Only` on specific tables), not blanket database access.
- [ ] **Multi-Agent Authentication:** Cryptographic authentication is enforced for any inter-agent (agent-to-agent) handshakes to prevent lateral privilege escalation.
- [ ] **No Local MCP Bridging:** Developer environments using Model Context Protocol (MCP) are sandbox-isolated from production data.

## 3. Active Production Monitoring
- [ ] **AI TRiSM Observability:** Tooling is in place to track prompt semantic outputs, intent shifts, and token consumption (not just standard uptime).
- [ ] **OAuth Sprawl Prevention:** Agent is restricted from autonomously provisioning secondary micro-sessions or persistent access keys.

## 4. The Kill Switch
- [ ] **Centralized Circuit Breaker:** Platform engineers have an un-bypassable control to instantly revoke the agent's digital tokens.
- [ ] **Blast Radius Containment:** Terminating the agent does not fatally crash downstream enterprise legacy infrastructure.
- [ ] **Tested in Prod:** The kill switch has been successfully tested during standard operational drills.

## 5. Decommissioning & Expiration
- [ ] **Hard Expiry Timestamp:** Agent identity is provisioned with a hard, automated expiration date (e.g., 90 days).
- [ ] **Automated Termination:** If the business owner does not formally re-authorize the deployment, access privileges are automatically revoked.
- [ ] **Orphan Sweep:** Cross-cloud discovery tools verify the agent leaves no persistent ghost loops or active billing cycles upon retirement.
