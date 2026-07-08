# 9. Milestones and Success Criteria

The project is delivered through five milestones across two phases. ADA funds development and execution activities. Pilot Liquidity is released separately and only after the infrastructure is operational.

## Milestone Schedule

| Milestone | Timeline | ADA Release | Pilot Liquidity Release |
| ----- | ----- | ----- | ----- |
| M1: Specification and Design | Month 1 | 300,000 | — |
| M2: Infrastructure Delivery | Months 2-3 | 500,000 | — |
| M3: Pilot Round 1 | Months 4-5 | 400,000 | Approximately 30% of the pilot liquidity allocation |
| M4: Pilot Round 2 and Market Validation | Months 6-8 | 500,000 | Approximately additional 30% of the pilot liquidity allocation |
| M5: Pilot Round 3, Capital Readiness and Ecosystem Handover | Months 9-12 | 500,000 | Approximately additional 40% of the pilot liquidity allocation |

**Total Treasury Withdrawal: 2,900,000 ADA**

## Phase 1: Infrastructure

### M1: Specification and Design

#### Deliverables

* Tx metadata standard specification for identity proofs, verification status and compliance information.
* Indexer architecture document.
* Confirmed SACCO cohort with signed partnership agreements.
* Pilot operating model covering participant roles, settlement flow and risk parameters.

#### Success Criteria

* Metadata specification published and open for community review.
* Indexer design reviewed by Fallen Icarus for alignment with Cardano credit market architecture, CIP-89, and compatibility with Pogun's implementation.
* At least three SACCOs confirmed for pilot participation (Three Ethiopian SACCOs have signed Memorandums of Understanding to participate in the initial pilot, with many additional institutions currently progressing through onboarding discussions).
* Pilot operating model approved by project partners.

**ADA Release:** 300,000

### M2: Infrastructure Delivery

#### Deliverables

* Working off-chain indexer deployed to testnet.
* Metadata standard implemented and validated against Pogun's credit market architecture, with compatibility for alternative Cardano credit market implementations.
* Developer documentation and integration guides.
* Settlement workflow validated end-to-end on testnet.

#### Success Criteria

* A Loan Request UTxO containing verification metadata can be created, indexed, verified, queried and filtered through the API.
* Documentation is sufficient for a third-party developer to integrate with the metadata standard and indexer.
* Settlement workflow confirmed operational.
* Testnet demonstration completed.

**ADA Release:** 500,000

## Phase 2: Pilot

### M3: Pilot Round 1

#### Deliverables

* First pilot liquidity deployment into live loan contracts with verified SACCOs.
* Infrastructure deployed to mainnet.
* dRep monitoring dashboard operational.
* First public progress report.

#### Success Criteria

* Up to 30,000 USDM deployed across at least two SACCOs.
* End-to-end flow validated on mainnet:
  * metadata attachment,
  * proof verification,
  * indexed discovery,
  * on-chain funding,
  * settlement into ETB,
  * loan servicing underway.
* dRep dashboard displaying live loan status and deployment metrics.
* Public progress report published.

**ADA Release:** 400,000

**Pilot Liquidity Release:** ≈ 30,000$

### M4: Pilot Round 2 and Market Validation

#### Deliverables

* Second USDM deployment incorporating recycled capital from Round 1 repayments together with an additional ≈ 30,000 USDM Treasury allocation.
* Infrastructure improvements based on operational feedback.
* Additional SACCOs onboarded where appropriate.
* Assessment of more granular lending models, including lending-program and borrower-level Loan Request UTxOs.
* Sundial-led engagement with prospective stablecoin providers, institutional allocators, market makers and Bitcoin-backed capital participants.
* Validation of compliance, reporting, discovery, custody and operational requirements for future capital providers.

#### Success Criteria

* Repayment activity recorded on-chain from Round 1 loans.
* Additional ≈ 30,000 USDM deployed, plus any recycled capital.
* Public progress report published.
* Prospective capital providers have evaluated the metadata standard, indexer and pilot workflows.
* Capital provider requirements documented and prioritized for implementation.

**ADA Release:** 500,000

**Pilot Liquidity Release:** ≈ 30,000$ (contingent on demonstrated repayment activity from Round 1)

### M5: Pilot Round 3, Capital Readiness and Ecosystem Handover

#### Deliverables

* Final USDM deployment incorporating recycled capital from previous lending rounds together with the final ≈ 40,000 USDM Treasury allocation, completing the ≈  100,000 USDM pilot.
* Pilot case study covering operational outcomes, repayment performance, capital recycling and infrastructure performance.
* Documented SACCO feedback on onboarding, operational friction and scalability.
* Sundial Capital Provider Readiness Framework documenting requirements gathered from prospective stablecoin providers, institutional allocators, market makers and Bitcoin-backed capital participants.
* Final infrastructure refinements based on pilot and capital-provider feedback, including recommendations for metadata, indexer and institutional workflow integration.
* Documentation of participation models for future stablecoin, ADA and Bitcoin-backed capital providers.
* Final public documentation, open-source release and ecosystem handover.
* Return of remaining Treasury principal and Treasury-entitled proceeds.

#### Success Criteria

* Approximately 100,000 USDM cumulatively deployed across three Treasury deployment rounds.
* Multiple lending and repayment cycles completed with on-chain repayment history.
* Treasury capital recycling successfully demonstrated.
* SACCO feedback collected and published.
* Capital Provider Readiness Framework completed and published.
* Infrastructure recommendations finalized based on institutional validation.
* Final documentation and open-source deliverables published.
* Treasury principal and Treasury-entitled proceeds returned according to the approved participation framework.

**ADA Release:** 500,000

**Pilot Liquidity Release:** ≈ 40,000$ (contingent on demonstrated repayment activity from Round 2)

## Pilot Liquidity Release Principles

USDM is released in three tranches. Each tranche after the first requires evidence that previously deployed capital has been successfully utilized and that repayment activity is occurring on-chain.

Progress can be independently verified through the indexer API and dRep monitoring dashboard without relying solely on off-chain reporting.

If a deployment round materially underperforms, Treasury retains the ability to withhold subsequent USDM tranches.

At the conclusion of the pilot, remaining Treasury principal and Treasury-entitled proceeds are returned according to the approved participation framework.

---

[← 8. Consortium and Relevant Experience](08-consortium-and-relevant-experience.md) · [Table of Contents](../README.md) · [10. Risks and Mitigation →](10-risks-and-mitigation.md)
