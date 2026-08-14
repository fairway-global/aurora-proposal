# Aurora

Open Infrastructure for Institutional Credit Markets on Cardano

| Field | Detail |
| --- | --- |
| Amount Requested | **1,000,000 ADA** |
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
| **Treasury Request** | **1,000,000 ADA** |
| **Delivery Period** | Approximately **5 months** |
| **Purpose** | Build open market infrastructure that makes Cardano credit opportunities discoverable, filterable, verifiable and easier to evaluate across compatible lending implementations |
| **Primary Deliverables** | Metadata Standard, Verification Framework, Aurora Discovery Engine, open APIs, filtering and query tooling, Capital Provider Profile Standard, Reference Query Library, developer tooling, reference implementation, documentation and independent review |
| **Milestones** | **4 implementation milestones** |
| **Lead Implementer** | **Fairway** |
| **Technical Collaborator** | **Sundial** |
| **Technical Advisor** | **Fallen Icarus (Rusty)** |
| **Treasury Custody** | One dedicated **3-of-5 Aurora Treasury multisignature**, with all five keys held independently of the implementation participants |
| **Open Source** | Treasury-funded software, standards and reference implementations released under **Apache License 2.0** |

## Proposal Summary
Cardano's eUTxO model allows individual credit opportunities to exist as distinct on-chain financial objects rather than requiring all lending activity to be organized through pooled liquidity. A Loan Request UTxO can represent an individual funding request or credit opportunity with its own terms and lifecycle.

That transaction-based architecture provides the foundation for open credit markets, but settlement alone does not create a coherent market. Capital providers and applications still need consistent ways to describe opportunities, discover them across implementations, filter them according to relevant criteria, evaluate verification information and monitor the information associated with them.

Aurora provides that shared market layer.

Standardized metadata can enrich a Loan Request UTxO with machine-readable market information and verification references. The Aurora Discovery Engine indexes those opportunities and exposes them through open discovery and filtering interfaces. The Verification Framework allows compatible applications and capital providers to evaluate attached proofs or verification references according to their own requirements.

Aurora does not replace the underlying lending protocols. It does not originate loans, custody lending capital or decide which opportunities should receive funding. Lending execution remains with compatible credit-market infrastructure. Aurora provides the open standards and software around those lending agreements that allow otherwise independent opportunities to become discoverable, filterable and verifiable through common infrastructure.

The Treasury-funded implementation is therefore infrastructure-only. It does not require Treasury-funded lending capital, borrower deployment, stablecoin conversion, fiat settlement or commercial loan execution. Commercial activity can use the infrastructure later, but it is not a condition of Treasury delivery.

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

The implementation culminates in an end-to-end technical demonstration and public open-source release rather than a commercial lending pilot.

## Consortium and Delivery
Aurora is delivered as one integrated implementation.

**Fairway** acts as lead implementer and project coordinator, responsible for overall delivery and integration of the funded work.

**Sundial** contributes technical input where relevant to capital-provider-facing standards, discovery and filtering specifications, reference queries, API design and interoperability.

**Fallen Icarus (Rusty)** supports Aurora as a technical advisor and reviewer, providing architectural expertise relating to Cardano's transaction-based credit-market model, Loan Request UTxO design and eUTxO-specific implementation considerations.

Treasury funds Aurora's common public outputs rather than separate organizational work packages. Contributions from consortium partners and advisors form part of the same implementation and do not create separate Treasury custody or governance tracks.

## Governance Safeguards
The full **1,000,000 ADA** Treasury allocation is held in one dedicated **3-of-5 Aurora Treasury multisignature** controlled entirely by independent Cardano ecosystem representatives.

Fairway, Sundial, Fallen Icarus and other implementation contributors hold no Treasury signing keys. Every Treasury transaction requires approval from at least three of the five independent signers.

Delivery progresses through the four milestones defined in this proposal. Fairway publishes the required milestone evidence before expenditure may progress beyond the applicable cumulative milestone ceiling, while the Aurora Treasury Administrators review that evidence against the approved completion criteria. The Treasury wallet and transactions remain publicly auditable throughout implementation, and unspent Treasury funds are returned if the project terminates under the conditions defined in Section 9.

