# 6. Consortium and Relevant Experience
Aurora is delivered through an integrated implementation led by Fairway, with technical contributions from Sundial and advisory input from domain experts where appropriate.

Fairway is responsible for overall project delivery, coordination and integration of the funded work. Sundial contributes complementary technical expertise to selected open-source standards, interoperability requirements and reference implementations. Fallen Icarus (Rusty) supports the project as a technical advisor and reviewer on the underlying transaction-based credit-market architecture.

Treasury funds the resulting Aurora infrastructure and public deliverables rather than separate organizational work packages.

The implementation brings together experience in Cardano and Midnight infrastructure, verification systems, eUTxO-based credit markets, institutional finance and open technical standards. This allows Aurora to address both sides of the market-infrastructure problem: representing and exposing credit opportunities consistently on-chain, and ensuring that the resulting information can be discovered, filtered and evaluated through interfaces useful to future applications and capital providers.

## Fairway
Fairway is the lead implementer and project coordinator for Aurora.

Its relevance to the proposal comes from prior work across identity, verification and standards-based infrastructure on Cardano and Midnight, together with experience integrating institutional systems with blockchain-based infrastructure. This background is directly applicable to the Metadata Standard, Verification Framework, Aurora Discovery Engine, open APIs, developer tooling and reference implementation that form the core of Aurora.

Relevant prior delivery includes Catalyst-funded identity initiatives, work integrating Ethiopia's Fayda National ID system with Cardano-based verifiable credential infrastructure, and issuance of proof-of-graduation verifiable credentials with Ethiopian higher education institutions. Project Catalyst records document Fairway's earlier completed identity work and subsequent Fayda-focused implementation, while Fairway's Fund 12 proposal records prior partnerships with two Ethiopian higher education institutions and the issuance of 50 proof-of-graduation verifiable credentials.
 Evidence: [Recruitment Utilizing Atala PRISM — Project Catalyst](https://projectcatalyst.io/funds/8/accelerate-decentralized-identity/recruitment-utilizing-atala-prism); [Leveraging National ID system in Ethiopia — Project Catalyst](https://projectcatalyst.io/funds/12/cardano-use-cases-concept/leveraging-national-id-system-in-ethiopia-for-more-scalable-adoption-of-cardano-in-identity-solutions); [Fund 12 milestone record](https://milestones.projectcatalyst.io/projects/1200143/milestones).

These projects required coordination across credential infrastructure, blockchain integrations and institutional participants rather than development of isolated smart contracts alone.

Within Aurora, Fairway is responsible for coordinating the implementation as a whole, integrating technical contributions from consortium partners and advisors where appropriate and ensuring that the funded standards, software, documentation, reviews and technical demonstration are delivered as one coherent public-infrastructure project.

Fairway's role as lead implementer does not create exclusive rights over the resulting infrastructure. Treasury-funded software, standards and reference implementations remain open for independent use, operation, modification and extension under Apache License 2.0.

## Sundial
Sundial is a technical consortium collaborator contributing complementary expertise at the intersection of institutional credit infrastructure, Bitcoin-native finance and capital-provider interoperability.

Sundial Protocol develops Bitcoin-oriented financial infrastructure on Cardano. The team has operated a live testnet, completed a third-party security audit with Hacken and placed first in the Institutional Track at Paris Blockchain Week.

Within the Aurora implementation, Sundial contributes technical input to selected open-source components where its expertise is directly relevant, including:

* Capital Provider Profile Standard.
* Discovery and Filtering Specification.
* Reference Query Library.
* Market Discovery API design.
* Lightweight integration examples and related technical artifacts.
* Review of capital-provider interoperability across the relevant standards and interfaces.

These contributions are incorporated into Aurora's common technical outputs rather than treated as a separate platform or independently funded product.

Sundial's role is technical and standards-focused. It does not depend on Treasury-funded fundraising, business development, institutional relationship management or commercial capital allocation.

As with the rest of the Aurora implementation, technical contributions developed through the proposal remain available to future Cardano builders and compatible lending implementations on equal terms under the project's open-source commitments.

## Technical Advisor — Fallen Icarus (Rusty)
Fallen Icarus (Rusty) serves as a technical advisor to Aurora, providing architectural review and domain expertise relating to Cardano's transaction-based credit-market model and Loan Request UTxO design.

Rusty is a principal contributor to the open-source **cardano-loans** protocol and related Cardano peer-to-peer DeFi architecture using UTxO-based state and beacon-token discovery. The cardano-loans repository documents a peer-to-peer lending model in which loan requests, offers and active loans exist as distinct UTxOs and are made discoverable through beacon tokens, providing directly relevant architectural experience for Aurora's treatment of independently discoverable credit opportunities.

Evidence: [fallen-icarus/cardano-loans](https://github.com/fallen-icarus/cardano-loans); [cardano-loans releases](https://github.com/fallen-icarus/cardano-loans/releases).

His advisory contribution may include:

* Review of credit-market architecture.
* Loan Request UTxO design considerations.
* eUTxO-specific implementation considerations.
* Review of standards and technical interfaces where relevant.
* Architectural consistency between Aurora's discovery, metadata and verification infrastructure and the underlying transaction-based credit-market model.

His involvement strengthens technical continuity between the underlying credit architecture and the open market infrastructure developed through Aurora.

The advisory role does not constitute a separately funded organizational work package, does not create separate ownership of Treasury-funded deliverables and does not make Aurora operationally dependent on Fallen Icarus.

## Combined Delivery Capability
The implementation structure is intended to combine complementary capabilities without creating dependencies on any one proprietary workflow or individual contributor.

Fairway provides lead implementation, system integration, verification and market-infrastructure development capability. Sundial contributes specialized technical perspective on how capital-provider requirements should be represented, queried and integrated with open credit-market infrastructure. Rusty contributes architectural continuity and technical review relating to the underlying transaction-based credit-market model.

Together, these capabilities support an implementation that must work both from the perspective of Cardano builders publishing and indexing Loan Request UTxOs and from the perspective of future applications and capital providers that need to discover, filter and evaluate those opportunities.

The resulting standards and software are designed to remain independently operable. Adoption of Aurora does not require continued involvement from Fairway, Sundial or any individual advisor, and no participant receives exclusive rights to operate, commercialize or extend Treasury-funded outputs.

## Previous Delivery
Participants contributing to the Aurora implementation have previously delivered Catalyst-funded initiatives, open-source infrastructure, blockchain integrations, audited technical systems and ecosystem projects relevant to verification, lending infrastructure and institutional adoption.

The proposal therefore builds upon existing technical experience and delivered infrastructure rather than beginning from a greenfield position.

The purpose of that experience within this proposal is to support delivery of Aurora's public outputs. Prior commercial relationships, advisory activities or organizational initiatives do not form part of the Treasury-funded scope unless expressly included in the proposal deliverables.

---

[Previous](05-budget-and-resource-allocation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](07-milestones-and-success-criteria.md)
