# 6. Deliverables

## Phase 1: Infrastructure

1. **Tx metadata standard.** A versioned, open-source schema for attaching identity proofs, verification status, and compliance information to credit market UTxOs. Designed to be extensible beyond KYC and support future trust, reputation and verification use cases.
2. **Off-chain indexer.** An open-source service that monitors the chain for credit market UTxOs, verifies attached ZK proofs, tracks loan lifecycles, and exposes a query API for filtered loan discovery.
3. **Documentation.** Integration guides for originators, capital providers, and developers who want to build on the metadata standard or operate their own indexer infrastructure.
4. **Institutional Credit Market Framework.** Documentation of lessons learned regarding different Loan Request UTxO models, including SACCO-level, program-level and more granular lending structures evaluated during the pilot.

## Phase 2: Pilot

1. **Lending**. Live lending activity using the 700,000 ADA pilot liquidity allocation, targeting approximately USD 100,000 of lending capital following conversion into an approved Cardano-native USD-denominated stable asset.

2. **Pilot case study.** A public report covering operational outcomes, repayment performance, capital recycling metrics, and infrastructure performance under real-world conditions.
3. **SACCO feedback.** Documented feedback from participating SACCOs on the onboarding process, operational friction, and what would need to change for them to scale their participation.
4. **Reputation and Credit History Framework.** Documentation of how repayment history can be associated with lending entities and used to support future reputation and trust systems.

5. **dRep monitoring dashboard.** A lightweight tool allowing dReps to track the status and health of Treasury-funded loans in real time.
6. **Sundial Capital Provider Readiness Framework.** Documentation produced through engagement with prospective stablecoin providers, institutional allocators, market makers and Bitcoin-backed capital participants. The framework documents compliance requirements, reporting expectations, workflow integration, operational requirements and recommended infrastructure improvements required for broader participation in Cardano-native credit markets.

All infrastructure is open-source and available for the broader Cardano ecosystem to adopt or extend.

---

[← 5. Treasury Participation Model](05-treasury-participation-model.md) · [Table of Contents](../README.md) · [7. Budget and Resource Allocation →](07-budget-and-resource-allocation.md)
