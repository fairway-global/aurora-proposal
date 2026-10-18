# 11. Governance Submission Requirements
This section records the procedural and governance information required to align the final AURORA Treasury Withdrawal action with the proposal approved by the community.

## Canonical Proposal Reference
The final Treasury Withdrawal governance action will reference an immutable canonical version of this proposal hosted through IPFS or an equivalent content-addressed storage system.

The governance action metadata will reference the canonical document through the applicable URI and cryptographic hash so that the proposal submitted on-chain can be verified against the version reviewed by the community. The final governance action will reference only the completed canonical version of the proposal.

The final immutable reference, governance metadata and Treasury recipient credential will be generated only after the proposal text, five independent AURORA Treasury Administrators and 3-of-5 AURORA Treasury multisignature have been finalized.

Any on-chain and off-chain proposal metadata will be prepared so that the scope, requested amount and referenced proposal remain consistent with the final canonical document.

## Treasury Recipient and Administrators
Fairway is the Treasury Withdrawal Recipient and lead implementer. If approved and enacted, the withdrawal will initially be received into a dedicated 3-of-5 AURORA Treasury multisignature operated by the independent AURORA Treasury Administrators, who hold and disburse funds under this proposal. Fairway and other implementation contributors do not control that withdrawal credential or hold signing authority over the administrator multisignature.

The five independent signers of that multisignature collectively serve as the **AURORA Treasury Administrators** for Treasury-governance purposes.

Fairway remains the **Lead Implementer and project coordinator** but holds no Treasury signing key. Sundial, Fallen Icarus and other implementation contributors likewise hold no Treasury signing authority.

The AURORA Treasury Administrators hold undisbursed funds, review milestone evidence, authorize implementation instalments and supporting-cost disbursements, monitor fund use and delivery under the oversight arrangements below, maintain public custody transparency and administer the refund provisions in Section 9.

An interim independent Treasury-use audit will take place following publication of the M2 technical outputs. The final independent Treasury-use audit will be completed during M4 before final project closure. Both audits cover the funding arrangement and records defined below. The reviewer will be independent of Fairway, Sundial, Fallen Icarus and the AURORA Treasury Administrators.

The interim audit runs separately from technical milestone acceptance. Its completion is not an additional M2 acceptance criterion. Material findings concerning fund misuse or delivery remain grounds for suspending further disbursements under Section 9.

## Net Change Limit
This Treasury Withdrawal will only be submitted and enacted where the requested **940,000 ADA** withdrawal is within the applicable Net Change Limit established through Cardano governance.

Compliance will be assessed against the available Net Change Limit at the time the governance action is submitted, taking account of any Treasury Withdrawals already counted against the same applicable period.

If sufficient Net Change Limit is not available, the Treasury Withdrawal will not be submitted or enacted until the applicable governance conditions permit the requested withdrawal.

This commitment reflects the constitutional requirement that Treasury Withdrawals must not exceed the Net Change Limit applicable to the relevant period.

## Prior Treasury Funding Disclosure
Fairway has not previously received direct funding through a Cardano Treasury Withdrawal governance action for AURORA or substantially similar scope during the 24 months preceding this submission.

Fairway has received Treasury-derived ADA through Project Catalyst during that period for separate identity and credential projects, including the Fund 12 project "Leveraging National ID system in Ethiopia for more scalable adoption of Cardano in identity solutions" (project ID 1200143).

This prior funding is disclosed separately from the AURORA request, which funds the infrastructure deliverables defined in Section 4.

## Treasury Audit and Oversight
The proposal reserves approximately 20,000 ADA for independent Treasury-use audits and oversight within the Review, Hosting & Technical Contingency allocation.

The audits will examine:

* administrator-held balances and transactions;
* authorization of implementation payments against the agreed funding limits and milestone evidence;
* supporting-cost expenditure and any approved budget reallocations, including their purpose and associated implementation work;
* expenditure from the separate Review, Hosting & Technical Contingency allocation;
* delivery against the approved public outputs; and
* material deviations, unresolved findings and any required Treasury returns.

Fairway's Core Infrastructure Development payments are fixed payments for agreed delivery. Their assessment does not require routine reconciliation against Fairway's internal payroll, contributor compensation, supplier invoices or implementation margin. The reviews are project-specific and do not constitute an audit of Fairway's general company accounts.

Public oversight reporting will identify amounts disbursed, funds remaining under administrator custody, milestone status, supporting-cost expenditure and material unresolved findings.

These Treasury-use audits are separate from the software security and legal reviews. They provide independent oversight of the funding arrangement and use of Treasury ADA.

## Treasury ADA Treatment
Treasury ADA remains in the dedicated auditable AURORA Treasury multisignature until disbursed under the approved funding arrangement. Implementation instalments are then held and managed by Fairway in its designated implementation wallet.

While held by the AURORA Treasury Administrators, that ADA will **not be delegated to a stake pool operator** and will remain delegated to the predefined **Abstain** voting option in accordance with the applicable Cardano Treasury-governance requirements.

All Treasury wallet balances and transactions will remain publicly auditable.

## Conflicts and Related Parties
Fairway is the Lead Implementer.

Sundial is a technical consortium collaborator.

Fallen Icarus / Rusty serves as a technical advisor and architectural reviewer.

None of these implementation participants holds a signing key to the AURORA Treasury multisignature.

The AURORA Treasury Administrators are independent from the implementation consortium.

Any material conflict of interest relating to a Treasury transaction, milestone review or other governance decision must be disclosed. An Administrator with a material conflict must not participate in the relevant approval, and the transaction must still satisfy the required **3-of-5 multisignature threshold using non-conflicted Administrators**.

Changes to individual contributors or Administrators do not alter the approved Treasury amount, funded scope, milestone structure or Fairway's responsibility for overall project delivery.

---

[Previous](10-conclusion.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](appendix-a-verification-framework.md)