## Open Ecosystem Commitment
Aurora complements existing and future Cardano lending implementations rather than replacing them.

The infrastructure is designed to remain protocol independent, modular and optional. It does not require one lending protocol, identity provider, verification technology or Fairway-operated service. The Discovery Engine and associated interfaces are intended to be independently operable, allowing future builders to adopt the standards without depending on the original implementation team. This matches the governing design requirement that Aurora remain open, reusable and operable without Fairway.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**. Any individual or organization may use, operate, modify, extend or commercialize those outputs in accordance with the license terms without requiring exclusive permission from Fairway, Sundial, Fallen Icarus or any other contributor.

The lasting Treasury-funded output is therefore not a private lending platform or a single deployment. It is reusable Cardano market infrastructure that future lending protocols, applications, verification providers and capital providers can build upon independently.

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
This proposal addresses both problems through a shared market layer around independent Loan Request UTxOs.

Standardized metadata enriches each opportunity with machine-readable market information and verification references. Open discovery and indexing infrastructure then makes those opportunities searchable across compatible implementations. Capital providers and applications can discover, filter and evaluate opportunities according to their own requirements while funding and settlement continue through the underlying lending infrastructure.

Aurora does not replace lending protocols or determine which opportunities should receive capital. It establishes the open standards, verification framework, discovery infrastructure, APIs and developer tooling required for independent Cardano credit opportunities to function as a coherent market.

Treasury funding builds and demonstrates this reusable infrastructure. Live lending, commercial onboarding and the generation of real repayment and underwriting evidence remain activities for separately funded commercial deployment.

# 3. Proposed Solution
This proposal builds shared market infrastructure for Cardano credit markets through open standards, verification infrastructure, discovery and indexing, filtering capabilities and developer interfaces that operate around compatible lending implementations.

The broader objective is to establish the shared market infrastructure that allows independent lending opportunities to be published, indexed, discovered, filtered, verified, evaluated and monitored through open standards rather than isolated integrations. The proposal intentionally focuses on shared market infrastructure rather than lending logic. Existing and future Cardano credit market implementations remain free to innovate independently while using common infrastructure for standardized market information, verification and discovery.

The solution does not modify core lending smart contracts. Instead, standardized metadata and verification references can be associated with individual Loan Request UTxOs, while open off-chain infrastructure reads, organizes and exposes that information to compatible applications and capital providers. A Loan Request UTxO enriched with this standardized metadata is referred to here as a “colored” Loan Request UTxO. The term is descriptive and does not represent a new ledger primitive.

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

A Loan Request UTxO enriched in this way becomes a “colored” Loan Request UTxO that can be interpreted consistently by Aurora-compatible infrastructure.

### Indexing and Verification
The Aurora Discovery Engine reads and organizes compatible Loan Request UTxOs and their associated metadata, transforming otherwise independent on-chain lending opportunities into a searchable market.

Where verification information is attached, the Verification Framework allows relevant proofs or verification references to be evaluated against the applicable schema or policy. Verification remains extensible so that different credential systems, proof systems and verification providers can coexist without becoming mandatory components of the underlying lending protocol.

The resulting standardized market information and verification status can be exposed through open APIs for use by capital providers, lending applications and other ecosystem participants.

### Discovery and Evaluation
Capital providers and compatible applications query the Aurora Discovery Engine to discover lending opportunities.

Opportunities can be filtered according to published metadata and query specifications, including criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other attributes supported by the applicable schema.

Aurora exposes the information required to discover, filter and evaluate opportunities but does not determine whether an opportunity should receive capital. Individual capital providers remain responsible for applying their own risk, eligibility, compliance and allocation criteria.

Aurora's Capital Discovery & Allocation Layer extends this open infrastructure with selected technical contributions from Sundial through a Capital Provider Profile Standard, Discovery and Filtering Specification, Reference Query Library, Market Discovery API contribution and lightweight reference integration artifacts. These outputs describe how capital-provider requirements can be represented and translated into queries against Aurora-compatible credit opportunities without creating a proprietary allocation system.

