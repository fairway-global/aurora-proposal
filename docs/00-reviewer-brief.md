# Reviewer Brief

Aurora asks the Cardano Treasury to fund open infrastructure for institutional credit markets: a metadata standard, an off-chain verification indexer, developer documentation, and a real-world pilot that validates the infrastructure through regulated Ethiopian SACCOs.

## Why It Matters

Cardano already has the architectural ingredients for loan-first credit markets: eUTxO state, programmable loan objects, and discovery through beacon-style patterns. The missing layer is institutional trust infrastructure. Professional capital providers need to know who they are funding, what compliance checks apply, how repayment performance is tracked, and how risk is reported without turning the base lending protocol into a permissioned system.

Aurora keeps those concerns outside the core contracts. Identity, verification, compliance references, and repayment reputation are attached as optional metadata and verified by open indexer infrastructure. That makes the work reusable by Pogun and by future Cardano credit market implementations.

## Funding Request

| Component | ADA | Purpose |
| --- | ---: | --- |
| Operating Budget | 2,200,000 | Metadata standard, indexer, tooling, documentation, pilot execution, reporting, audits, and ecosystem coordination |
| Pilot Liquidity | 700,000 | Independently administered revolving lending capital, converted into an approved Cardano-native USD-denominated stable asset |
| **Total** | **2,900,000** | **12-month delivery and pilot validation** |

## Reviewer Signals

| Question | Where to Review |
| --- | --- |
| What public good is funded? | [Proposed Solution](./03-proposed-solution.md), [Deliverables](./06-deliverables.md) |
| How are Treasury funds protected? | [Treasury Participation Model](./05-treasury-participation-model.md), [Governance and Oversight](./11-governance-and-oversight.md) |
| How is pilot risk contained? | [Pilot Implementation](./04-pilot-implementation.md), [Risks and Mitigation](./10-risks-and-mitigation.md) |
| What gets delivered at each milestone? | [Milestones and Success Criteria](./09-milestones-and-success-criteria.md) |
| What happens after the pilot? | [Treasury Participation Model](./05-treasury-participation-model.md), [Conclusion](./12-conclusion.md) |

## Core Safeguards

- Independent 2-of-3 Treasury Trustee custody for the full Treasury allocation.
- Separate 3-of-5 Development Fund multisignature with independent signer majority.
- Pilot liquidity released progressively across 30% / 30% / 40% deployment rounds.
- Public milestone reports, published wallet addresses, indexer visibility, and dRep monitoring dashboard.
- Remaining Treasury principal and Treasury-entitled proceeds returned at pilot conclusion.
- Open-source release under Apache License 2.0 no later than M2.

---

[Proposal Home](../README.md) · [Full proposal](../proposal.md)
