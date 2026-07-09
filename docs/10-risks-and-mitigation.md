# 10. Risks and Mitigation

**Pogun implementation timing.** The pilot is designed for compatibility with Pogun's credit market architecture, which remains the preferred implementation. However, deployment is not dependent on Pogun's production launch. During the infrastructure phase (M1-M2), development and testing proceed against Fallen Icarus' cardano-loans architecture and other compatible development environments. If Pogun's mainnet deployment is delayed, the pilot may instead utilize an alternative audited Cardano credit market infrastructure implementation that preserves compatibility with the metadata standard and underlying credit market architecture. Pilot liquidity will not be deployed until an approved audited implementation is available, and any necessary milestone adjustments will be coordinated with the Treasury administrator.

**Repayment risk.** Treasury capital is deployed to participating SACCOs rather than individual borrowers. SACCOs remain responsible for underwriting, monitoring, collections and absorbing losses arising from SME or individual borrower defaults under their existing lending operations.

The pilot uses a progressive funding model, with capital released across three deployment rounds. Continued participation and larger allocations depend on successful repayment performance during earlier rounds. A SACCO that fails to meet its repayment obligations may be suspended or permanently excluded from future participation, with repayment history forming the basis of its on-chain institutional credit record.

The purpose of the pilot is not to eliminate credit risk, but to transparently measure repayment performance, validate risk-management approaches and establish the institutional reputation required for sustainable, market-driven capital formation after the pilot concludes.

**SACCO adoption.** SACCOs may need more time to adopt new processes than anticipated. The pilot starts with the simplest model (one loan per SACCO) and only moves to more granular structures when institutions are operationally ready. Fairway's existing relationships with the initial SACCO cohort reduce onboarding friction, but expansion to additional institutions may take longer than planned.

**Exchange rate exposure.** Loans are denominated in USDM but disbursed in Ethiopian Birr. Currency movements during the loan term create risk. SACCOs, as institutions with diversified portfolios, are better positioned to absorb this than individual borrowers, which is one reason the pilot targets SACCOs rather than end-borrowers directly.

**Settlement delays**. The pilot initially utilizes Encryptus for cross-border settlement. Operational or regulatory delays may affect individual deployments. Capital is deployed incrementally, allowing settlement workflows to be validated at small scale before subsequent deployment rounds. Equivalent regulated settlement providers may be adopted if required.

**Infrastructure iteration.** The metadata standard and indexer are new and will need refinement based on real-world usage.

---

[← 9. Milestones and Success Criteria](09-milestones-and-success-criteria.md) · [Table of Contents](../README.md) · [11. Governance and Oversight →](11-governance-and-oversight.md)