### Repayment History and Performance
Aurora is designed to track relevant loan-lifecycle information exposed by compatible lending implementations, including repayment events where those events are available on-chain.

Over time, repayment history can contribute to portable institutional credit histories and broader institutional track records that future capital providers can evaluate through the same open infrastructure. Standardizing and exposing this information reduces the need for each future participant to reconstruct historical performance independently.

Treasury funding establishes the infrastructure required to index and expose this information. The real lending activity that generates repayment, default and underwriting evidence remains outside the Treasury-funded scope.

### Funding and Settlement
Aurora does not custody capital, fund loans or perform settlement.

Once a capital provider has evaluated an opportunity, funding takes place through the compatible lending infrastructure that created the underlying Loan Request UTxO. Any subsequent fiat conversion, regulated settlement, borrower disbursement, loan servicing or other commercial operation remains the responsibility of the relevant market participants and service providers.

This separation allows Aurora to provide reusable market infrastructure without requiring one lending protocol, settlement provider, jurisdiction or commercial deployment model.

## What We Build
### Metadata Standard
A versioned, open specification describing credit-market opportunities and the metadata references associated with Loan Request UTxOs.

The standard is designed to support standardized market information while remaining extensible across lending models, jurisdictions, verification systems and future credit-market applications.

### Verification Framework
An extensible framework for attaching and evaluating verifiable institutional, eligibility, compliance and other proof-based information associated with Loan Request UTxOs.

The framework does not require a single identity system, credential issuer, proof system or verification provider. Different verification mechanisms may coexist while participants retain responsibility for determining which evidence they require.

### Aurora Discovery Engine
An open-source service that indexes compatible Loan Request UTxOs and associated metadata, supports discovery and filtering, exposes verification information, tracks relevant loan-lifecycle information and provides open APIs for compatible applications.

The Discovery Engine transforms independent lending opportunities into a searchable market without becoming the underlying lending protocol or a centralized marketplace. It is designed to be independently operable so that builders do not need to depend on Fairway or a single hosted API.

### Developer Tooling and Reference Implementation
Open developer tooling, documentation and a reference implementation demonstrating how compatible applications can attach standardized metadata, index Loan Request UTxOs, query the Discovery Engine, apply published filtering criteria and evaluate verification references.

A Treasury-funded technical demonstration will validate this lifecycle on testnet without requiring live lending or Treasury-funded loan capital.

### Capital Discovery & Allocation Layer
Aurora includes an open-source Capital Discovery & Allocation Layer developed with selected technical contributions from Sundial.

Its outputs include the Capital Provider Profile Standard, Discovery and Filtering Specification, Reference Query Library, Market Discovery API contribution, lightweight integration artifacts and supporting documentation.

These components remain open standards and reference tooling rather than a proprietary capital-allocation product.

All Treasury-funded software, standards and reference implementations will be released under Apache License 2.0. The resulting infrastructure is designed for the broader Cardano ecosystem to adopt, extend and operate independently without requiring Fairway, Sundial or any single lending implementation.

# 4. Deliverables
The project delivers open-source market infrastructure that can be adopted, extended and operated independently by future Cardano credit market implementations.

Treasury funding covers the standards, software, reference implementations, documentation and technical validation required to make independent Loan Request UTxOs discoverable, filterable, verifiable and usable in institutional and professional capital-provider workflows. It does not fund lending capital, commercial onboarding or live loan execution.

## Core Infrastructure Deliverables
1. **Metadata Standard.**
   A versioned, open specification describing credit-market opportunities and the metadata references associated with Loan Request UTxOs. The standard defines how institutionally relevant information can be attached consistently without modifying the underlying lending protocol and remains extensible across lending models, jurisdictions and verification systems.

