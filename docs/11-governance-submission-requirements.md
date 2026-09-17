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
This Treasury Withdrawal will only be submitted and enacted where the requested **940,000 ADA** withdrawal is within the applicable Net Change Limit established through Cardano governance.

Compliance will be assessed against the available Net Change Limit at the time the governance action is submitted, taking account of any Treasury Withdrawals already counted against the same applicable period.

If sufficient Net Change Limit is not available, the Treasury Withdrawal will not be submitted or enacted until the applicable governance conditions permit the requested withdrawal.

This commitment reflects the constitutional requirement that Treasury Withdrawals must not exceed the Net Change Limit applicable to the relevant period.

## Prior Treasury Funding Disclosure
Aurora has not previously received funding through a Cardano **Treasury Withdrawal governance action** for this project or substantially similar Treasury-funded scope during the preceding 24 months.

Fairway and other contributors may have participated in Project Catalyst, commercial projects or other Cardano ecosystem initiatives. These are separate funding mechanisms and do not constitute prior Treasury Withdrawal funding for Aurora.

Before submission, this disclosure will be confirmed against the final Treasury recipient and the entities materially participating in the proposal so that the statement accurately reflects the constitutional 24-month disclosure requirement.

## Treasury Audit and Oversight
The proposal includes funding within the **Review, Hosting & Technical Contingency** allocation for independent Treasury-use audit and oversight.

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

---

[Previous](10-conclusion.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](appendix-a-verification-framework.md)
