# 4. Deliverables
The project delivers open-source market infrastructure that can be adopted, extended and operated independently by future Cardano credit market implementations.

Treasury funding covers the standards, software, reference implementations, documentation and technical validation required to make independent Loan Request UTxOs discoverable, filterable, verifiable and institutionally usable. It does not fund lending capital, commercial onboarding or live loan execution.

## Core Infrastructure Deliverables
1. **Metadata Standard.**
   A versioned, open specification describing credit-market opportunities and the metadata references associated with Loan Request UTxOs. The standard defines how institutionally relevant information can be attached consistently without modifying the underlying lending protocol and remains extensible across lending models, jurisdictions and verification systems.

2. **Verification Framework.**
   An extensible framework for attaching and evaluating institutional, eligibility, compliance and other proof-based information associated with Loan Request UTxOs. The framework supports multiple credential systems, proof systems and verification providers without requiring a single identity or compliance infrastructure.

3. **Aurora Discovery Engine.**
   An open-source service that indexes compatible Loan Request UTxOs and associated metadata, exposes lending opportunities through open APIs, supports discovery and filtering, provides access to verification information and tracks relevant loan-lifecycle information exposed by compatible lending implementations.
    The Discovery Engine will be independently operable so that third-party builders are not required to depend on Fairway or a single hosted service.

4. **Filtering and Query Capabilities.**
   Open filtering capabilities based on published metadata schemas and query specifications. Compatible applications and capital providers will be able to identify opportunities according to criteria such as jurisdiction, duration, asset, ticket size, verification requirements and other standardized attributes supported by the applicable schema.

5. **Open APIs.**
   Public interfaces for querying Aurora-compatible credit opportunities, associated metadata, verification information and relevant lifecycle information.
   The APIs are intended to reduce protocol-specific integration work and enable wallets, lending applications, analytics services and other ecosystem participants to build against common market infrastructure.

6. **Developer Tooling and Reference Implementation.**
    Open tooling and reference code demonstrating how developers can create Aurora-compatible metadata, identify and index Loan Request UTxOs, query the Discovery Engine, apply filtering criteria and evaluate verification references.

    The reference implementation will demonstrate the complete infrastructure flow without requiring adoption of any single lending protocol or commercial deployment model.

7. **Documentation.**
    Technical documentation covering the Metadata Standard, Verification Framework, Discovery Engine, APIs, filtering model and reference implementation.

    Documentation will include sufficient integration and operating guidance for third-party developers to adopt the standards and operate the relevant infrastructure independently.

## Capital Discovery & Allocation Layer
Aurora includes selected technical contributions from Sundial relating to capital-provider requirements, discovery, filtering and interoperability within the broader Aurora implementation.

These contributions include:

**Capital Provider Profile Standard.**
 An open schema for representing requirements such as jurisdiction, ticket size, duration, asset, verification requirements and risk preferences.

**Discovery and Filtering Specification.**
 A published specification describing how capital-provider requirements can be translated into discovery and filtering criteria against Aurora-compatible credit opportunities.

**Reference Query Library.**
 Open examples demonstrating how prospective capital providers and compatible applications can query and filter opportunities using the published standards.

**Market Discovery API Contribution.**
 API definitions and related implementation contributions required to expose capital-provider-relevant discovery and filtering capabilities through the Aurora infrastructure.

**Lightweight Integration Artifacts.**
 Reference examples or lightweight SDK components demonstrating how external applications can integrate the Capital Provider Profile Standard and query specifications.

**Documentation.**
 Technical documentation sufficient for third parties to use, implement and extend the relevant standards and interfaces without dependence on Sundial.

These components form part of Aurora’s common open-source infrastructure rather than a separate Sundial product or independently funded workstream. Sundial contributes technical expertise where relevant, while Fairway remains responsible for integrated delivery of the proposal as lead implementer.

The Capital Discovery & Allocation Layer does not allocate Treasury capital, make lending decisions or create a proprietary capital-allocation product. It provides open standards and reference tooling that future market participants may use according to their own requirements.

## Technical Demonstration
The project will include a testnet technical demonstration showing that the core infrastructure operates together as intended.

The demonstration will show that a compatible Loan Request UTxO can be:

1. created through compatible lending infrastructure;
2. enriched with standardized metadata;
3. identified and indexed by the Aurora Discovery Engine;
4. discovered through an open API;
5. filtered according to published criteria;
6. associated with verification information that can be evaluated through the Verification Framework; and
7. consumed by a compatible reference application or query workflow.

The technical demonstration validates the infrastructure rather than commercial lending performance. It does not require Treasury-funded loan capital, fiat settlement, borrower disbursement or live SACCO lending.

## Security and Legal Review
The funded scope includes independent review appropriate to the infrastructure being delivered.

The security review will assess the Treasury-funded software and relevant technical interfaces before final release.

The legal review will assess the open infrastructure, standards and intended operating model within the scope of this proposal. It does not constitute legal approval of future lending activity or commercial deployments, which remain the responsibility of the relevant participants.

## Open-Source Release and Public Documentation
All Treasury-funded software, standards and reference implementations will be released under the **Apache License 2.0**.

Public repositories will contain the applicable source code, specifications, documentation and implementation materials required for third parties to inspect, operate, modify and extend the infrastructure.

The project will also publish public progress reporting against the approved milestones and deliverables.

The resulting infrastructure remains available to the Cardano ecosystem regardless of whether future builders use Fairway, Sundial or any particular lending implementation.

---

[Previous](03-proposed-solution.md) · [Home](../README.md) · [Full Proposal](../proposal.md) · [Next](05-budget-and-resource-allocation.md)