2. **Verification Framework.**
   An extensible framework for attaching and evaluating institutional, eligibility, compliance and other proof-based information associated with Loan Request UTxOs. The framework supports multiple credential systems, proof systems and verification providers without requiring a single identity or compliance infrastructure.

3. **Aurora Discovery Engine.**
   An open-source service that indexes compatible Loan Request UTxOs and associated metadata, exposes lending opportunities through open APIs, supports discovery and filtering, provides access to verification information and tracks relevant loan-lifecycle information exposed by compatible lending implementations.
    The Discovery Engine will be independently operable so that third-party builders are not required to depend on Fairway or a single hosted service.

4. **Filtering and Query Capabilities.**
   Open filtering capabilities based on published metadata schemas and query specifications. Compatible applications and capital providers will be able to identify opportunities according to criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other standardized attributes supported by the applicable schema.

5. **Open APIs.**
   Public interfaces for querying Aurora-compatible credit opportunities, associated metadata, verification information and relevant lifecycle information.
   The APIs are intended to reduce protocol-specific integration work and enable wallets, lending applications, analytics services and other ecosystem participants to build against common market infrastructure.

6. **Developer Tooling and Reference Implementation.**
    Open tooling and reference code demonstrating how developers can create Aurora-compatible metadata, identify and index Loan Request UTxOs, query the Discovery Engine, apply filtering criteria and evaluate verification references.

    The reference implementation will demonstrate the complete infrastructure flow without requiring adoption of any single lending protocol or commercial deployment model.

7. **Documentation.**
    Technical documentation covering the Metadata Standard, Verification Framework, Discovery Engine, APIs, filtering model and reference implementation.

    Documentation will include sufficient integration and operating guidance for third-party developers to adopt the standards and operate the relevant infrastructure independently.

## Capital Discovery & Allocation Layer
Aurora includes selected technical contributions from Sundial relating to capital-provider requirements, discovery, filtering and interoperability within the broader Aurora implementation.

These contributions include:

**Capital Provider Profile Standard.**
 An open schema for representing requirements such as jurisdiction, ticket size, duration, asset, verification requirements and risk preferences.

**Discovery and Filtering Specification.**
 A published specification describing how capital-provider requirements can be translated into discovery and filtering criteria against Aurora-compatible credit opportunities.

**Reference Query Library.**
 Open examples demonstrating how prospective capital providers and compatible applications can query and filter opportunities using the published standards.

**Market Discovery API Contribution.**
 API definitions and related implementation contributions required to expose capital-provider-relevant discovery and filtering capabilities through the Aurora infrastructure.

**Lightweight Integration Artifacts.**
 Reference examples or lightweight SDK components demonstrating how external applications can integrate the Capital Provider Profile Standard and query specifications.

**Documentation.**
 Technical documentation sufficient for third parties to use, implement and extend the relevant standards and interfaces without dependence on Sundial.

These components form part of Aurora’s common open-source infrastructure rather than a separate Sundial product or independently funded workstream. Sundial contributes technical expertise where relevant, while Fairway remains responsible for integrated delivery of the proposal as lead implementer.

The Capital Discovery & Allocation Layer does not allocate Treasury capital, make lending decisions or create a proprietary capital-allocation product. It provides open standards and reference tooling that future market participants may use according to their own requirements.

## Technical Demonstration
The project will include a testnet technical demonstration showing that the core infrastructure operates together as intended.

The demonstration will show that a compatible Loan Request UTxO can be:

1. created through compatible lending infrastructure;
2. enriched with standardized metadata;
3. identified and indexed by the Aurora Discovery Engine;
4. discovered through an open API;
5. filtered according to published criteria;
6. associated with verification information that can be evaluated through the Verification Framework; and
7. consumed by a compatible reference application or query workflow.

The technical demonstration validates the infrastructure rather than commercial lending performance. It does not require Treasury-funded loan capital, fiat settlement, borrower disbursement or live SACCO lending.

## Security and Legal Review
The funded scope includes independent review appropriate to the infrastructure being delivered.

The security review will assess the Treasury-funded software and relevant technical interfaces before final release.

