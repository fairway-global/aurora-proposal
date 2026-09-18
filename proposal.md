# Aurora

Open Infrastructure for Institutional Credit Markets on Cardano

| Field | Detail |
| --- | --- |
| Amount Requested | **940,000 ADA** |
| Lead Implementer | **Fairway** |
| Treasury Custody | Independent **3-of-5 Aurora Treasury Multisig** |
| Technical Collaborator | **Sundial Protocol** |
| Delivery Period | Approximately **5 months** |

## Table of Contents

- [1. Summary](#1-summary)
- [2. Motivation](#2-motivation)
- [3. Proposed Solution](#3-proposed-solution)
- [4. Deliverables](#4-deliverables)
- [5. Budget and Resource Allocation](#5-budget-and-resource-allocation)
- [6. Consortium and Relevant Experience](#6-consortium-and-relevant-experience)
- [7. Milestones and Success Criteria](#7-milestones-and-success-criteria)
- [8. Risks and Mitigation](#8-risks-and-mitigation)
- [9. Governance and Oversight](#9-governance-and-oversight)
- [10. Conclusion](#10-conclusion)
- [11. Governance Submission Requirements](#11-governance-submission-requirements)
- [Appendix A: Verification Framework](#appendix-a-verification-framework)

# 1. Summary
## Proposal at a Glance
| Category | Summary |
| ----- | ----- |
| **Treasury Request** | **940,000 ADA** |
| **Delivery Period** | Approximately **5 months** |
| **Purpose** | Establish shared open-source market infrastructure for Cardano credit markets, making credit opportunities discoverable, filterable, verifiable and easier to evaluate across compatible lending implementations |
| **Primary Deliverables** | Metadata Standard, Verification Framework, Aurora Discovery Engine, Filtering & Query Tooling, Open APIs, Capital Provider Profile + Reference Query Library, Developer Tooling + Reference Implementation, Documentation + Independent Review |
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
* **Aurora Discovery Engine** for indexing compatible Loan Request UTxOs, exposing standardized market information and providing relevant lifecycle visibility.
* **Filtering & Query Tooling** for identifying opportunities according to standardized attributes and published criteria.
* **Open APIs** for accessing Aurora-compatible credit opportunities, metadata, verification information and relevant lifecycle information.
* **Capital Provider Profile + Reference Query Library** for representing capital-provider requirements and translating them into reusable market queries.
* **Developer Tooling + Reference Implementation** demonstrating how compatible applications can integrate with Aurora.
* **Documentation + Independent Review** supporting independent implementation and operation, backed by security and legal review within the funded infrastructure scope.

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

# 2. Motivation
In traditional lending, every loan begins as an individual agreement between specific parties with its own terms, risk profile, repayment schedule and settlement conditions. Much like a transaction, each loan exists as a discrete financial object that can be originated, funded, serviced, transferred and settled independently. Only after loans are created do financial institutions aggregate them into portfolios, funds or securitized products.

Most DeFi lending protocols reverse this process. Capital is first deposited into a shared pool, and borrowers draw from that pool according to predefined rules. While effective for certain use cases, this model does not reflect how many real-world credit markets operate.

Cardano's eUTxO architecture is well suited to the loan-first model. Its transaction-based architecture can represent individual financial relationships as distinct on-chain objects rather than requiring every lending opportunity to be organized through a shared liquidity pool.

Individual lending opportunities can therefore exist as separate Loan Request UTxOs with their own terms, state and lifecycle. They can be independently published, funded and settled through compatible lending infrastructure before being aggregated into larger credit portfolios.

This creates the technical foundation for open credit markets built around individual financial agreements. It does not, by itself, create the shared market infrastructure required for institutions and other capital providers to discover, compare and evaluate those agreements across independent implementations.

Two problems currently prevent individual Cardano credit opportunities from functioning coherently and being usable in institutional and professional capital-provider workflows.

## Institutions need shared market infrastructure, not just permissionless settlement.
Cardano credit market implementations can enable parties to negotiate and settle individual lending agreements on-chain. Institutional lenders, regulated financial institutions and professional capital providers, however, require more than settlement. They need standardized ways to discover lending opportunities, evaluate relevant information, apply their own eligibility and compliance requirements and monitor performance over time before allocating capital.

Without standardized metadata, discovery, filtering and verification infrastructure, each participant must interpret lending opportunities through protocol-specific integrations and independently reconstruct the information required for evaluation.

Advances in verifiable credentials, zero-knowledge proofs and other proof systems make it possible to associate institutional, eligibility, compliance and other verification information with an opportunity without requiring sensitive underlying data to be published on-chain. Implemented through optional transaction metadata and open verification references rather than changes to lending protocols, this infrastructure can support participants that require additional assurance while preserving permissionless use of the underlying market.

Verification is therefore one component of the required market layer. Institutions must also be able to index opportunities, filter them according to published attributes, compare relevant information and monitor their lifecycle through consistent interfaces.

## Independent credit markets need shared standards, not isolated integrations.
Without common standards, each lending protocol, application and capital provider must develop its own metadata format, indexing logic, discovery interface, verification workflow and reporting model.

This creates fragmented market information and repeated integration work. Lending opportunities may exist on-chain but remain difficult to discover or compare across implementations. Capital providers must conduct similar technical integration and due-diligence work separately for each protocol, while builders must recreate infrastructure that provides substantially the same market functions.

This fragmentation becomes more costly as additional lending models, jurisdictions, verification systems and capital-provider requirements emerge. Proprietary discovery systems may solve the immediate needs of individual applications, but they do not establish common infrastructure that future Cardano builders can adopt and operate independently.

Open standards provide a different path. A common Metadata Standard can describe lending opportunities consistently. Shared indexing and discovery infrastructure can expose those opportunities through open APIs. Published filtering and verification specifications can allow capital providers and compatible applications to evaluate opportunities according to their own requirements without depending on one proprietary marketplace or exclusive lending protocol.

The result is reusable market infrastructure rather than a collection of isolated integrations.

## Bringing the Two Together
Aurora addresses both problems by establishing a shared market layer around independent Loan Request UTxOs.

Standardized metadata enriches each opportunity with machine-readable market information and verification references. Open discovery and indexing infrastructure then makes those opportunities searchable across compatible implementations. Capital providers and applications can discover, filter and evaluate opportunities according to their own requirements while funding and settlement continue through the underlying lending infrastructure.

Aurora does not replace lending protocols or determine which opportunities should receive capital. It establishes the open standards, verification framework, discovery infrastructure, APIs and developer tooling required for independent Cardano credit opportunities to function as a coherent market.

Treasury funding builds and demonstrates this reusable infrastructure.

# 3. Proposed Solution
This proposal builds shared market infrastructure for Cardano credit markets through open standards, verification infrastructure, discovery and indexing, filtering capabilities and developer interfaces that operate around compatible lending implementations. The intent is to establish a common Cardano market stack that compatible credit applications can share rather than requiring each team to recreate the same discovery, filtering and verification infrastructure independently.

The broader objective is to establish the shared market infrastructure that allows independent lending opportunities to be published, indexed, discovered, filtered, verified, evaluated and monitored through open standards rather than isolated integrations. The proposal intentionally focuses on shared market infrastructure rather than lending logic. Existing and future Cardano credit market implementations remain free to innovate independently while using common infrastructure for standardized market information, verification and discovery.

The solution does not modify core lending smart contracts. Instead, standardized metadata and verification references can be associated with individual Loan Request UTxOs, while open off-chain infrastructure reads, organizes and exposes that information to compatible applications and capital providers. A Loan Request UTxO enriched with this standardized metadata is referred to here as a "colored" Loan Request UTxO. The term is descriptive and does not represent a new ledger primitive.

This separation allows Aurora to remain compatible with different lending implementations rather than requiring participants to adopt a single protocol, verification provider or commercial workflow.

## Why metadata instead of smart contract logic?
### Efficiency
Institutional verification may involve credential systems, proof systems and policy requirements that are unnecessary for the execution of the underlying lending agreement itself.

Keeping this information and the corresponding verification logic outside the core lending contracts avoids coupling lending execution to additional verification requirements. The off-chain infrastructure can evaluate relevant proofs and verification references without increasing the execution requirements of the underlying lending contracts.

### Flexibility
Verification and market-information requirements differ across jurisdictions, capital providers and use cases and may evolve over time. A versioned Metadata Standard and extensible Verification Framework can support new metadata fields, credential types, proof systems and verification providers without requiring lending contracts to be redeployed or migrated.

This also allows different participants to apply different requirements to the same underlying market rather than imposing one global verification policy on every user.

### Permissionlessness
The underlying credit market contracts remain independent of Aurora and fully usable without Aurora metadata.

Participants that require additional information can use Aurora-compatible metadata, verification and filtering infrastructure to evaluate opportunities according to their own requirements. Participants that do not require these capabilities can continue interacting directly with the underlying lending infrastructure.

Aurora therefore provides optional market infrastructure rather than creating a protocol-level participation requirement.

## How It Works
### Loan Origination
An originator creates a Loan Request UTxO through a compatible Cardano lending implementation.

Depending on the underlying implementation, a Loan Request UTxO may represent an institutional funding request, a lending facility, a lending program or another individual credit opportunity.

The originator may attach standardized metadata or references describing institutionally relevant information associated with that opportunity. This may include verification references, jurisdiction, duration, asset, ticket size, eligibility information or other attributes defined by the applicable metadata schema.

A Loan Request UTxO enriched in this way becomes a "colored" Loan Request UTxO that can be interpreted consistently by Aurora-compatible infrastructure.

### Indexing and Verification
The Aurora Discovery Engine reads and organizes compatible Loan Request UTxOs and their associated metadata, transforming otherwise independent on-chain lending opportunities into a searchable market.

Where verification information is attached, the Verification Framework allows relevant proofs or verification references to be evaluated against the applicable schema or policy. Verification remains extensible so that different credential systems, proof systems and verification providers can coexist without becoming mandatory components of the underlying lending protocol.

The resulting standardized market information and verification status can be exposed through open APIs for use by capital providers, lending applications and other ecosystem participants.

### Discovery and Evaluation
Capital providers and compatible applications query the Aurora Discovery Engine to discover lending opportunities.

Opportunities can be filtered according to published metadata and query specifications, including criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other attributes supported by the applicable schema.

Aurora exposes the information required to discover, filter and evaluate opportunities but does not determine whether an opportunity should receive capital. Individual capital providers remain responsible for applying their own risk, eligibility, compliance and allocation criteria.

Aurora's Capital Discovery Layer extends this open infrastructure with selected technical contributions from Sundial through a Capital Provider Profile Standard, Discovery and Filtering Specification, Reference Query Library, Market Discovery API contribution and lightweight reference integration artifacts. These outputs describe how capital-provider requirements can be represented and translated into queries against Aurora-compatible credit opportunities without creating a proprietary allocation system.

### Repayment History and Performance
Aurora is designed to track relevant loan-lifecycle information exposed by compatible lending implementations, including repayment events where those events are available on-chain.

Over time, repayment history can contribute to portable institutional credit histories and broader institutional track records that future capital providers can evaluate through the same open infrastructure. Standardizing and exposing this information reduces the need for each future participant to reconstruct historical performance independently.

Treasury funding establishes the infrastructure required to index and expose this information.

### Funding and Settlement
Funding and settlement remain functions of the compatible lending infrastructure underlying each opportunity. Aurora provides the discovery, market-information and verification layer around those lending agreements rather than replacing their execution logic.

## What We Build
Aurora delivers a set of open standards, software and developer infrastructure intended to become reusable components of Cardano's credit-market stack. The components are designed to work across compatible lending implementations and support independent operation, integration and extension across the ecosystem.

### Metadata Standard
A versioned, open specification for describing credit-market opportunities and the metadata references associated with Loan Request UTxOs.

The standard provides a common way for compatible lending implementations to expose market information such as jurisdiction, duration, asset, ticket size, verification references and other relevant attributes without requiring changes to their underlying lending logic.

It is designed to remain extensible across lending models, jurisdictions, verification systems and future Cardano credit applications.

### Verification Framework
An open and extensible framework for attaching and evaluating institutional, eligibility, compliance and other proof-based information associated with Loan Request UTxOs.

The framework does not require a single identity system, credential issuer, proof system or verification provider. Different verification mechanisms may coexist, while applications and capital providers remain responsible for determining which evidence and policies they require.

This allows verification to become a shared market capability without introducing a universal participation requirement or making Aurora dependent on one proprietary verification stack.

### Aurora Discovery Engine
An open-source service that indexes compatible Loan Request UTxOs and associated metadata, supports discovery and filtering, exposes verification information, tracks relevant loan-lifecycle information and provides open APIs for compatible applications.

The Discovery Engine turns otherwise independent credit opportunities into a searchable market layer without becoming the underlying lending protocol or a proprietary marketplace.

It is designed to be independently operable and accessible through open APIs, allowing lending protocols, wallets, analytics providers and other applications to integrate with the same shared market infrastructure.

### Filtering & Query Tooling
Open filtering and query capabilities for identifying Aurora-compatible credit opportunities according to published metadata and query specifications.

Compatible applications and capital providers can filter opportunities according to criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other standardized attributes supported by the applicable schema.

### Open APIs
Public interfaces for querying Aurora-compatible credit opportunities, associated metadata, verification information and relevant lifecycle information.

These interfaces allow wallets, lending applications, analytics services, capital-provider systems and other Cardano applications to build against common market infrastructure rather than creating separate protocol-specific integrations for the same functions.

### Capital Provider Profile + Reference Query Library
An open Capital Provider Profile Standard for representing requirements such as jurisdiction, ticket size, duration, asset, verification requirements and risk preferences, together with a Reference Query Library demonstrating how those requirements can be translated into reusable queries against Aurora-compatible credit opportunities.

Together with the Discovery and Filtering Specification, Market Discovery API contributions and related integration artifacts, these components form Aurora's **Capital Discovery Layer**. Selected technical contributions to this infrastructure will be developed with Sundial.

These components remain open standards and reference tooling rather than a proprietary capital-allocation system.

### Developer Tooling + Reference Implementation
Open developer tooling, documentation and a reference implementation demonstrating how compatible applications can create Aurora-compatible metadata, identify and index Loan Request UTxOs, query the Discovery Engine, apply published filtering criteria and evaluate verification references.

The reference implementation is intended to reduce duplicated integration work across the ecosystem and provide a practical starting point for future Cardano builders adopting the standards.

A Treasury-funded technical demonstration will validate the end-to-end infrastructure flow on testnet.

### Documentation + Independent Review
Technical and operating documentation will support independent implementation and operation of the standards, software and interfaces.

Independent security and legal review will assess the Treasury-funded infrastructure within the scope of this proposal, as detailed in Section 4.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**.

The resulting infrastructure is intended to become part of Cardano's shared credit-market stack: initially implemented through Aurora, but available for lending protocols, applications, capital providers and future builders to adopt, operate and extend independently.

# 4. Deliverables
The project delivers open-source infrastructure for a shared Cardano credit market.

Treasury funding covers the standards, software, reference implementations, documentation and technical validation required to make independent Loan Request UTxOs discoverable, filterable, verifiable and easier to evaluate across compatible credit-market applications.

## Public Infrastructure Deliverables
1. **Metadata Standard.**
   A versioned, open specification describing credit-market opportunities and the metadata references associated with Loan Request UTxOs. The standard defines how institutionally relevant information can be attached consistently without modifying the underlying lending protocol and remains extensible across lending models, jurisdictions and verification systems.

2. **Verification Framework.**
   An extensible framework for attaching and evaluating institutional, eligibility, compliance and other proof-based information associated with Loan Request UTxOs. The framework supports multiple credential systems, proof systems and verification providers without requiring a single identity or compliance infrastructure.

3. **Aurora Discovery Engine.**
   An open-source service that indexes compatible Loan Request UTxOs and associated metadata, exposes lending opportunities through open APIs, supports discovery and filtering, provides access to verification information and tracks relevant loan-lifecycle information exposed by compatible lending implementations. The Discovery Engine will support independent deployment and operation, with published interfaces and operating documentation for third-party builders.

4. **Filtering & Query Tooling.**
   Open filtering capabilities based on published metadata schemas and query specifications. Compatible applications and capital providers will be able to identify opportunities according to criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other standardized attributes supported by the applicable schema.

5. **Open APIs.**
   Public interfaces for querying Aurora-compatible credit opportunities, associated metadata, verification information and relevant lifecycle information.
   The APIs are intended to reduce protocol-specific integration work and enable wallets, lending applications, analytics services and other ecosystem participants to build against common market infrastructure.

6. **Capital Provider Profile + Reference Query Library.**
   Aurora includes selected technical contributions from Sundial relating to capital-provider requirements, discovery, filtering and interoperability within the broader Aurora implementation.

   **Capital Provider Profile Standard.** An open schema for representing requirements such as jurisdiction, ticket size, duration, asset, verification requirements and risk preferences.

   **Discovery and Filtering Specification.** A published specification describing how capital-provider requirements can be translated into discovery and filtering criteria against Aurora-compatible credit opportunities.

   **Reference Query Library.** Open examples demonstrating how prospective capital providers and compatible applications can query and filter opportunities using the published standards.

   **Market Discovery API Contribution.** API definitions and related implementation contributions required to expose capital-provider-relevant discovery and filtering capabilities through the Aurora infrastructure.

   **Lightweight Integration Artifacts.** Reference examples or lightweight SDK components demonstrating how external applications can integrate the Capital Provider Profile Standard and query specifications.

   **Documentation.** Technical documentation sufficient for third parties to use, implement and extend the relevant standards and interfaces without dependence on Sundial.

   The Capital Discovery Layer does not allocate Treasury capital, make lending decisions or create a proprietary capital-allocation product. It provides open standards and reference tooling that future market participants may use according to their own requirements.

   Together with the Discovery and Filtering Specification, Market Discovery API contributions and related integration artifacts, these components form Aurora's **Capital Discovery Layer**. Sundial contributes technical expertise to selected components, while Fairway remains responsible for integrated delivery as lead implementer.

7. **Developer Tooling + Reference Implementation.**
    Open tooling and reference code demonstrating how developers can create Aurora-compatible metadata, identify and index Loan Request UTxOs, query the Discovery Engine, apply filtering criteria and evaluate verification references.

    The reference implementation will demonstrate the complete infrastructure flow without requiring adoption of any single lending protocol or commercial deployment model.

8. **Documentation + Independent Review.**
    Technical documentation covering the Metadata Standard, Verification Framework, Discovery Engine, APIs, filtering model and reference implementation.

    Technical and operating documentation will provide sufficient integration and operating guidance for technically capable third parties to inspect, integrate and operate the relevant infrastructure independently.

    The funded scope also includes independent security review of the Treasury-funded software and relevant technical interfaces, together with independent legal review of the open infrastructure, standards, documentation and intended operating model within the scope of this proposal.

    The security review will assess the Treasury-funded software and relevant technical interfaces before final release.

## Technical Demonstration
The project will include a testnet technical demonstration showing how the core Aurora components operate together.

The demonstration will show that a compatible Loan Request UTxO can be:

1. created through compatible lending infrastructure;
2. enriched with standardized metadata;
3. identified and indexed by the Aurora Discovery Engine;
4. discovered through an open API;
5. filtered according to published criteria;
6. associated with verification information that can be evaluated through the Verification Framework; and
7. consumed by a compatible reference application or query workflow.

The demonstration will validate the **end-to-end operation and interoperability of the infrastructure**, from Loan Request UTxO creation and metadata through discovery, filtering, verification and application-level consumption.

## Open-Source Release and Public Documentation
All Treasury-funded software, standards and reference implementations will be released under the **Apache License 2.0**.

Public repositories will contain the applicable source code, specifications, documentation and implementation materials required for third parties to inspect, operate, modify and extend the infrastructure.

The project will also publish public progress reporting against the approved milestones and deliverables.

The resulting infrastructure remains available to the Cardano ecosystem regardless of whether future builders use Fairway, Sundial or any particular lending implementation.

# 5. Budget and Resource Allocation
The Treasury withdrawal requests **940,000 ADA** for the 5-month delivery of Aurora's open credit-market infrastructure, equivalent to approximately **$188,000 at a reference price of $0.20 per ADA**.

The budget covers the development and delivery of the technical standards, open-source software, testing, documentation, independent review, hosting and supporting infrastructure defined in this proposal.

Treasury funding is allocated to the open infrastructure and public deliverables defined in this proposal, rather than to separate organizational work packages.

| Allocation | ADA | Approx. USD\* | Primary Scope |
| ----- | ----- | ----- | ----- |
| Core Infrastructure Development | **800,000** | **$160,000** | Metadata and verification standards, Aurora Discovery Engine, APIs, filtering capabilities, developer tooling, reference implementation, Capital Discovery Layer components, technical demonstration, documentation and project delivery |
| Review, Hosting & Technical Contingency | **140,000** | **$28,000** | Covers approximately **60,000 ADA** for independent security and legal review, **20,000 ADA** for independent Treasury-use audit and oversight, **30,000 ADA** for infrastructure hosting and technical operations, and **30,000 ADA** for technical contingency within the approved Aurora scope. |
| **Total** | **940,000** | **$188,000** |  |

\*Illustrative values calculated using a reference ADA price of **US$0.20**.

The USD values are provided solely to assist reviewers in understanding the approximate scale of the proposal. Treasury funding is requested in ADA. The deliverables described in this proposal are defined by scope and milestone completion rather than by subsequent movements in the ADA/USD exchange rate.

The budget reflects responsibility for producing public deliverables rather than compensation of individual contributors or consortium members. Internal allocation of implementation resources is managed by the lead implementer and does not alter the Treasury-funded scope, milestone requirements or public deliverables.

All Treasury-funded software, standards and reference implementations will be released under Apache License 2.0.

## Core Infrastructure Development
The **800,000 ADA** Core Infrastructure Development allocation funds implementation of the public infrastructure defined in Section 4.

This includes:

* Metadata Standard development.
* Verification Framework implementation.
* Aurora Discovery Engine development.
* Indexing, discovery and filtering capabilities.
* Open APIs.
* Developer tooling.
* Reference implementation.
* Capital Provider Profile Standard.
* Discovery and Filtering Specification.
* Reference Query Library.
* Market Discovery API design and implementation contributions.
* Lightweight Capital Discovery SDK components or reference integration examples.
* Technical documentation and integration guidance.
* Testnet technical demonstration.
* Open-source repository preparation and release.
* Project coordination and public progress reporting.

These deliverables belong to the proposal rather than to individual consortium members. They are developed under a unified implementation programme led by Fairway, with technical contributions from consortium partners where appropriate.

The Core Infrastructure Development allocation is monitored against the deliverables and milestone outputs defined in Sections 4 and 7. Material changes in resource allocation across the approved delivery areas will be disclosed through milestone reporting.

## Implementation Responsibility
Fairway acts as lead implementer and is responsible for overall delivery of the Treasury-funded work.

This includes coordinating engineering, standards development, technical integration, documentation, testing, external reviews, milestone delivery and public reporting. Fairway may coordinate technical contributions from consortium collaborators and other approved contributors where appropriate, while remaining accountable for delivery of the funded scope as a whole.

This structure does not imply that every individual deliverable must be implemented exclusively by Fairway personnel. Treasury funds the completed public infrastructure and associated milestones rather than a prescribed division of labour between contributors.

## Consortium Technical Collaboration
Sundial acts as a strategic technical collaborator within the unified Aurora implementation.

Its contribution focuses on selected open-source components relating to the interaction between capital-provider requirements and Aurora-compatible market information, including:

* Capital Provider Profile Standard.
* Discovery and Filtering Specification.
* Reference Query Library.
* Market Discovery API design.
* Lightweight integration examples and related technical artifacts.
* Review of capital-provider interoperability across the relevant standards and interfaces.

These contributions are developed as part of the proposal's shared technical deliverables and remain available to the ecosystem under the same open-source commitments as the rest of the Treasury-funded infrastructure.

## Review, Hosting & Technical Contingency
The **140,000 ADA** Review, Hosting & Technical Contingency allocation covers external and project-wide requirements necessary to deliver the infrastructure responsibly.

These resources include:

* Independent security review of the Treasury-funded software and relevant technical interfaces.
* Independent legal review of the open infrastructure, standards and intended operating model within the scope of this proposal.
* Infrastructure hosting required for development, testing and the technical demonstration.
* Technical contingency for unforeseen implementation requirements within the approved infrastructure scope.
* **Independent Treasury-use audit and oversight**, including reconciliation of Treasury transactions against reported expenditure, approved budget categories and milestone expenditure ceilings.

These resources are limited to external review, infrastructure operations, Treasury-use oversight and technical requirements directly related to the approved Aurora scope.

Any use of technical contingency remains limited to delivery of the approved proposal scope, requires written justification and authorization by the Aurora Treasury Administrators, and will be disclosed in the next public milestone report. Unused contingency remains unspent Treasury ADA and is subject to the proposal's normal reconciliation and refund provisions.

## Resource Allocation Principles
The allocation follows three principles.

* Treasury funds are allocated according to the infrastructure and supporting work required to deliver the approved public outputs rather than according to the internal compensation arrangements of consortium members.
* Fairway remains responsible for overall delivery while technical contributions from consortium partners are incorporated into the same implementation programme where appropriate.
* External expenditure is limited to independent review, Treasury-use audit and oversight, hosting and technical contingency directly related to delivery of the public infrastructure.

Internal allocation of implementation resources may be adjusted by the lead implementer as required to complete the approved work, provided that the total Treasury request, funded scope, milestone requirements and public deliverables remain unchanged.

The resulting budget therefore maps directly to the public outputs defined in Section 4 and limits Treasury expenditure to infrastructure that remains available to Cardano after the funded delivery period ends.

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

# 7. Milestones and Success Criteria
Aurora is delivered through four milestones over approximately five months.

Each milestone is tied to concrete public outputs that can be independently reviewed. Fairway remains responsible for integrated delivery of the proposal, with technical contributions from consortium partners and advisors incorporated where appropriate.

| Milestone | Timeline | ADA Allocation | Primary Outcome |
| ----- | ----- | ----- | ----- |
| M1: Specifications & Architecture | Month 1 | **140,000** | Core standards and implementation architecture finalized |
| M2: Core Build | Months 2–3 | **320,000** | Discovery, verification, indexing, filtering and API infrastructure operational on testnet |
| M3: Integration & Technical Demonstration | Month 4 | **290,000** | Reference implementation, developer tooling and complete testnet workflow demonstrated |
| M4: Independent Review & Public Release | Month 5 | **190,000** | Independent review completed and final open-source infrastructure released |
| **Total** | **Approximately 5 months** | **940,000** |  |

## M1: Specifications & Architecture
**Timeline:** Month 1
 **ADA Allocation:** **140,000 ADA**

### Key Outputs
* Metadata Standard.
* Verification Framework specification.
* Aurora Discovery Engine architecture.
* Discovery and Filtering Specification.
* Capital Provider Profile Standard.
* Initial API, query and implementation architecture.

Technical review may include contributions from Sundial and architectural input from Fallen Icarus where relevant to capital-provider interoperability, Loan Request UTxO design and eUTxO-specific credit-market architecture.

### Completion Criteria
* Core specifications and architecture documents are published in public repositories.
* The architecture defines how compatible Loan Request UTxOs are indexed, discovered, filtered and associated with verification information.
* The specifications remain protocol independent and do not require a single verification provider, lending implementation or hosted Aurora operator.
* Public milestone report published with links to the completed outputs.

## M2: Core Build
**Timeline:** Months 2–3
 **ADA Allocation:** **320,000 ADA**

### Key Outputs
* Operational Aurora Discovery Engine on testnet.
* Verification Framework implementation.
* Indexing, discovery and filtering functionality.
* Open API implementation.
* Initial developer tooling and technical documentation.

### Completion Criteria
* Aurora can identify and index compatible Loan Request UTxOs and associated metadata on testnet.
* The public API can retrieve and filter indexed opportunities using published metadata criteria.
* Verification information can be exposed and evaluated through the Verification Framework.
* The Discovery Engine can be deployed in a test environment without dependence on a Fairway-hosted API.
* Source code and milestone documentation are publicly available.
* Interim independent Treasury-use expenditure and reconciliation review completed and published.

## M3: Integration & Technical Demonstration
**Timeline:** Month 4
 **ADA Allocation:** **290,000 ADA**

### Key Outputs
* Reference implementation.
* Reference Query Library.
* Capital-provider filtering integration.
* Market Discovery API integration.
* Lightweight integration examples and developer tooling.
* Developer and integration documentation.
* End-to-end testnet technical demonstration.

### Completion Criteria
* The reference implementation demonstrates a compatible Loan Request UTxO being enriched with standardized metadata, indexed, discovered, filtered and associated with verification information.
* Published reference queries demonstrate how capital-provider requirements can be translated into discovery and filtering criteria.
* A technically capable third party can use the published APIs, tooling and documentation to reproduce the principal workflow.
* Public milestone report published.

## M4: Independent Review & Public Release
**Timeline:** Month 5
**ADA Allocation:** **190,000 ADA**

Independent review preparation may begin during the preceding implementation milestone so that security, legal and documentation work does not unnecessarily extend the project timeline.

### Key Outputs
* Independent security review of the Treasury-funded software and relevant interfaces.
* Independent Treasury-use audit and oversight report covering Treasury expenditure and reconciliation against the approved scope and milestone ceilings.
* Independent legal review within the infrastructure-only scope of the proposal.
* Resolution or documented remediation of material findings.
* Final specifications, software, APIs, tooling, reference implementation and documentation.
* Public repositories, build instructions and operating documentation.
* Final project report.

### Completion Criteria
* Required independent reviews are completed and material findings affecting release are addressed or transparently documented.
* Independent Treasury-use audit and oversight has been completed and included in the final project reporting.
* All Treasury-funded software, standards and reference implementations are publicly released under **Apache License 2.0**.
* Public repositories contain sufficient source code, specifications, documentation and deployment instructions for independent inspection and operation.
* A technically capable third party can deploy and operate the relevant Aurora infrastructure using the published repositories, documentation and deployment instructions.
* Final report maps the completed public outputs against the proposal deliverables and milestone requirements.

## Milestone Expenditure Principles
The milestone allocations define the maximum cumulative Treasury expenditure as implementation progresses. At project commencement, up to **140,000 ADA** may be used for M1. Following completion and approval of M1, the cumulative expenditure ceiling increases to **460,000 ADA**; following M2, to **750,000 ADA**; and following M3, to the full **940,000 ADA**. Completion of M4 triggers final reconciliation and reporting.

Fairway is responsible for the integrated delivery of Aurora. The Aurora Treasury Administrators review the published milestone evidence before authorizing progression to each subsequent expenditure ceiling.

# 8. Risks and Mitigation
Aurora's infrastructure-only scope limits Treasury risk primarily to technical delivery, interoperability, security and long-term usability of the resulting public infrastructure.

**Compatibility with underlying lending infrastructure.**
Aurora operates alongside compatible lending implementations rather than replacing the underlying lending contracts. Differences in Loan Request UTxO structures may therefore affect integration and testing.

Aurora mitigates this risk through open interfaces and clearly defined metadata, discovery and verification specifications. The reference implementation and testnet demonstration will validate compatibility against representative Loan Request UTxO structures while preserving flexibility across different implementations.

**Interoperability and specification risk.**
Different lending implementations, capital-provider requirements and future use cases may require metadata or query structures that are not known at the time of the initial release.

The Metadata Standard, Verification Framework and filtering specifications are therefore designed to be **versioned, extensible and modular**. Published schemas and open APIs allow the infrastructure to evolve as new requirements emerge without forcing changes to the underlying lending protocols.

**Verification-system dependency.**
Verification requirements may rely on different credential systems, proof systems or verification providers.

Aurora does not depend on a single verification technology. The Verification Framework separates verification references and policies from the underlying lending contracts, allowing multiple verification systems to coexist and evolve independently.

**Security and implementation risk.**
Defects in the Discovery Engine, APIs, verification logic or developer tooling could produce incorrect indexing, filtering or verification results.

The project includes independent security review of the Treasury-funded software and relevant interfaces. Material findings affecting the funded release must be addressed or clearly documented before final completion. Aurora is also designed as a market-information and discovery layer rather than a custody or transaction-execution layer, which limits the impact of defects within the infrastructure itself.

**Operational usability risk.**
Open-source infrastructure provides limited value if it is difficult for third parties to deploy, integrate or maintain.

Aurora mitigates this through public repositories, Apache License 2.0, deployment instructions, developer documentation, open APIs and reference implementations. Final completion criteria include demonstrating that the infrastructure can be deployed and operated by a technically capable third party using the published materials.

**Adoption risk.**
Open standards do not guarantee adoption by future lending protocols, applications or capital providers.

Aurora mitigates this by keeping the infrastructure optional, protocol-independent and reusable. Existing lending implementations do not need to replace their core contracts, while the APIs, reference implementation and query standards are intended to reduce the work required to integrate with the shared market layer. Treasury delivery is measured by the completion and usability of the public infrastructure rather than by speculative adoption targets.

**Delivery schedule risk.**
The approximately five-month implementation period requires standards development, implementation, integration, review and documentation to progress in parallel where appropriate.

Fairway is responsible for coordinating the integrated delivery. The four-milestone structure provides intermediate verification of specifications, core functionality and the end-to-end technical demonstration before final release. Independent review preparation may begin before implementation is fully complete to reduce delays at the final milestone.

**Legal and regulatory interpretation.**
Open infrastructure intended for institutional credit markets may raise questions about how standards, verification references and interfaces are described or used in different contexts.

The funded scope therefore includes independent legal review of the infrastructure, documentation and intended operating model, with any material findings incorporated into the final release.

# 9. Governance and Oversight
Aurora uses a single, independently controlled Treasury custody structure for the implementation of the project.

The full **940,000 ADA** Treasury allocation is held in a dedicated **3-of-5 Aurora Treasury multisignature wallet** controlled by independent Cardano ecosystem representatives. Fairway is responsible for project delivery but holds no Treasury signing key. Sundial, Fallen Icarus and other implementation contributors likewise hold no signing authority over Treasury funds.

Expenditure progresses against the four milestones defined in Section 7. Fairway publishes the required milestone evidence before expenditure may progress beyond each cumulative milestone ceiling, and every Treasury transaction requires approval from at least three of the five Aurora Treasury Administrators.

## Aurora Treasury Multisig
The Aurora Treasury multisignature is the sole custody wallet for the Treasury allocation.

All Treasury funds remain under independent **3-of-5 multisignature control** until used for approved project expenditure.

### Proposed Aurora Treasury Administrators
| Role | Representative | X |
| ----- | ----- | ----- |
| Independent Governance Signer | James "Blockjock" Meidinger | @blockjock2017 |
| Independent Governance Signer | Christian Taylor | @DeOpenSourceGuy |
| Independent Governance Signer | Elder Millennial | @TheElderMillenial |
| Independent Technical Signer | Wilco USDM | @iamwilco |
| Independent Signer | Kriss Baird | @krissbaird |

No implementation consortium member holds a signing key.

For Treasury-governance purposes, the five independent multisignature signers collectively serve as the **Aurora Treasury Administrators**. This designation does not create a separate governance body or additional custody structure. The Administrators are the same five Aurora Treasury Administrators who control the 3-of-5 Aurora Treasury multisignature.

The Aurora Treasury Administrators are responsible for:

* custody of Treasury funds;
* reviewing milestone evidence;
* authorizing expenditure within the approved project scope and milestone limits;
* monitoring use of Treasury funds and progress against the approved deliverables;
* suspending further expenditure where material delivery problems arise;
* maintaining public transparency over Treasury balances and transactions; and
* returning unspent Treasury funds if the project terminates.

The Aurora Treasury Administrators do not manage engineering, determine Aurora's technical architecture, choose implementation contributors, divide work between consortium participants or acquire ownership or control over Treasury-funded outputs.

Any material conflict of interest relating to a proposed transaction or milestone decision must be disclosed. A conflicted Administrator must abstain from the relevant approval, and the transaction must still satisfy the required 3-of-5 multisignature threshold using non-conflicted signers.

A material conflict includes a direct financial interest, or a material indirect financial interest through an employer, controlled entity or close commercial affiliate, in a proposed Treasury payment or paid project engagement.

If an Administrator resigns, loses access to a signing key or becomes permanently unavailable, the remaining Administrators may, **where the existing multisignature remains capable of satisfying its 3-of-5 authorization threshold**, authorize replacement with another independent Cardano ecosystem representative. Where replacement requires creation of a new multisignature credential, the unspent Treasury balance may be migrated to a replacement 3-of-5 Aurora Treasury multisignature preserving the same independence and signing threshold. Any signer replacement and resulting custody address will be publicly disclosed before funds are moved.

## Milestone Oversight
The milestone schedule controls the maximum cumulative Treasury expenditure authorized as implementation progresses. The unspent Treasury balance remains in the same Aurora Treasury multisignature throughout the project; milestone progression does not involve transfers between separate project wallets.

| Milestone | ADA Allocation |
| ----- | ----- |
| M1: Specifications & Architecture | **140,000** |
| M2: Core Build | **320,000** |
| M3: Integration & Technical Demonstration | **290,000** |
| M4: Independent Review & Public Release | **190,000** |
| **Total** | **940,000** |

At project commencement, expenditure of up to 140,000 ADA is authorized for M1. Following approval of M1, the cumulative expenditure ceiling increases to 460,000 ADA. Following approval of M2, it increases to 750,000 ADA. Following approval of M3, the full 940,000 ADA becomes available for completion of M4. Completion of M4 triggers final reconciliation and reporting.

Before expenditure may progress to the next cumulative milestone ceiling:

1. Fairway publishes the milestone evidence required under Section 7.
2. The Aurora Treasury Administrators review the published outputs against the approved completion criteria.
3. Progression to the next cumulative expenditure ceiling requires authorization through the 3-of-5 Aurora Treasury multisignature.

Milestone review is evidence-based and practical. The Treasury Administrators confirm that the relevant specifications, repositories, software, documentation, demonstrations or independent-review outputs have been published and reasonably satisfy the approved completion criteria. They are not expected to reproduce the engineering work or independently reimplement Aurora.

Treasury funds may be used only for the approved Aurora infrastructure scope and milestone deliverables defined in this proposal.

## Operational Responsibility
Fairway remains responsible as lead implementer and project coordinator for delivery of Aurora.

Fairway coordinates implementation planning, consortium contributions, external technical and professional services, milestone evidence, public reporting and overall delivery of the approved scope.

Sundial contributes technical implementation input where relevant to the common Aurora outputs. Fallen Icarus may provide architectural review and advisory input where relevant to the underlying credit-market architecture and Loan Request UTxO model.

These contributions remain part of one integrated Aurora implementation and do not create separate Treasury budgets, custody arrangements or governance tracks.

The Aurora Treasury Administrators oversee Treasury custody, expenditure and milestone accountability but do not direct day-to-day implementation.

## Transparency and Reporting
The Aurora Treasury multisignature address will be published before project expenditure begins.

All Treasury transactions remain publicly auditable on-chain.

Fairway will publish one public progress report for each milestone. Each report will:

* link to the relevant public specifications, repositories, software, documentation or review materials;
* summarize completion against the applicable milestone criteria;
* state Treasury expenditure to date; and
* identify any material delivery issues or remediation items.

The final report will map the completed Treasury-funded outputs against the approved proposal deliverables and provide links to the final open-source repositories and documentation.

Treasury ADA held in the Aurora Treasury multisignature prior to approved project expenditure will not be delegated to a stake pool operator and will remain delegated to the predefined Abstain voting option in accordance with the applicable Cardano Treasury governance requirements.

## Refund and Remediation
If a milestone is materially incomplete, the Aurora Treasury Administrators may suspend further Treasury expenditure while Fairway addresses the identified deficiencies.

If the milestone remains incomplete **60 days after its target date** and no satisfactory remediation plan has been agreed with the Aurora Treasury Administrators, further expenditure may remain suspended and the project may proceed to termination under the conditions below.

If the project terminates before completion, all unspent ADA remaining in the Aurora Treasury multisignature will be returned to the Cardano Treasury using the applicable Treasury return mechanism.

Legitimately incurred expenditure against approved project work remains project expenditure and is accounted for through public milestone reporting and financial reconciliation.

Changes to individual contributors do not change the approved Aurora deliverables or Fairway's responsibility for overall project delivery.

# 10. Conclusion
Aurora is designed to provide a shared market layer for Cardano credit markets.

The proposal funds the open standards, software and developer infrastructure required to make independent Loan Request UTxOs easier to describe, index, discover, filter and verify through common interfaces. The goal is to reduce the need for each lending implementation to build its own isolated discovery and verification stack.

The funded outputs include the Metadata Standard, Verification Framework, Aurora Discovery Engine, open APIs, filtering capabilities, developer tooling, reference implementation, technical documentation and capital-provider discovery standards. Together, these components form reusable infrastructure around compatible lending implementations while leaving the underlying lending logic to those protocols and applications.

Fairway leads the integrated delivery of Aurora, with technical contributions from Sundial and advisory input from Fallen Icarus where relevant. The project is delivered through four milestone-gated stages over approximately five months, with Treasury funds held under independent **3-of-5 multisignature control** throughout implementation.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**, with public repositories, documentation and operating instructions intended to make the infrastructure straightforward for technically capable third parties to inspect, deploy, integrate, modify and extend.

The long-term value of Aurora is in creating a common set of market standards and open infrastructure that future Cardano lending applications, verification systems and capital providers can build on. Establishing that shared layer early gives the ecosystem a more interoperable foundation for credit-market discovery, filtering and verification as the market develops.

Treasury funds the infrastructure once. The ecosystem can continue building on it thereafter.

# 11. Governance Submission Requirements
This section records the procedural and governance information required to align the final Aurora Treasury Withdrawal action with the proposal approved by the community.

## Canonical Proposal Reference
The final Treasury Withdrawal governance action will reference an immutable canonical version of this proposal hosted through IPFS or an equivalent content-addressed storage system.

The governance action metadata will reference the canonical document through the applicable URI and cryptographic hash so that the proposal submitted on-chain can be verified against the version reviewed by the community. The final governance action will reference only the completed canonical version of the proposal.

The final immutable reference, governance metadata and Treasury recipient credential will be generated only after the proposal text, five independent Aurora Treasury Administrators and 3-of-5 Aurora Treasury multisignature have been finalized.

Any on-chain and off-chain proposal metadata will be prepared so that the scope, requested amount and referenced proposal remain consistent with the final canonical document.

## Treasury Recipient and Administrators
The on-chain Treasury Withdrawal destination and Treasury custody structure for Aurora will be the dedicated 3-of-5 Aurora Treasury multisignature. Fairway and other implementation contributors do not directly control the Treasury withdrawal credential or hold signing authority over that multisignature.

The five independent signers of that multisignature collectively serve as the **Aurora Treasury Administrators** for Treasury-governance purposes.

Fairway remains the **Lead Implementer and project coordinator** but holds no Treasury signing key. Sundial, Fallen Icarus and other implementation contributors likewise hold no Treasury signing authority.

The Aurora Treasury Administrators are responsible for monitoring Treasury expenditure, reviewing milestone evidence, authorizing transactions within the approved scope and expenditure ceilings, maintaining public custody transparency and returning unspent funds if the project terminates.

Their designation does not give them responsibility for engineering, technical architecture or day-to-day project management.

Independent Treasury-use oversight will include an interim expenditure and reconciliation review following M2 and a final independent Treasury-use audit following M4. The reviews will assess Treasury transactions against reported expenditure, approved budget categories and applicable cumulative milestone ceilings. The reviewer will be independent of Fairway, Sundial, Fallen Icarus and the Aurora Treasury Administrators.

## Net Change Limit
This Treasury Withdrawal will only be submitted and enacted where the requested **940,000 ADA** withdrawal is within the applicable Net Change Limit established through Cardano governance.

Compliance will be assessed against the available Net Change Limit at the time the governance action is submitted, taking account of any Treasury Withdrawals already counted against the same applicable period.

If sufficient Net Change Limit is not available, the Treasury Withdrawal will not be submitted or enacted until the applicable governance conditions permit the requested withdrawal.

This commitment reflects the constitutional requirement that Treasury Withdrawals must not exceed the Net Change Limit applicable to the relevant period.

## Prior Treasury Funding Disclosure
Aurora has not previously received funding through a Cardano **Treasury Withdrawal governance action** for this project or substantially similar Treasury-funded scope during the preceding 24 months.

Fairway and other contributors may have participated in Project Catalyst, commercial projects or other Cardano ecosystem initiatives. These are separate funding mechanisms and do not constitute prior Treasury Withdrawal funding for Aurora.

Before submission, this disclosure will be confirmed against the final Treasury recipient and the entities materially participating in the proposal so that the statement accurately reflects the constitutional 24-month disclosure requirement.

## Treasury Audit and Oversight
The proposal includes funding within the **Review, Hosting & Technical Contingency** allocation for independent Treasury-use audit and oversight.

Oversight will include reconciliation of Treasury transactions and reported project expenditure, review of expenditure against the approved scope and milestone ceilings, and reporting of material deviations or unresolved issues.

This is separate from the independent software security review and legal review included in the technical delivery scope.

The audit and oversight commitment is intended to satisfy the constitutional requirement for Treasury Withdrawals to provide for independent review and oversight of the use of Treasury ADA.

Treasury oversight reporting will track cumulative ADA expenditure against the applicable milestone ceiling, expenditure by approved budget category, milestone completion status, use of contingency, material unresolved review findings and any material variance from the approved delivery schedule.

## Treasury ADA Treatment
Treasury ADA held in the Aurora Treasury multisignature before approved project expenditure will remain in the dedicated auditable Aurora Treasury custody structure.

While held by the Aurora Treasury Administrators, that ADA will **not be delegated to a stake pool operator** and will remain delegated to the predefined **Abstain** voting option in accordance with the applicable Cardano Treasury-governance requirements.

All Treasury wallet balances and transactions will remain publicly auditable.

## Conflicts and Related Parties
Fairway is the Lead Implementer.

Sundial is a technical consortium collaborator.

Fallen Icarus / Rusty serves as a technical advisor and architectural reviewer.

None of these implementation participants holds a signing key to the Aurora Treasury multisignature.

The Aurora Treasury Administrators are independent from the implementation consortium.

Any material conflict of interest relating to a Treasury transaction, milestone review or other governance decision must be disclosed. An Administrator with a material conflict must not participate in the relevant approval, and the transaction must still satisfy the required **3-of-5 multisignature threshold using non-conflicted Administrators**.

Changes to individual contributors or Administrators do not alter the approved Treasury amount, funded scope, milestone structure or Fairway's responsibility for overall project delivery.

# Appendix A: Verification Framework
Aurora's Verification Framework provides an open and extensible way for credit opportunities to reference institutional, eligibility, compliance and other proof-based information without making any single verification system a requirement of the underlying lending protocol.

Verification is one component of Aurora's broader market infrastructure. It supports discovery, filtering and evaluation by allowing compatible applications and capital providers to determine whether attached evidence satisfies their own requirements.

The framework does not determine who should receive capital, perform regulatory enforcement or create a universal participation policy.

## Framework Principles
### Technology Agnostic
Aurora does not require a specific identity provider, credential issuer, proof system or verification technology.

Different verification mechanisms may coexist within the same market infrastructure. The Metadata Standard and Verification Framework are designed so that additional credential types, proof systems and verification providers can be supported without requiring changes to the underlying lending protocol.

This allows Aurora to evolve as verification technologies and institutional requirements change.

### Proof-Based
Aurora-compatible Loan Request UTxOs may reference verifiable information that can be evaluated against an applicable schema or policy.

Depending on the use case, this may include institutional status, eligibility information, compliance-related evidence or other proof-based attributes relevant to a capital provider or application.

Aurora exposes the relevant verification references and provides infrastructure for evaluating them. Individual participants remain responsible for determining which evidence they require and how that evidence affects their own decisions.

### Privacy Compatible
The Verification Framework is designed to support privacy-preserving verification.

Sensitive underlying information does not need to be published directly on Cardano simply because a participant requires additional assurance. Where supported by the relevant verification system, applications may rely on proofs, attestations, selective disclosure or other verification references instead of exposing the underlying data.

Aurora therefore standardizes how verification information can be associated with market opportunities without prescribing where sensitive information must be stored or how every proof must be generated.

### Optional Participation
Aurora metadata and verification are optional market infrastructure.

The underlying lending implementation remains independently usable without Aurora metadata. Participants that require additional information may use Aurora-compatible metadata, filtering and verification capabilities, while participants that do not require those capabilities may interact directly with the underlying lending infrastructure.

Different credit opportunities may therefore support different verification or eligibility requirements without imposing one global participation standard across Cardano credit markets.

### Extensibility
Verification requirements vary across jurisdictions, applications and capital providers and may change over time.

The framework is therefore designed around versioned schemas and extensible verification references rather than fixed assumptions about one identity system or compliance model.

Future verification mechanisms can be incorporated where they are compatible with the published interfaces without requiring Aurora to become the issuer, custodian or central authority for the underlying information.

## Verification in the Aurora Architecture
Verification operates alongside, rather than in place of, Aurora's other market-infrastructure functions.

A compatible Loan Request UTxO may be enriched with standardized metadata containing or referencing relevant verification information. The Aurora Discovery Engine indexes that opportunity and exposes its standardized market information through open APIs.

Applications and capital providers can then:

1. discover compatible credit opportunities;
2. filter them according to relevant metadata and requirements;
3. identify associated verification information; and
4. evaluate that information against the applicable schema or policy.

The result of verification becomes one input into evaluation by the relevant participant. Aurora does not itself make the lending, underwriting or capital-allocation decision.

This separation allows the same underlying opportunity to be evaluated according to different policies without requiring the lending protocol to enforce one universal institutional standard.

## Verification Providers and Future Systems
The funded framework is not dependent on any particular identity or privacy infrastructure.

Compatible implementations may use verifiable credentials, zero-knowledge proofs, attestations, selective-disclosure systems or other verification mechanisms supported by the relevant schemas and interfaces.

Privacy-preserving systems such as Midnight may therefore be integrated where technically appropriate, but Aurora does not depend on Midnight for operation and Treasury funding does not establish a proprietary identity or credential system.

Similarly, future applications may associate repayment history, institutional performance or other verifiable information with compatible credit-market entities. Aurora provides the shared infrastructure through which such information can be referenced, indexed and exposed.

## Participant Responsibilities
Aurora provides verification infrastructure rather than regulatory enforcement.

Participants remain responsible for their own legal, regulatory, risk and operational requirements.

In particular:

* capital providers determine which evidence and verification standards they require;
* verification providers determine what information they verify and how they substantiate it;
* lending implementations determine the requirements imposed by their own contracts or applications; and
* originators and other participants determine which credentials, proofs or supporting evidence they make available.

The Verification Framework allows these different requirements to coexist through open standards rather than imposing a single global compliance model on all Aurora-compatible activity.

All Treasury-funded Verification Framework specifications, reference implementations and related software are released under **Apache License 2.0** and remain available for independent implementation and extension.

**AURORA:**

Open Infrastructure for Institutional Credit Markets on Cardano

Sundial Protocol  ·  Fairway Oy  ·  Fallen Icarus

Cardano Treasury Proposal  ·  2026

Cardano Treasury Proposal  ·  2026
