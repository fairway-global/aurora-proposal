# 3. Proposed Solution

This proposal builds an optional metadata and trust layer designed for Cardano credit market infrastructure, with initial integration targeting Pogun's credit market architecture while remaining compatible with alternative implementations.

The broader objective is to establish the foundations of a Cardano-native credit market, where lending opportunities can be discovered, evaluated and funded through open market infrastructure. Rather than modifying the underlying lending protocol, the proposal focuses on the metadata, verification and discovery infrastructure required to support institutional participation.

The solution does not modify core lending smart contracts. Instead, it uses Cardano transaction metadata to attach identity and compliance information to loan UTxOs, and an off-chain indexer to read and verify that metadata. This allows the infrastructure to remain compatible with Pogun's architecture while also supporting alternative audited credit market implementations where appropriate.

## Why metadata instead of smart contract logic?

### Efficiency

Verification of identity, compliance and eligibility proofs using zero-knowledge systems can be computationally expensive. Cardano's on-chain execution budgets and available Plutus primitives are not designed for this workload.

By moving proof verification to the off-chain indexer, we avoid these constraints entirely. The indexer can execute arbitrarily complex verification logic without affecting transaction costs or throughput.

### Flexibility

Compliance requirements differ across jurisdictions and evolve over time. A metadata standard can be versioned and extended without redeploying or migrating smart contracts. New credential types, proof systems and regulatory frameworks can be supported through updates to the indexer and metadata schema rather than changes to the lending protocol itself.

### Permissionlessness

The core credit market contracts remain untouched and fully open. Any participant can still originate, fund or repay a loan without metadata attached. Participants who require additional assurances can use metadata and verification frameworks to evaluate opportunities, while participants who do not require them can interact directly with the underlying market.

Verification therefore becomes optional infrastructure rather than a protocol requirement.

## How It Works

### Loan Origination

A SACCO or other originator creates a Loan Request UTxO through a compatible Cardano credit market implementation, with the initial pilot targeting Pogun's credit market architecture.

Depending on the implementation, a Loan Request UTxO may represent a SACCO funding request, a lending program, or an individual lending opportunity.

Optionally, the originator may attach transaction metadata containing a zero-knowledge proof derived from a verifiable credential, such as a Veridian SSI credential or CIP-170 aligned proof.

### Indexing and Verification

The off-chain indexer monitors the blockchain for credit market UTxOs which are identified by their beacon tokens (CIP-89).

When metadata is present, the indexer verifies the attached proof against the relevant credential schema and exposes the verification status through a public API.

### Discovery and Funding

Capital providers query the indexer to discover lending opportunities.

Participants may filter opportunities according to their own requirements, including jurisdiction, verification status or other metadata attributes.

Any participant may fund a lending opportunity through the underlying credit market contracts. Verification metadata simply enables additional discovery and filtering mechanisms for participants who require them.

### Repayment and Reputation

As loans are repaid, repayment history is trustlessly associated with the originating entity and its verification credentials.

Over time, these repayment records can contribute to privacy-preserving reputation systems and future trust frameworks, including those enabled by Midnight and other zero-knowledge technologies.

### Settlement

The pilot described later combines this infrastructure with regulated settlement infrastructure, initially provided through Encryptus, to support conversion between Cardano-native USD-denominated stable assets and local fiat currencies. The consortium may utilize equivalent regulated settlement providers where operational, regulatory or technical considerations make this appropriate.

## What We Build

### Metadata Standard

A versioned schema for attaching identity proofs, verification status and loan-level compliance information to credit market UTxOs.

The standard is designed to be extensible and support additional trust and verification use cases over time.

### Off-Chain Indexer

A service that reads credit market UTxOs, verifies attached proofs, tracks loan lifecycles and exposes a query API for discovery and filtering.

Both components will be released as open public infrastructure for the broader Cardano ecosystem to adopt, extend and operate independently and to integrate into future credit market applications. The off-chain indexer could be run locally to avoid dependence on a third-party API service.

![Cardano Credit Market](../assets/cardano-credit-market.png)

*Image 1. 	Cardano Credit market*

---

[← 2. Motivation](02-motivation.md) · [Table of Contents](../README.md) · [4. Pilot Implementation →](04-pilot-implementation.md)