The legal review will assess the open infrastructure, standards and intended operating model within the scope of this proposal. It does not constitute legal approval of future lending activity or commercial deployments, which remain the responsibility of the relevant participants.

## Open-Source Release and Public Documentation
All Treasury-funded software, standards and reference implementations will be released under the **Apache License 2.0**.

Public repositories will contain the applicable source code, specifications, documentation and implementation materials required for third parties to inspect, operate, modify and extend the infrastructure.

The project will also publish public progress reporting against the approved milestones and deliverables.

The resulting infrastructure remains available to the Cardano ecosystem regardless of whether future builders use Fairway, Sundial or any particular lending implementation.

# 5. Budget and Resource Allocation
The Treasury withdrawal requests **1,000,000 ADA** for the 5-month delivery of Aurora's open credit-market infrastructure.

The revised budget funds software development, technical standards, testing, documentation, independent review, hosting and public project delivery. It does not include lending liquidity, commercial pilot execution, SACCO onboarding, stablecoin conversion or settlement operations.

Treasury funding is allocated according to the work required to deliver the approved public infrastructure rather than according to how consortium members divide implementation resources internally.

| Allocation | ADA | Approx. USD\* | Primary Scope |
| ----- | ----- | ----- | ----- |
| Core Infrastructure Development | **800,000** | **$152,000** | Metadata and verification standards, Aurora Discovery Engine, APIs, filtering capabilities, developer tooling, reference implementation, Capital Discovery & Allocation components, technical demonstration, documentation and project delivery |
| Shared Review, Hosting & Technical Contingency | **200,000** | **$38,000** | Covers approximately **80,000 ADA** for independent security and legal review, **30,000 ADA** for independent Treasury-use audit and oversight, **40,000 ADA** for infrastructure hosting and technical operations, and **50,000 ADA** for technical contingency within the approved Aurora scope. |
| **Total** | **1,000,000** | **$190,000** |  |

\*Illustrative values calculated using a reference ADA price of **US$0.19**.

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

The Core Infrastructure Development allocation is monitored against the deliverables and milestone outputs defined in Sections 4 and 7. Material changes in how the allocation is used across those approved delivery areas will be disclosed through milestone reporting.

The allocation does not fund commercial lending activity, SACCO onboarding, loan capital, settlement operations, private capital formation, institutional fundraising or revenue-generating deployment.

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

Sundial's role does not include Treasury-funded fundraising, business development, institutional relationship management, commercial onboarding or capital allocation.

## Shared Review, Hosting & Technical Contingency
The **200,000 ADA** Shared Review, Hosting & Technical Contingency allocation covers external and project-wide requirements necessary to deliver the infrastructure responsibly.

These resources include:

* Independent security review of the Treasury-funded software and relevant technical interfaces.
* Independent legal review of the open infrastructure, standards and intended operating model within the scope of this proposal.
* Infrastructure hosting required for development, testing and the technical demonstration.
* Technical contingency for unforeseen implementation requirements within the approved infrastructure scope.
* **Independent Treasury-use audit and oversight**, including reconciliation of Treasury transactions against reported expenditure, approved budget categories and milestone expenditure ceilings.

These resources do not fund commercial lending operations, regulatory work for a live lending pilot, stablecoin settlement, custody of lending capital or activities outside the Treasury-funded deliverables.

Any use of technical contingency remains limited to delivery of the approved proposal scope, requires written justification and authorization by the Aurora Treasury Administrators, and will be disclosed in the next public milestone report. Unused contingency remains unspent Treasury ADA and is subject to the proposal's normal reconciliation and refund provisions.

## Resource Allocation Principles
The revised allocation follows four principles.

First, Treasury funds are allocated according to the infrastructure and supporting work required to deliver the approved public outputs rather than according to the internal compensation arrangements of consortium members.

Second, Fairway remains responsible for overall delivery while technical contributions from consortium partners are incorporated into the same implementation programme where appropriate.

Third, external expenditure is limited to independent review, Treasury-use audit and oversight, hosting and technical contingency directly related to delivery of the public infrastructure.

