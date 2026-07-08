# 2. Motivation

In traditional lending, every loan begins as an individual agreement between specific parties with its own terms, risk profile, repayment schedule, and settlement conditions. Much like a transaction, each loan exists as a discrete financial object that can be originated, funded, serviced, transferred, and settled independently. Only after loans are created do financial institutions aggregate them into portfolios, funds, or securitized products.

Most DeFi lending protocols reverse this process. Capital is first deposited into a shared pool, and borrowers draw from that pool according to predefined rules. While effective for certain use cases, this model does not reflect how most real-world credit markets operate.

Cardano's eUTxO architecture is uniquely suited to the loan-first model. Unlike account-based DeFi, where lending is typically organized around shared liquidity pools, Cardano's transaction-based architecture naturally represents individual financial relationships as distinct on-chain objects. This makes it well suited for programmable institutional credit markets built around discrete lending agreements.

Individual loans can exist as distinct on-chain UTxOs with their own state and logic, allowing them to be independently discovered, funded, and settled before being aggregated into larger credit portfolios. This creates a strong foundation for programmable credit markets that more closely resemble real-world lending.

Two problems block real-world credit activity on Cardano today.

## Institutions need KYC, but on-chain lending is pseudonymous.

Pogun's credit market already lets any two parties negotiate and fund a loan on-chain. But institutional lenders, regulated entities, and professional capital allocators operate under compliance frameworks that require verifiable identity and eligibility checks.

Without a way to attach those assurances to on-chain activity, these participants simply cannot use the market.

Advances in zero-knowledge technologies make it possible to verify that a counterparty satisfies specific requirements without exposing sensitive personal data. Implemented as optional transaction metadata rather than changes to the core contracts, this compliance layer can be added without compromising the permissionless nature of the underlying protocol.

## SACCOs need capital, but traditional finance rails are too expensive.

Savings and Credit Cooperative Organizations (SACCOs) are regulated, member-owned financial institutions that provide savings and lending services to their local communities. In many emerging markets they form the primary source of credit for individuals and SMEs underserved by commercial banks. Rather than creating new lending institutions, this proposal connects digital capital with trusted financial institutions that already understand their borrowers, operate within local regulatory frameworks and have established loan servicing capabilities.

Ethiopia was selected as the initial pilot jurisdiction because of established consortium relationships, experienced local partners and a mature cooperative financial sector. The infrastructure itself remains **jurisdiction agnostic** and is designed to support institutional credit markets wherever compatible financial institutions and regulated settlement providers exist.

Demand for lending capacity far exceeds what they can fund internally, and the cost of capital through conventional channels is prohibitive. Through Fairway's local partnerships, the consortium has already secured pilot participation from Ethiopian SACCOs and continues expanding its institutional network.

The opportunity extends far beyond a small pilot cohort. Cooperative financial institutions are among the most scalable channels for deploying productive capital. Rather than onboarding thousands of individual businesses one by one, a single institutional relationship immediately provides access to an established lending operation with existing borrowers, underwriting processes, repayment collection and local regulatory compliance.

This allows Cardano-native capital to scale through existing financial infrastructure rather than replacing it.

## Bringing the Two Together

This proposal addresses both problems together: build the metadata and verification infrastructure that lets institutions participate, then validate it through a Treasury-backed pilot that puts real capital to work for SACCOs that need it.

The result is not simply a lending pilot, but a practical test of whether Cardano can support a new category of programmable credit markets built around open Credit Markets, optional verification, and real-world capital formation.

---

[← 1. Summary](01-summary.md) · [Table of Contents](../README.md) · [3. Proposed Solution →](03-proposed-solution.md)
