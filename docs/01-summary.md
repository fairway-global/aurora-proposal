# 1. Summary
## Proposal at a Glance
| Category | Summary |
| ----- | ----- |
| **Treasury Request** | **940,000 ADA** |
| **Delivery Period** | Approximately **5 months** |
| **Purpose** | Establish shared open-source market infrastructure for Cardano credit markets, making credit opportunities discoverable, filterable, verifiable and easier to evaluate across compatible lending implementations |
| **Primary Deliverables** | Metadata Standard, Verification Framework, Aurora Discovery Engine, open APIs, filtering and query tooling, Capital Provider Profile Standard, Reference Query Library, developer tooling, reference implementation, documentation and independent review |
| **Milestones** | **4 implementation milestones** |
| **Lead Implementer** | **Fairway** |
| **Technical Collaborator** | **Sundial** |
| **Technical Advisor** | **Fallen Icarus (Rusty)** |
| **Treasury Custody** | One dedicated **3-of-5 Aurora Treasury multisignature**, with all five keys held independently of the implementation participants |
| **Open Source** | Treasury-funded software, standards and reference implementations released under **Apache License 2.0** |

## Proposal Summary
Cardano's eUTxO model allows individual credit opportunities to exist as distinct on-chain financial objects rather than requiring all lending activity to be organized through pooled liquidity. For the purposes of this proposal, a **Loan Request UTxO** refers to a UTxO created by compatible lending infrastructure that represents an individual funding request or credit opportunity.

That transaction-based architecture provides the foundation for open credit markets, but settlement alone does not create a coherent market. Capital providers and applications still need consistent ways to describe opportunities, discover them across implementations, filter them according to relevant criteria, evaluate verification information and monitor the information associated with them.

Aurora provides that shared market layer.

Like other foundational Cardano infrastructure, Aurora is designed as common standards and tooling that multiple protocols, applications and capital providers can adopt and operate across the ecosystem.

Standardized metadata can enrich a Loan Request UTxO with machine-readable market information and verification references. The Aurora Discovery Engine indexes those opportunities and exposes them through open discovery and filtering interfaces. The Verification Framework allows compatible applications and capital providers to evaluate attached proofs or verification references according to their own requirements.

Aurora does not replace the underlying lending protocols. It does not originate loans, custody lending capital or decide which opportunities should receive funding. Lending execution remains with compatible credit-market infrastructure. Aurora provides the open standards and software around those lending agreements that allow otherwise independent opportunities to become discoverable, filterable and verifiable through common infrastructure.

The Treasury-funded implementation therefore focuses on building and validating the shared technical infrastructure described in this proposal.

## Core Public Outputs
Treasury funding produces a common set of reusable public outputs:

* **Metadata Standard** for describing Aurora-compatible credit opportunities and associated metadata references.
* **Verification Framework** for attaching and evaluating institutional, eligibility, compliance and other proof-based information.
* **Aurora Discovery Engine** for indexing, discovery, filtering, verification-information exposure and relevant lifecycle visibility.
* **Open APIs and filtering capabilities** for compatible applications and capital providers.
* **Capital Provider Profile Standard** and **Reference Query Library** for expressing capital-provider requirements and translating them into open discovery and filtering workflows.
* **Developer tooling and reference implementation** demonstrating how compatible applications can integrate with Aurora.
* **Technical documentation and operating instructions** supporting independent implementation and operation.
* **Independent security and legal review** within the funded infrastructure scope.

The implementation culminates in an end-to-end technical demonstration and public open-source release.

## Consortium and Delivery
Aurora is delivered as one integrated implementation.

**Fairway** acts as lead implementer and project coordinator, responsible for overall delivery and integration of the funded work.

**Sundial** contributes technical input where relevant to capital-provider-facing standards, discovery and filtering specifications, reference queries, API design and interoperability.

**Fallen Icarus (Rusty)** supports Aurora as a technical advisor and reviewer, providing architectural expertise relating to Cardano's transaction-based credit-market model, Loan Request UTxO design and eUTxO-specific implementation considerations.

Treasury funds Aurora's common public outputs rather than separate organizational work packages. Contributions from consortium partners and advisors form part of the same implementation and do not create separate Treasury custody or governance tracks.

## Governance Safeguards
The full **940,000 ADA** Treasury allocation is held in one dedicated **3-of-5 Aurora Treasury multisignature** controlled entirely by independent Cardano ecosystem representatives.

Fairway, Sundial, Fallen Icarus and other implementation contributors hold no Treasury signing keys. Every Treasury transaction requires approval from at least three of the five independent signers.

Delivery progresses through the four milestones defined in this proposal. Fairway publishes the required milestone evidence before expenditure may progress beyond the applicable cumulative milestone ceiling, while the Aurora Treasury Administrators review that evidence against the approved completion criteria. The Treasury wallet and transactions remain publicly auditable throughout implementation, and unspent Treasury funds are returned if the project terminates under the conditions defined in Section 9.

## Open Ecosystem Commitment
Aurora complements existing and future Cardano lending implementations rather than replacing them.

The infrastructure is designed to remain protocol-independent, modular and optional. Its standards, Discovery Engine and interfaces can be adopted and operated across different lending implementations, verification technologies and applications.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**, allowing organizations and developers to use, operate, modify, extend and commercialize the resulting infrastructure under the terms of the license.

The lasting Treasury-funded output is reusable Cardano market infrastructure that future lending protocols, applications, verification providers and capital providers can build upon and extend.

---

[Previous](00-reviewer-brief.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](02-motivation.md)
