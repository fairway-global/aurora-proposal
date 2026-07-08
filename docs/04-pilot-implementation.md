# 4. Pilot Implementation

The pilot validates the metadata and indexer infrastructure described in Section 3 through real lending activity with Ethiopian Savings and Credit Cooperative Organizations (SACCOs). An ADA allocation reserved for pilot liquidity is converted into USDM (or another approved Cardano-native USD-denominated stable asset) and deployed through the pilot. Encryptus initially provides the settlement infrastructure connecting on-chain lending activity with local banking rails.

Ethiopian SACCOs provide an attractive environment for validation. They already originate and service loans, possess established borrower relationships, and face significant unmet demand for lending capital.

The consortium has already secured pilot participation from Ethiopian SACCOs and continues expanding its institutional network in preparation for deployment. The initial pilot validates the infrastructure with a small cohort of institutions before progressively expanding participation as operational experience and on-chain credit histories are established.

The pilot therefore begins with existing financial institutions that have already agreed in principle to participate, rather than requiring the consortium to recruit lending partners after Treasury funding is received.

## Structure

The pilot begins with the simplest operational model: one Loan Request UTxO per participating SACCO.

Each SACCO publishes a funding request through Pogun's credit market contracts (or similar) and receives capital to support its existing lending operations. The SACCO continues using its established underwriting, servicing and repayment processes while the pilot validates Cardano's ability to coordinate capital participation and repayment tracking. This approach minimizes operational complexity while the infrastructure is new.

As participating institutions become familiar with the framework, subsequent deployment rounds may evaluate more granular structures, including Loan Request UTxOs representing lending programs, loan categories or individual business lending opportunities.

The objective is not to prescribe a single market structure from the outset, but to determine which levels of granularity create the most efficient and scalable credit market while remaining practical for participating institutions.

## Process Flow

1. **Loan Request.** A participating SACCO publishes a Loan Request UTxO through Pogun's credit market contracts (or similar) with verification metadata attached.

2. **Verification.** The off-chain indexer verifies the SACCO's attached proof and exposes the lending opportunity through the discovery interface.

3. **Funding.** Following conversion into USDM, pilot capital is deployed into eligible lending opportunities through the credit market infrastructure.

4. **Settlement.** Encryptus initially supports conversion between USDM (or another approved Cardano-native USD-denominated stable asset) and locally accessible fiat currency. Pilot capital is transferred from funded Loan Request UTxOs to the designated settlement address, converted and paid to participating SACCOs through their existing banking relationships. Loan repayments follow the reverse settlement path and return to the credit market infrastructure for capital recycling. The consortium may utilize equivalent regulated settlement providers where operational, regulatory or technical considerations make this appropriate.

5. **Servicing.** SACCOs remain responsible for:

   1. Borrower onboarding.
   2. Underwriting decisions.
   3. Local compliance.
   4. Repayment collection.
   5. Recovery processes where required.
   6. Exchange rate risk between USDM and the local fiat currency.

   Repayment events are recorded on-chain and contribute to the development of verifiable credit histories and future reputation systems.

6. **Capital Recycling.** As loans are repaid, Treasury capital becomes available for redeployment into new lending opportunities. Subsequent deployment rounds may incorporate additional institutions and alternative Loan Request UTxO structures based on operational feedback and pilot outcomes.

## Why This Is Low Risk

The pilot launches with participating SACCOs that have already executed Memorandums of Understanding with the consortium and already perform lending as their core business.

Rather than replacing existing financial institutions, Cardano supplies capital and infrastructure to organizations that already possess local expertise, borrower relationships and servicing capabilities.

Treasury capital is not exposed to a single institution. The pilot begins with three independent SACCOs and progressively expands only where repayment performance and operational readiness have been demonstrated.

$100k goes a long way in Ethiopia. Typical SACCO loans are small and short, so the pilot can fund meaningful lending activity across multiple institutions without requiring a large Treasury commitment.

SACCOs already have the legal structures, borrower relationships, and servicing operations in place. Cardano is not taking on the role of lender; it is supplying capital to institutions that already know how to lend.

Targeting SACCOs rather than end-borrowers also manages exchange rate risk. Loans are denominated in USDM (or another approved Cardano-native USD-denominated stable asset), but disbursed in Ethiopian Birr, creating currency exposure. SACCOs, as institutions with diversified loan portfolios and operational reserves, are better positioned to absorb this risk than individual SME borrowers would be.

Because all loans live on-chain as UTxOs, dReps and any other Cardano stakeholder can monitor loan health in real time without relying on off-chain reporting. The indexer API makes this data queryable, and a lightweight dashboard for dReps to track the status of Treasury-funded loans is a natural addition to the tooling scope.

The phased deployment model further reduces risk by validating operational processes before expanding participation or introducing more sophisticated market structures.

## What the Pilot Proves

The pilot validates the complete lifecycle of a Cardano-native credit market:

* Metadata attachment.
* Zero-knowledge proof verification.
* Indexed loan discovery.
* On-chain capital participation.
* Stablecoin settlement.
* Real-world loan disbursement.
* Repayment tracking.
* Capital recycling.
* Reputation formation.

The primary objective of the pilot is to validate Cardano's novel technical approach to programmable credit markets. The resulting economic impact, expanding lending capacity for regulated financial institutions and improving access to affordable capital, is the real-world validation of that infrastructure rather than the primary deliverable itself.

More broadly, the pilot evaluates whether Cardano's eUTxO architecture can support programmable institutional credit markets at scale.

The pilot also validates whether the metadata standard, indexer and reporting infrastructure satisfy the requirements of prospective capital providers evaluating future participation.

The long-term objective is to establish the foundations for open credit market infrastructure capable of supporting institutional, stablecoin, ADA and Bitcoin-backed capital participation across multiple jurisdictions and lending models.

---

[← 3. Proposed Solution](03-proposed-solution.md) · [Table of Contents](../README.md) · [5. Treasury Participation Model →](05-treasury-participation-model.md)
