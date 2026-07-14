# 1. Summary

## Proposal at a Glance

| Category | Summary |
| ----- | ----- |
| **Treasury Request** | **2,900,000 ADA** |
| **Development Budget** | **2,200,000 ADA** |
| **Pilot Liquidity** | **700,000 ADA** (targeting approximately USD 100,000 equivalent at conversion) |
| **Delivery Period** | 12 months |
| **Purpose** | Build open-source institutional credit market infrastructure and validate it through a Treasury-backed SACCO pilot |
| **Primary Deliverables** | Metadata standard, off-chain indexer, developer tooling, dRep dashboard, pilot case study, Capital Provider Readiness Framework |
| **Funding Model** | Development funding released only upon milestone approval. Pilot liquidity released progressively (30% / 30% / 40%) based on successful deployment and repayment performance. |
| **Treasury Custody** | Independent 2-of-3 Treasury multisignature administered by Independent Treasury Trustees. Development and pilot liquidity follow separate governance workflows. |
| **Development Custody** | Independent 3-of-5 multisignature with two consortium signers and three independent signers. |
| **Treasury Protection** | Progressive deployments, milestone gating, public reporting, independent audits, published wallet addresses, and dRep monitoring dashboard. |
| **End of Pilot** | Remaining Treasury principal together with Treasury-entitled proceeds returned according to the approved participation framework. |
| **Open Source** | Apache License 2.0; repositories, documentation and build instructions published no later than M2. |

## Governance Safeguards

* Independent Treasury Trustees control Treasury custody.
* Treasury funds remain undelegated and delegated to **Abstain** until approved disbursement.
* Public milestone reporting and independent financial review.
* Canonical proposal published through immutable IPFS reference.
* Remaining Treasury principal and Treasury-entitled proceeds returned at project completion.
* Undistributed development funds refunded if milestones are not completed.

## Proposal Summary

Cardano's eUTxO model enables decentralized credit markets built around individual Loan Request UTxOs rather than pooled liquidity. The infrastructure is designed as reusable, jurisdiction-agnostic public infrastructure that can support institutional credit markets wherever compatible lending institutions and regulated settlement providers exist. This proposal, led by Fairway in collaboration with Fallen Icarus and Sundial, delivers the infrastructure and market validation required to establish open, programmable credit markets on Cardano.

The project consists of two complementary phases.

## Phase 1: Build Open Credit Market Infrastructure

The project establishes an optional metadata and trust layer that enables identity, compliance and other trust signals to be attached to Cardano-native lending without modifying the underlying smart contracts.

A versioned transaction metadata standard and open-source off-chain indexer allow participants to verify zero-knowledge proofs derived from verifiable credentials while keeping the underlying lending infrastructure fully permissionless. The same framework is designed to support future trust, reputation and verification use cases beyond KYC.

The infrastructure is designed to integrate with Pogun's credit market architecture and other compatible Cardano lending implementations while remaining independent of any single protocol. The objective is to establish reusable public infrastructure that multiple credit market implementations can adopt rather than creating another isolated lending platform.

## Phase 2: Validate Through Real Lending

The infrastructure is validated through a Treasury-backed pilot with Ethiopian Savings and Credit Cooperative Organizations (SACCOs).

The primary objective of the pilot is to validate Cardano's novel technical approach to programmable institutional credit markets. The resulting economic impact, expanding lending capacity for regulated financial institutions and improving access to affordable capital, serves as the real-world validation of that infrastructure rather than the primary deliverable itself.

In addition to the operating budget, the Treasury Withdrawal includes a 700,000 ADA allocation reserved exclusively for pilot lending liquidity, targeting approximately USD 100,000 of lending capital at the time of withdrawal. Following withdrawal, this allocation is converted into USDM (or another approved Cardano-native USD-denominated stable asset) and deployed into verified lending opportunities. Participating SACCOs continue performing borrower onboarding, underwriting, loan servicing and collections through their existing legal and operational frameworks, while loan metadata, verification status, funding events and repayment history are recorded on-chain, creating transparent and verifiable lending activity.

