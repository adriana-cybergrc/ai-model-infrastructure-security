# R3 Research Closure — AI Model Infrastructure Security

**Decision date:** 2026-11-14  
**Decision:** NO-GO — close as an independent research candidate  
**Scope reviewed:** attack propagation, privilege relationships, security boundaries across AI models, agents, tools, identities, APIs, connectors, and enterprise infrastructure; narrowed hypothesis of compositional authority and attack reachability.

## 1. Executive decision

The broad R3 framing is not independently differentiated from attack-graph analysis, agent threat modeling, agent inventories/bills of materials, and existing agent-security taxonomies.

The narrowed residual hypothesis — formal composition of authority across multi-agent delegation, including attenuation, revocation, shared budgets, and enforcement at consequential resource boundaries — also fails the current originality gate. Recent 2026 technical drafts describe these mechanisms directly, including delegation graphs, non-amplifying authority, multi-hop delegation, revocation, concurrent branches, shared effect budgets, protected accounting, atomic reservations, and resource-side verification. Other 2026 material addresses cross-organizational delegation and revocation freshness.

Some of these sources are Internet-Drafts or independent technical proposals rather than finalized standards or peer-reviewed evidence. They are not treated as proof of industry adoption. They nevertheless demonstrate that the proposed mechanism-level combination is already being articulated, so the present R3 framing cannot be defended as original.

## 2. Candidate formulations reviewed

### R3-A — broad infrastructure attack propagation

Model attack paths and privilege relationships across models, agents, tools, identities, APIs, connectors, and enterprise infrastructure.

**Reduction:** this is covered in substantial part by attack graphs, agent threat modeling, multi-layer security frameworks, and agent component inventories. Adding AI-specific node types or additional graph attributes is not sufficient novelty.

### R3-B — compositional authority and containment

Establish formal properties for authority propagation and containment across dynamic, multi-agent enterprise environments.

Candidate properties included:

- delegated authority cannot exceed the authority of the delegator;
- revocation invalidates descendant delegations and stale credentials;
- concurrent delegation cannot multiply a shared consequential-effect budget;
- a tool or connector change cannot silently expand the effect authorized by the originating principal;
- actual resource-side execution is checked against current authority rather than relying only on upstream task descriptions.

**Reduction and direct overlap:**

- The 2026 IETF Internet-Draft *Multi-Agent Authority Control* describes protected delegation graphs, constrained authority subsets, delegation depth, authorization generations, shared effect budgets, and rules against unauthorized permission aggregation.
- The same draft explicitly addresses concurrent delegation and shared budgets, protected accounting, atomic reservation, duplicate spending, distributed consistency, and offline suballocations.
- The 2026 WIMSE cross-organizational delegation draft addresses recursive delegation, authority attenuation, cross-domain revocation/freshness, and composable audit.
- The 2026 agent-principal-binding draft separates identity, authority, delegation state, verifier responsibility, freshness, and fail-closed behavior.
- Other 2026 technical drafts discuss revocation closure and time-indexed capability graphs.

These antecedents substantially overlap the proposed residual contribution. Recasting them as an AI-infrastructure security framework would not establish a distinct formal result.

## 3. Prior-art references

1. *Secure AI Execution-Finality, Part 5: Multi-Agent Delegation, Conflict Arbitration, and Quorum Authority*, Internet-Draft, October 2026. https://datatracker.ietf.org/doc/draft-das-multi-agent-authority-control/
2. *Cross-Organizational Delegation for Workload Identity in Multi-System Environments (WIMSE)*, Internet-Draft, 2026. https://datatracker.ietf.org/doc/draft-reece-wimse-cross-org-delegation/
3. *Security Principal and Verifier Binding for Agent Communication Protocols*, Internet-Draft, August 2026. https://www.ietf.org/ietf-ftp/internet-drafts/draft-bu-agentproto-security-principal-binding-06.html
4. *Boundary Jurisdiction Architecture for Agentic and Delegated Systems*, Internet-Draft, 2026. https://datatracker.ietf.org/doc/draft-watts-boundary-jurisdiction-architecture/
5. *Authenticated Delegation Between Autonomous AI Agents* (2026). https://doi.org/10.5281/zenodo.22727194
6. OWASP Agentic Top 10. https://owasp.org/www-project-top-10-for-large-language-model-applications/
7. OWASP MAESTRO. https://genai.owasp.org/

## 4. Rejection rationale

R3 is closed because:

- the broad graph-based threat model reduces to existing attack-graph and agent threat-modeling approaches;
- authority attenuation and multi-hop delegation are already explicitly addressed;
- revocation propagation and descendant invalidation are already specified in current agent identity/delegation proposals;
- concurrent delegation with shared budgets, atomic reservations, and distributed accounting is directly described in a 2026 Internet-Draft;
- no independent compositional theorem, algorithmic guarantee, or counterexample class was established that is not already covered by these approaches.

This is a decision about the current candidate framing, not a claim that all enterprise agent-infrastructure security problems are solved.

## 5. What is preserved

- Original repository scaffold and all pre-existing files.
- Original research scope and candidate framing.
- This negative decision record and its references.
- The distinction between attack-path discovery, identity, authority, delegation, revocation, resource-side enforcement, and execution effects.

No source code, prototype, benchmark, dataset, or experimental claim is authorized by this closure.

## 6. Final status

**CLOSED — NO-GO as an independent research candidate (2026-11-14).**

Reopening requires a materially different question, focused prior-art review, formal semantics for authority and effects, and a demonstrated result that cannot be reduced to attack graphs, capability security, delegated authorization, distributed budget accounting, or existing agent identity/delegation proposals.

No novelty claim is made.
