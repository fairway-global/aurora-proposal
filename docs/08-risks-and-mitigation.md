# 8. Risks and Mitigation
Aurora's infrastructure-only scope limits Treasury risk primarily to technical delivery, interoperability, security and long-term usability of the resulting public infrastructure.

The remaining risks relate primarily to technical delivery, interoperability, security and long-term usability of the public infrastructure.

**Underlying credit-market implementation dependency.** Aurora operates around compatible lending infrastructure rather than replacing the underlying lending contracts. Differences in Loan Request UTxO structures or delays in individual lending implementations could therefore affect integration testing.

Aurora mitigates this risk by defining its metadata, discovery and verification infrastructure through open interfaces rather than depending on one exclusive lending protocol. The reference implementation and testnet demonstration are intended to validate compatibility against representative Loan Request UTxO structures while preserving protocol independence.

**Interoperability and specification risk.** Different lending implementations, capital-provider requirements and future use cases may require metadata or query structures that are not known at the time of the initial release.

The Metadata Standard, Verification Framework and filtering specifications are therefore designed to be versioned, extensible and modular. Published schemas and open APIs allow future implementations to extend the infrastructure without requiring changes to the underlying lending protocol or dependence on proprietary rules.

**Verification-system dependency.** Institutional verification requirements may rely on different credential systems, proof systems or verification providers.

Aurora does not require a single verification technology. The Verification Framework separates verification references and policies from the underlying lending contracts so that multiple verification systems can coexist and evolve independently.

**Security and implementation risk.** Defects in the Discovery Engine, APIs, verification logic or developer tooling could produce incorrect indexing, filtering or verification results.

The project includes independent security review of the Treasury-funded software and relevant interfaces. Material findings affecting the funded release must be addressed or transparently documented before final completion. The architecture also keeps Aurora separate from custody and lending-contract execution, limiting the consequences of defects in the market-information layer.

**Independent operability risk.** Open-source code provides limited public value if the infrastructure can only be operated through Fairway-hosted services or undocumented internal dependencies.

Aurora mitigates this through public repositories, Apache License 2.0, build and deployment instructions, developer documentation and final completion criteria requiring a technically capable third party to operate the relevant infrastructure without dependence on Fairway, Sundial or any individual advisor.

**Adoption risk.** Open standards do not guarantee adoption by future lending protocols, applications or capital providers.

The proposal mitigates this risk by keeping the infrastructure optional, protocol independent and reusable. Aurora does not require existing lending implementations to change their core contracts, and its APIs, reference implementation and query standards are intended to reduce the integration work required for third-party adoption. Treasury delivery is measured by completion and usability of the public infrastructure rather than by speculative adoption targets.

**Delivery schedule risk.** The approximately five-month implementation period is intentionally focused but requires standards development, implementation, integration, review and documentation to progress in parallel where appropriate.

Fairway remains responsible for coordinating the integrated delivery. The four milestone structure provides intermediate verification of specifications, core functionality and the end-to-end technical demonstration before final release. Independent review preparation may begin before implementation is fully complete so that review does not unnecessarily delay the final milestone.

**Legal and regulatory interpretation.** Aurora provides open market infrastructure rather than regulatory enforcement, custody or lending services. Nevertheless, standards and interfaces intended for institutional use may raise legal questions about how the infrastructure should be described or operated.

The funded scope therefore includes independent legal review of the open infrastructure and intended operating model. Future lending activity, jurisdiction-specific compliance and commercial deployment remain outside the Treasury proposal and remain the responsibility of the relevant market participants.

---

[Previous](07-milestones-and-success-criteria.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](09-governance-and-oversight.md)
