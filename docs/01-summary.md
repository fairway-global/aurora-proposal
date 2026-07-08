# 1. Summary

Cardano's eUTxO model enables decentralized credit markets built around individual Loan Request UTxOs rather than pooled liquidity. The infrastructure is designed as reusable, jurisdiction-agnostic public infrastructure that can support institutional credit markets wherever compatible lending institutions and regulated settlement providers exist. This proposal, led by Fairway in collaboration with Fallen Icarus and Sundial, delivers the infrastructure and market validation required to establish open, programmable credit markets on Cardano.

The project consists of two complementary phases.

## Phase 1: Build Open Credit Market Infrastructure

The project establishes an optional metadata and trust layer that enables identity, compliance and other trust signals to be attached to Cardano-native lending without modifying the underlying smart contracts.

A versioned transaction metadata standard and open-source off-chain indexer allow participants to verify zero-knowledge proofs derived from verifiable credentials while keeping the underlying lending infrastructure fully permissionless. The same framework is designed to support future trust, reputation and verification use cases beyond KYC.

The infrastructure is designed to integrate with Pogun's credit market and other compatible Cardano lending implementations, while remaining independent of any single protocol or production deployment.

## Phase 2: Validate Through Real Lending

The infrastructure is validated through a Treasury-backed pilot with Ethiopian Savings and Credit Cooperative Organizations (SACCOs).

The primary objective of the pilot is to validate Cardano's novel technical approach to programmable institutional credit markets. The resulting economic impact, expanding lending capacity for regulated financial institutions and improving access to affordable capital, serves as the real-world validation of that infrastructure rather than the primary deliverable itself.

In addition to the operating budget, the Treasury Withdrawal includes a 700,000 ADA allocation reserved exclusively for pilot lending liquidity, targeting approximately USD 100,000 of lending capital at the time of withdrawal. Following withdrawal, this allocation is converted into USDM (or another approved Cardano-native USD-denominated stable asset) and deployed into verified lending opportunities. Participating SACCOs continue performing borrower onboarding, underwriting, loan servicing and collections through their existing legal and operational frameworks, while loan metadata, verification status, funding events and repayment history are recorded on-chain, creating transparent and verifiable lending activity.

The pilot follows a phased deployment model, beginning with SACCO-level Loan Request UTxOs and evaluating more granular lending structures as participating institutions and infrastructure mature.

Pilot liquidity is recycled as loans are repaid, allowing the same Treasury allocation to support multiple lending rounds while establishing the first on-chain credit histories for participating institutions. Once that trustless on-chain track record exists, participating SACCOs can continue attracting future capital without further Treasury funding.

Throughout the pilot, Sundial leads capital-provider development and market-readiness activities, engaging prospective stablecoin providers, institutional allocators, market makers and Bitcoin-backed capital participants to validate the compliance, reporting and operational requirements needed for broader market adoption.

The pilot's lasting value is not the lending activity itself, but the reusable metadata standard, indexer, institutional credit histories and capital-provider framework that remain available to the broader Cardano ecosystem.

## Open Ecosystem Commitment

Sundown extends existing Cardano lending infrastructure rather than replacing it.

The project introduces an optional metadata, verification and discovery layer that complements existing lending protocols, including Pogun, while preserving open participation and avoiding liquidity fragmentation.

The pilot is designed to remain compatible with the credit market architecture pioneered by Fallen Icarus and implemented by Pogun. Where appropriate, it may integrate with Pogun's production infrastructure. However, the objectives of this proposal do not depend on any single implementation. Should Pogun's production deployment be delayed or unavailable, the consortium may utilize equivalent audited lending contracts or compatible partner infrastructure while preserving the same metadata standard, indexer architecture and credit market model.

All infrastructure, standards and implementation learnings developed through the project will be open source and available for the broader Cardano ecosystem to adopt, extend and integrate into future credit market applications.

The consortium does not seek Treasury funding to operate a private lending platform. Treasury funding establishes reusable open infrastructure, including metadata standards, verification frameworks, indexing infrastructure and operational models, that any Cardano credit market participant may adopt without requiring Fairway or continued Treasury funding.

## Consortium

* **Fairway** leads infrastructure development, pilot execution and institutional onboarding.
* **Fallen Icarus** provides credit market architecture, technical review and lending protocol expertise.
* **Sundial** leads capital provider engagement and market readiness, ensuring the infrastructure supports future participation by institutional, stablecoin and Bitcoin-backed capital providers.

## Pilot Service Providers

The pilot utilizes independent operational service providers that are **not recipients of Treasury funding** and are **not members of the delivery consortium**.

* **Independent Treasury Trustees (2-of-3 multisignature custody)** provide independent custody and governance of the Treasury allocation. They receive Treasury funds, approve development milestone releases, authorize the ADA-to-stablecoin conversion, administer pilot liquidity according to the approved governance framework and return the remaining Treasury principal together with Treasury-entitled proceeds at the conclusion of the pilot.
* **Encryptus (Initial regulated settlement partner).** Provides regulated cross-border settlement infrastructure connecting Cardano-native stable assets with local banking rails for pilot capital deployment and repayment.

---

[Table of Contents](../README.md) · [2. Motivation →](02-motivation.md)