Fourth, no portion of the Treasury withdrawal is reserved for lending capital or commercial deployment.

Internal allocation of implementation resources may be adjusted by the lead implementer as required to complete the approved work, provided that the total Treasury request, funded scope, milestone requirements and public deliverables remain unchanged.

The resulting budget therefore maps directly to the public outputs defined in Section 4 and limits Treasury expenditure to infrastructure that remains available to Cardano after the funded delivery period ends.

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

# 7. Milestones and Success Criteria
Aurora is delivered through four milestones over approximately five months.

Each milestone is tied to concrete public outputs that can be independently reviewed. Fairway remains responsible for integrated delivery of the proposal, with technical contributions from consortium partners and advisors incorporated where appropriate.

| Milestone | Timeline | ADA Allocation | Primary Outcome |
| ----- | ----- | ----- | ----- |
| M1: Specifications & Architecture | Month 1 | **150,000** | Core standards and implementation architecture finalized |
| M2: Core Build | Months 2–3 | **350,000** | Discovery, verification, indexing, filtering and API infrastructure operational on testnet |
| M3: Integration & Technical Demonstration | Month 4 | **300,000** | Reference implementation, developer tooling and complete testnet workflow demonstrated |
| M4: Independent Review & Public Release | Month 5 | **200,000** | Independent review completed and final open-source infrastructure released |
| **Total** | **Approximately 5 months** | **1,000,000** |  |

## M1: Specifications & Architecture
**Timeline:** Month 1
 **ADA Allocation:** **150,000 ADA**

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
 **ADA Allocation:** **350,000 ADA**

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
 **ADA Allocation:** **300,000 ADA**

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
* The technical demonstration requires no Treasury-funded lending capital, borrower deployment, fiat settlement or commercial loan execution.
* Public milestone report published.

## M4: Independent Review & Public Release
**Timeline:** Month 5
**ADA Allocation:** **200,000 ADA**

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
* A technically capable third party can operate the relevant Aurora infrastructure without dependence on Fairway, Sundial or any individual advisor.
* Final report maps the completed public outputs against the proposal deliverables and milestone requirements.

## Milestone Expenditure Principles
The milestone allocations define the maximum cumulative Treasury expenditure authorized as implementation progresses. At project commencement, expenditure of up to **150,000 ADA** is authorized for M1. Following approval of M1, the cumulative expenditure ceiling increases to **500,000 ADA**; following approval of M2, to **800,000 ADA**; and following approval of M3, to the full **1,000,000 ADA**. Completion of M4 triggers final project reconciliation and reporting.

Fairway remains responsible for integrated delivery of Aurora, while the Aurora Treasury Administrators review the public milestone evidence before authorizing progression to the next expenditure ceiling.

# 8. Risks and Mitigation
Aurora's infrastructure-only scope limits Treasury risk primarily to technical delivery, interoperability, security and long-term usability of the resulting public infrastructure.

**Underlying credit-market implementation dependency.** Aurora operates around compatible lending infrastructure rather than replacing the underlying lending contracts. Differences in Loan Request UTxO structures or delays in individual lending implementations could therefore affect integration testing.

Aurora mitigates this risk by defining its metadata, discovery and verification infrastructure through open interfaces rather than depending on one exclusive lending protocol. The reference implementation and testnet demonstration are intended to validate compatibility against representative Loan Request UTxO structures while preserving protocol independence.

**Interoperability and specification risk.** Different lending implementations, capital-provider requirements and future use cases may require metadata or query structures that are not known at the time of the initial release.

The Metadata Standard, Verification Framework and filtering specifications are therefore designed to be versioned, extensible and modular. Published schemas and open APIs allow future implementations to extend the infrastructure without requiring changes to the underlying lending protocol or dependence on proprietary rules.

**Verification-system dependency.** Institutional verification requirements may rely on different credential systems, proof systems or verification providers.

Aurora does not require a single verification technology. The Verification Framework separates verification references and policies from the underlying lending contracts so that multiple verification systems can coexist and evolve independently.

