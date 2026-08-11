# 9. Governance and Oversight
Aurora uses a single, independently controlled Treasury custody structure designed for a focused infrastructure implementation.

The full **1,000,000 ADA** Treasury allocation is held in a dedicated **3-of-5 Aurora Treasury multisignature wallet** controlled entirely by independent Cardano ecosystem representatives. Fairway leads delivery of the project but holds no Treasury signing key. Sundial, Fallen Icarus and other implementation contributors likewise hold no signing authority over Treasury funds.

Project expenditure progresses against the four milestones defined in Section 7. Fairway publishes milestone evidence before expenditure may progress beyond the applicable cumulative milestone ceiling, and every Treasury transaction requires approval from at least three of the five independent signers.

## Aurora Treasury Multisig
The Aurora Treasury multisignature is the sole custody wallet for the Treasury allocation.

All Treasury funds remain under independent **3-of-5 multisignature control** until used for approved project expenditure.

### Proposed Independent Signers
| Role | Representative | X |
| ----- | ----- | ----- |
| Independent Governance Signer | James "Blockjock" Meidinger | @blockjock2017 |
| Independent Governance Signer | Christian Taylor | @DeOpenSourceGuy |
| Independent Governance Signer | Elder Millennial | @TheElderMillenial |
| Independent Technical Signer | Adrian / PurritoGeneral | @PurritoGeneral |
| Independent Signer | **TBA** | — |

No implementation consortium member holds a signing key.

For Treasury-governance purposes, the five independent multisignature signers collectively serve as the **Aurora Treasury Administrators**. This designation does not create a separate governance body or additional custody structure. The Administrators are the same five independent signers who control the 3-of-5 Aurora Treasury multisignature.

The Aurora Treasury Administrators are responsible for:

* custody of Treasury funds;
* reviewing milestone evidence;
* authorizing expenditure within the approved project scope and milestone limits;
* monitoring use of Treasury funds and progress against the approved deliverables;
* suspending further expenditure where material delivery problems arise;
* maintaining public transparency over Treasury balances and transactions; and
* returning unspent Treasury funds if the project terminates.

The Aurora Treasury Administrators do not manage engineering, determine Aurora's technical architecture, choose implementation contributors, divide work between consortium participants or acquire ownership or control over Treasury-funded outputs.

Any material conflict of interest relating to a proposed transaction or milestone decision must be disclosed. A conflicted Administrator must abstain from the relevant approval, and the transaction must still satisfy the required 3-of-5 multisignature threshold using non-conflicted signers.

If an Administrator resigns, loses access to a signing key or becomes permanently unavailable, the remaining Administrators may, **where the existing multisignature remains capable of satisfying its 3-of-5 authorization threshold**, authorize replacement with another independent Cardano ecosystem representative. Where replacement requires creation of a new multisignature credential, the unspent Treasury balance may be migrated to a replacement 3-of-5 Aurora Treasury multisignature preserving the same independence and signing threshold. Any signer replacement and resulting custody address will be publicly disclosed before funds are moved.

## Milestone Oversight
The milestone schedule controls the maximum cumulative Treasury expenditure authorized as implementation progresses. The full Treasury allocation remains in the same Aurora Treasury multisignature throughout the project; milestone progression does not involve transfers between separate project wallets.

| Milestone | ADA Allocation |
| ----- | ----- |
| M1: Specifications & Architecture | **150,000** |
| M2: Core Build | **350,000** |
| M3: Integration & Technical Demonstration | **300,000** |
| M4: Independent Review & Public Release | **200,000** |
| **Total** | **1,000,000** |

At project commencement, expenditure of up to 150,000 ADA is authorized for M1. Following approval of M1, the cumulative expenditure ceiling increases to 500,000 ADA. Following approval of M2, it increases to 800,000 ADA. Following approval of M3, the full 1,000,000 ADA becomes available for completion of M4. M4 completion triggers final reconciliation and reporting.

Before expenditure may progress to the next cumulative milestone ceiling:

1. Fairway publishes the milestone evidence required under Section 7.
2. The Aurora Treasury Administrators review the published outputs against the approved completion criteria.
3. Progression to the next cumulative expenditure ceiling requires authorization through the 3-of-5 Aurora Treasury multisignature.

Milestone review is evidence-based and practical. Signers confirm that the relevant specifications, repositories, software, documentation, demonstrations or independent-review outputs have been published and reasonably satisfy the approved criteria.

They are not expected to reproduce the engineering work or independently reimplement Aurora.

Treasury funds may be used only for the approved Aurora infrastructure scope and may not be used for lending capital, commercial lending activity, borrower funding, stablecoin settlement or unrelated company expenditure.

## Operational Responsibility
Fairway remains responsible as lead implementer and project coordinator for delivery of Aurora.

Fairway coordinates implementation planning, consortium contributions, external technical and professional services, milestone evidence, public reporting and overall delivery of the approved scope.

Sundial contributes technical implementation input where relevant to the common Aurora outputs. Fallen Icarus may provide architectural review and advisory input where relevant to the underlying credit-market architecture and Loan Request UTxO model.

These contributions remain part of one integrated Aurora implementation and do not create separate Treasury budgets, custody arrangements or governance tracks.

The Aurora Treasury Administrators oversee Treasury custody, expenditure and milestone accountability but do not direct day-to-day implementation.

## Transparency and Reporting
The Aurora Treasury multisignature address will be published before project expenditure begins.

All Treasury transactions remain publicly auditable on-chain.

Fairway will publish one public progress report for each milestone. Each report will:

* link to the relevant public specifications, repositories, software, documentation or review materials;
* summarize completion against the applicable milestone criteria;
* state Treasury expenditure to date; and
* identify any material delivery issues or remediation items.

The final report will map the completed Treasury-funded outputs against the approved proposal deliverables and provide links to the final open-source repositories and documentation.

Treasury ADA held in the Aurora Treasury multisignature prior to approved project expenditure will not be delegated to a stake pool operator and will remain delegated to the predefined Abstain voting option in accordance with the applicable Cardano Treasury governance requirements.

## Refund and Remediation
If a milestone is materially incomplete, the Aurora Treasury Administrators may suspend further Treasury expenditure while Fairway addresses the identified deficiencies.

If the milestone remains incomplete **60 days after its target date** and no satisfactory remediation plan has been agreed with the independent signers, further expenditure may remain suspended and the project may proceed to termination under the conditions below.

If the project terminates before completion, all unspent ADA remaining in the Aurora Treasury multisignature will be returned to the Cardano Treasury using the applicable Treasury return mechanism.

Legitimately incurred expenditure against approved project work remains project expenditure and is accounted for through public milestone reporting and financial reconciliation.

Changes to individual contributors do not change the approved Aurora deliverables or Fairway's responsibility for overall project delivery.

---

[Previous](08-risks-and-mitigation.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](10-conclusion.md)
