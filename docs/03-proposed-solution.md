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

### Developer Tooling and Reference Implementation
Open developer tooling, documentation and a reference implementation demonstrating how compatible applications can create Aurora-compatible metadata, identify and index Loan Request UTxOs, query the Discovery Engine, apply published filtering criteria and evaluate verification references.

The reference implementation is intended to reduce duplicated integration work across the ecosystem and provide a practical starting point for future Cardano builders adopting the standards.

A Treasury-funded technical demonstration will validate the end-to-end infrastructure flow on testnet.

### Capital Discovery Layer
Aurora includes an open-source Capital Discovery Layer developed with selected technical contributions from Sundial.

Its outputs include the Capital Provider Profile Standard, Discovery and Filtering Specification, Reference Query Library, Market Discovery API contribution, lightweight integration artifacts and supporting documentation.

These components provide common ways for capital-provider requirements to be represented and translated into queries against Aurora-compatible credit opportunities. They remain open standards and reference tooling rather than a proprietary capital-allocation system.

All Treasury-funded software, standards and reference implementations will be released under **Apache License 2.0**.

The resulting infrastructure is intended to become part of Cardano's shared credit-market stack: initially implemented through Aurora, but available for lending protocols, applications, capital providers and future builders to adopt, operate and extend independently.

---

[Previous](02-motivation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](04-deliverables.md)