**Security and implementation risk.** Defects in the Discovery Engine, APIs, verification logic or developer tooling could produce incorrect indexing, filtering or verification results.

The project includes independent security review of the Treasury-funded software and relevant interfaces. Material findings affecting the funded release must be addressed or transparently documented before final completion. The architecture also keeps Aurora separate from custody and lending-contract execution, limiting the consequences of defects in the market-information layer.

**Independent operability risk.** Open-source code provides limited public value if the infrastructure can only be operated through Fairway-hosted services or undocumented internal dependencies.

Aurora mitigates this through public repositories, Apache License 2.0, build and deployment instructions, developer documentation and final completion criteria requiring a technically capable third party to operate the relevant infrastructure without dependence on Fairway, Sundial or any individual advisor.

**Adoption risk.** Open standards do not guarantee adoption by future lending protocols, applications or capital providers.

The proposal mitigates this risk by keeping the infrastructure optional, protocol independent and reusable. Aurora does not require existing lending implementations to change their core contracts, and its APIs, reference implementation and query standards are intended to reduce the integration work required for third-party adoption. Treasury delivery is measured by completion and usability of the public infrastructure rather than by speculative adoption targets.

**Delivery schedule risk.** The approximately five-month implementation period is intentionally focused but requires standards development, implementation, integration, review and documentation to progress in parallel where appropriate.

Fairway remains responsible for coordinating the integrated delivery. The four milestone structure provides intermediate verification of specifications, core functionality and the end-to-end technical demonstration before final release. Independent review preparation may begin before implementation is fully complete so that review does not unnecessarily delay the final milestone.

**Legal and regulatory interpretation.** Aurora provides open market infrastructure rather than regulatory enforcement, custody or lending services. Nevertheless, standards and interfaces intended for institutional use may raise legal questions about how the infrastructure should be described or operated.

The funded scope therefore includes independent legal review of the open infrastructure and intended operating model. Future lending activity, jurisdiction-specific compliance and commercial deployment remain outside the Treasury proposal and remain the responsibility of the relevant market participants.

# 9. Governance and Oversight
Aurora uses a single, independently controlled Treasury custody structure designed for a focused infrastructure implementation.

The full **1,000,000 ADA** Treasury allocation is held in a dedicated **3-of-5 Aurora Treasury multisignature wallet** controlled entirely by independent Cardano ecosystem representatives. Fairway leads delivery of the project but holds no Treasury signing key. Sundial, Fallen Icarus and other implementation contributors likewise hold no signing authority over Treasury funds.

Project expenditure progresses against the four milestones defined in Section 7. Fairway publishes milestone evidence before expenditure may progress beyond the applicable cumulative milestone ceiling, and every Treasury transaction requires approval from at least three of the five Aurora Treasury Administrators.

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

For Treasury-governance purposes, the five independent multisignature signers collectively serve as the **Aurora Treasury Administrators**. This designation does not create a separate governance body or additional custody structure. The Administrators are the same five individuals who control the 3-of-5 Aurora Treasury multisignature.

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
The milestone schedule controls the maximum cumulative Treasury expenditure authorized as implementation progresses. The full Treasury allocation remains in the same Aurora Treasury multisignature throughout the project; milestone progression does not involve transfers between separate project wallets.

| Milestone | ADA Allocation |
| ----- | ----- |
| M1: Specifications & Architecture | **150,000** |
| M2: Core Build | **350,000** |
| M3: Integration & Technical Demonstration | **300,000** |
| M4: Independent Review & Public Release | **200,000** |
| **Total** | **1,000,000** |

At project commencement, expenditure of up to 150,000 ADA is authorized for M1. Following approval of M1, the cumulative expenditure ceiling increases to 500,000 ADA. Following approval of M2, it increases to 800,000 ADA. Following approval of M3, the full 1,000,000 ADA becomes available for completion of M4. M4 completion triggers final reconciliation and reporting.

Before expenditure may progress to the next cumulative milestone ceiling:

