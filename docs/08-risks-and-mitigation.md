# 8. Risks and Mitigation
Aurora's infrastructure-only scope limits Treasury risk primarily to technical delivery, interoperability, security and long-term usability of the resulting public infrastructure.

**Compatibility with underlying lending infrastructure.**
Aurora operates alongside compatible lending implementations rather than replacing the underlying lending contracts. Differences in Loan Request UTxO structures may therefore affect integration and testing.

Aurora mitigates this risk through open interfaces and clearly defined metadata, discovery and verification specifications. The reference implementation and testnet demonstration will validate compatibility against representative Loan Request UTxO structures while preserving flexibility across different implementations.

**Interoperability and specification risk.**
Different lending implementations, capital-provider requirements and future use cases may require metadata or query structures that are not known at the time of the initial release.

The Metadata Standard, Verification Framework and filtering specifications are therefore designed to be **versioned, extensible and modular**. Published schemas and open APIs allow the infrastructure to evolve as new requirements emerge without forcing changes to the underlying lending protocols.

**Verification-system dependency.**
Verification requirements may rely on different credential systems, proof systems or verification providers.

Aurora does not depend on a single verification technology. The Verification Framework separates verification references and policies from the underlying lending contracts, allowing multiple verification systems to coexist and evolve independently.

**Security and implementation risk.**
Defects in the Discovery Engine, APIs, verification logic or developer tooling could produce incorrect indexing, filtering or verification results.

The project includes independent security review of the Treasury-funded software and relevant interfaces. Material findings affecting the funded release must be addressed or clearly documented before final completion. Aurora is also designed as a market-information and discovery layer rather than a custody or transaction-execution layer, which limits the impact of defects within the infrastructure itself.

**Operational usability risk.**
Open-source infrastructure provides limited value if it is difficult for third parties to deploy, integrate or maintain.

Aurora mitigates this through public repositories, Apache License 2.0, deployment instructions, developer documentation, open APIs and reference implementations. Final completion criteria include demonstrating that the infrastructure can be deployed and operated by a technically capable third party using the published materials.

**Adoption risk.**
Open standards do not guarantee adoption by future lending protocols, applications or capital providers.

Aurora mitigates this by keeping the infrastructure optional, protocol-independent and reusable. Existing lending implementations do not need to replace their core contracts, while the APIs, reference implementation and query standards are intended to reduce the work required to integrate with the shared market layer. Treasury delivery is measured by the completion and usability of the public infrastructure rather than by speculative adoption targets.

**Delivery schedule risk.**
The approximately five-month implementation period requires standards development, implementation, integration, review and documentation to progress in parallel where appropriate.

Fairway is responsible for coordinating the integrated delivery. The four-milestone structure provides intermediate verification of specifications, core functionality and the end-to-end technical demonstration before final release. Independent review preparation may begin before implementation is fully complete to reduce delays at the final milestone.

**Legal and regulatory interpretation.**
Open infrastructure intended for institutional credit markets may raise questions about how standards, verification references and interfaces are described or used in different contexts.

The funded scope therefore includes independent legal review of the infrastructure, documentation and intended operating model, with any material findings incorporated into the final release.

---

[Previous](07-milestones-and-success-criteria.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](09-governance-and-oversight.md)
