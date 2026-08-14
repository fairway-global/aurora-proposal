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

---

[Previous](02-motivation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](04-deliverables.md)