1. Fairway publishes the milestone evidence required under Section 7.
2. The Aurora Treasury Administrators review the published outputs against the approved completion criteria.
3. Progression to the next cumulative expenditure ceiling requires authorization through the 3-of-5 Aurora Treasury multisignature.

Milestone review is evidence-based and practical. Signers confirm that the relevant specifications, repositories, software, documentation, demonstrations or independent-review outputs have been published and reasonably satisfy the approved criteria.

They are not expected to reproduce the engineering work or independently reimplement Aurora.

Treasury funds may be used only for the approved Aurora infrastructure scope and may not be used for lending capital, commercial lending activity, borrower funding, stablecoin settlement or unrelated company expenditure.

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
Aurora establishes shared market infrastructure for Cardano credit markets.

The proposal funds the open standards, software and developer infrastructure required to make independent Loan Request UTxOs discoverable, filterable, verifiable and easier to evaluate through common interfaces rather than isolated protocol-specific integrations.

The funded outputs include the Metadata Standard, Verification Framework, Aurora Discovery Engine, open APIs, filtering capabilities, developer tooling, reference implementation, technical documentation and related capital-provider discovery standards. Together, these components provide a reusable market layer around compatible lending implementations without replacing their underlying lending logic.

Aurora does not custody lending capital, originate loans, make credit decisions or require one lending protocol, verification provider, settlement provider or commercial deployment model. Treasury funding is limited to development and technical validation of the public infrastructure. Commercial lending, borrower deployment and the generation of real repayment, default and underwriting evidence remain outside the funded scope.

Fairway leads delivery of the integrated implementation, with technical contributions from Sundial and advisory input from Fallen Icarus where relevant. These roles support delivery of a common set of Aurora outputs rather than separate Treasury-funded organizational work packages.

The project is delivered through four milestone-gated stages over approximately five months. Treasury funds remain under independent 3-of-5 multisignature control throughout implementation, with no implementation participant holding a Treasury signing key.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**, with public repositories, documentation and operating instructions designed to allow technically capable third parties to inspect, operate, modify and extend the infrastructure without dependence on Fairway, Sundial or any individual contributor.

The lasting value of Aurora is therefore not a single lending deployment or proprietary platform. It is a common set of standards and open infrastructure that future Cardano builders, lending implementations, verification providers and capital providers can adopt independently.

By establishing that shared layer now, Cardano gains reusable infrastructure for credit-market discovery, filtering and verification before incompatible proprietary approaches become the default.

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
This Treasury Withdrawal will only be submitted and enacted where the requested **1,000,000 ADA** withdrawal is within the applicable Net Change Limit established through Cardano governance.

Compliance will be assessed against the available Net Change Limit at the time the governance action is submitted, taking account of any Treasury Withdrawals already counted against the same applicable period.

If sufficient Net Change Limit is not available, the Treasury Withdrawal will not be submitted or enacted until the applicable governance conditions permit the requested withdrawal.

This commitment reflects the constitutional requirement that Treasury Withdrawals must not exceed the Net Change Limit applicable to the relevant period.

## Prior Treasury Funding Disclosure
Aurora has not previously received funding through a Cardano **Treasury Withdrawal governance action** for this project or substantially similar Treasury-funded scope during the preceding 24 months.

Fairway and other contributors may have participated in Project Catalyst, commercial projects or other Cardano ecosystem initiatives. These are separate funding mechanisms and do not constitute prior Treasury Withdrawal funding for Aurora.

Before submission, this disclosure will be confirmed against the final Treasury recipient and the entities materially participating in the proposal so that the statement accurately reflects the constitutional 24-month disclosure requirement.

## Treasury Audit and Oversight
The proposal includes funding within the **Shared Review, Hosting & Technical Contingency** allocation for independent Treasury-use audit and oversight.

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

Similarly, future applications may associate repayment history, institutional performance or other verifiable information with compatible credit-market entities. Aurora provides the shared infrastructure through which such information can be referenced, indexed and exposed; the commercial activity that generates real repayment or performance evidence remains outside the Treasury-funded scope.

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