The pilot follows a phased deployment model, beginning with SACCO-level Loan Request UTxOs and evaluating more granular lending structures as participating institutions and infrastructure mature.

Pilot liquidity is recycled as loans are repaid, allowing the same Treasury allocation to support multiple lending rounds while establishing the first on-chain credit histories for participating institutions. Once that trustless on-chain track record exists, participating SACCOs can continue attracting future capital without further Treasury funding.

Throughout the pilot, Sundial contributes ecosystem partnerships and institutional market expertise to validate that the infrastructure developed through this proposal can support future participation by stablecoin providers, institutional allocators, Bitcoin-backed capital providers and other professional market participants.

The pilot's lasting value is not the lending activity itself, but the reusable metadata standard, indexer, institutional credit histories and capital-provider framework that remain available to the broader Cardano ecosystem.

## Open Ecosystem Commitment

Aurora extends existing Cardano lending infrastructure rather than replacing it.

The project is designed to complement existing credit market initiatives rather than compete with them. Protocols such as Pogun focus on originating and settling credit relationships. Aurora provides reusable metadata, verification and discovery infrastructure that enables institutional participation across compatible credit market implementations. By separating lending logic from institutional infrastructure, future builders can innovate independently while sharing common standards rather than recreating institutional onboarding, verification and discovery systems.

The pilot is designed to remain compatible with the credit market architecture pioneered by Fallen Icarus and implemented by Pogun. Where appropriate, it may integrate with Pogun's production infrastructure. However, the objectives of this proposal do not depend on any single implementation. Should Pogun's production deployment be delayed or unavailable, the consortium may utilize equivalent audited lending contracts or compatible partner infrastructure while preserving the same metadata standard, indexer architecture and credit market model.

All software, standards and implementation learnings developed through the project will be released as open source under the Apache License 2.0 (or your chosen license). Public source repositories, documentation and build instructions will be published no later than completion of M2. The Cardano ecosystem may freely use, audit, modify, fork and integrate the resulting infrastructure into future credit market applications in accordance with the license terms.

The consortium does not seek Treasury funding to operate a private lending platform. No consortium member receives preferential rights to operate or commercialize the resulting infrastructure. Any individual or organization may use, operate, extend or commercialize the open-source outputs under the terms of the applicable license without requiring Fairway, Sundial, Fallen Icarus or further Treasury funding.

Treasury funding establishes reusable open infrastructure, including metadata standards, verification frameworks, indexing infrastructure and operational models, that any Cardano credit market participant may adopt without requiring Fairway or continued Treasury funding.

The purpose of this proposal is to establish an **open, community-owned institutional layer** for Cardano credit markets before proprietary implementations emerge. Any future credit market implementation may build upon these standards without requiring Fairway, Sundial, Fallen Icarus or additional Treasury funding.

## Consortium

* **Fairway** leads infrastructure development, pilot execution and institutional onboarding.
* **Fallen Icarus** provides credit market architecture, technical review and lending protocol expertise.
* **Sundial** contributes institutional market expertise, ecosystem relationships and capital-provider engagement activities that help ensure the resulting infrastructure meets the operational, compliance and reporting requirements of future private capital providers.

## Pilot Service Providers

The pilot utilizes independent operational service providers that are **not recipients of Treasury funding** and are **not members of the delivery consortium**.

* **Independent Treasury Trustees (2-of-3 multisignature custody)** provide independent custody and governance of the Treasury allocation. They receive Treasury funds, approve development milestone releases, authorize the ADA-to-stablecoin conversion, administer pilot liquidity according to the approved governance framework and return the remaining Treasury principal together with Treasury-entitled proceeds at the conclusion of the pilot.
* **Encryptus (Initial regulated settlement partner).** Provides regulated cross-border settlement infrastructure connecting Cardano-native stable assets with local banking rails for pilot capital deployment and repayment.

---

[Proposal Home](../README.md) · [Full proposal](../proposal.md) · [2. Motivation →](./02-motivation.md)
