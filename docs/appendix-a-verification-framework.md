# Appendix A: Verification Framework
Aurora's Verification Framework provides an open and extensible way for credit opportunities to reference institutional, eligibility, compliance and other proof-based information without making any single verification system a requirement of the underlying lending protocol.

Verification is one component of Aurora's broader market infrastructure. It supports discovery, filtering and evaluation by allowing compatible applications and capital providers to determine whether attached evidence satisfies their own requirements.

The framework does not determine who should receive capital, perform regulatory enforcement or create a universal participation policy.

## Framework Principles
### Technology Agnostic
Aurora does not require a specific identity provider, credential issuer, proof system or verification technology.

Different verification mechanisms may coexist within the same market infrastructure. The Metadata Standard and Verification Framework are designed so that additional credential types, proof systems and verification providers can be supported without requiring changes to the underlying lending protocol.

This allows Aurora to evolve as verification technologies and institutional requirements change.

### Proof-Based
Aurora-compatible Loan Request UTxOs may reference verifiable information that can be evaluated against an applicable schema or policy.

Depending on the use case, this may include institutional status, eligibility information, compliance-related evidence or other proof-based attributes relevant to a capital provider or application.

Aurora exposes the relevant verification references and provides infrastructure for evaluating them. Individual participants remain responsible for determining which evidence they require and how that evidence affects their own decisions.

### Privacy Compatible
The Verification Framework is designed to support privacy-preserving verification.

Sensitive underlying information does not need to be published directly on Cardano simply because a participant requires additional assurance. Where supported by the relevant verification system, applications may rely on proofs, attestations, selective disclosure or other verification references instead of exposing the underlying data.

Aurora therefore standardizes how verification information can be associated with market opportunities without prescribing where sensitive information must be stored or how every proof must be generated.

### Optional Participation
Aurora metadata and verification are optional market infrastructure.

The underlying lending implementation remains independently usable without Aurora metadata. Participants that require additional information may use Aurora-compatible metadata, filtering and verification capabilities, while participants that do not require those capabilities may interact directly with the underlying lending infrastructure.

Different credit opportunities may therefore support different verification or eligibility requirements without imposing one global participation standard across Cardano credit markets.

### Extensibility
Verification requirements vary across jurisdictions, applications and capital providers and may change over time.

The framework is therefore designed around versioned schemas and extensible verification references rather than fixed assumptions about one identity system or compliance model.

Future verification mechanisms can be incorporated where they are compatible with the published interfaces without requiring Aurora to become the issuer, custodian or central authority for the underlying information.

## Verification in the Aurora Architecture
Verification operates alongside, rather than in place of, Aurora's other market-infrastructure functions.

A compatible Loan Request UTxO may be enriched with standardized metadata containing or referencing relevant verification information. The Aurora Discovery Engine indexes that opportunity and exposes its standardized market information through open APIs.

Applications and capital providers can then:

1. discover compatible credit opportunities;
2. filter them according to relevant metadata and requirements;
3. identify associated verification information; and
4. evaluate that information against the applicable schema or policy.

The result of verification becomes one input into evaluation by the relevant participant. Aurora does not itself make the lending, underwriting or capital-allocation decision.

This separation allows the same underlying opportunity to be evaluated according to different policies without requiring the lending protocol to enforce one universal institutional standard.

## Verification Providers and Future Systems
The funded framework is not dependent on any particular identity or privacy infrastructure.

Compatible implementations may use verifiable credentials, zero-knowledge proofs, attestations, selective-disclosure systems or other verification mechanisms supported by the relevant schemas and interfaces.

Privacy-preserving systems such as Midnight may therefore be integrated where technically appropriate, but Aurora does not depend on Midnight for operation and Treasury funding does not establish a proprietary identity or credential system.

Similarly, future applications may associate repayment history, institutional performance or other verifiable information with compatible credit-market entities. Aurora provides the shared infrastructure through which such information can be referenced, indexed and exposed; the commercial activity that generates real repayment or performance evidence remains outside the Treasury-funded scope.

## Participant Responsibilities
Aurora provides verification infrastructure rather than regulatory enforcement.

Participants remain responsible for their own legal, regulatory, risk and operational requirements.

In particular:

* capital providers determine which evidence and verification standards they require;
* verification providers determine what information they verify and how they substantiate it;
* lending implementations determine the requirements imposed by their own contracts or applications; and
* originators and other participants determine which credentials, proofs or supporting evidence they make available.

The Verification Framework allows these different requirements to coexist through open standards rather than imposing a single global compliance model on all Aurora-compatible activity.

All Treasury-funded Verification Framework specifications, reference implementations and related software are released under **Apache License 2.0** and remain available for independent implementation and extension.

**AURORA:**

Open Infrastructure for Institutional Credit Markets on Cardano

Sundial Protocol  ·  Fairway Oy  ·  Fallen Icarus

Cardano Treasury Proposal  ·  2026

---

[Previous](11-governance-submission-requirements.md) · [Home](../README.md) · [Full Proposal](../proposal.md)
