# 6. Consortium and Relevant Experience
Aurora is delivered through an integrated implementation led by Fairway, with technical contributions from Sundial and advisory input from domain experts where appropriate.

Fairway is responsible for overall project delivery, coordination and integration of the funded work. Sundial contributes complementary technical expertise to selected open-source standards, interoperability requirements and reference implementations. Fallen Icarus (Rusty) supports the project as a technical advisor and reviewer on the underlying transaction-based credit-market architecture.

Treasury funds the resulting Aurora infrastructure and public deliverables rather than separate organizational work packages.

The implementation brings together experience in Cardano and Midnight infrastructure, verification systems, eUTxO-based credit markets, institutional finance and open technical standards. This allows Aurora to address both sides of the market-infrastructure problem: representing and exposing credit opportunities consistently on-chain, and ensuring that the resulting information can be discovered, filtered and evaluated through interfaces useful to future applications and capital providers.

## Fairway
Fairway leads the implementation of Aurora and coordinates the project.

Our background is broader than any one part of the stack. We have worked on Cardano and Midnight infrastructure, institutional integrations, verification systems, zero-knowledge proofs and credential schema design. A recurring challenge across those projects has been how to define standards that are useful enough to create interoperability, but flexible enough that different applications can still make their own technical and policy choices.

That is very close to the problem Aurora is solving. The Metadata Standard, Verification Framework and Discovery Engine all depend on having common structures for describing and querying credit opportunities without tying the market to one lending protocol, proof system or jurisdiction.

We have also delivered Catalyst-funded projects with real institutional participants, including work around Ethiopia's Fayda National ID system, Cardano credential infrastructure and higher-education credentials.

Evidence: [Recruitment Utilizing Atala PRISM — Project Catalyst](https://projectcatalyst.io/funds/8/accelerate-decentralized-identity/recruitment-utilizing-atala-prism); [Leveraging National ID system in Ethiopia — Project Catalyst](https://projectcatalyst.io/funds/12/cardano-use-cases-concept/leveraging-national-id-system-in-ethiopia-for-more-scalable-adoption-of-cardano-in-identity-solutions); [Fund 12 milestone record](https://milestones.projectcatalyst.io/projects/1200143/milestones).

More recently, we have built and tested privacy-preserving verification systems using zero-knowledge technology across Midnight and other blockchain environments. That has meant working directly with proof flows, metadata and schemas that need to remain usable across different products and integrations.

Fairway has also been working for several years on the broader question of how institutional markets can use public blockchain infrastructure, particularly around compliant DeFi, identity and credit. A lot of the thinking behind Aurora grew out of that work.

**Further reading:** [Fairway Insights](https://fairway.global/insights.html)

For Aurora, Fairway is responsible for the overall architecture, implementation and integration of the different technical workstreams, including the standards, Discovery Engine, verification layer, APIs, developer tooling and documentation.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**.

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

## Combined Delivery Capability
The implementation structure combines complementary capabilities across market infrastructure, capital-provider interoperability and eUTxO credit architecture.

Fairway provides lead implementation, system integration, verification and market-infrastructure development capability. Sundial contributes specialized technical perspective on how capital-provider requirements should be represented, queried and integrated with open credit-market infrastructure. Rusty contributes architectural continuity and technical review relating to the underlying transaction-based credit-market model.

Together, these capabilities support an implementation that must work both from the perspective of Cardano builders publishing and indexing Loan Request UTxOs and from the perspective of future applications and capital providers that need to discover, filter and evaluate those opportunities.

The resulting standards and software are designed to remain independently operable.

---

[Previous](05-budget-and-resource-allocation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](07-milestones-and-success-criteria.md)
