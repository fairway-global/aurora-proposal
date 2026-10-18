# 9. Governance and Oversight
If the Treasury Withdrawal is approved and enacted, the full 940,000 ADA allocation will initially be received into a dedicated 3-of-5 AURORA Treasury multisignature controlled by independent Cardano ecosystem representatives.

Fairway is responsible for delivery but holds no signing key to that multisignature. Sundial, Fallen Icarus and other implementation contributors likewise hold no signing authority over funds held by the administrators.

The administrators authorize implementation instalments and supporting-cost disbursements under Section 7. Each transaction from the multisignature requires at least three independent signatures. Implementation instalments are paid to Fairway's designated implementation wallet, beginning at project commencement. Subsequent releases follow review of the preceding milestone against its approved completion criteria.

Fairway controls its implementation wallet, manages implementation resources and remains accountable for delivery. Independent audits cover the funding arrangement described in Section 11. Funds remaining under administrator custody are publicly auditable and subject to the refund provisions below.

## AURORA Treasury Multisig
The AURORA Treasury multisignature holds funds pending authorized disbursement. Undisbursed funds remain under independent 3-of-5 control. Implementation instalments leave this custody structure when transferred to Fairway under the approved payment schedule.

### Proposed AURORA Treasury Administrators
| Role | Representative | X |
| ----- | ----- | ----- |
| Independent Governance Signer | James "Blockjock" Meidinger | @blockjock2017 |
| Independent Governance Signer | Christian Taylor | @DeOpenSourceGuy |
| Independent Governance Signer | Elder Millennial | @TheElderMillenial |
| Independent Technical Signer | Wilco USDM | @iamwilco |
| Independent Signer | Eddie D | @eddie_d123 |

No implementation consortium member holds a signing key.

For Treasury-governance purposes, the five independent multisignature signers collectively serve as the **AURORA Treasury Administrators**. This designation does not create a separate governance body or additional custody structure. The Administrators are the same five AURORA Treasury Administrators who control the 3-of-5 AURORA Treasury multisignature.

The AURORA Treasury Administrators are responsible for:

* holding undisbursed Treasury funds;
* reviewing milestone evidence against the approved completion criteria;
* authorizing implementation instalments and supporting-cost disbursements within the approved funding limits;
* monitoring fund use and delivery through the records and independent audits defined in Section 11;
* suspending further disbursements where material delivery problems or evidence of fund misuse arise;
* maintaining public transparency over administrator-held balances and disbursements; and
* returning funds remaining under administrator custody in accordance with the refund provisions.

The AURORA Treasury Administrators do not manage engineering, determine AURORA's technical architecture, choose implementation contributors, divide work between consortium participants or acquire ownership or control over Treasury-funded outputs.

Any material conflict of interest relating to a proposed transaction or milestone decision must be disclosed. A conflicted Administrator must abstain from the relevant approval, and the transaction must still satisfy the required 3-of-5 multisignature threshold using non-conflicted signers.

A material conflict includes a direct financial interest, or a material indirect financial interest through an employer, controlled entity or close commercial affiliate, in a proposed Treasury payment or paid project engagement.

If an Administrator resigns, loses access to a signing key or becomes permanently unavailable, the remaining Administrators may, **where the existing multisignature remains capable of satisfying its 3-of-5 authorization threshold**, authorize replacement with another independent Cardano ecosystem representative. Where replacement requires creation of a new multisignature credential, the unspent Treasury balance may be migrated to a replacement 3-of-5 AURORA Treasury multisignature preserving the same independence and signing threshold. Any signer replacement and resulting custody address will be publicly disclosed before funds are moved.

## Milestone Oversight
The milestone schedule governs releases from the AURORA Treasury multisignature under Section 7. Implementation instalments are transferred to Fairway's designated implementation wallet. Funds not yet disbursed remain under administrator custody.

| Milestone | ADA Allocation |
| ----- | ----- |
| M1: Specifications & Architecture | **140,000** |
| M2: Core Build | **320,000** |
| M3: Integration & Technical Demonstration | **290,000** |
| M4: Independent Review & Public Release | **190,000** |
| **Total** | **940,000** |

The initial release funds commencement of M1. Each subsequent stage is funded following acceptance of the preceding milestone, within the cumulative disbursement limits defined in Section 7.

Before each subsequent release:

1. Fairway publishes the milestone evidence required under Section 7.
2. The AURORA Treasury Administrators review the published outputs against the approved completion criteria.
3. At least three independent administrators authorize the relevant disbursement.

Implementation payments are advances for the next stage of agreed work. They are not reimbursements requiring Fairway to demonstrate equivalent internal expenditure.

Milestone review is evidence-based and practical. The Treasury Administrators confirm that the relevant specifications, repositories, software, documentation, demonstrations or independent-review outputs have been published and reasonably satisfy the approved completion criteria. They are not expected to reproduce the engineering work or independently reimplement AURORA.

Treasury funds may be used only for the approved AURORA infrastructure scope and milestone deliverables defined in this proposal.

## Operational Responsibility
Fairway remains responsible as lead implementer and project coordinator for delivery of AURORA.

Fairway coordinates implementation planning, consortium contributions, external technical and professional services, milestone evidence, public reporting and overall delivery of the approved scope.

Sundial contributes technical implementation input where relevant to the common AURORA outputs. Fallen Icarus may provide architectural review and advisory input where relevant to the underlying credit-market architecture and Loan Request UTxO model.

These contributions remain part of one integrated AURORA implementation and do not create separate Treasury budgets, custody arrangements or governance tracks.

The AURORA Treasury Administrators oversee custody, disbursements and milestone accountability. Fairway controls day-to-day implementation, staffing, subcontracting and internal resource allocation. Routine implementation expenses paid from Fairway's implementation wallet do not require administrator approval.

## Transparency and Reporting
The AURORA Treasury multisignature address will be published before project expenditure begins.

All Treasury transactions remain publicly auditable on-chain.

Fairway will publish one public progress report for each milestone. Each report will:

* link to the relevant public specifications, repositories, software, documentation or review materials;
* summarize completion against the applicable milestone criteria;
* state implementation payments received, supporting-cost disbursements and the balance remaining under administrator custody; and
* identify any material delivery issues or remediation items.

The final report will map the completed Treasury-funded outputs against the approved proposal deliverables and provide links to the final open-source repositories and documentation.

Treasury ADA held in the AURORA Treasury multisignature prior to approved project expenditure will not be delegated to a stake pool operator and will remain delegated to the predefined Abstain voting option in accordance with the applicable Cardano Treasury governance requirements.

## Refund and Remediation
If a milestone is materially incomplete, the AURORA Treasury Administrators may suspend further disbursements while Fairway addresses the identified deficiencies.

If the milestone remains incomplete 60 days after its target date and no satisfactory remediation plan has been agreed, further disbursements may remain suspended and the project may proceed to termination.

If the project terminates before completion, all ADA remaining under administrator custody will be returned to the Cardano Treasury using the applicable Treasury return mechanism.

Implementation payments for completed and accepted work are assessed against the agreed outputs and are not recalculated against Fairway's actual internal costs. Release of an advance does not constitute acceptance of unfinished work or remove Fairway's responsibility for its delivery.

Changes to individual contributors do not change the approved AURORA deliverables or Fairway's responsibility for overall project delivery.

---

[Previous](08-risks-and-mitigation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](10-conclusion.md)
