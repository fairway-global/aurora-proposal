# 2. Motivation
In traditional lending, every loan begins as an individual agreement between specific parties with its own terms, risk profile, repayment schedule and settlement conditions. Much like a transaction, each loan exists as a discrete financial object that can be originated, funded, serviced, transferred and settled independently. Only after loans are created do financial institutions aggregate them into portfolios, funds or securitized products.

Most DeFi lending protocols reverse this process. Capital is first deposited into a shared pool, and borrowers draw from that pool according to predefined rules. While effective for certain use cases, this model does not reflect how many real-world credit markets operate.

Cardano's eUTxO architecture is well suited to the loan-first model. Its transaction-based architecture can represent individual financial relationships as distinct on-chain objects rather than requiring every lending opportunity to be organized through a shared liquidity pool.

Individual lending opportunities can therefore exist as separate Loan Request UTxOs with their own terms, state and lifecycle. They can be independently published, funded and settled through compatible lending infrastructure before being aggregated into larger credit portfolios.

This creates the technical foundation for open credit markets built around individual financial agreements. It does not, by itself, create the shared market infrastructure required for institutions and other capital providers to discover, compare and evaluate those agreements across independent implementations.

Two problems currently prevent individual Cardano credit opportunities from functioning coherently and being usable in institutional and professional capital-provider workflows.

## Institutions need shared market infrastructure, not just permissionless settlement.
Cardano credit market implementations can enable parties to negotiate and settle individual lending agreements on-chain. Institutional lenders, regulated financial institutions and professional capital providers, however, require more than settlement. They need standardized ways to discover lending opportunities, evaluate relevant information, apply their own eligibility and compliance requirements and monitor performance over time before allocating capital.

Without standardized metadata, discovery, filtering and verification infrastructure, each participant must interpret lending opportunities through protocol-specific integrations and independently reconstruct the information required for evaluation.

Advances in verifiable credentials, zero-knowledge proofs and other proof systems make it possible to associate institutional, eligibility, compliance and other verification information with an opportunity without requiring sensitive underlying data to be published on-chain. Implemented through optional transaction metadata and open verification references rather than changes to lending protocols, this infrastructure can support participants that require additional assurance while preserving permissionless use of the underlying market.

Verification is therefore one component of the required market layer. Institutions must also be able to index opportunities, filter them according to published attributes, compare relevant information and monitor their lifecycle through consistent interfaces.

## Independent credit markets need shared standards, not isolated integrations.
Without common standards, each lending protocol, application and capital provider must develop its own metadata format, indexing logic, discovery interface, verification workflow and reporting model.

This creates fragmented market information and repeated integration work. Lending opportunities may exist on-chain but remain difficult to discover or compare across implementations. Capital providers must conduct similar technical integration and due-diligence work separately for each protocol, while builders must recreate infrastructure that provides substantially the same market functions.

This fragmentation becomes more costly as additional lending models, jurisdictions, verification systems and capital-provider requirements emerge. Proprietary discovery systems may solve the immediate needs of individual applications, but they do not establish common infrastructure that future Cardano builders can adopt and operate independently.

Open standards provide a different path. A common Metadata Standard can describe lending opportunities consistently. Shared indexing and discovery infrastructure can expose those opportunities through open APIs. Published filtering and verification specifications can allow capital providers and compatible applications to evaluate opportunities according to their own requirements without depending on one proprietary marketplace or exclusive lending protocol.

The result is reusable market infrastructure rather than a collection of isolated integrations.

## Bringing the Two Together
Aurora addresses both problems by establishing a shared market layer around independent Loan Request UTxOs.

Standardized metadata enriches each opportunity with machine-readable market information and verification references. Open discovery and indexing infrastructure then makes those opportunities searchable across compatible implementations. Capital providers and applications can discover, filter and evaluate opportunities according to their own requirements while funding and settlement continue through the underlying lending infrastructure.

Aurora does not replace lending protocols or determine which opportunities should receive capital. It establishes the open standards, verification framework, discovery infrastructure, APIs and developer tooling required for independent Cardano credit opportunities to function as a coherent market.

Treasury funding builds and demonstrates this reusable infrastructure.

---

[Previous](01-summary.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](03-proposed-solution.md)
